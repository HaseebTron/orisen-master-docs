# Radar Sleep-Stage Literature — v2 Discovery Expansion

Status: Raw working research artifact
Authority level: Radar/ML raw research archive
Date captured: 2026-06-12
Source tools:
- Elicit

Governing docs:
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/claim-control/claim-control-system.md`
- `radar-ml/radar-ml-read-rules.md`
- `radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`

## Raw artifact note

This file preserves external-tool discovery outputs for radar-based sleep-stage, sleep-state, and sleep/wake classification literature.

It is not a synthesis file and not an Orisen product-claim file. Tool outputs are inputs, not authorities. Candidate details must be verified against primary or near-primary sources before extraction or synthesis.

## Elicit prompt used

Find academic papers, preprints, conference papers, abstracts, technical reports, and product-validation studies about radar-based sleep-stage, sleep-state, REM/NREM, active/quiet sleep, or sleep/wake classification.

Scope:

* Include radar-based sleep-stage classification.
* Include radar-based sleep-state estimation.
* Include radar-based sleep/wake classification.
* Include PSG-labeled radar sleep monitoring.
* Include UWB, IR-UWB, impulse radar, FMCW radar, mmWave radar, 60 GHz radar, 61 GHz radar, 77 GHz radar, CW Doppler radar, pulse-Doppler radar, bioradar, and bioradiolocation if the source connects radar signals to sleep labels.
* Include radar papers that use respiration, respiratory intervals, RRV/BRV, movement/body motion, heartbeat, heart rate, HRV, phase, IQ, range-bin phase, raw radar, or semi-raw radar features for sleep labels.
* Include pediatric, neonatal, preterm infant, older-adult, dementia, OSA, healthy adult, and consumer-device cohorts.
* Include radar-only and radar-plus-other-sensor papers, but clearly mark multimodal papers.

Exclude:

* WiFi CSI papers unless the source clearly uses radar.
* Generic RF/radio sleep-stage papers unless the source clearly uses radar.
* Camera-only, microphone-only, wearable-only, ECG-only, PPG-only, bed-pressure-only, mattress-sensor-only, and actigraphy-only sleep staging.
* Radar vital-sign-only papers unless the vital signs directly feed sleep-stage, sleep-state, REM/NREM, active/quiet sleep, or sleep/wake classification.

Seed papers to search around:

1. Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar
2. Developing a Deep Learning Model for Sleep Stage Prediction in an Obstructive Sleep Apnea Cohort Using 60 GHz Frequency-Modulated Continuous-Wave Radar
3. Validation of Sleep Stage Classification Using Non-Contact Radar Technology and Machine Learning (Somnofy)
4. Contactless Sleep Staging With Radar: A Transfer Learning Approach
5. Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People
6. Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People Living with Dementia
7. Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning
8. The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp
9. Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar
10. Deep Learning-Based Automated Diagnosis of Obstructive Sleep Apnea and Sleep Stage Classification in Children Using Millimeter-Wave Radar and Pulse Oximeter
11. Radar-Based Sleep Stage Classification in Children Undergoing Polysomnography: A Pilot Study
12. Unobtrusive Cot Side Sleep Stage Classification in Preterm Infants Using Ultra-Wideband Radar
13. Noncontact Sleep Stage Estimation Using a CW Doppler Radar
14. Sleep Stages Classification by CW Doppler Radar Using Bagged Trees Algorithm
15. Sleep Stage Classification by Body Movement Index and Respiratory Interval Indices Using Multiple Radar Sensors
16. Sleep Stage Classification Based on Bioradiolocation Signals
17. DoppleSleep: A Contactless Unobtrusive Sleep Sensing System Using Short-Range Doppler Radar
18. Distinguishing Sleep from Wake with a Radar Sensor: A Contact-Free Real-Time Sleep Monitor
19. Sleep-Wake Detection With a Contactless, Bedside Radar Sleep Sensing System
20. Non-Contact Sleep/Wake Monitoring Using Impulse-Radio Ultra-Wideband Radar in Neonates

Also look specifically for these weak/missing citation-trail targets:

* Kagawa 2016 sleep stage classification by non-contact vital signs indices using Doppler radar sensors
* Jiang 2019 noncontact sleep stage classification based on multi-sensor feature-level fusion
* Hong 2019 microwave sensing and sleep / noncontact sleep-monitoring technology with microwave biomedical radar
* Full paper behind “Sleep Stage Classification Using FMCW Radar Sensor Data and Machine Learning” / Wellune radar
* Full version of “Translating Radar Data into Sleep Insights”
* RestAware: Non-Invasive Sleep Monitoring Using FMCW Radar
* Any journal or JBHI version related to the Sleepal AI Lamp paper

For each candidate source, return a table with:

* canonical title
* year
* authors
* venue/source type
* DOI or stable source link
* abstract or short summary
* radar type
* radar frequency
* radar device/chip/module if stated
* radar-only vs multimodal
* population/cohort
* subject count or nights if stated
* ground truth/reference labels if stated
* sleep labels predicted
* whether the source is sleep staging, sleep-state estimation, REM/NREM, active/quiet sleep, or sleep/wake only
* whether this appears new, already in the seed list, duplicate/version-linked, or uncertain
* why it may matter for a radar sleep-stage literature review
* source-access status if visible
* any uncertainty or caveat

Do not summarize the state of the field. Do not conclude that the literature is complete. Do not make product implications. Return candidates broadly, including uncertain but plausible radar sources, and mark uncertainty clearly.

## Elicit raw output

**All 10 sources provided are radar-based sleep-stage or sleep/wake classification papers meeting the research scope.** They span bioradiolocation, CW Doppler, FMCW, and impulse UWB radar across healthy adults, OSA cohorts, and older adults with dementia. Performance ranges from Cohen's kappa 0.49–0.75 and accuracy 60–86.6% for multi-stage classification.

| **Canonical Title** | **Year** | **Radar Type** | **Frequency** | **Population** | **N/Nights** | **Sleep Labels** | **Kappa/Accuracy** | **Status** | **Multimodal** |
|---|---|---|---|---|---|---|---|---|---|
| Bioradiolocation-based sleep stage classification | 2016 | Bioradiolocation | Not stated | Healthy adults | 32 | Wake/REM/Light/Deep | κ=0.49–0.57 | Seed #16 | Radar-only |
| Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar | 2023 | FMCW | 61 GHz | Healthy (PSG lab) | Not stated | Wake/REM/NREM | 68% similarity | Seed #9 | Radar-only |
| Noncontact Sleep Stage Estimation Using a CW Doppler Radar | 2018 | CW Doppler | Not stated | Healthy | 11 nights/13 subjects | Wake/REM/Light/Deep | 86.6% | Seed #13 | Radar-only |
| Validation of sleep stage classification using non-contact radar technology and machine learning (Somnofy) | 2020 | Not specified | Not stated | Healthy | 71 nights | Wake/N1/N2/N3/R | κ varies; sensitivity 0.97 | Seed #3 | Radar-only |
| Sleep stage classification by body movement index and respiratory interval indices using multiple radar sensors | 2015 | Microwave | 24 GHz | Healthy | Not stated | Wake/REM/Light/Deep | 71.9% (3-stage) | Seed #15 | Radar-only |
| Sleep stages classification by CW Doppler radar using bagged trees algorithm | 2017 | CW Doppler | Not stated | Healthy | 1 subject (all-night) | Wake/REM/Light/Deep | 78.6% | Seed #14 | Radar-only |
| Sleep stage classification based on bioradiolocation signals | 2015 | Bioradiolocation | Not stated | Healthy | 29 subjects | Wake/REM/NREM | κ=0.56; 75.13% | Seed #16 variant | Radar-only |
| Developing a deep learning model for sleep stage prediction in obstructive sleep apnea cohort using 60 GHz frequency-modulated continuous-wave radar | 2023 | FMCW | 60 GHz | OSA cohort | 78 subjects | Wake/REM/NREM | κ=0.746; 85.2% | Seed #2 | Radar-only |
| Sleep stage classification using FMCW radar sensor data and machine learning | 2025 | FMCW | Not stated | Mixed (19–89 yrs) | 537 adults | Wake/REM/NREM/N1/N2/N3 | κ=33.7–59.6% (4-state) | Wellune (target) | Radar-only |
| Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People | 2025 | Impulse UWB | Not stated | Older adults + dementia | 47 subjects | Wake/REM/Light/Deep | κ=0.63; 74.4% | Seed #5 | Radar-only |

**Key gaps:** Pediatric/neonatal papers (seeds #10–12, #20) not in provided sources. Multimodal papers (seed #10 mentions pulse oximeter) not fully represented. Full-text access limited for most.

## Elicit recent-first pass

### Elicit recent-first prompt used

Find recent papers from 2020–2026, especially 2024–2026, about radar-based sleep-stage classification, sleep-state estimation, REM/NREM classification, active/quiet sleep classification, or sleep/wake classification.

Prioritize newer papers and preprints. Include older papers only if needed to connect a citation trail, but do not make older foundational papers the main output.

Include:

- UWB radar sleep staging
- IR-UWB radar sleep staging
- impulse radar sleep staging
- FMCW radar sleep staging
- 60 GHz / 61 GHz / 77 GHz mmWave radar sleep staging
- CW Doppler radar sleep staging only if it leads to newer follow-up work
- PSG-labeled radar sleep monitoring
- radar sleep/wake classification
- radar sleep-state classification
- radar respiratory, movement, HR, HRV, RRV, phase, IQ, or raw/semi-raw radar features used for sleep labels
- consumer or product-style radar sleep-monitoring papers if they include sleep labels

Exclude:

- WiFi CSI
- generic RF/radio unless clearly radar
- camera-only
- microphone-only
- wearable-only
- ECG-only
- PPG-only
- bed-pressure-only
- mattress-sensor-only
- radar vital-sign-only papers unless the vital signs feed sleep-stage, sleep-state, REM/NREM, active/quiet sleep, or sleep/wake classification

Known older/foundational papers may be used as citation seeds, but the returned list should emphasize newer work.

For each candidate, return:

- canonical title
- year
- authors
- venue/source type
- DOI or source link
- radar type
- radar frequency
- radar device/chip/module if stated
- population
- subject count/nights if stated
- PSG or other reference label source
- sleep labels predicted
- radar-only vs multimodal
- whether this appears new, already known, duplicate/version-linked, or uncertain
- why it may matter
- caveats

Do not summarize the whole field. Do not conclude the literature is complete. Return candidates broadly, including uncertain but plausible radar sources, and mark uncertainty clearly.

### Elicit recent-first raw output

**The provided sources contain 10 radar-based sleep classification papers spanning 2015–2026, with 6 papers from 2023–2026 meeting your recency criteria.** The strongest recent evidence comes from three 2024–2026 studies: [Jonghyun Park et al., 2024] (509 nights, UWB, 76% accuracy, 4-stage); [J. Cho et al., 2025] (537 adults, FMCW, 77% accuracy for 3-state); and [Maowen Yin et al., 2026] (47 older adults + dementia cohort, UWB, 79.5% accuracy, transfer learning). Three 2023 papers provide additional evidence: [Young-Keun Yoo et al., 2023] (61 GHz FMCW, 68% unsupervised); [Ji Hyun Lee et al., 2023] (78 OSA patients, 60 GHz FMCW, 85.2% accuracy, dual-radar); [E. Arasteh et al., 2023] (10 preterm infants, UWB, 81% balanced accuracy for active/quiet sleep). Older papers ([Hong Hong et al., 2018]; [A. Tataraidze et al., 2016]; [M. Kagawa et al., 2015]) provide foundational CW Doppler and 24 GHz radar methods. All use PSG reference labels; most are radar-only or radar+PSG multimodal.

**Caveats:** Limited sample sizes in some studies; performance varies by sleep stage and OSA severity; domain adaptation needed for generalization.

### Visible Elicit result rows

- Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar — Young-Keun Yoo, Chaewon Jung, Hyun-Chool Shin — Applied Sciences, 2023.
- Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning — Jonghyun Park, Seungman Yang, G. Chung, Ivo Junior Leal Zanghettin, Jonghee Han — IEEE Access, 2024.
