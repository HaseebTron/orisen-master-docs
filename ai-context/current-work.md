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
- `ai-context/repo-governance/repo-backlog.md` records future docs, cleanup items, and recurring checks.
- `ai-context/claim-control/claim-control-roadmap.md` tracks evidence categories, missing evidence, and where each evidence type lives.
- `ai-context/claim-control/claim-control-log.md` records real evidence and what claims it supports.
- `ai-context/claim-control/claim-control-system.md` defines evidence-strength and classification rules.
- `ai-context/handoff-rules.md` decides when to continue, refresh, start a new chat, or move projects.
- `marketing/post-performance-log.md` records detailed marketing post/campaign execution, metrics, lessons, and follow-up experiments.
- `product/old-mvp/` records detailed historical context about the old physical MVP/prototype.
- `ai-context/current-work.md` tracks the active work queue, recent completions, blockers, and immediate next steps.

## Current focus

Strengthen the Orisen master-docs repo so ChatGPT can use it as a reliable source-of-truth system for company/product/claims/workflow decisions.

The current phase is upstream evidence, ICP, and claim-boundary cleanup before moving into Orisen Marketing for X/Twitter execution.

## Next-step routing rule

Whenever the user asks what to do next, this file should help the assistant answer both:

1. what the next substantive task is
2. where that task should happen

The assistant should state one of:

- Continue this chat.
- Refresh context and continue this chat.
- Start a new chat in the same project.
- Move to another Orisen project.

If refresh, new chat, handoff, or project move is recommended, the assistant must use the large, bold, all-caps heading format defined in `ai-context/handoff-rules.md`, such as:

```markdown
# **NEW CHAT RECOMMENDED**
```

or:

```markdown
# **MOVE TO ANOTHER PROJECT RECOMMENDED**
```

This is intentionally loud so the user does not miss it during long Orisen workflows.

## Immediate next steps

### 1. Update `product/target-customer.md`

Use the now-captured evidence base:

- summer 2024 customer interviews
- old MVP prototype/pilot evidence
- old MVP user feedback
- LinkedIn/waitlist evidence
- Leila Jalali expert commentary
- Benji Ozynski expert commentary
- evidence weighting rules in `ai-context/claim-control/claim-control-roadmap.md`

Goal:

- Sharpen the primary ICP around people who repeatedly fail between alarm time and actually being out of bed.
- Make clear this is not for generic alarm-clock users or casual sleep optimizers.
- Treat student/full-time/gender/age/etc. patterns as hypotheses only, not validated segment conclusions.
- Treat teens/young adults and shift workers as segments worth investigating, not validated demographic ICPs.

Recommended place:

- New chat in Orisen General if the current chat is already long or has covered multiple workstreams.
- Continue current chat only if it is short and already focused on product/customer docs.

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
- Incorporate expert caution that theoretically plausible sleep-intervention mechanisms still require empirical testing.

Recommended place:

- Same clean Orisen General chat as `product/target-customer.md` if both are being updated together.

### 3. Then move to Orisen Marketing for X execution

After the two upstream docs above are updated, start a fresh chat in the Orisen Marketing project for:

- `marketing/positioning-and-messaging.md`
- `marketing/twitter-content-strategy.md`
- `marketing/customer-voice-log.md`
- `marketing/twitter-post-bank.md`
- actual X/Twitter posts

Recommended place:

- Orisen Marketing + GTM project, new chat.

## In progress

- Evidence collection and classification.
- Converting known Orisen signals into conservative claim-control entries.
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

- `product/old-mvp/old-mvp.md`
- `product/old-mvp/old-mvp-test-row-labels.md`
- `product/old-mvp/old-mvp-bypass-and-failure-notes.md`
- `product/old-mvp/old-mvp-user-feedback.md`
- `ai-context/claim-control/claim-control-log.md`

Status:

- Strongest current support for wake-completion wedge.
- Supports early signal that presence-based wake completion can get users out of bed closer to alarm time.
- Does not prove production reliability, broad robustness, reduced grogginess, reduced sleep inertia, sleep-stage-aware intervention, or artificial sleep phase transitioning.

### Traffic from website / marketing

Source files:

- `marketing/post-performance-log.md`
- `ai-context/claim-control/claim-control-log.md`

Status:

- One founder LinkedIn post and limited external sharing.
- 66 waitlist signups excluding founder/test signup.
- About 22% internal high-intent/relevant traffic conversion estimate.
- About 16% blended historical conversion.
- About 6% later lower-intent incremental conversion.
- Useful as early demand/message-resonance signal, not paid validation.

### Expert commentary

Source files:

- `research/expert-commentary/raw/leila-jalali-meeting-notes.md`
- `research/expert-commentary/raw/benji-ozynski-meeting-notes.md`
- `research/expert-commentary/expert-commentary-synthesis.md`
- `ai-context/claim-control/claim-control-log.md`

Status:

- Captured as expert commentary / early external validation / claim-discipline input.
- Useful for technical plausibility, claim discipline, and future research direction.
- Supports treating artificial sleep phase transitioning as a plausible but unvalidated roadmap hypothesis.
- Supports caution that grogginess and sleep inertia are multi-cause and should not be claimed as solved without direct validation.
- Supports caution that sleep-intervention theory must be tested empirically because subjective outcomes may not match theory.
- Does not prove Orisen efficacy, clinical validation, market demand, or hard demographic segment conclusions.

### External market / literature / community evidence

Source file:

- `ai-context/claim-control/claim-control-roadmap.md`

Status:

- Roadmap created.
- Expert commentary is partially filled.
- Other external source files are still mostly missing.
- `ai-context/claim-control/claim-control-roadmap.md` now defines the future raw/source folder convention.

Future source files may include:

- `research/external-research/research-papers/raw/`
- `research/external-research/articles-and-media/raw/`
- `research/external-research/reddit-forums/raw/`
- `research/external-research/competitor-reviews/raw/`
- `research/external-research/market-and-category/raw/`

Each future category may have synthesis docs by topic when there is actual source material to analyze.

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

### 2026-05-20 — Added proactive handoff / refresh visibility rules

Completed:

- Updated `ai-context/handoff-rules.md` with stricter proactive warning triggers.
- Updated `ai-context/start-here.md` with a visible handoff warning rule.
- Updated this file with a next-step routing rule.

Why:

- The assistant previously waited too long to recommend switching chats or refreshing context.
- Future warnings should be hard to miss because they must use large, bold, all-caps headings.

### 2026-05-20 — Updated boot and context docs to point to claim-control paths

Completed:

- Updated `ai-context/start-here.md` to point claim/evidence/validation routing to `ai-context/claim-control/claim-control-system.md`.
- Updated `ai-context/context-map.md` to use `ai-context/claim-control/claim-control-system.md`, `ai-context/claim-control/claim-control-log.md`, and `ai-context/claim-control/claim-control-roadmap.md` instead of the old `validation/` paths.

Why:

- The old `validation/` folder was excessive and too easy to misunderstand as a separate validation workstream.
- Claim control is more accurate because these docs mainly govern claim strength, evidence boundaries, and what marketing/fundraising/product language can safely say.

### 2026-05-19 — Moved validation docs into claim-control

Completed:

- Created `ai-context/claim-control/`.
- Moved/renamed the former validation docs into:
  - `ai-context/claim-control/claim-control-system.md`
  - `ai-context/claim-control/claim-control-log.md`
  - `ai-context/claim-control/claim-control-roadmap.md`
- Removed the standalone `validation/` folder after moving the relevant files.
- Updated affected references in repo docs where found.

Why:

- These files are not raw evidence folders and not product docs.
- Their job is AI/context governance: how evidence affects claim strength, public wording, and source-of-truth decisions.

### 2026-05-19 — Added Benji Ozynski expert commentary evidence

Completed:

- Created `research/expert-commentary/raw/benji-ozynski-meeting-notes.md`.
- Updated the expert-commentary synthesis with Benji Ozynski evidence.
- Updated claim-control files with an expert commentary evidence entry.

Key interpretation:

- Temperature may be a relevant future intervention variable, but this is not validated for Orisen yet.
- Actigraphy and PSG validation may be useful for future studies.
- Sleep-stage-aware intervention and artificial sleep phase transitioning must be empirically tested.
- A clinic/research collaboration could become important validation infrastructure.

Claim boundary:

- Does not prove Orisen reduces grogginess.
- Does not prove Orisen reduces sleep inertia.
- Does not prove Orisen detects or manipulates sleep stages.
- Does not prove Orisen has clinical validation.
- Does not prove future research collaboration is secured until confirmed.

### 2026-05-19 — Added Leila Jalali expert commentary evidence

Completed:

- Created `research/expert-commentary/raw/leila-jalali-meeting-notes.md`.
- Updated the expert-commentary synthesis with Leila Jalali evidence.
- Updated claim-control files with an expert commentary evidence entry.
- Updated the claim-control roadmap to mark expert commentary as partially filled.
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
- Updated the claim-control roadmap with a raw data / synthesis convention.
- Updated future external-research paths to use category folders with optional `raw/` subfolders.

Why:

- Raw/source data should stay separate from synthesis and interpretation.
- The repo should avoid duplicating raw data.
- Future external research should follow the same source-to-synthesis evidence chain.

### 2026-05-18 — Added claim-control roadmap

Completed:

- Created the original roadmap now located at `ai-context/claim-control/claim-control-roadmap.md`.
- Defined four main evidence categories:
  - Direct customer discovery
  - Prototype / pilot evidence
  - Traffic from website / marketing
  - External market / literature / community evidence
- Made the roadmap an index/to-do file that points to detailed evidence files instead of duplicating them.
- Added future external research categories for:
  - research papers
  - market/category evidence
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
- Updated claim-control log.
- Separated conversion into:
  - about 22% high-intent / relevant-traffic conversion estimate
  - about 16% blended historical conversion
  - about 6% later lower-intent incremental conversion

Claim boundary:

- The 22% number is an internal directional estimate for relevant early launch traffic, not a universal website conversion rate.

### 2026-05-18 — Added old MVP qualitative user feedback

Completed:

- Created `product/old-mvp/old-mvp-user-feedback.md`.
- Updated claim-control log.
- Captured that testers said the old MVP was much better at waking them on time compared with before.
- Captured Dennis's founder-reported purchase-interest signal around a roughly $100 discussed price point.
- Captured user pull for easier wake-up / less-groggy direction.

Claim boundary:

- Supports wake-completion value and roadmap pull.
- Does not prove paid demand, price point, reduced grogginess, sleep inertia reduction, or artificial sleep phase transitioning.

### 2026-05-18 — Added old MVP pilot/test evidence

Completed:

- Updated `product/old-mvp/old-mvp.md` with detailed old MVP pilot/test participant data for:
  - founder
  - Hamza/Humza
  - Dennis
  - Sabeeh
- Added detailed test definitions for bed time, alarm time, wake-up time, get-out-of-bed time, sleepy rating, irritation rating, mood rating, and energy rating.
- Added Dennis, Hamza/Humza, and Sabeeh test tables.
- Added tester-specific interpretations and limitations.
- Updated claim-control log with a pilot/test evidence entry.

Classification:

- Early validation / small prototype pilot signal.
- Evidence strength: Level 2 to early Level 3 for wake-completion mechanism.

### 2026-05-18 — Added old MVP prototype documentation and evidence

Completed:

- Created `product/old-mvp/old-mvp.md`.
- Documented the old physical MVP/prototype architecture, component-level behavior, and presence-based wake-completion loop.
- Updated claim-control log with a technical prototype evidence entry.

### 2026-05-18 — Added marketing post performance log

Completed:

- Created `marketing/post-performance-log.md`.
- Added the 2026-02-04 founder LinkedIn waitlist launch post as the first entry.

### 2026-05-18 — Added waitlist and LinkedIn launch evidence

Completed:

- Updated claim-control log with the first detailed website/waitlist evidence entry.

### 2026-05-18 — Added current work tracker

Completed:

- Created `ai-context/current-work.md`.

### 2026-05-18 — Clarified copied software snapshot docs

Completed:

- Updated `software/software-read-rules.md` to explain that some files in the `software/` folder are copied or synced from the separate software implementation repo.

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
- `ai-context/repo-governance/repo-backlog.md` tracks future cleanup and missing docs
- `claim-control-roadmap.md` tracks evidence categories and missing evidence
- `claim-control-log.md` tracks real evidence
- `post-performance-log.md` tracks detailed marketing execution and performance learning
- `product/old-mvp/` tracks detailed historical prototype context
