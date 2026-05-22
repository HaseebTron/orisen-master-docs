# Radar and ML Context Map

## Purpose

This file is the routing map for Orisen radar, signal processing, sleep-stage modeling, and intervention-loop work.

Use it to decide which docs to read for radar module decisions, vital-sign extraction, movement extraction, datasets, model design, sleep-stage estimation, and artificial sleep phase transitioning experiments.

This file does not replace product, claims, validation, or engineering docs.

## File inventory rule

This file does not maintain this folder's file inventory.

For the current repo-wide file map, see:

- `ai-context/repo-file-map.md`

This context map should define task-based reading paths, not duplicate folder structure or current/planned file inventories.

## Always read first for important radar/ML work

For radar/ML work that may affect product claims, roadmap, or fundraising, start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`

## Radar/ML folder role

The radar/ML docs should define:

- Radar module evaluation
- Vital-sign extraction strategy
- RRV extraction
- HRV extraction
- Movement extraction
- Sleep-stage model approach
- Dataset and paper notes
- Model validation approach
- Sensor-informed wake intervention logic
- Artificial sleep phase transitioning experiments
- Technical evidence needed before stronger claims

## Mid-chat context expansion

If a radar/ML chat later asks a more specific technical question than the initial baseline docs covered, expand context inside the same chat instead of rerunning the full boot workflow.

Before answering, read this context map and the most relevant task-specific docs below.

State which extra files were read when the context expansion is meaningful.

If a radar/ML question changes product truth, public claims, roadmap priority, first customer-ready product scope, marketing claims, or fundraising story, escalate to Orisen General.

## Main workstreams and routing

### Radar module evaluation

Use for questions like:

- Should Orisen use XM125 / Acconeer A121?
- Should Orisen use V-LD3 or a TI-based radar module?
- Which module is better for presence, breathing, heart signal, RRV, HRV, or sleep staging?
- What are the hardware/software tradeoffs?
- What radar module should be tested first?

Read:

- `radar-ml/radar-module-decision.md` if it exists
- `hardware/hardware-context-map.md` if hardware constraints matter
- `software/software-context-map.md` if firmware integration matters
- `product/roadmap.md`
- `product/claims-and-evidence.md`

### Signal processing and feature extraction

Use for questions like:

- How do we extract respiratory rate variability?
- How do we extract heart rate variability?
- How do we extract movement?
- Should we use raw radar data or manufacturer pipeline outputs?
- What data quality is needed for sleep-stage modeling?

Read:

- `radar-ml/vital-signs-pipeline.md` if it exists
- `radar-ml/research-notes.md` if it exists
- `radar-ml/technical-validation.md` if it exists
- `software/software-context-map.md` if firmware or data logging matters

### Sleep-stage modeling

Use for questions like:

- How should Orisen classify sleep stages?
- Which features should feed the model?
- Which papers or datasets matter?
- How accurate does the model need to be?
- Should Orisen use HRV, RRV, movement, or radar-derived features?
- What is realistic for MVP, pilot, and v1?

Read:

- `radar-ml/sleep-stage-model.md` if it exists
- `radar-ml/research-notes.md` if it exists
- `radar-ml/vital-signs-pipeline.md` if it exists
- `radar-ml/technical-validation.md` if it exists
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`

### Paper, repo, and dataset review

Use for questions like:

- What does this paper actually prove?
- Does this GitHub repo take raw radar data or derived features?
- Can we reuse this model?
- Which dataset should we use?
- What are the limitations of a study?

Read:

- `radar-ml/research-notes.md` if it exists
- `radar-ml/sleep-stage-model.md` if it exists
- `radar-ml/vital-signs-pipeline.md` if it exists

Also read the external paper, repo, or dataset directly when provided or when current accuracy matters.

Do not infer that a paper proves Orisen's product claims unless the evidence is directly applicable.

### Intervention loop

Use for questions like:

- How should audio/light interventions respond to sensed sleep state?
- Can Orisen move someone from deep sleep to light sleep before waking?
- What would artificial sleep phase transitioning require?
- How do we test whether intervention reduces grogginess?
- What should be MVP versus long-term?

Read:

- `radar-ml/intervention-loop.md` if it exists
- `radar-ml/sleep-stage-model.md` if it exists
- `radar-ml/technical-validation.md` if it exists
- `product/roadmap.md`
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`

### Technical validation

Use for questions like:

- What do we need to validate before claiming sleep-stage awareness?
- What tests should we run first?
- What evidence is needed for radar signal quality?
- How do we decide whether a radar/ML approach is good enough?

Read:

- `radar-ml/technical-validation.md` if it exists
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`

If a referenced doc does not exist yet, use the available upstream docs and recommend creating the missing doc only if the task requires it.

## Claims boundary

Radar/ML work may support future claims, but it does not create public claims by itself.

Escalate to Orisen General before changing claims around:

- Sleep-stage detection accuracy
- Grogginess reduction
- Sleep inertia reduction
- Artificial sleep phase transitioning
- Real-time sleep-state control
- Clinical or medical claims

## Radar/ML interpretation rules

- Radar/ML docs are downstream from product truth and evidence boundaries.
- Do not treat technical possibility as validated product evidence.
- Do not turn research-paper claims into Orisen public claims without evidence.
- Separate presence detection, vital-sign extraction, sleep-stage estimation, and intervention control.
- Presence-based wake completion is the validated wedge.
- Sleep-stage-aware intervention and artificial sleep phase transitioning are strategically important but currently need technical validation and careful claims.
- If a radar/ML decision changes product roadmap or public claims, escalate to Orisen General.
