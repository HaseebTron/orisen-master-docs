# Radar and ML Context Map

## Purpose

This file is the routing map for Orisen radar, signal processing, sleep-stage modeling, and intervention-loop work.

Use it to decide which docs to read for radar module decisions, vital-sign extraction, movement extraction, datasets, model design, sleep-stage estimation, and artificial sleep phase transitioning experiments.

This file does not replace product, claims, validation, or engineering docs.

## Always read first for important radar/ML work

For radar/ML work that may affect product claims, roadmap, or fundraising, start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `validation/evidence-log.md`

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

## Main workstreams

### Radar module evaluation

Use for:

- XM125 / Acconeer A121 evaluation
- V-LD3 / TI radar evaluation
- Sensor placement
- Signal quality
- Hardware/software tradeoffs

### Signal processing

Use for:

- Respiratory rate variability
- Heart rate variability
- Movement detection
- Presence detection quality
- Raw radar data versus manufacturer pipeline outputs

### Sleep-stage modeling

Use for:

- Feature engineering
- Sleep-stage classification
- Dataset selection
- Research paper interpretation
- Model accuracy requirements
- Real-time model constraints

### Intervention loop

Use for:

- Sensor-informed wake intervention
- Gradual audio/light feedback loop
- Artificial sleep phase transitioning experiments
- Measuring whether interventions reduce perceived grogginess

## Claims boundary

Radar/ML work may support future claims, but it does not create public claims by itself.

Escalate to Orisen General before changing claims around:

- Sleep-stage detection accuracy
- Grogginess reduction
- Sleep inertia reduction
- Artificial sleep phase transitioning
- Real-time sleep-state control
- Clinical or medical claims

## Current status

This is a starter context map.

Detailed radar/ML docs should be added as the work becomes active.

## Planned docs

Potential future docs:

- `radar-ml/radar-module-decision.md`
- `radar-ml/vital-signs-pipeline.md`
- `radar-ml/sleep-stage-model.md`
- `radar-ml/intervention-loop.md`
- `radar-ml/research-notes.md`
- `radar-ml/technical-validation.md`
