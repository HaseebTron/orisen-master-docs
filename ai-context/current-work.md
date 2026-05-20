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
- `validation/evidence-roadmap.md` tracks evidence categories, missing evidence, and where each evidence type lives.
- `validation/evidence-log.md` records real evidence and what claims it supports.
- `validation/evidence-standard.md` defines evidence-strength and classification rules.
- `marketing/post-performance-log.md` records detailed marketing post/campaign execution, metrics, lessons, and follow-up experiments.
- `product/old-mvp.md` records detailed historical context about the old physical MVP/prototype.
- `ai-context/current-work.md` tracks the active work queue, recent completions, blockers, and immediate next steps.

## Current focus

Strengthen the Orisen master-docs repo so ChatGPT can use it as a reliable source-of-truth system for company/product/claims/workflow decisions.

The current phase is upstream evidence, ICP, and claim-boundary cleanup before moving into Orisen Marketing for X/Twitter execution.

## Immediate next steps

### 1. Update `product/target-customer.md`

Use the now-captured evidence base:

- summer 2024 customer interviews
- old MVP prototype/pilot evidence
- old MVP user feedback
- LinkedIn/waitlist evidence
- Leila Jalali expert commentary
- evidence weighting rules in `validation/evidence-roadmap.md`

Goal:

- Sharpen the primary ICP around people who repeatedly fail between alarm time and actually being out of bed.
- Make clear this is not for generic alarm-clock users or casual sleep optimizers.
- Treat student/full-time/gender/age/etc. patterns as hypotheses only, not validated segment conclusions.
- Treat teens/young adults and shift workers as segments worth investigating, not validated demographic ICPs.

### 2. Update `product/claims-and-evidence.md`

Use the same evidence base to clarify:

- safe claims
- careful claims
- unsupported claims
- roadmap claims
- evidence required to strengthen claims

Goal:

- Keep marketing and fundraising downstream from evidence.
- Clearly separate wake-completion evidence from unvalidated grogginess, sleep inertia, sleep-stage detection, and artificial sleep phase transitioning claims.
- Incorporate expert caution that grogginess and sleep inertia are multi-cause and that sleep-stage intervention likely requires continuous feedback-based validation.

### 3. Then move to Orisen Marketing for X execution

After the two upstream docs above are updated, start a fresh chat in the Orisen Marketing project for:

- `marketing/positioning-and-messaging.md`
- `marketing/twitter-content-strategy.md`
- `marketing/customer-voice-log.md`
- `marketing/twitter-post-bank.md`
- actual X/Twitter posts

## In progress

- Evidence collection and classification.
- Converting known Orisen signals into conservative evidence-log entries.
- Capturing marketing execution details and metrics separately from validation claims.
- Capturing old MVP/prototype history, pilot details, and technical evidence.
- Preparing upstream product/customer/claim docs for marketing use.

## Evidence currently captured

### Direct customer discovery

Source files:

- `research/customer-interviews/raw/2024-alarm-clock-responses.csv`
- `research/customer-interviews/2024-alarm-clock-interviews.md`

Status:

- Captured as small-sample qualitative discovery.
- Useful for pain patterns and customer language.
- Not valid for subgroup conclusions by occupation, gender, ethnicity, religion, age, student/full-time status, or living situation.

### Prototype / pilot evidence

Source files:

- `product/old-mvp.md`
- `product/old-mvp-test-row-labels.md`
- `product/old-mvp-bypass-and-failure-notes.md`
- `product/old-mvp-user-feedback.md`
- `validation/evidence-log.md`

Status:

- Strongest current support for wake-completion wedge.
- Supports early signal that presence-based wake completion can get users out of bed closer to alarm time.
- Does not prove production reliability, broad robustness, reduced grogginess, reduced sleep inertia, sleep-stage-aware intervention, or artificial sleep phase transitioning.

### Traffic from website / marketing

Source files:

- `marketing/post-performance-log.md`
- `validation/evidence-log.md`

Status:

- One founder LinkedIn post and limited external sharing.
- 66 waitlist signups excluding founder/test signup.
- About 22% internal high-intent/relevant traffic conversion estimate.
- About 16% blended historical conversion.
- About 6% later lower-intent incremental conversion.
- Useful as early demand/message-resonance signal, not paid validation.

### Expert commentary

Source files:

- `research/external-research/expert-commentary/raw/leila-jalali-meeting-notes.md`
- `research/external-research/expert-commentary/expert-commentary.md`
- `validation/evidence-log.md`

Status:

- Captured as expert commentary / early external validation / claim-discipline input.
- Useful for technical plausibility, claim discipline, and future research direction.
- Supports treating artificial sleep phase transitioning as a plausible but unvalidated roadmap hypothesis.
- Supports caution that grogginess and sleep inertia are multi-cause and should not be claimed as solved without direct validation.
- Does not prove Orisen efficacy, clinical validation, market demand, or hard demographic segment conclusions.

### External market / literature / community evidence

Source file:

- `validation/evidence-roadmap.md`

Status:

- Roadmap created.
- Expert commentary is partially filled.
- Other external source files are still mostly missing.
- `validation/evidence-roadmap.md` now defines the future raw/source folder convention.

Future source files may include:

- `research/external-research/sleep-inertia/sleep-inertia-research.md`
- `research/external-research/market-reports/market-research-notes.md`
- `research/external-research/articles-and-media/articles-and-media-notes.md`
- `research/external-research/reddit-forums/reddit-customer-language.md`
- `research/external-research/competitor-reviews/competitor-review-research.md`
- more files under `research/external-research/expert-commentary/`

Each future category may have a `raw/` folder when there is actual raw/source material to store.

## Blocked or waiting on input

No blocker for the immediate next step.

Useful future inputs:

- more customer interviews, especially severe oversleepers/heavy sleepers
- screenshots/descriptions of the three LinkedIn launch post images
- waitlist signup profile data, if available
- exact old MVP tester quotes, if recoverable
- old MVP photos/videos/diagrams
- external research sources: papers, competitor reviews, Reddit/forum threads, market reports, articles, expert notes

## Recently completed

### 2026-05-19 — Added Leila Jalali expert commentary evidence

Completed:

- Created `research/external-research/expert-commentary/raw/leila-jalali-meeting-notes.md`.
- Created `research/external-research/expert-commentary/expert-commentary.md`.
- Updated `validation/evidence-log.md` with an expert commentary evidence entry.
- Updated `validation/evidence-roadmap.md` to mark expert commentary as partially filled.
- Added sleep spindles and arousal threshold to future sleep-inertia research topics.

Key interpretation:

- Artificial sleep phase transitioning is a plausible but unvalidated roadmap hypothesis.
- If pursued, it likely requires continuous feedback-based intervention, not a one-time shift.
- Grogginess and sleep inertia are multi-cause and must stay claim-sensitive.
- Teens/young adults and shift workers are worth investigating, but not validated ICPs from this alone.

Claim boundary:

- Does not prove Orisen reduces grogginess.
- Does not prove Orisen reduces sleep inertia.
- Does not prove Orisen detects or manipulates sleep stages.
- Does not prove Orisen has clinical validation.
- Does not prove hard demographic segment conclusions.

### 2026-05-18 — Added raw/source data convention

Completed:

- Moved the summer 2024 interview raw CSV into `research/customer-interviews/raw/2024-alarm-clock-responses.csv`.
- Removed the duplicate CSV from `research/customer-interviews/2024-alarm-clock-responses.csv`.
- Updated `research/customer-interviews/2024-alarm-clock-interviews.md` to point to the new raw CSV path.
- Updated `validation/evidence-roadmap.md` with a raw data / synthesis convention.
- Updated future external-research paths to use category folders with optional `raw/` subfolders.

Why:

- Raw/source data should stay separate from synthesis and interpretation.
- The repo should avoid duplicating raw data.
- Future external research should follow the same source-to-synthesis evidence chain.

### 2026-05-18 — Added evidence roadmap

Completed:

- Created `validation/evidence-roadmap.md`.
- Defined four main evidence categories:
  - Direct customer discovery
  - Prototype / pilot evidence
  - Traffic from website / marketing
  - External market / literature / community evidence
- Made the evidence roadmap an index/to-do file that points to detailed evidence files instead of duplicating them.
- Added future external research categories for:
  - sleep inertia research
  - market reports/surveys
  - articles/media notes
  - Reddit/forum posts
  - competitor product reviews
  - sleep clinic/expert commentary

Why:

- The repo needs a category-specific evidence roadmap so future chats know what evidence exists, what is missing, and where the detailed source files live.

### 2026-05-18 — Added 2024 customer interview data and synthesis

Completed:

- Created `research/customer-interviews/raw/2024-alarm-clock-responses.csv`.
- Created `research/customer-interviews/2024-alarm-clock-interviews.md`.
- Added small-sample qualitative synthesis of summer 2024 campus/mall interviews.
- Clarified that this data can support pain-pattern hypotheses and customer language, but not statistical segmentation.

Classification:

- User interview evidence / early customer discovery.
- Evidence strength: Level 1 to Level 2.

Claim boundary:

- Supports the hypothesis that some users have repeated wake-up/get-out-of-bed problems and that non-camera sensing has privacy value.
- Does not prove market size, willingness to pay, product-market fit, subgroup segment ranking, or Orisen efficacy.

### 2026-05-18 — Clarified high-intent waitlist conversion

Completed:

- Updated `marketing/post-performance-log.md`.
- Updated `validation/evidence-log.md`.
- Separated conversion into:
  - about 22% high-intent / relevant-traffic conversion estimate
  - about 16% blended historical conversion
  - about 6% later lower-intent incremental conversion

Claim boundary:

- The 22% number is an internal directional estimate for relevant early launch traffic, not a universal website conversion rate.

### 2026-05-18 — Added old MVP qualitative user feedback

Completed:

- Created `product/old-mvp-user-feedback.md`.
- Updated `validation/evidence-log.md`.
- Captured that testers said the old MVP was much better at waking them on time compared with before.
- Captured Dennis's founder-reported purchase-interest signal around a roughly $100 discussed price point.
- Captured user pull for easier wake-up / less-groggy direction.

Claim boundary:

- Supports wake-completion value and roadmap pull.
- Does not prove paid demand, price point, reduced grogginess, sleep inertia reduction, or artificial sleep phase transitioning.

### 2026-05-18 — Added old MVP pilot/test evidence

Completed:

- Updated `product/old-mvp.md` with detailed old MVP pilot/test participant data for:
  - founder
  - Hamza/Humza
  - Dennis
  - Sabeeh
- Added detailed test definitions for bed time, alarm time, wake-up time, get-out-of-bed time, sleepy rating, irritation rating, mood rating, and energy rating.
- Added Dennis, Hamza/Humza, and Sabeeh test tables.
- Added tester-specific interpretations and limitations.
- Updated `validation/evidence-log.md` with a pilot/test evidence entry.

Classification:

- Early validation / small prototype pilot signal.
- Evidence strength: Level 2 to early Level 3 for wake-completion mechanism.

### 2026-05-18 — Added old MVP prototype documentation and evidence

Completed:

- Created `product/old-mvp.md`.
- Documented the old physical MVP/prototype architecture, component-level behavior, and presence-based wake-completion loop.
- Updated `validation/evidence-log.md` with a technical prototype evidence entry.

### 2026-05-18 — Added marketing post performance log

Completed:

- Created `marketing/post-performance-log.md`.
- Added the 2026-02-04 founder LinkedIn waitlist launch post as the first entry.

### 2026-05-18 — Added waitlist and LinkedIn launch evidence

Completed:

- Updated `validation/evidence-log.md` with the first detailed website/waitlist evidence entry.

### 2026-05-18 — Added current work tracker

Completed:

- Created `ai-context/current-work.md`.

### 2026-05-18 — Clarified copied software snapshot docs

Completed:

- Updated `software/software-context-map.md` to explain that some files in the `software/` folder are copied or synced from the separate software implementation repo.

### 2026-05-18 — Added strategic decision-log entries

Completed:

- Added decision-log entries for wake-completion, target audience, non-contact direction, hardware-led direction, MVP scope, and grogginess/sleep-phase-aware intervention claim sensitivity.

## Deferred / not now

- Do not create `ai-context/master-context-paste.md` right now.
- Do not create more creative strategy docs until the upstream customer and claims docs are updated.
- Do not move into Orisen Marketing execution until `product/target-customer.md` and `product/claims-and-evidence.md` are updated.

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
- `evidence-roadmap.md` tracks evidence categories and missing evidence
- `evidence-log.md` tracks real evidence
- `post-performance-log.md` tracks detailed marketing execution and performance learning
- `old-mvp.md` tracks detailed historical prototype context
