# Radar Sleep Stage Literature — Extraction Pass 1

Status: Raw working research artifact  
Authority level: Radar/ML raw research archive  
Date captured: 2026-06-12  
Source: Extraction Pass 1 from Orisen Radar + ML literature-review workflow  
Not source of truth  
Not product evidence  
Do not use as Orisen product claims

## Raw artifact note

This file preserves Extraction Pass 1 for the screened P0 radar sleep-stage literature sources.

It is not a validated source-of-truth claim file. It should not be used as public product claims, technical performance claims, or evidence that Orisen can detect sleep stages, reduce grogginess, reduce sleep inertia, control sleep state, or perform sleep-phase-aware intervention.

Confidence labels below refer to confidence in the extracted detail, not confidence in the paper's result.

## Context loaded

Baseline files read:

- `ai-context/start-here.md`
- `ai-context/project-routing.md`
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/repo-governance/cross-repo-boundaries.md`

Task-specific files read:

- `radar-ml/radar-ml-read-rules.md`
- `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`

Files attempted but not found:

- None.

The P0 list below comes from the screening file's clean P0 list, which said to keep Extraction Pass 1 to these 12 sources. This is Extraction Pass 1, not a final synthesis and not an Orisen product-claim update. Radar/ML read rules also require direct paper/source review and warn not to treat paper results as Orisen claims.

Legend: **H/M/L** = confidence in that extracted detail, not confidence in the paper's result.

| Source | Year | Source type | Radar/device/chip/module | Radar type | Frequency | Placement/distance | Subjects/nights | Population | Radar-only or multimodal | Ground truth | Sleep labels predicted | Confidence / notes |
|---|---:|---|---|---|---|---|---|---|---|---|---|---|
| **Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar** | 2021 | Journal, IEEE JBHI. Source checked indirectly through a later comparison/reference page: [MDPI Applied Sciences reference/comparison page](https://www.mdpi.com/2076-3417/13/7/4468) | IR-UWB radar from title/reference. **M** | IR-UWB. **M** | not stated | not stated | not stated | not stated | Radar-only implied by title, but primary methods not accessed. **L** | not stated | Sleep-stage classification; secondary comparison table suggests four-stage IR-UWB, but primary still needs verification. **L/M** | **Low overall for methods.** Bibliographic identity is verified from a secondary reference, but the primary paper/full abstract was not accessed in this pass. |
| **Developing a Deep Learning Model for Sleep Stage Prediction in an Obstructive Sleep Apnea Cohort Using 60 GHz FMCW Radar** | 2024 | Journal article, *Journal of Sleep Research*. Source: [Seoul National University Elsevier Pure page](https://snu.elsevierpure.com/en/publications/developing-a-deep-learning-model-for-sleep-stage-prediction-in-ob/) | Radar 1/Radar 2; specific chip/module not stated. **M** | FMCW radar. **H** | 60 GHz. **H** | not stated | 78 participants; overnight PSG with radar monitoring. **H** | Adult OSA cohort. **H** | Radar-based; multiple radar inputs tested, PSG used as reference. **H** | PSG. **H** | Wakefulness, REM, NREM grouped as N1+N2+N3. **H** | **High for abstract-level extraction.** Hardware module, exact placement, and distance are not stated on the accessible source page. |
| **Validation of Sleep Stage Classification Using Non-Contact Radar Technology and Machine Learning (Somnofy®)** | 2020 | Journal per screening file. | Somnofy®; exact hardware not verified from primary in this pass. **L** | not verified | not stated | not stated | not stated | not stated | not verified | PSG validation implied by screening/title, but primary not verified. **L** | not stated | **Low overall.** Keep in P0 because screening marked it foundational, but it needs primary paper/full text chase before real extraction. |
| **Contactless Sleep Staging With Radar: A Transfer Learning Approach** | 2026 | Journal per screening/discovery; PubMed access was blocked/cache-missed in this pass. | not stated in accessible primary page | not stated | not stated | not stated | 44 synchronized PSG recordings from discovery only; not primary-verified here. **L** | not stated | Radar + transfer learning; exact input modalities not verified. **L** | PSG synchronized recordings from discovery only. **L** | Five-class radar sleep staging from discovery only. **L** | **Low overall until journal page/full text is accessible.** Extract journal first; compare 2025 preprint only if journal lacks methods. |
| **Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People** | 2025 | Journal per screening/discovery. | Commercial impulse/UWB radar from discovery only. **L** | Impulse / UWB radar. **L** | not stated | not stated | not primary-verified | Older adults. **M** | Radar-based; exact inference inputs not verified. **L** | PSG implied by discovery/PubMed snippet, not directly verified here. **L** | Wake, REM, light, deep from discovery only. **L** | **Low overall for extracted details.** PubMed hit was not accessible because of reCAPTCHA; needs full source chase. |
| **Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People Living with Dementia** | 2026 | Preprint, arXiv. Source: [arXiv abstract](https://arxiv.org/abs/2601.04057) | Ultra-wideband radar; specific device/module not stated. **H/M** | UWB radar. **H** | not stated | not stated | Validation on radar dataset of 47 older adults; 18 with prodromal or mild Alzheimer disease. **H** | Older adults, mean age 71.2; includes AD-related impairment subgroup. **H** | Radar-based target domain; trained with large-scale PSG datasets plus radar data/domain adaptation. **H** | PSG datasets and radar dataset; exact scoring workflow not stated on abstract page. **M** | Wakefulness, REM, light sleep, deep sleep. **H** | **Medium-high.** Abstract gives the core extraction, but exact radar hardware, placement, distance, and number of nights need PDF methods verification. |
| **Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning** | 2024 | Journal, IEEE Access. Source: [Samsung Research page](https://research.samsung.com/research-papers/Ultra-Wideband-Radar-Based-Sleep-Stage-Classification-in-Smartphone-Using-an-End-to-End-Deep-Learning) | Customized Samsung Galaxy smartphone with UWB radar chip. **H** | UWB radar. **H** | not stated | Smartphone placed on a table near the bed; exact distance not stated. **H/M** | 509 nights of UWB radar + in-lab PSG. **H** | Various participants including patients with apnea. **H/M** | Radar-only inference input appears to be UWB radar; PSG used as reference. **H/M** | Nocturnal in-lab PSG; expert-annotated stages. **H** | Wake, REM, light sleep, deep sleep. **H** | **High for page-level extraction.** Frequency and exact placement distance are not stated on the Samsung page. |
| **The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp** | 2026 | Preprint, arXiv; intended submission to *Physiological Measurement*. Sources: [arXiv abstract](https://arxiv.org/abs/2604.16442), [arXiv PDF](https://arxiv.org/pdf/2604.16442) | Sleepal AI Lamp with 60 GHz FMCW radar sensor. **H** | FMCW radar. **H** | 60 GHz. **H** | Bedside table, oriented toward thoracic region; exact distance not stated. **H/M** | 1,022 valid overnight recordings after exclusions. **H** | Adults 18+; broad sample including healthy participants and OSA-severity heterogeneity. **H/M** | Radar-only features for model input: respiratory and motion-related features from radar. **H** | PSG; expert-labeled / AASM-scored sleep stages. **H** | Binary sleep/wake and four-stage: wake, light NREM N1+N2, deep NREM N3, REM. **H** | **High for preprint details.** Still preprint/product-led, so synthesis should keep caveats. |
| **Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar** | 2023 | Journal, *Applied Sciences*. Source: [MDPI full text](https://www.mdpi.com/2076-3417/13/7/4468) | BitSensing single-channel FMCW radar; 1 Tx / 3 Rx hardware, best-SNR channel used. **H** | FMCW radar. **H** | Abstract says 61 GHz; specs table lists center frequency 60 GHz. **M; discrepancy to verify** | Installed 0.4 m above headboard facing subject's chest; radar range 0-0.75 m. **H** | 85 participants; average >6h simultaneously with PSG. **H** | PSG lab participants; adult status not explicitly stated in extracted lines. **M** | Radar-only; uses breathing and movement data extracted from FMCW radar. **H** | PSG readings by clinical specialists. **H** | Wake, REM, NREM. **H** | **High overall.** Main unresolved item is 60 vs 61 GHz wording inconsistency. |
| **Deep Learning-Based Automated Diagnosis of OSA and Sleep Stage Classification in Children Using Millimeter-Wave Radar and Pulse Oximeter** | 2025 | Journal per screening; accessible method details from 2024 arXiv preprint. **M** Source used for methods: [ar5iv rendering of arXiv preprint](https://ar5iv.org/abs/2409.19276) | QSA600 millimeter-wave radar-based device + pulse oximeter. **H from preprint** | Millimeter-wave radar. **H** | not stated | not stated | 281 children, ages 1-18. **H** | Pediatric sleep-center cohort. **H** | Multimodal: radar-based device plus pulse oximeter. **H** | PSG manually scored. **H** | Wake-sleep; Wake-REM-Light-Deep; Wake-REM-N1-N2-N3. **H** | **Medium-high.** Technical details are verified from the preprint, but the 2025 journal full page was not accessible in this pass. |
| **Radar-Based Sleep Stage Classification in Children Undergoing Polysomnography: A Pilot Study** | 2021 | Journal, *Sleep Medicine*. Source checked indirectly through later comparison/reference page: [MDPI Applied Sciences reference/comparison page](https://www.mdpi.com/2076-3417/13/7/4468) | IR-UWB radar suggested by secondary comparison table; exact device not primary-verified. **L/M** | IR-UWB from secondary table. **L/M** | not stated | not stated | not stated | Children undergoing PSG. **M** | Radar-based; exact modality stack not verified. **L** | PSG from title/reference. **M** | Three-stage classification suggested by secondary comparison table. **L/M** | **Low-to-medium.** Bibliographic identity is verified from a secondary reference; full primary extraction still needed. |
| **Unobtrusive Cot Side Sleep Stage Classification in Preterm Infants Using Ultra-Wideband Radar** | 2023 | Journal, *Frontiers in Sleep*. Source: [Frontiers full text](https://www.frontiersin.org/journals/sleep/articles/10.3389/frsle.2023.1150962/full) | Xethru X2M200 radar module, Novelda. **H** | UWB radar. **H** | Pulses in 6.0-8.5 and 7.25-10.2 GHz bands; carrier frequency 7.46 GHz used. **H** | Cot/incubator-side NICU setup; detection zone 0.4-1 m; X2M200 detects 0.5-2.5 m. **H** | 10 preterm infants. **H** | Preterm infants, 29-34 weeks postmenstrual age. **H** | Radar + video-labeled behavioral sleep reference; radar features from body/breathing movement. **H** | Behavioral sleep stage classification for preterm infants, scored from video; not PSG. **H** | Active sleep and quiet sleep; wake assessed but intermediate sleep left out. **H** | **High.** Strong extraction, but neonatal labels are not adult AASM sleep stages. |

## Unresolved details to verify later

- Primary access still needed for Somnofy 2020, Attention-Based LSTM 2021, Contactless Sleep Staging transfer-learning 2026, Unobtrusive Sleep Health Assessment 2025, and Radar-Based Sleep Stage Classification in Children 2021.
- Hardware specifics missing for several sources: exact radar module/chip, antenna setup, placement geometry, and distance are often not available from abstracts or metadata pages.
- Frequency unresolved for multiple UWB/IR-UWB papers and the pediatric QSA600 paper.
- Label mapping needs cleanup across adult AASM labels, grouped labels, pediatric labels, and neonatal active/quiet sleep.
- Do not synthesize Orisen implications yet beyond technical relevance. Current Orisen docs still treat validated sleep-stage sensing and vital-sign sensing as not yet validated product capabilities.

## Suggested next step

Run a focused **Primary-Source Chase Pass** for the five weak P0 rows before synthesis: locate PDFs, publisher pages, DOI pages, institutional pages, or author PDFs, then rerun Extraction Pass 1 only for those unresolved rows.
