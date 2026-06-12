# Radar Sleep Stage Literature — Primary-Source Chase Pass 1

Status: Raw working research artifact  
Authority level: Radar/ML raw research archive  
Date captured: 2026-06-12  
Source: Primary-Source Chase Pass after Extraction Pass 1  
Not source of truth  
Not product evidence  
Do not use as Orisen product claims

## Raw artifact note

This file preserves the Primary-Source Chase Pass run after Extraction Pass 1 for five weak P0 radar sleep-stage literature rows.

It is not a validated source-of-truth claim file. It should not be used as public product claims, technical performance claims, or evidence that Orisen can detect sleep stages, reduce grogginess, reduce sleep inertia, control sleep state, or perform sleep-phase-aware intervention.

The goal of this pass was only to improve missing extraction fields from legal primary or near-primary sources where accessible.

## Primary-source chase results

| Weak P0 source | Best legal source found | Radar/device/chip/module | Radar type | Frequency | Placement/distance | Subjects/nights | Population | Radar-only vs multimodal | Ground truth | Sleep labels predicted | Chase result |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar** | Primary DOI identified as **10.1109/JBHI.2021.3072644**; PubMed entry exists but returned reCAPTCHA. The accessible PubMed “similar articles” listing confirms title, IEEE JBHI venue, year, pages, DOI, and PMID. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | not stated from accessible primary page | IR-UWB radar from title/reference. Secondary comparison confirms IR-UWB and four-stage classification. ([MDPI Applied Sciences](https://www.mdpi.com/2076-3417/13/7/4468)) | not stated | not stated | not stated | not stated | Radar-only implied by title, but not primary-verified | not stated | Four-stage classification appears in secondary comparison table, but primary full details still unresolved. ([MDPI Applied Sciences](https://www.mdpi.com/2076-3417/13/7/4468)) | **Partially improved only.** Bibliographic/DOI confidence improved; methods remain unresolved because primary content was not accessible. |
| **Validation of Sleep Stage Classification Using Non-Contact Radar Technology and Machine Learning (Somnofy®)** | No primary source located in this chase. Multiple targeted searches for the exact title, Somnofy, radar, PSG, and validation returned no usable primary hit. | not stated | not stated | not stated | not stated | not stated | not stated | not stated | not stated | not stated | **Still unresolved.** Keep as weak P0 / source-chase-needed. |
| **Contactless Sleep Staging With Radar: A Transfer Learning Approach** | TechRxiv source identified from prior discovery, but direct TechRxiv page returned **403 Forbidden**. PubMed URL for PMID 41970655 returned cache miss. | not stated | not stated | not stated | not stated | not stated | not stated | not stated | not stated | not stated | **Still unresolved from primary source.** Do not patch methods from discovery-only claims yet. |
| **Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People** | Primary PubMed entry identified indirectly from PubMed “similar articles”: **IEEE Transactions on Biomedical Engineering**, online ahead of print, DOI **10.1109/TBME.2025.3548780**, PMID **40048348**. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | not stated from accessible primary page | Impulse radar from title only; later related arXiv transfer-learning paper describes the relevant radar domain as UWB radar, but that is not the primary 2025 paper. ([arXiv](https://arxiv.org/abs/2601.04057)) | not stated | not stated | not stated from primary; later related arXiv validates on 47 older adults, mean age 71.2, including 18 with prodromal/mild Alzheimer disease, but do **not** treat that as direct extraction for the 2025 paper. ([arXiv](https://arxiv.org/abs/2601.04057)) | Older people from title; exact population not primary-verified | not stated | not stated | not stated from primary; later related arXiv uses wakefulness, REM, light sleep, deep sleep. ([arXiv](https://arxiv.org/abs/2601.04057)) | **Bibliographic source improved only.** Keep methods unresolved until IEEE/PubMed abstract or PDF is accessible. |
| **Radar-Based Sleep Stage Classification in Children Undergoing Polysomnography: A Pilot Study** | PubMed page accessible; DOI **10.1016/j.sleep.2021.03.022**. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | UWB radar; exact device/module/chip not stated on PubMed abstract. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | Ultra-wideband radar. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | not stated | not stated | 32 children undergoing clinical PSG. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | Ages 2 months to 14 years. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | Radar-only model input appears to use radar-derived body movement and breathing-rate features; PSG was reference. PubMed states 38 features were calculated from motion signals and breathing rate from raw radar signals. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | PSG as gold standard. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | Wake/sleep; wake/REM/NREM; wake/REM/light/deep. ([PubMed](https://pubmed.ncbi.nlm.nih.gov/33866298)) | **Meaningfully improved.** PubMed gives core extraction fields, but exact device/module, radar frequency, and placement/distance remain unresolved. |

## Fields still unresolved

- **Attention-Based LSTM / IR-UWB 2021:** exact radar module/chip, frequency, placement/distance, subject count, population, PSG/label details, and label set still need primary abstract/PDF access.
- **Somnofy 2020:** the whole row remains unresolved because I could not locate a primary source in this chase.
- **Krauss transfer-learning 2026:** primary source pages were identified/attempted but not legally accessible through this session; all method fields remain unresolved.
- **Yin impulse-radar older-people 2025:** bibliographic identity/DOI improved, but method fields remain unresolved until PubMed/IEEE content is accessible.
- **de Goederen pediatric UWB 2021:** exact radar module/chip, frequency, and placement/distance are still unresolved; PubMed filled subjects, age range, ground truth, radar type, and labels.

## Recommended patch to Extraction Pass 1

Patch the five weak rows like this:

1. **Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar**
   - Source type: `Journal, IEEE Journal of Biomedical and Health Informatics, 2021; DOI 10.1109/JBHI.2021.3072644; PMID 33848253`
   - Radar type: `IR-UWB radar`
   - Sleep labels predicted: `four-stage classification appears in secondary comparison; primary label set still not verified`
   - Confidence / notes: `Bibliographic details improved, but primary methods remain unresolved due PubMed reCAPTCHA / inaccessible IEEE content.`

2. **Validation of Sleep Stage Classification Using Non-Contact Radar Technology and Machine Learning (Somnofy®)**
   - Change confidence note to: `Primary source not found in this chase; keep as unresolved weak P0 until DOI/publisher/PubMed/author copy is found.`
   - Do **not** fill hardware, subjects, labels, or PSG from memory.

3. **Contactless Sleep Staging With Radar: A Transfer Learning Approach**
   - Change confidence note to: `TechRxiv/PubMed routes attempted but inaccessible in this session; keep all method fields as not stated until primary source is accessible.`
   - Do **not** patch 44 recordings or five-class labels unless the journal/preprint source is later accessible.

4. **Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People**
   - Source type: `Journal, IEEE Transactions on Biomedical Engineering, 2025 online ahead of print; DOI 10.1109/TBME.2025.3548780; PMID 40048348`
   - Radar type: `Impulse radar from title; exact device/frequency not stated from accessible primary metadata`
   - Confidence / notes: `Bibliographic details improved; methods still unresolved. Later 2026 related arXiv should not be treated as direct extraction for this 2025 paper without PDF confirmation.`

5. **Radar-Based Sleep Stage Classification in Children Undergoing Polysomnography: A Pilot Study**
   - Radar type: `Ultra-wideband radar`
   - Subjects/nights: `32 children undergoing clinical PSG`
   - Population: `children, ages 2 months to 14 years`
   - Radar-only or multimodal: `radar-derived body movement and breathing-rate features; PSG used as reference`
   - Ground truth: `polysomnography`
   - Sleep labels predicted: `wake/sleep; wake/REM/NREM; wake/REM/light/deep`
   - Still unresolved: `specific radar module/chip, frequency, placement/distance`
   - Confidence / notes: `PubMed abstract verified core extraction fields; hardware implementation details still need full text/PDF.`
