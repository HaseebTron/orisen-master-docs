# Radar Sleep-Stage Literature — v2 Discovery Expansion

Status: Raw working research artifact
Authority level: Radar/ML raw research archive
Date captured: 2026-06-12
Source tools:
- Elicit
- Semantic Scholar Graph API
- OpenAlex Works API

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

## Automated Semantic Scholar / OpenAlex citation expansion pass

Date captured: 2026-06-13 (appended to the 2026-06-12 raw discovery artifact)

Source tools:
- Semantic Scholar Graph API: title/fallback search, citations, references, and recommendations endpoints.
- OpenAlex Works API: title cross-checks and recent-first keyword searches.

Scope note: This is a raw metadata and citation-discovery pass only. It does not perform full-text extraction, method extraction, source ranking, synthesis, or Orisen product-claim interpretation. API metadata and snippets are inputs to later verification, not final truth.

API notes and caveats:
- Seed 1: OpenAlex did not return a high-overlap in-scope title match
- Seed 2: OpenAlex did not return a high-overlap in-scope title match
- Seed 5: Semantic Scholar title/fallback search returned no plausible in-scope result
- Seed 6: OpenAlex did not return a high-overlap in-scope title match
- Seed 8: OpenAlex did not return a high-overlap in-scope title match
- Generated candidate list was conservatively pruned before append to omit apnea-only, vital-sign-only, and unrelated PSG/radar false positives that did not clearly involve sleep-stage, sleep-state, active/quiet sleep, or sleep/wake labels.
- OpenAlex title results were accepted only when the returned title had high overlap with the searched title; lower-overlap title-search results were ignored.
- Exact duplicates were lightly grouped by title/year, with discovery paths preserved; likely version-linked and already-known items were not removed.

### Seed metadata matches

#### Seed 1: Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning
- Best Semantic Scholar match: Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning
- Query used: Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning
- Year: 2024
- Authors: Jonghyun Park, Seungman Yang, G. Chung, Ivo Junior Leal Zanghettin, Jonghee Han
- Venue/source type: IEEE Access; JournalArticle
- DOI/stable ID: 10.1109/ACCESS.2024.3390391
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/f4034e7a8956d379d358e6352af6b7e92d71beda)
- OpenAlex URL: not available
- PDF/source URL: [source](https://ieeexplore.ieee.org/ielx7/6287639/6514899/10504259.pdf)

#### Seed 2: Sleep stage classification using FMCW radar sensor data and machine learning
- Best Semantic Scholar match: Sleep stage classification Using FMCW radar sensor data and machine learning
- Query used: Wellune radar sleep stage classification FMCW
- Year: 2025
- Authors: J. Cho, J. H. Shin, W. Park
- Venue/source type: Sleep &amp; Breathing disorders
- DOI/stable ID: 10.1183/23120541.sleepandbreathing-2025.4
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/71a4ed664ff40fdcd293737f9080ea8e2c496f30)
- OpenAlex URL: not available
- PDF/source URL: not available

#### Seed 3: Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People Living with Dementia
- Best Semantic Scholar match: Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People living with Dementia
- Query used: Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People Living with Dementia
- Year: 2026
- Authors: Maowen Yin, K. K. Ravindran, Charalambos Hadjipanayi, Alan Bannon, Adrien Rapeaux, C. D. Monica, T. Lande, Derk-Jan Dijk
- Venue/source type: IEEE transactions on bio-medical engineering; JournalArticle
- DOI/stable ID: 10.48550/arXiv.2601.04057
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/c4a294ee2e241247266a2d2be605fdf008cede66)
- OpenAlex URL: [OpenAlex](https://openalex.org/W7119557951)
- PDF/source URL: not available

#### Seed 4: The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp
- Best Semantic Scholar match: The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp
- Query used: The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp
- Year: 2026
- Authors: Z. Diao, Yueting Li, Jianpeng Wang, Shengyu Guan, Xinwei Wang, Wenxiong Cui, Xintong Shi, Tong Liu
- Venue/source type: not stated
- DOI/stable ID: 2604.16442
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/ea82f1407660a5cac396c27958dbeaa82d138f35)
- OpenAlex URL: [OpenAlex](https://openalex.org/W7154626198)
- PDF/source URL: not available

#### Seed 5: Developing a Deep Learning Model for Sleep Stage Prediction in an Obstructive Sleep Apnea Cohort Using 60 GHz Frequency-Modulated Continuous-Wave Radar
- Best Semantic Scholar match: Developing a deep learning model for sleep stage prediction in obstructive sleep apnea cohort using 60 GHz frequency-modulated continuous-wave radar
- Query used: Semantic Scholar keyword/API search: 60 GHz FMCW radar sleep stage prediction
- Year: 2023
- Authors: Ji Hyun Lee, Hyunwoo Nam, Dong Hyun Kim, Dae Lim Koo, Jae Won Choi, Seung-No Hong, E. Jeon, Sungmook Lim
- Venue/source type: Journal of Sleep Research; JournalArticle
- DOI/stable ID: 10.1111/jsr.14050
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/9fee440b1cb677abf7cccd89a347a0acfa51e735)
- OpenAlex URL: not available
- PDF/source URL: [source](https://onlinelibrary.wiley.com/doi/pdfdirect/10.1111/jsr.14050)

#### Seed 6: Unobtrusive Cot Side Sleep Stage Classification in Preterm Infants Using Ultra-Wideband Radar
- Best Semantic Scholar match: Unobtrusive cot side sleep stage classification in preterm infants using ultra-wideband radar
- Query used: Unobtrusive Cot Side Sleep Stage Classification in Preterm Infants Using Ultra-Wideband Radar
- Year: 2023
- Authors: E. Arasteh, E. D. de Groot, Demi van den Ende, T. Alderliesten, X. Long, R. de Goederen, M. Benders, J. Dudink
- Venue/source type: Frontiers in Sleep; JournalArticle
- DOI/stable ID: 10.3389/frsle.2023.1150962
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/0bbfd5fdcc11efa9572211adc6d9febec5cbe22b)
- OpenAlex URL: not available
- PDF/source URL: [source](https://www.frontiersin.org/articles/10.3389/frsle.2023.1150962/pdf)

#### Seed 7: Validation of Sleep Stage Classification Using Non-Contact Radar Technology and Machine Learning
- Best Semantic Scholar match: Validation of sleep stage classification using non-contact radar technology and machine learning (Somnofy).
- Query used: Toften Somnofy radar sleep stage classification
- Year: 2020
- Authors: Stale Toften, S. Pallesen, Maria Hrozanova, F. Moen, J. Grnli
- Venue/source type: Sleep Medicine; JournalArticle
- DOI/stable ID: 10.1016/j.sleep.2020.02.022
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/423c9b884bc2f82426fc7ed8136a467ed8eab177)
- OpenAlex URL: [OpenAlex](https://openalex.org/W3010200460)
- PDF/source URL: [source](https://ntnuopen.ntnu.no/ntnu-xmlui/bitstream/11250/2683973/1/fulltext.pdf)

#### Seed 8: Noncontact Sleep Stage Estimation Using a CW Doppler Radar
- Best Semantic Scholar match: Noncontact Sleep Stage Estimation Using a CW Doppler Radar
- Query used: Noncontact Sleep Stage Estimation Using a CW Doppler Radar
- Year: 2018
- Authors: Hong Hong, Li Zhang, Chen Gu, Yusheng Li, Guangxin Zhou, Xiaohua Zhu
- Venue/source type: IEEE Journal on Emerging and Selected Topics in Circuits and Systems; JournalArticle
- DOI/stable ID: 10.1109/JETCAS.2017.2789278
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/78c45ae8af2a00e7619f375c62d21ac16f4edf44)
- OpenAlex URL: not available
- PDF/source URL: not available

### Raw candidate entries

#### Candidate 1: Contactless Sleep Staging With Radar: A Transfer Learning Approach
- Discovery path: cited by seed 1
- Canonical title: Contactless Sleep Staging With Radar: A Transfer Learning Approach
- Year: 2026
- Authors: Daniel Krauss, R. Richer, Nils C. Albrecht, Jelena Jukic, Carlos Herrera Krebber, Paul Zwiessele, Alexander German, A. Koelpin
- Venue/source type: IEEE Open Journal of Engineering in Medicine and Biology; JournalArticle
- DOI or stable ID: 10.1109/OJEMB.2026.3667047
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/9480916c16a4c4a734fe56f2cfefcc998e8d8ace)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: Accurate sleep monitoring is essential to assess sleep quality and diagnose sleep disorders. Although sleep laboratories provide precise assessments, they are expensive, labor-intensive, and unsuitable for ...
- Radar terms visible: radar
- Sleep-label terms visible: sleep stage, sleep staging, rem, polysomnography, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: not stated
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes not stated and sleep stage, sleep staging, rem, polysomnography, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 2: The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp
- Discovery path: best Semantic Scholar title/fallback match for seed 4; OpenAlex title cross-check for seed 4; cited by seed 7; OpenAlex keyword/API search: FMCW radar sleep staging PSG; OpenAlex keyword/API search: UWB radar sleep stage classification PSG; OpenAlex keyword/API search: 60 GHz FMCW radar sleep stage prediction; OpenAlex keyword/API search: UWB radar active quiet sleep classification
- Canonical title: The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp
- Year: 2026
- Authors: Z. Diao, Yueting Li, Jianpeng Wang, Shengyu Guan, Xinwei Wang, Wenxiong Cui, Xintong Shi, Tong Liu
- Venue/source type: not stated
- DOI or stable ID: 10.5281/zenodo.19602868
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/ea82f1407660a5cac396c27958dbeaa82d138f35)
- OpenAlex URL: [OpenAlex](https://openalex.org/W7154626198)
- PDF/source URL if available: [source/PDF](https://arxiv.org/abs/arXiv:2604.16442)
- Abstract/snippet if available: Sleep staging is essential for the assessment of sleep quality and the diagnosis of sleep-related disorders. Conventional polysomnography (PSG), while considered the gold standard, is intrusive, ...
- Radar terms visible: radar
- Sleep-label terms visible: sleep stage, sleep stages, sleep staging, rem, nrem, polysomnography, psg, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: not stated
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes not stated and sleep stage, sleep stages, sleep staging, rem, nrem, polysomnography, psg, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 3: Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People living with Dementia
- Discovery path: cited by seed 1; best Semantic Scholar title/fallback match for seed 3; OpenAlex title cross-check for seed 3; cited by seed 7; cited by seed 8; OpenAlex keyword/API search: FMCW radar sleep staging PSG
- Canonical title: Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People living with Dementia
- Year: 2026
- Authors: Maowen Yin, K. K. Ravindran, Charalambos Hadjipanayi, Alan Bannon, Adrien Rapeaux, C. D. Monica, T. Lande, Derk-Jan Dijk
- Venue/source type: IEEE transactions on bio-medical engineering; JournalArticle
- DOI or stable ID: 10.48550/arXiv.2601.04057
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/c4a294ee2e241247266a2d2be605fdf008cede66)
- OpenAlex URL: [OpenAlex](https://openalex.org/W7119557951)
- PDF/source URL if available: [source/PDF](https://arxiv.org/pdf/2601.04057)
- Abstract/snippet if available: OBJECTIVE Ultra-wideband (UWB) radar technology offers a promising solution for unobtrusive and cost-effective in-home sleep monitoring. However, the limited availability of radar sleep data poses challenges ...
- Radar terms visible: radar, uwb, ultra-/ wideband
- Sleep-label terms visible: sleep stage, sleep stages, sleep staging, polysomnography, psg, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: UWB / IR-UWB / impulse radar
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes UWB / IR-UWB / impulse radar and sleep stage, sleep stages, sleep staging, polysomnography, psg, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 4: Contactless Sleep Staging with Radar: A Transfer Learning Approach
- Discovery path: OpenAlex keyword/API search: mmWave radar sleep stage classification PSG
- Canonical title: Contactless Sleep Staging with Radar: A Transfer Learning Approach
- Year: 2025
- Authors: Daniel Krauss, Robert Richer, Nils C. Albrecht, Jelena Jukic, Carlos Herrera Krebber, Paul Zwiessele, Alexander German, Alexander Koelpin
- Venue/source type: not stated; preprint
- DOI or stable ID: 10.36227/techrxiv.174535565.58795771/v1
- Semantic Scholar URL: not available
- OpenAlex URL: [OpenAlex](https://openalex.org/W4409656302)
- PDF/source URL if available: [source/PDF](https://www.techrxiv.org/doi/pdf/10.36227/techrxiv.174535565.58795771)
- Abstract/snippet if available: Accurate sleep monitoring is essential to assess sleep quality and diagnose sleep disorders. Although sleep laboratories provide precise assessments, they are expensive, labor-intensive, and unsuitable for ...
- Radar terms visible: radar
- Sleep-label terms visible: sleep stage, sleep staging, rem, polysomnography, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: not stated
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: likely duplicate/version-linked with the 2026 journal version; preserve for version tracking
- Reason captured: Metadata includes not stated and sleep stage, sleep staging, rem, polysomnography, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 5: Sleep Stage Classification Through LSTM Model Based on Unique Spectrum Features from CW Radar Signal
- Discovery path: cited by seed 8
- Canonical title: Sleep Stage Classification Through LSTM Model Based on Unique Spectrum Features from CW Radar Signal
- Year: 2025
- Authors: Hao Wu, Shuqin Dong, Changzhan Gu
- Venue/source type: IEEE International Wireless Symposium
- DOI or stable ID: 10.1109/IWS65943.2025.11177838
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/2805771f3bc4f6cf01c75e7f6c3f69eb03043531)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: Sleep stage classification plays a vital role in sleep disorder diagnosis and disease prevention, where non-contact microwave radar emerges as a promising non-invasive monitoring method. This ...
- Radar terms visible: radar, microwave radar
- Sleep-label terms visible: sleep stage, polysomnography, psg
- Likely radar type/frequency/device if visible: microwave radar
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: appears new or not yet clearly present in v1/v2
- Reason captured: Metadata includes microwave radar and sleep stage, polysomnography, psg terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 6: Sleep stage classification Using FMCW radar sensor data and machine learning
- Discovery path: best Semantic Scholar title/fallback match for seed 2
- Canonical title: Sleep stage classification Using FMCW radar sensor data and machine learning
- Year: 2025
- Authors: J. Cho, J. H. Shin, W. Park
- Venue/source type: Sleep &amp; Breathing disorders
- DOI or stable ID: 10.1183/23120541.sleepandbreathing-2025.4
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/71a4ed664ff40fdcd293737f9080ea8e2c496f30)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: not available
- Radar terms visible: radar, fmcw
- Sleep-label terms visible: sleep stage
- Likely radar type/frequency/device if visible: FMCW
- Ground truth/reference labels if visible: not stated
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes FMCW and sleep stage terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 7: Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People
- Discovery path: reference of seed 3; cited by seed 7
- Canonical title: Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People
- Year: 2025
- Authors: Maowen Yin, Charalambos Hadjipanayi, K. K. Ravindran, Alan Bannon, Adrien Rapeaux, C. D. Monica, T. Lande, Derk-Jan Dijk
- Venue/source type: IEEE Transactions on Biomedical Engineering; JournalArticle
- DOI or stable ID: 10.1109/TBME.2025.3548780
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/038675346570d5c7632fa73558a56069ea2b238b)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: Objective: Ultra-wideband (UWB) radar technology has emerged as a promising alternative for creating portable and cost-effective in-home monitoring devices. Although there exists good evidence supporting its ...
- Radar terms visible: radar, uwb, ultra-/ wideband
- Sleep-label terms visible: sleep stage, sleep stages, rem, polysomnography, psg, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: UWB / IR-UWB / impulse radar
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes UWB / IR-UWB / impulse radar and sleep stage, sleep stages, rem, polysomnography, psg, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 8: Sleep stage estimation method based on state transition using millimeter-wave radar
- Discovery path: cited by seed 7; cited by seed 8; Semantic Scholar keyword/API search: FMCW radar sleep staging PSG
- Canonical title: Sleep stage estimation method based on state transition using millimeter-wave radar
- Year: 2024
- Authors: Yi Lu, Zhaocheng Yang, Jianhua Zhou
- Venue/source type: International Conference on Signal Processing Systems; Conference
- DOI or stable ID: 10.1117/12.3023191
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/cc804a84ef36baf549c2632d8fb74567a699ee81)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: Due to the excellent advantages of the radar sensor, it is considered to be one of the most potential technologies for the sleep monitoring. In this ...
- Radar terms visible: radar, fmcw, millimet(?:er|re)[ -]wave
- Sleep-label terms visible: sleep stage, sleep staging, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: FMCW; mmWave / millimeter-wave
- Ground truth/reference labels if visible: not stated
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes FMCW; mmWave / millimeter-wave and sleep stage, sleep staging, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 9: Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning
- Discovery path: best Semantic Scholar title/fallback match for seed 1
- Canonical title: Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning
- Year: 2024
- Authors: Jonghyun Park, Seungman Yang, G. Chung, Ivo Junior Leal Zanghettin, Jonghee Han
- Venue/source type: IEEE Access; JournalArticle
- DOI or stable ID: 10.1109/ACCESS.2024.3390391
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/f4034e7a8956d379d358e6352af6b7e92d71beda)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://ieeexplore.ieee.org/ielx7/6287639/6514899/10504259.pdf)
- Abstract/snippet if available: As an increasing number of people suffer from sleep disorders, such as insomnia or sleep apnea, sleep monitoring and management using consumer devices have gained increasing ...
- Radar terms visible: radar, uwb, ultra-/ wideband
- Sleep-label terms visible: sleep stage, sleep stages, rem, polysomnography, psg, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: UWB / IR-UWB / impulse radar
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes UWB / IR-UWB / impulse radar and sleep stage, sleep stages, rem, polysomnography, psg, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 10: Developing a deep learning model for sleep stage prediction in obstructive sleep apnea cohort using 60 GHz frequency-modulated continuous-wave radar
- Discovery path: reference of seed 4; Semantic Scholar keyword/API search: FMCW radar sleep staging PSG; Semantic Scholar keyword/API search: 60 GHz FMCW radar sleep stage prediction
- Canonical title: Developing a deep learning model for sleep stage prediction in obstructive sleep apnea cohort using 60 GHz frequency-modulated continuous-wave radar
- Year: 2023
- Authors: Ji Hyun Lee, Hyunwoo Nam, Dong Hyun Kim, Dae Lim Koo, Jae Won Choi, Seung-No Hong, E. Jeon, Sungmook Lim
- Venue/source type: Journal of Sleep Research; JournalArticle
- DOI or stable ID: 10.1111/jsr.14050
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/9fee440b1cb677abf7cccd89a347a0acfa51e735)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://onlinelibrary.wiley.com/doi/pdfdirect/10.1111/jsr.14050)
- Abstract/snippet if available: Given the significant impact of sleep on overall health, radar technology offers a promising, non-invasive, and cost-effective avenue for the early detection of sleep disorders, even ...
- Radar terms visible: radar, fmcw, 60 ghz
- Sleep-label terms visible: sleep stage, sleep stages, rem, nrem, polysomnography, psg
- Likely radar type/frequency/device if visible: FMCW; 60 GHz
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes FMCW; 60 GHz and sleep stage, sleep stages, rem, nrem, polysomnography, psg terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 11: Non-contact determination of sleep/wake state in residential environments by neural network learning of microwave radar and electroencephalogram-electrooculogram measurements
- Discovery path: cited by seed 8
- Canonical title: Non-contact determination of sleep/wake state in residential environments by neural network learning of microwave radar and electroencephalogram-electrooculogram measurements
- Year: 2023
- Authors: Xiaorui Wang, D. Matsushita
- Venue/source type: Building and Environment
- DOI or stable ID: 10.1016/j.buildenv.2023.110095
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/2c5489e56dfb200c5b51e082ac992cf13d11cb4a)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: not available
- Radar terms visible: radar, microwave radar
- Sleep-label terms visible: sleep/wake
- Likely radar type/frequency/device if visible: microwave radar
- Ground truth/reference labels if visible: not stated
- Appears new/already in v1/duplicate/version-linked/uncertain: appears new or not yet clearly present in v1/v2
- Reason captured: Metadata includes microwave radar and sleep/wake terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 12: Three Contactless Sleep Technologies Compared With Actigraphy and Polysomnography in a Heterogeneous Group of Older Men and Women in a Model of Mild Sleep Disturbance: Sleep Laboratory Study
- Discovery path: reference of seed 3
- Canonical title: Three Contactless Sleep Technologies Compared With Actigraphy and Polysomnography in a Heterogeneous Group of Older Men and Women in a Model of Mild Sleep Disturbance: Sleep Laboratory Study
- Year: 2023
- Authors: K. K. G Ravindran, C. della Monica, G. Atzori, D. Lambert, Hanan Hassanin, V. Revell, D. Dijk
- Venue/source type: JMIR mHealth and uHealth; JournalArticle
- DOI or stable ID: 10.2196/46338
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/c8fa92fda26ce69a0f9ac81e95a121024f01a278)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://mhealth.jmir.org/2023/1/e46338/PDF)
- Abstract/snippet if available: Background Contactless sleep technologies (CSTs) hold promise for longitudinal, unobtrusive sleep monitoring in the community and at scale. They may be particularly useful in older populations ...
- Radar terms visible: radar
- Sleep-label terms visible: sleep stage, polysomnography, psg, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: not stated
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: uncertain; reference of seed 3 with contactless sleep-technology and PSG metadata, radar type not stated
- Reason captured: Metadata includes not stated and sleep stage, polysomnography, psg, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis. Keep as uncertain until the full text confirms which contactless technologies are radar-based.

#### Candidate 13: Unobtrusive cot side sleep stage classification in preterm infants using ultra-wideband radar
- Discovery path: best Semantic Scholar title/fallback match for seed 6
- Canonical title: Unobtrusive cot side sleep stage classification in preterm infants using ultra-wideband radar
- Year: 2023
- Authors: E. Arasteh, E. D. de Groot, Demi van den Ende, T. Alderliesten, X. Long, R. de Goederen, M. Benders, J. Dudink
- Venue/source type: Frontiers in Sleep; JournalArticle
- DOI or stable ID: 10.3389/frsle.2023.1150962
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/0bbfd5fdcc11efa9572211adc6d9febec5cbe22b)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://www.frontiersin.org/articles/10.3389/frsle.2023.1150962/pdf)
- Abstract/snippet if available: Background Sleep is an important driver of development in infants born preterm. However, continuous unobtrusive sleep monitoring of infants in the neonatal intensive care unit (NICU) ...
- Radar terms visible: radar, uwb, ultra-/ wideband
- Sleep-label terms visible: sleep stage, quiet sleep, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: UWB / IR-UWB / impulse radar
- Ground truth/reference labels if visible: not stated
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes UWB / IR-UWB / impulse radar and sleep stage, quiet sleep, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 14: Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar
- Discovery path: reference of seed 4; cited by seed 8; Semantic Scholar keyword/API search: FMCW radar sleep staging PSG; Semantic Scholar keyword/API search: 60 GHz FMCW radar sleep stage prediction
- Canonical title: Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar
- Year: 2023
- Authors: Young-Keun Yoo, Chaewon Jung, Hyun-Chool Shin
- Venue/source type: Applied Sciences
- DOI or stable ID: 10.3390/app13074468
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/da9fd396a7eb57d40d44336e6e4c5944c14978d7)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://www.mdpi.com/2076-3417/13/7/4468/pdf?version=1680595044)
- Abstract/snippet if available: The paper proposes a unsupervised method for detecting the three stages of sleep-wake, rapid eye movement (REM) sleep, and non-REM sleep-using biosignals obtained from a 61 ...
- Radar terms visible: radar, fmcw, 61 ghz
- Sleep-label terms visible: sleep stage, sleep stages, sleep-/ state, rem, non-/ rem, polysomnography, psg
- Likely radar type/frequency/device if visible: FMCW; 61 GHz
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes FMCW; 61 GHz and sleep stage, sleep stages, sleep-/ state, rem, non-/ rem, polysomnography, psg terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 15: Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar
- Discovery path: reference of seed 1; reference of seed 3
- Canonical title: Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar
- Year: 2021
- Authors: H. Kwon, S. Choi, Dongseok Lee, Dongyeon Son, H. Yoon, Mi Hyun Lee, Y. Lee, K. Park
- Venue/source type: IEEE journal of biomedical and health informatics; JournalArticle
- DOI or stable ID: 10.1109/JBHI.2021.3072644
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/dab1b9028a3f7f538635abf7b7b273ea0d30d72e)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: Manual scoring of sleep stages from polysomnography (PSG) records is essential to understand the sleep quality and architecture. Since the PSG requires specialized personnel, a lab ...
- Radar terms visible: radar, uwb, ultra-/ wideband, ir-/ uwb, impulse-/ radio
- Sleep-label terms visible: sleep stage, sleep stages, sleep staging, rem, polysomnography, psg
- Likely radar type/frequency/device if visible: UWB / IR-UWB / impulse radar
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes UWB / IR-UWB / impulse radar and sleep stage, sleep stages, sleep staging, rem, polysomnography, psg terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 16: Distinguishing sleep from wake with a radar sensor: a contact-free real-time sleep monitor
- Discovery path: reference of seed 3
- Canonical title: Distinguishing sleep from wake with a radar sensor: a contact-free real-time sleep monitor
- Year: 2021
- Authors: H. Heglum, H. Kallestad, D. Vethe, K. Langsrud, T. Sand, M. Engstrm
- Venue/source type: Sleep; JournalArticle
- DOI or stable ID: 10.1093/sleep/zsab060
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/e6a549795e29f4f974ad4448ffcd5f1c33cd3a2e)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://academic.oup.com/sleep/article-pdf/44/8/zsab060/39624133/zsab060.pdf)
- Abstract/snippet if available: Abstract This work aimed to evaluate whether a radar sensor can distinguish sleep from wakefulness in real time. The sensor detects body movements without direct physical ...
- Radar terms visible: radar
- Sleep-label terms visible: sleep/wake, polysomnography, sleep monitor
- Likely radar type/frequency/device if visible: not stated
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes not stated and sleep/wake, polysomnography, sleep monitor terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 17: Non-contact Sleep/Wake Monitoring Using Impulse-Radio Ultrawideband Radar in Neonates
- Discovery path: reference of seed 6
- Canonical title: Non-contact Sleep/Wake Monitoring Using Impulse-Radio Ultrawideband Radar in Neonates
- Year: 2021
- Authors: Won Hyuk Lee, Seung Hyun Kim, J. Na, Y. Lim, Seok-Hyun Cho, Sung Ho Cho, Hyun-Kyung Park
- Venue/source type: Frontiers in Pediatrics; JournalArticle
- DOI or stable ID: 10.3389/fped.2021.782623
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/588f85f6bba4bf257efa4d46061c2a4e55ac35b5)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://www.frontiersin.org/articles/10.3389/fped.2021.782623/pdf)
- Abstract/snippet if available: Background: The gold standard for sleep monitoring, polysomnography (PSG), is too obtrusive and limited for practical use with tiny infants or in neonatal intensive care unit ...
- Radar terms visible: radar, uwb, ir-/ uwb, impulse-/ radio
- Sleep-label terms visible: sleep/wake, polysomnography, psg, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: UWB / IR-UWB / impulse radar
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes UWB / IR-UWB / impulse radar and sleep/wake, polysomnography, psg, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 18: Radar-based sleep stage classification in children undergoing polysomnography: a pilot-study.
- Discovery path: reference of seed 3; reference of seed 6
- Canonical title: Radar-based sleep stage classification in children undergoing polysomnography: a pilot-study.
- Year: 2021
- Authors: R. de Goederen, S. Pu, M. Silos Viu, D. Doan, S. Overeem, W. Serdijn, K. Joosten, X. Long
- Venue/source type: Sleep Medicine; JournalArticle
- DOI or stable ID: 10.1016/j.sleep.2021.03.022
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/8a5f85701bca1b20081e609a54623c174ab97298)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://doi.org/10.1016/j.sleep.2021.03.022)
- Abstract/snippet if available: STUDY OBJECTIVES Unobtrusive monitoring of sleep and sleep disorders in children presents challenges. We investigated the possibility of using Ultra-Wide band (UWB) radar to measure sleep ...
- Radar terms visible: radar, uwb
- Sleep-label terms visible: sleep stage, sleep stages, rem, non-/ rem, sleep classification, polysomnography
- Likely radar type/frequency/device if visible: UWB / IR-UWB / impulse radar
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes UWB / IR-UWB / impulse radar and sleep stage, sleep stages, rem, non-/ rem, sleep classification, polysomnography terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 19: Performance Evaluation of the Circadia Contactless Breathing Monitor and Sleep Analysis Algorithm for Sleep Stage Classification
- Discovery path: reference of seed 3
- Canonical title: Performance Evaluation of the Circadia Contactless Breathing Monitor and Sleep Analysis Algorithm for Sleep Stage Classification
- Year: 2020
- Authors: T. Lauteslager, S. Kampakis, A. Williams, M. Maslik, F. Siddiqui
- Venue/source type: Annual International Conference of the IEEE Engineering in Medicine and Biology Society; JournalArticle, Conference
- DOI or stable ID: 10.1109/EMBC44109.2020.9175419
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/a007021570043140ae64ddd035098fbf31b77389)
- OpenAlex URL: not available
- PDF/source URL if available: [source/PDF](https://doi.org/10.1109/embc44109.2020.9175419)
- Abstract/snippet if available: Although polysomnography (PSG) remains the gold standard for studying sleep in the lab, the development of wearable and 'nearable' non-EEG based sleep monitors has the potential ...
- Radar terms visible: radar
- Sleep-label terms visible: sleep stage, sleep stages, sleep staging, rem, polysomnography, psg, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: not stated
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: appears new or not yet clearly present in v1/v2
- Reason captured: Metadata includes not stated and sleep stage, sleep stages, sleep staging, rem, polysomnography, psg, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 20: Validation of sleep stage classification using non-contact radar technology and machine learning (Somnofy).
- Discovery path: reference of seed 1; reference of seed 4; best Semantic Scholar title/fallback match for seed 7; OpenAlex title cross-check for seed 7
- Canonical title: Validation of sleep stage classification using non-contact radar technology and machine learning (Somnofy).
- Year: 2020
- Authors: Stale Toften, S. Pallesen, Maria Hrozanova, F. Moen, J. Grnli
- Venue/source type: Sleep Medicine; JournalArticle
- DOI or stable ID: 10.1016/j.sleep.2020.02.022
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/423c9b884bc2f82426fc7ed8136a467ed8eab177)
- OpenAlex URL: [OpenAlex](https://openalex.org/W3010200460)
- PDF/source URL if available: [source/PDF](https://ntnuopen.ntnu.no/ntnu-xmlui/bitstream/11250/2683973/1/fulltext.pdf)
- Abstract/snippet if available: OBJECTIVE To validate automatic sleep stage classification using deep neural networks on sleep assessed by radar technology in the commercially available sleep assistant Somnofy against polysomnography ...
- Radar terms visible: radar
- Sleep-label terms visible: sleep stage, polysomnography, psg
- Likely radar type/frequency/device if visible: not stated
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes not stated and sleep stage, polysomnography, psg terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

#### Candidate 21: Noncontact Sleep Stage Estimation Using a CW Doppler Radar
- Discovery path: reference of seed 1; best Semantic Scholar title/fallback match for seed 8
- Canonical title: Noncontact Sleep Stage Estimation Using a CW Doppler Radar
- Year: 2018
- Authors: Hong Hong, Li Zhang, Chen Gu, Yusheng Li, Guangxin Zhou, Xiaohua Zhu
- Venue/source type: IEEE Journal on Emerging and Selected Topics in Circuits and Systems; JournalArticle
- DOI or stable ID: 10.1109/JETCAS.2017.2789278
- Semantic Scholar URL: [Semantic Scholar](https://www.semanticscholar.org/paper/78c45ae8af2a00e7619f375c62d21ac16f4edf44)
- OpenAlex URL: not available
- PDF/source URL if available: not available
- Abstract/snippet if available: Sleep stage estimation is crucial to the evaluation of sleep quality and is a proven biometric in diagnosing cardiovascular diseases. In this paper, we design a ...
- Radar terms visible: radar, doppler
- Sleep-label terms visible: sleep stage, polysomnography, sleep monitor, sleep monitoring
- Likely radar type/frequency/device if visible: CW Doppler; Doppler
- Ground truth/reference labels if visible: PSG/polysomnography visible
- Appears new/already in v1/duplicate/version-linked/uncertain: already in v1/v2 raw artifacts
- Reason captured: Metadata includes CW Doppler; Doppler and sleep stage, polysomnography, sleep monitor, sleep monitoring terms.
- Caveats: Metadata-level capture only; no deep extraction performed. Verify against primary/full text before screening or synthesis.

### Automated pass counts

- Raw candidate entries in this automated pass: 21
- Candidate entries dated 2024-2026: 9
- Candidate entries marked uncertain or likely duplicate/version-linked: 2
- Candidate entries marked uncertain, duplicate/version-linked, or already present in v1/v2 raw artifacts: 16
- Completeness claim: not made.
