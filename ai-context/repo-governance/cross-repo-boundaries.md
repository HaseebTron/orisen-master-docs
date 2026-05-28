# Cross-Repo Boundaries

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-27
Governing docs:
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/source-of-truth-rules.md`
- `software/software-read-rules.md`
- `radar-ml/radar-ml-read-rules.md`
Downstream docs:
- `ai-context/start-here.md`
- `ai-context/project-routing.md`
- `software/software-read-rules.md`
- `radar-ml/radar-ml-read-rules.md`
- `HaseebTron/Orisen/docs/repo-boundaries.md`

## Purpose

This file defines the boundary between Orisen's company source-of-truth repo and its implementation repo.

Use this file before deciding whether a software, firmware, app, cloud, radar/ML/control, Codex, GitHub, repo-placement, or source-of-truth-vs-implementation task belongs in `HaseebTron/orisen-master-docs`, `HaseebTron/Orisen`, or both.

## Core Rule

`orisen-master-docs` decides what should be true. Orisen implements, tests, and proves what is true.

## Repo Roles

`HaseebTron/orisen-master-docs` is the company/source-of-truth brain.

It owns:

- company truth and AI operating rules
- product direction, product promise, roadmap, and positioning boundaries
- claims, evidence interpretation, validation requirements, and claim safety
- research interpretation and strategic technical decisions
- source-of-truth docs, read-rules, repo governance, and promotion decisions
- cross-domain decisions that affect software, radar/ML, hardware, marketing, fundraising, or customer promise

`HaseebTron/Orisen` is the implementation/code/testing repo.

It owns:

- firmware, app, backend, cloud, ML service, and integration code
- active slice specs, implementation decisions, experiments, and debugging notes
- build configs, parsers, logging scripts, training and inference code, simulations, and test harnesses
- firmware audio/light logic and device behavior implementation
- test logs, runtime evidence, and implementation reality

## When To Read Only `orisen-master-docs`

Read only `HaseebTron/orisen-master-docs` when the task asks:

- what Orisen should be, promise, prioritize, claim, validate, or fundraise around
- whether a capability belongs in MVP, first customer-ready product, roadmap, or long-term vision
- how research should be interpreted for product, claims, validation, or strategy
- where docs should live or how repo governance should work
- whether implementation results should change source-of-truth docs

## When To Read Only `HaseebTron/Orisen`

Read only `HaseebTron/Orisen` when the task is strictly implementation-local and does not change source-of-truth:

- code changes, build errors, firmware/app/backend debugging, and test execution
- active slice implementation, local architecture, configs, and logs
- parser, logging, model training, inference, simulation, or device behavior work
- Git diffs, file-level code review, dependency changes, or local developer workflow

If the implementation task may affect product promise, claims, roadmap, validation, fundraising, or positioning, read both repos before deciding.

## When To Read Both Repos

Read both repos when a task mixes:

- product truth with implementation behavior
- roadmap or claims with code, logs, experiments, or tests
- radar/ML/control strategy with firmware, parsers, training, inference, simulations, or test logs
- source-of-truth docs with active implementation docs
- Codex/GitHub edits where repo placement is uncertain
- an implementation result that may need promotion into source-of-truth docs

## Wrong-Repo Warning Behavior

Before editing, if the task appears to belong in the other repo, stop and warn the user.

Use this format:

# **REPO BOUNDARY WARNING**

Reason:
- [Why this appears to belong in the other repo.]

Recommended repo:
- [`HaseebTron/orisen-master-docs` or `HaseebTron/Orisen`]

Suggested action:
- [Move the work / split the work / read both repos first / ask before editing.]

Do not continue editing until the repo boundary is clear.

## Promotion Logic

Implementation results from `HaseebTron/Orisen` are evidence, not automatic source-of-truth.

Promote implementation results back into `orisen-master-docs` only when they change or clarify:

- product promise, roadmap, validation status, or claims
- research interpretation or technical feasibility
- fundraising, marketing, positioning, or public language
- architecture assumptions that affect customer experience or reliability promise

Before promotion:

1. Read the relevant source-of-truth docs.
2. Separate observed implementation evidence from interpretation.
3. State what changed, what remains unproven, and which master-docs file should be updated.
4. Update only the source-of-truth docs that become stale, incomplete, or contradictory.

Do not use implementation docs or test logs to silently redefine company truth.

## Radar/ML/Control Split

These belong in `HaseebTron/orisen-master-docs`:

- TI radar decisions
- vital-sign strategy
- sleep-stage model approach
- intervention-loop theory
- validation plans
- claims boundaries
- research interpretation that affects product, roadmap, fundraising, or positioning

These belong in `HaseebTron/Orisen`:

- TI radar firmware
- parsers and logging scripts
- ML training and inference code
- controller simulations
- firmware audio/light logic
- test logs and experiment outputs

If radar/ML/control work includes both strategy and implementation, split the work or read both repos before editing.

## Claims Safety Rule

If radar/ML/control work affects public claims, product promise, roadmap, fundraising, or positioning, escalate to Orisen General and `orisen-master-docs` before treating it as truth.

Do not treat technical possibility, a successful test, a paper result, or a model output as a public Orisen claim until the relevant source-of-truth and claim-control docs support it.
