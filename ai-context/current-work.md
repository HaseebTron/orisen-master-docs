# Current Work

## Purpose

This file tracks the active operational work happening in the Orisen master-docs repo.

Use it when the user asks:

- what are the next steps?
- what did we just finish?
- what is blocked?
- what should I do next?
- where did we leave off?

This file is not a replacement for source-of-truth docs, the decision log, the evidence log, or the repo backlog.

## Relationship to other tracking docs

- `ai-context/decision-log.md` records major decisions and why they were made.
- `ai-context/repo-backlog.md` records future docs, cleanup items, and recurring checks.
- `validation/evidence-log.md` records real evidence and what claims it supports.
- `ai-context/current-work.md` tracks the active work queue, recent completions, blockers, and immediate next steps.

## Current focus

Strengthen the Orisen master-docs repo so ChatGPT can use it as a reliable source-of-truth system for company/product/claims/workflow decisions.

The current phase is moving from repo architecture into evidence and validation discipline.

## Immediate next steps

1. Fill `validation/evidence-log.md` with real evidence.
   - Add only real evidence.
   - Do not invent user quotes, numbers, test results, or validation.
   - Start with old prototype feedback, waitlist/signup data, LinkedIn post performance, technical prototype progress, and expert/user conversations.

2. Update `product/claims-and-evidence.md` after evidence entries are added.
   - Map safe claims, careful claims, unsupported claims, and evidence required for stronger claims.
   - Make sure marketing/fundraising claims stay downstream from evidence.

3. Create `validation/validation-roadmap.md`.
   - Define which claims Orisen wants to eventually make.
   - Define what evidence is required for each claim.
   - Define early pilot/test plans for wake completion, grogginess reduction, sleep inertia, sensor-informed wake behavior, and radar/sleep-stage work.

4. Later, create `marketing/customer-voice-log.md` if enough raw user language exists.
   - Store raw customer language separately from source-of-truth strategy.
   - Use it to improve messaging without treating every quote as validated proof.

## In progress

- Evidence collection and classification planning.
- Preparing to convert known Orisen signals into conservative evidence-log entries.

## Blocked or waiting on input

The evidence-log update is waiting on raw evidence from the founder, such as:

- old prototype tester count
- old prototype tester comments or observed behavior
- exact waitlist/signup numbers
- website visitor numbers or conversion rates, if available
- LinkedIn post performance details
- customer/user interview notes
- expert call notes
- technical prototype test results
- software build/test milestones that should be classified as built but not customer-validated

Do not add specific evidence entries until the raw data is provided or available in a trusted source file.

## Recently completed

### 2026-05-18 — Added current work tracker

Completed:
- Created `ai-context/current-work.md` to track active next steps, completed work, blockers, and deferred items.

Why:
- Future chats should be able to answer "what next?" from repo state instead of relying on chat scrollback.

### 2026-05-18 — Clarified copied software snapshot docs

Completed:
- Updated `software/software-context-map.md` to explain that some files in the `software/` folder are copied or synced from the separate software implementation repo.
- Clarified that copied software docs are context snapshots, not the live software source of truth.
- Clarified that `HaseebTron/Orisen` wins for live implementation reality.
- Clarified that higher-level master-docs files win for product truth, roadmap meaning, claims, and customer promise.

### 2026-05-18 — Added strategic decision-log entries

Completed:
- Added decision-log entries for:
  - presence-based wake completion as the first wedge
  - painful wake-up users as the first target audience
  - non-contact product direction
  - hardware-led product direction
  - engineering MVP not shrinking first customer-ready product vision
  - grogginess reduction and sleep-phase-aware intervention as strategic but claim-sensitive

### 2026-05-18 — Added repo integrity check workflow

Completed:
- Added a `Repo integrity check session` section to `ai-context/start-here.md`.
- Added recurring repo integrity check item to `ai-context/repo-backlog.md`.

### 2026-05-18 — Fixed software/product authority ambiguity

Completed:
- Updated `ai-context/source-of-truth-rules.md` with a product-scope authority tiebreaker.
- Added authority notes to:
  - `software/p1-overview.md`
  - `software/p2-mvp-scope.md`

### 2026-05-18 — Strengthened AI operating behavior

Completed:
- Updated `ai-context/ai-operating-mode.md` with:
  - incoming information rule
  - stronger conflict handling
  - stop-and-surface rule for task-relevant conflicts

### 2026-05-18 — Fixed product context map stale listings

Completed:
- Updated `product/product-context-map.md` so existing product docs are listed as stable instead of planned.
- Added validation docs to claims/evidence routing.

## Deferred / not now

- Do not create `ai-context/master-context-paste.md` right now.
  - Reason: current workflow assumes ChatGPT can read GitHub directly.
  - Revisit only if another AI tool or workflow needs a pasteable fallback context pack.

- Do not create creative strategy docs yet, such as:
  - red-team docs
  - assumption graveyard
  - strategic tripwires
  - parallel-worlds docs
  - kill-condition docs

Reason:
- The repo needs real evidence and decision memory first, not more architecture.

## Update rule

Update this file when:

- a meaningful work item is completed
- the immediate next steps change
- a blocker appears or is resolved
- a new active workstream starts
- a current workstream is intentionally deferred

Do not update this file for every tiny wording edit or minor formatting cleanup.

When in doubt:

- `current-work.md` tracks operational status
- `decision-log.md` tracks durable decisions
- `repo-backlog.md` tracks future cleanup and missing docs
- `evidence-log.md` tracks real evidence
