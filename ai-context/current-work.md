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
- `marketing/post-performance-log.md` records detailed marketing post/campaign execution, metrics, lessons, and follow-up experiments.
- `ai-context/current-work.md` tracks the active work queue, recent completions, blockers, and immediate next steps.

## Current focus

Strengthen the Orisen master-docs repo so ChatGPT can use it as a reliable source-of-truth system for company/product/claims/workflow decisions.

The current phase is evidence, validation, and marketing-learning discipline.

## Immediate next steps

1. Continue filling `validation/evidence-log.md` with real evidence.
   - Add only real evidence.
   - Do not invent user quotes, numbers, test results, or validation.
   - Next likely evidence sources:
     - old prototype tester feedback
     - technical prototype/software progress
     - expert/user conversations
     - more detailed customer language if available

2. Add or refine marketing-learning docs as real data appears.
   - Use `marketing/post-performance-log.md` for detailed content/campaign metrics and lessons.
   - Add future posts to that file as new marketing experiments run.
   - Consider `marketing/customer-voice-log.md` later if enough raw user language exists.

3. Update `product/claims-and-evidence.md` after enough evidence entries are added.
   - Map safe claims, careful claims, unsupported claims, and evidence required for stronger claims.
   - Make sure marketing/fundraising claims stay downstream from evidence.

4. Create `validation/validation-roadmap.md`.
   - Define which claims Orisen wants to eventually make.
   - Define what evidence is required for each claim.
   - Define early pilot/test plans for wake completion, grogginess reduction, sleep inertia, sensor-informed wake behavior, and radar/sleep-stage work.

## In progress

- Evidence collection and classification.
- Converting known Orisen signals into conservative evidence-log entries.
- Capturing marketing execution details and metrics separately from validation claims.

## Blocked or waiting on input

The next evidence-log updates are waiting on additional raw evidence from the founder, such as:

- old prototype tester count
- old prototype tester comments or observed behavior
- customer/user interview notes
- expert call notes
- technical prototype test results
- software build/test milestones that should be classified as built but not customer-validated

The marketing post log can be improved later if the founder provides:

- descriptions or screenshots of the three images used in the launch post
- comment themes from the post
- signup profile details, if available
- future post/campaign metrics

Do not add specific evidence entries until the raw data is provided or available in a trusted source file.

## Recently completed

### 2026-05-18 — Added marketing post performance log

Completed:
- Created `marketing/post-performance-log.md`.
- Added the 2026-02-04 founder LinkedIn waitlist launch post as the first entry.
- Included:
  - exact post copy
  - context, goal, and hypothesis
  - creative/distribution notes
  - performance summary
  - detailed metrics timeline
  - derived metrics
  - what likely worked
  - what was weak or uncertain
  - claim boundaries
  - lessons
  - follow-up experiments

Why:
- The evidence log should classify validation and claim support conservatively.
- The post-performance log should preserve detailed marketing execution data so future content and GTM decisions can learn from what worked and what did not.

### 2026-05-18 — Added waitlist and LinkedIn launch evidence

Completed:
- Updated `validation/evidence-log.md` with the first detailed evidence entry:
  - 66 waitlist signups excluding founder/test signup
  - about 415 estimated total website visits
  - about 16% estimated visitor-to-waitlist conversion
  - one founder LinkedIn post with 23.4k impressions, 197 likes, 69 comments, 296 LinkedIn-reported link visits, 13 sends, and 6 saves
  - limited external sharing from a friend

Classification:
- Early signal.
- Evidence strength: Level 1 to Level 2.

Claim boundary:
- Supports early demand/message-resonance signal.
- Does not prove willingness to pay, retention, product-market fit, broad-market demand, clinical efficacy, grogginess reduction, sleep-stage estimation, or artificial sleep phase transitioning.

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
- `marketing/post-performance-log.md` tracks detailed marketing execution and performance learning
