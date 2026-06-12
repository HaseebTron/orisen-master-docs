# Radar Sleep Stage Literature — Screening Pass 1

Status: Raw working research artifact
Authority level: Radar/ML raw research archive
Date captured: 2026-06-12
Source: ChatGPT screening pass based on `discovery-pass-2026-06-12.md`
Governing docs:
- `ai-context/source-of-truth-rules.md`
- `ai-context/claim-control/claim-control-system.md`
- `radar-ml/radar-ml-read-rules.md`

## Raw artifact note

This file preserves a working screening pass over the radar sleep-stage literature discovery output.

It is not a validated source-of-truth claim file. The categories, priorities, and confidence labels are working research judgments meant to guide the next extraction pass. They should not be used as public product claims, technical performance claims, or evidence that Orisen can detect sleep stages, reduce grogginess, reduce sleep inertia, control sleep state, or perform sleep-phase-aware intervention.

---

# Screening Pass 1 — canonical source list

## Priority definitions

| Priority | Meaning |
|---|---|
| **P0** | Extract first. Directly relevant, likely high-value for Orisen radar/ML path. |
| **P1** | Extract after P0. Relevant, but narrower, older, weaker, pediatric/neonatal, or sleep/wake only. |
| **P2** | Useful background or citation-trail source, not first extraction. |
| **Hold** | Do not extract yet. First chase full text, verify radar/labels, or find a stronger source. |
| **Exclude** | Out of scope for this radar-only discovery pass. |

“Confidence” below means confidence in the **screening decision**, not confidence in the paper’s results.

---

## P0 — extract first

| Canonical source title | Year | Source type | Category | Subtype / caveat | Duplicate / version group | Priority | Confidence | Reason | Next action |
|---|---:|---|---:|---|---|---:|---|---|---|
| **Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar** | 2021 | Journal | A | Radar-only, adult, PSG-anchored, IR-UWB | Unique | P0 | High | One of the clearest modern radar sleep-stage papers. Direct radar → sleep labels. | Extract Pass 1 |
| **Developing a Deep Learning Model for Sleep Stage Prediction in an Obstructive Sleep Apnea Cohort Using 60 GHz FMCW Radar** | 2024 | Journal | A | Radar-only, adult OSA cohort, 60 GHz FMCW | Unique | P0 | High | Very relevant to mmWave/FMCW sleep-stage prediction. | Extract Pass 1 |
| **Validation of Sleep Stage Classification Using Non-Contact Radar Technology and Machine Learning (Somnofy®)** | 2020 | Journal | A | Commercial nearable radar, PSG validation | Somnofy line | P0 | High | Foundational product-style radar sleep-stage validation. | Extract Pass 1 |
| **Contactless Sleep Staging With Radar: A Transfer Learning Approach** | 2026 | Journal | A | Transfer learning, PSG-synchronized radar | Krauss transfer-learning group | P0 | High | Modern ML approach, likely important for cross-modal/domain transfer ideas. | Extract journal first |
| **Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People** | 2025 | Journal | A | Older adults, impulse/UWB radar | Yin older-adult line | P0 | High | Important older-adult cohort and likely bridge to 2026 transfer-learning work. | Extract Pass 1 |
| **Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People Living with Dementia** | 2026 | Preprint | A | Older adults / dementia, transfer learning, UWB radar | Yin older-adult line | P0 | High | Distinct high-value paper because it targets older adults/dementia and transfer learning. | Extract Pass 1, mark preprint |
| **Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning** | 2024 | Journal | A | Smartphone UWB radar, PSG-synchronized | Samsung UWB line | P0 | High | Strategically important form factor and likely large dataset. | Extract Pass 1 |
| **The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp** | 2026 | Preprint | A | Product-led, 60 GHz FMCW, large radar-PSG dataset | Sleepal line | P0 | Medium-high | Very relevant and large, but preprint/product-led, so keep caveats. | Extract Pass 1, mark preprint |
| **Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar** | 2023 | Journal | A | Radar-only, 60/61 GHz FMCW, unsupervised method | Unique | P0 | High | Good contrast against deep-learning supervised papers; likely useful baseline. | Extract Pass 1 |
| **Deep Learning-Based Automated Diagnosis of Obstructive Sleep Apnea and Sleep Stage Classification in Children Using Millimeter-Wave Radar and Pulse Oximeter** | 2025 | Journal | A | Pediatric, mmWave radar + pulse oximeter, multimodal | Wang pediatric mmWave group | P0 | High | Direct staging, but not radar-only. Extract with multimodal caveat. | Extract Pass 1, flag multimodal |
| **Radar-Based Sleep Stage Classification in Children Undergoing Polysomnography: A Pilot Study** | 2021 | Journal | A | Pediatric UWB radar, PSG | Dutch pediatric UWB line | P0 | High | Strong pediatric PSG benchmark with multiple label granularities. | Extract Pass 1 |
| **Unobtrusive Cot Side Sleep Stage Classification in Preterm Infants Using Ultra-Wideband Radar** | 2023 | Journal | A | Preterm infants, active/quiet sleep, neonatal-specific labels | Dutch neonatal/preterm UWB line | P0 | High | Not adult AASM staging, but direct radar sleep-state/stage classification. | Extract Pass 1 with population caveat |

---

## P1 — extract after P0

| Canonical source title | Year | Source type | Category | Subtype / caveat | Duplicate / version group | Priority | Confidence | Reason | Next action |
|---|---:|---|---:|---|---|---:|---|---|---|
| **Contactless Sleep Staging with Radar: A Transfer Learning Approach** | 2025 | Preprint | A | Preprint version of 2026 journal | Krauss transfer-learning group | P1 | High | Do not extract separately unless preprint has fuller methods/details. | Compare only if journal lacks detail |
| **Deep Learning-Based Automated Diagnosis of OSA and Sleep Stage Classification in Children Using Millimeter-Wave Radar and Pulse Oximeter** | 2024 | Preprint | A | Preprint version of 2025 journal | Wang pediatric mmWave group | P1 | High | Version-linked duplicate. Useful if journal inaccessible or methods differ. | Compare only if needed |
| **Sleep-Stage Estimation Method Based on State Transition Using Millimeter-Wave Radar** | 2024 | Conference | C | State-transition method, mmWave/FMCW, label details unclear | Unique | P1 | Medium | Potentially valuable non-deep-learning method, but needs verification of ground truth and labels. | Chase full paper, then extract if clear |
| **Noncontact Sleep Stage Estimation Using a CW Doppler Radar** | 2018 | Journal | A | Foundational CW Doppler radar staging | Nanjing CW Doppler line | P1 | Medium-high | Important older direct staging paper. Need full text for exact labels/hardware. | Extract after P0 |
| **Sleep Stages Classification by CW Doppler Radar Using Bagged Trees Algorithm** | 2017 | Conference | A | Foundational CW Doppler radar staging | Nanjing CW Doppler line | P1 | Medium-high | Important predecessor/companion to 2018 CW Doppler work. | Extract after P0 |
| **Sleep Stage Classification by Body Movement Index and Respiratory Interval Indices Using Multiple Radar Sensors** | 2015 | Conference | A | Multiple radar sensors, derived movement/respiration indices | Kagawa line | P1 | High | Early direct radar sleep-stage paper. | Extract after P0 |
| **Sleep Stage Classification Based on Bioradiolocation Signals** | 2015 | Conference | A | Bioradar / bioradiolocation, early work | Tataraidze line | P1 | Medium-high | Direct title match and historically important. Need verify details. | Extract after P0 |
| **DoppleSleep: A Contactless Unobtrusive Sleep Sensing System Using Short-Range Doppler Radar** | 2015 | Conference | C | Sleep vs wake and REM vs NREM, weaker/non-PSG labels | UW DoppleSleep line | P1 | Medium | Important foundational paper, but label source appears weaker than PSG. | Extract after P0 with caveat |
| **Distinguishing Sleep from Wake with a Radar Sensor: A Contact-Free Real-Time Sleep Monitor** | 2021 | Journal | B | Sleep/wake only, real-time radar monitor | NTNU / Novelda-linked line | P1 | High | Relevant to sleep/wake and real-time operation, not staging. | Extract after P0 |
| **Sleep-Wake Detection With a Contactless, Bedside Radar Sleep Sensing System** | 2021 | Technical report | B | Google Nest Hub / consumer bedside radar, sleep-wake only | Google Nest line | P1 | High | Very relevant consumer sleep/wake paper, not sleep staging. | Extract after P0 |
| **Non-Contact Sleep/Wake Monitoring Using Impulse-Radio Ultra-Wideband Radar in Neonates** | 2021 | Journal | B | Neonatal sleep/wake, IR-UWB | Neonatal IR-UWB line | P1 | High | In-scope, but sleep/wake only and neonatal-specific. | Extract after adult/pediatric staging papers |

---

## P2 — useful background, not first extraction

| Canonical source title | Year | Source type | Category | Subtype / caveat | Duplicate / version group | Priority | Confidence | Reason | Next action |
|---|---:|---|---:|---|---|---:|---|---|---|
| **A Pilot Study of Impulse Radio Ultra Wideband Radar Technology as a New Tool for Sleep Assessment** | 2018 | Journal | D | Sleep assessment metrics, likely not direct staging | Somnofy / IR-UWB predecessor | P2 | Medium-high | Useful historical predecessor, but appears more sleep-summary than stage classification. | Background extraction only if needed |
| **Contact-Free Radar Recordings of Body Movement Can Reflect Ultradian Dynamics of Sleep** | 2022 | Journal | D | Movement/ultradian dynamics, not clear stage classifier | NTNU / Heglum line | P2 | Medium | Useful mechanistic context, not a primary staging paper. | Hold for background |
| **Observing Ultradian Sleep Dynamics with a Non-Contact Radar Sensor** | 2024 | Conference/abstract | D | Ultradian dynamics, no clear stage classifier | NTNU / Heglum line | P2 | Low-medium | Likely adjacent. Needs full source before more work. | Hold / citation trail |
| **Translating Radar Data into Sleep Insights: A Comparative Study of Machine Learning Models** | 2024 | Poster/other | C or D | ML sleep insights, full details unclear | NTNU / Heglum line | P2 | Low-medium | Potentially relevant but too thin from discovery output. | Chase full abstract/manuscript |
| **RestAware: Non-Invasive Sleep Monitoring Using FMCW Radar** | 2025 | Preprint | C or D | Sleep-state classification claimed in snippet, details unclear | Unique | P2 | Low-medium | Worth checking, but not enough evidence yet to classify as A. | Chase full text before extraction |

---

## Hold — verify before deciding

| Canonical source title | Year | Source type | Category | Subtype / caveat | Duplicate / version group | Priority | Confidence | Reason | Next action |
|---|---:|---|---:|---|---|---:|---|---|---|
| **Sleep Stage Classification Using FMCW Radar Sensor Data and Machine Learning** | 2025 | Conference abstract | A-lite / Hold | Wellune radar, abstract-level only | Wellune line | Hold | Medium | Looks directly relevant, but only abstract-level details were found. | Find full paper or fuller abstract |
| **Any companion JBHI / journal version of Sleepal AI Lamp paper** | Unknown | Unknown | A if exists | Mentioned but not identified | Sleepal line | Hold | Low | The discovery report says a companion submission may exist, but not confirmed. | Search later |
| **Full paper behind RestAware** | 2025 | Preprint | C/D pending | FMCW radar sleep monitoring/classification | RestAware line | Hold | Low-medium | Need verify labels, ground truth, radar details. | Search later |
| **Full version of “Translating Radar Data into Sleep Insights”** | 2024 | Poster/other | C/D pending | ML sleep insights | NTNU line | Hold | Low | Too thin to extract now. | Search later |

---

## Exclude

| Canonical source title | Year | Source type | Category | Subtype / caveat | Duplicate / version group | Priority | Confidence | Reason | Next action |
|---|---:|---|---:|---|---|---:|---|---|---|
| **Learning Sleep Stages from Radio Signals: A Conditional Adversarial Architecture** | 2017 | Conference | G | RF/radio, not clearly radar | MIT RF sleep line | Exclude | Medium-high | Very relevant-looking, but outside radar-only scope unless full text proves radar formulation. | Exclude for now |
| **WiFi-Sleep: Sleep Stage Monitoring Using Commodity Wi-Fi Devices** | 2021 | Journal | G | Wi-Fi sleep staging | Wi-Fi sleep line | Exclude | High | Explicitly Wi-Fi, not radar. | Exclude |
| **SMARS: Sleep Monitoring via Ambient Radio Signals** | 2021 | Journal | G | Ambient RF/radio, not clearly radar | Ambient radio line | Exclude | Medium-high | Outside radar-only scope unless later proven to use radar. | Exclude |

---

# Clean P0 list for Extraction Pass 1

Use these first in the fresh extraction chat:

1. **Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar**
2. **Developing a Deep Learning Model for Sleep Stage Prediction in an OSA Cohort Using 60 GHz FMCW Radar**
3. **Validation of Sleep Stage Classification Using Non-Contact Radar Technology and Machine Learning (Somnofy®)**
4. **Contactless Sleep Staging With Radar: A Transfer Learning Approach**
5. **Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People**
6. **Using Legacy Polysomnography Data to Train a Radar System to Quantify Sleep in Older Adults and People Living with Dementia**
7. **Ultra-Wideband Radar-Based Sleep Stage Classification in Smartphone Using an End-to-End Deep Learning**
8. **The Breakthrough of Sleep: A Contactless Approach for Accurate Sleep Stage Detection Using the Sleepal AI Lamp**
9. **Unsupervised Detection of Multiple Sleep Stages Using a Single FMCW Radar**
10. **Deep Learning-Based Automated Diagnosis of OSA and Sleep Stage Classification in Children Using Millimeter-Wave Radar and Pulse Oximeter**
11. **Radar-Based Sleep Stage Classification in Children Undergoing Polysomnography: A Pilot Study**
12. **Unobtrusive Cot Side Sleep Stage Classification in Preterm Infants Using Ultra-Wideband Radar**

Keep P0 to these **12** for the first extraction chat. Then P1 can be a second extraction batch.

## Mini missing-source chase before extraction

Before starting Extraction Pass 1, do a very small citation-trail search for these:

| Missing / weakly captured source | Why chase it |
|---|---|
| **Kagawa 2016 — Sleep stage classification by non-contact vital signs indices using Doppler radar sensors** | Likely direct radar staging follow-up to Kagawa 2015. |
| **Jiang 2019 — Noncontact Sleep Stage Classification Based on Multi-Sensor Feature-Level Fusion** | May show why radar was combined with other sensors. |
| **Hong 2019 — Microwave sensing and sleep: noncontact sleep-monitoring technology with microwave biomedical radar** | Likely useful review/citation-trail source from CW Doppler group. |
| **Full Wellune radar paper behind 2025 abstract** | Could be directly relevant if a full paper exists. |
| **de Chazal 2011 non-contact biomotion sleep/wake** | Only include if it is truly radar/radar-like, not just adjacent sensing. |

This should be a **small gap-fill**, not a new broad Deep Research pass.
