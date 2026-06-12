# Radar Sleep-Stage Literature Review Workflow

Status: Working strategy
Authority level: Radar/ML research workflow
Last reviewed: 2026-06-12
Governing docs:
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/claim-control/claim-control-system.md`
- `radar-ml/radar-ml-read-rules.md`
Downstream docs:
- `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/extraction-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/primary-source-chase-pass-1-2026-06-12.md`

## Purpose

This file preserves the workflow, intent, scope, current state, completed passes, next steps, and handoff instructions for the radar sleep-stage literature review.

It is meant to let a new ChatGPT chat continue the review without needing the old planning chat.

Keep raw research artifacts separate from this workflow/status document. The raw files preserve source material and working extraction passes; this file explains how to continue the work.

This file must not turn the literature review into Orisen product claims.

## Scope

The current research scope is radar-based sleep-stage, sleep-phase, sleep-state, and sleep/wake classification.

Radar vital-sign-only papers are out of scope unless the vital-sign signals directly feed into sleep-stage or sleep-state classification.

Exclude WiFi CSI, camera, microphone, wearable-only, ECG-only, PPG-only, bed pressure-only, and mattress sensor-only sources unless they are explicitly needed as background for feature design, validation design, or comparison.

Prioritize sources that connect radar signals to PSG labels, sleep-stage labels, sleep-state labels, or sleep/wake labels.

## What this workflow is trying to answer

This workflow is trying to determine:

- Which radar devices, radar types, and signal outputs have been used for sleep-stage or sleep-state classification.
- Which radar-derived inputs and features repeatedly appear in credible papers.
- Whether respiration and movement are enough, or whether papers rely on HR, HRV, RRV, waveform, phase, IQ, or raw/semi-raw radar data.
- Which methods, datasets, and feature pipelines look reproducible for Orisen.
- Which papers are least applicable to Orisen because of population, hardware, label, validation, or modality mismatch.
- What radar data access Orisen should require before trusting a module for sleep-stage-aware wake intervention experiments.
- What Orisen should test before relying on sleep-stage-aware or sleep-state-aware intervention.

## Full intended workflow

### Phase 1: Discovery using Deep Research

#### 1A: Search papers/preprints

- Focus only on radar -> sleep-stage / sleep-state / sleep-wake classification.
- Exclude papers that only do HR/RR/vital signs unless those signals are used for sleep-stage classification.
- Prioritize 2020-2026, but include older foundational papers if important.
- Status: completed in `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`.

#### 1B: Search GitHub repos

- Search after the paper list is made.
- Use paper titles, author names, model names, dataset names, and keywords from the papers.
- Separate true radar sleep-stage repos from generic sleep-stage or vital-sign repos.
- Status: not started.

#### 1C: Search datasets

- Look for datasets with radar + PSG/sleep labels.
- Also note non-radar datasets only if they are useful for feature/model design.
- Status: not started.

#### 1D: Search patents/company material only if needed

- Use for background and competitive intelligence.
- Do not treat patents as validation.
- Status: not started.

### Phase 2: GPT review / screening

- Deduplicate all sources.
- Categorize each source:
  - A: Direct radar sleep-stage classification.
  - B: Radar sleep/wake classification.
  - C: Radar sleep-state estimation with PSG or sleep labels.
  - D: Radar sleep monitoring but no clear stage/state classification.
  - E: Radar vital signs only, save for later.
  - F: Non-radar sleep-stage feature guidance, save for later.
  - G: Exclude.
- Decide which papers are worth full extraction.
- Status: Screening Pass 1 completed in `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`.

### Phase 3: First extraction pass

- For each included paper, extract objective facts:
  - Hyperlinked title.
  - Year.
  - Specific radar/device/chip/module used.
  - Radar type.
  - Frequency.
  - Placement and distance.
  - Subject count / nights.
  - Ground truth.
  - Sleep labels predicted.
- If the paper does not state the exact radar, write "not stated."
- Do not guess the radar model.
- Status: Extraction Pass 1 completed in `radar-ml/radar-sleep-stage-literature/raw/extraction-pass-1-2026-06-12.md`.

### Phase 4: Second extraction pass

- Extract deeper technical details:
  - Radar inputs/features used.
  - Whether they used respiration, motion, HR, HRV, RRV, waveform, phase, IQ, radar cube, etc.
  - Model/method.
  - Epoch length.
  - Accuracy / kappa / F1 / sensitivity / specificity.
  - Real-time vs offline.
  - Code/data availability.
  - Key limitations.
  - Relevance to Orisen.
- Status: likely next step, but only after classifying which papers are ready vs pending.

### Phase 5: Verification pass

- Re-check the most important papers.
- Verify:
  - Exact radar used.
  - Exact input features.
  - Exact ground truth.
  - Exact performance numbers.
  - Whether code/data are actually available.
- Add confidence labels:
  - High: directly stated and verified.
  - Medium: strongly implied.
  - Low: uncertain.
  - Not stated: paper does not say.
- Status: partially started through `primary-source-chase-pass-1-2026-06-12.md`, but not complete for all papers.

### Phase 6: Synthesis

- Answer:
  - Which radars were most commonly used?
  - Which radar types seem most promising?
  - What features are repeatedly used for radar sleep staging?
  - Is respiration + movement enough, or do papers rely on HR/HRV too?
  - What accuracy/kappa ranges are realistic?
  - Which methods seem reproducible?
  - Which papers are least applicable to Orisen?
  - What radar data access should Orisen require?
  - What should Orisen test before trusting sleep-stage-aware wake intervention?
- Status: not started.

### Phase 7: Orisen decision output

- Convert the research into practical recommendations:
  - Best radar candidates to investigate.
  - Minimum required radar outputs.
  - Red flags for black-box sensors.
  - Experiments to run first.
  - Claims Orisen still cannot make.
- Status: not started.

## Completed passes

Completed raw passes:

1. Deep Research discovery pass.
2. Screening Pass 1.
3. Extraction Pass 1.
4. Primary-Source Chase Pass 1.

These are working research artifacts, not claim-control approvals and not Orisen product evidence.

## Archived raw files

All completed raw artifacts are archived under:

`radar-ml/radar-sleep-stage-literature/raw/`

Use `ai-context/repo-governance/repo-file-map.md` for the durable file inventory. Do not duplicate the full raw file tree in this workflow doc.

The current archived artifacts are:

- `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/extraction-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/primary-source-chase-pass-1-2026-06-12.md`

## Current state

The literature review has completed discovery, first screening, first objective extraction for screened P0 sources, and a partial primary-source chase for weak P0 rows.

The review is not ready for synthesis yet because several important papers still have unresolved primary-source details, and the next pass should first classify each paper by readiness.

Do not synthesize Orisen implications yet beyond technical relevance. Current Orisen source-of-truth docs still treat validated sleep-stage sensing, vital-sign sensing, grogginess reduction, sleep-inertia reduction, and sleep-stage-aware intervention as unvalidated.

## Current completed work

Current completed work:

- Discovery Pass 1 found candidate radar sleep-stage, sleep-state, and sleep/wake classification papers and separated likely false positives.
- Screening Pass 1 deduplicated and prioritized the candidate source list, including P0, P1, P2, Hold, and Exclude groups.
- Extraction Pass 1 extracted objective top-level details for the 12 screened P0 sources.
- Primary-Source Chase Pass 1 improved or confirmed unresolved details for several weak P0 rows, but did not resolve all primary-source gaps.

Current handoff state:

- The next chat should not start a broad synthesis.
- The next chat should read this workflow file first, then load only the raw artifacts needed for the immediate task.
- The next chat should classify papers as ready vs pending before starting Extraction Pass 2.
- The next chat should stop after readiness classification unless the user explicitly asks it to proceed into Extraction Pass 2.
- The next chat should preserve the raw files and write any new pass as a new file unless the user explicitly requests patching an existing raw artifact.

## Classification scheme

Use this scheme when screening or re-screening sources:

- A: Direct radar sleep-stage classification
- B: Radar sleep/wake classification
- C: Radar sleep-state estimation with PSG or sleep labels
- D: Radar sleep monitoring but no clear stage/state classification
- E: Radar vital signs only
- F: Non-radar sleep-stage source
- G: Exclude

Radar vital-sign-only sources belong in E unless the vital signs directly feed sleep-stage or sleep-state classification.

Non-radar sleep-stage sources belong in F only when they are useful for feature design, model design, validation design, or comparison. Otherwise exclude them.

## Readiness categories for Extraction Pass 2

Before Extraction Pass 2, assign each source one of these readiness categories:

- Ready for Extraction Pass 2
- Needs primary-source access first
- Needs bibliographic cleanup
- Duplicate / merge with another source
- Exclude
- Background only

Do not run deeper extraction on a paper whose identity, primary source, radar involvement, or label set is still too uncertain.

## Immediate next step

The likely immediate next step is `Extraction Pass 2`, but only after reading the archived files and classifying papers as ready vs pending.

The immediate next-chat task should be:

1. Read this workflow file.
2. Read `extraction-pass-1-2026-06-12.md` and `primary-source-chase-pass-1-2026-06-12.md`.
3. Read `screening-pass-1-2026-06-12.md` only if needed to confirm the original P0 list.
4. Read `discovery-pass-2026-06-12.md` only as needed for traceability or citation backtracking.
5. Classify the 12 P0 papers as ready vs pending for Extraction Pass 2.
6. Stop and wait for user approval before running Extraction Pass 2.

Extraction Pass 2 should extract:

- radar inputs/features used
- respiration waveform
- breathing rate
- breath-to-breath intervals / RRV / BRV
- heart rate
- heartbeat waveform
- inter-beat intervals / HRV
- movement/body motion
- posture
- radar phase / range-bin phase
- IQ / complex samples
- radar cube / raw or semi-raw radar data
- model/method
- epoch length
- reported performance: accuracy / F1 / Cohen's kappa / sensitivity / specificity
- real-time vs offline
- code/data availability
- key limitations
- reproducibility
- relevance to radar-based sleep-stage classification
- confidence level for extracted facts

Extraction Pass 2 should be objective extraction, not synthesis. It should record what each paper states, what is inferred, and what remains not stated.

## Rules for future chats

Before continuing this review, read:

- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/claim-control/claim-control-system.md`
- `radar-ml/radar-ml-read-rules.md`
- `radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`

For the next readiness-classification task, also read:

- `radar-ml/radar-sleep-stage-literature/raw/extraction-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/primary-source-chase-pass-1-2026-06-12.md`

Read these only as needed:

- `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`: use to confirm the original P0 list, categories, and source priority.
- `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`: use for traceability, citation backtracking, or source-discovery context.

Rules:

- Do not guess missing details.
- If the paper does not state something, write "not stated."
- Separate direct paper statements from inference.
- Prefer primary-source verification over Deep Research summaries.
- Keep citations and links traceable.
- Preserve confidence labels for extracted facts.
- Keep radar-only, radar-plus-other-sensor, and non-radar sources separate.
- Do not silently merge preprint and journal versions without noting the version relationship.
- Do not rewrite or overwrite raw artifacts unless the user explicitly asks.
- Do not write to the repo unless the user explicitly asks.

## Claim boundary

Do not treat papers as proof that Orisen can currently detect sleep stages, reduce grogginess, reduce sleep inertia, move users between sleep stages, or perform sleep-stage-aware wake intervention.

This literature review is technical evidence, design guidance, radar-selection input, and validation-planning input only.

Any future Orisen claim about sleep-stage sensing, vital-sign sensing, grogginess reduction, sleep-inertia reduction, sleep-phase-aware intervention, artificial sleep phase transitioning, or public product capability must go through Orisen-specific validation and claim-control review.

## Handoff prompt for a new chat

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

This is a continuation of the Orisen Radar + ML radar sleep-stage literature workflow.

Read and follow:

`radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`

Do not rely on memory from prior chats.
Do not write to the repo unless I explicitly ask.
Do not make Orisen product claims.

For this turn, do only the handoff/readiness step:

1. Confirm what files you read.
2. Summarize the current workflow state.
3. Classify the 12 P0 sources into:
   - Ready for Extraction Pass 2
   - Pending full-text/PDF/primary-source access
4. Explain what you recommend doing next.
5. Stop. Do not run Extraction Pass 2 yet.
```
