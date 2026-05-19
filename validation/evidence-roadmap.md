# Evidence Roadmap

## Purpose

This file tracks the evidence categories Orisen should eventually fill out.

It is not the evidence itself. It is a category-specific evidence to-do list and index.

Use this file to answer:

- What evidence do we already have?
- Where does each evidence type live in the repo?
- What evidence is missing?
- What should be collected next?
- What claims can each evidence category support or not support?

## Relationship to other files

This file points to detailed files in their natural folders instead of duplicating them.

- Use `validation/evidence-log.md` for conservative evidence entries and claim support.
- Use `validation/evidence-standard.md` for evidence classification rules.
- Use `product/claims-and-evidence.md` for public claim boundaries.
- Use `product/target-customer.md` for ICP and target-customer synthesis.
- Use research, product, and marketing folders for detailed source-specific evidence.

## Evidence system structure

```text
validation/evidence-roadmap.md
= what evidence categories exist, what is done, what is missing, and where to look

validation/evidence-log.md
= conservative evidence entries and supported/unsupported claim tracking

validation/evidence-standard.md
= rules for classifying evidence strength

product/claims-and-evidence.md
= what Orisen can safely claim publicly

research/, product/, marketing/
= detailed source files, raw notes, raw data, and synthesis docs
```

## Raw data and synthesis convention

For evidence categories that have raw/source material, use this pattern:

```text
research/<category>/raw/
= raw data, exported CSVs, rough notes, source excerpts, transcripts, source lists, screenshots, or copied source material

research/<category>/<synthesis-file>.md
= cleaned synthesis, interpretation, limitations, claim boundaries, and downstream implications
```

The same principle can apply outside `research/` when useful:

```text
product/<topic>/raw/
= raw prototype logs, raw tester notes, photos/videos links, unprocessed tables, or rough source material

marketing/<topic>/raw/
= exported analytics, raw post metrics, screenshots, or rough campaign notes
```

Current example:

```text
research/customer-interviews/raw/2024-alarm-clock-responses.csv
→ raw summer 2024 interview response data

research/customer-interviews/2024-alarm-clock-interviews.md
→ synthesis and interpretation of the interview data
```

Rules:

- Keep raw/source data separate from interpretation.
- Do not overwrite raw data with conclusions.
- Put synthesis outside the `raw/` folder.
- Do not create empty `raw/` folders before there is actual raw/source material.
- Every synthesis file should point back to its raw/source files.
- Downstream claim docs should rely on the evidence log and source-specific synthesis, not raw data alone.

## Current evidence categories

### 1. Direct customer discovery

Status: partially filled.

Purpose:

- Understand customer pain before product framing becomes too leading.
- Extract customer language.
- Identify possible ICP traits.
- Identify who is not the first customer.

Current source files:

- `research/customer-interviews/raw/2024-alarm-clock-responses.csv`
- `research/customer-interviews/2024-alarm-clock-interviews.md`

Current evidence:

- Summer 2024 campus/mall interviews.
- Small-sample qualitative discovery.
- Supports repeated wake-up failure and get-out-of-bed problems as plausible pain patterns.
- Supports non-camera/privacy direction directionally.

Evidence weighting:

- Low to medium for qualitative themes.
- Low for market sizing or segment ranking.
- Do not infer subgroup conclusions by occupation, gender, ethnicity, religion, student status, full-time work status, age group, or living situation.

Supports:

- Some people experience repeated wake-up and get-out-of-bed problems.
- Some people are not first customers because waking up is not a meaningful pain for them.
- Getting out of bed can be a distinct pain from waking up.
- Camera discomfort appears repeatedly enough to treat non-camera sensing as a meaningful hypothesis.

Does not support:

- Broad market demand.
- Validated ICP segment ranking.
- Willingness to pay.
- Product-market fit.
- Clinical efficacy.
- Reduced grogginess.
- Artificial sleep phase transitioning.

Next steps:

- Add more interviews with people who self-identify as severe oversleepers/heavy sleepers.
- Add interviews with people who have tried multiple alarm solutions.
- Add interviews with non-friend, cold users.
- Ask about actual past behavior, not hypothetical interest.
- Capture exact quotes and raw language for `marketing/customer-voice-log.md`.
- Track whether people have paid for any alarm/sleep solution before.

### 2. Prototype / pilot evidence

Status: partially filled and currently strongest for wake-completion wedge.

Purpose:

- Validate whether the core wake-completion behavior works in real mornings.
- Learn failure modes and bypass behavior.
- Separate technical prototype success from production validation.

Current source files:

- `product/old-mvp.md`
- `product/old-mvp-test-row-labels.md`
- `product/old-mvp-bypass-and-failure-notes.md`
- `product/old-mvp-user-feedback.md`
- `validation/evidence-log.md`

Current evidence:

- Old MVP users.
- Real wake-up behavior.
- Bypass attempts.
- Qualitative tester feedback.
- Founder-reported purchase-intent signal from Dennis.
- User pull for easier wake-up / less-groggy direction.

Supports:

- Presence-based wake completion is the strongest current wedge.
- The old MVP physically demonstrated the wake-completion loop.
- Test users experienced meaningful improvement versus normal wake-up behavior.
- Users may actively try to bypass the system, so anti-bypass design matters.
- Forced wake completion does not fully solve grogginess, supporting the roadmap need for easier wake-up.

Does not support:

- Production reliability.
- Broad bedroom robustness.
- Broad willingness to pay.
- Validated price point.
- Reduced grogginess.
- Reduced sleep inertia.
- Artificial sleep phase transitioning.
- Sleep-stage detection.
- Product-market fit.

Next steps:

- Preserve photos/videos of old MVP if available.
- Add exact tester quotes if recoverable.
- Add more precise row labels if new memory or records appear.
- Run next prototype tests with explicit event logging.
- Record bypass attempts, alarm edits, power changes, return-to-bed behavior, and wake-completion state transitions.
- Test with non-friend users when feasible.
- Separate strict on-time success from practical improvement versus baseline.
- Measure whether users keep using it after novelty fades.

### 3. Traffic from website / marketing

Status: partially filled.

Purpose:

- Measure message resonance and early demand signal.
- Learn which messages and channels drive relevant traffic.
- Track conversion quality over time.

Current source files:

- `marketing/post-performance-log.md`
- `validation/evidence-log.md`

Current evidence:

- One founder LinkedIn post.
- Waitlist conversion.
- Website traffic.
- Microsoft Clarity tracking after setup.
- LinkedIn link visit data.

Current conversion interpretation:

- High-intent / relevant traffic conversion estimate: about 22%.
- Overall blended historical conversion: about 16%.
- Later lower-intent incremental conversion: about 6%.

Supports:

- Early message resonance around painful wake-ups.
- Founder-led organic content can drive attention and waitlist interest.
- Relevant early launch traffic appears to convert meaningfully better than stale/curiosity traffic.

Does not support:

- Paid demand.
- Willingness to pay.
- Retention.
- Product-market fit.
- Technical efficacy.
- Clinical efficacy.
- Broad market demand.

Next steps:

- Track every major future post with copy, creative, timing, metrics, and derived metrics.
- Separate high-intent traffic from curiosity traffic.
- Track source attribution more cleanly.
- Add waitlist survey questions if possible.
- Ask waitlist users about severity, current solution, willingness to pay, and whether they want to beta test.
- Test X/Twitter content after source-of-truth positioning is ready.

### 4. External market / literature / community evidence

Status: mostly missing.

Purpose:

- Pressure-test Orisen against broader reality.
- Understand existing solutions and why they fail.
- Extract raw public customer language.
- Protect the company from overclaiming scientific/clinical outcomes.
- Support market/category framing for fundraising.

This category should not be used to “prove Orisen works.” It should be used to triangulate market pain, customer language, scientific plausibility, competitor gaps, and claim risk.

Recommended future folder pattern:

```text
research/external-research/sleep-inertia/raw/
research/external-research/sleep-inertia/sleep-inertia-research.md

research/external-research/market-reports/raw/
research/external-research/market-reports/market-research-notes.md

research/external-research/articles-and-media/raw/
research/external-research/articles-and-media/articles-and-media-notes.md

research/external-research/reddit-forums/raw/
research/external-research/reddit-forums/reddit-customer-language.md

research/external-research/competitor-reviews/raw/
research/external-research/competitor-reviews/competitor-review-research.md

research/external-research/expert-commentary/raw/
research/external-research/expert-commentary/expert-commentary.md
```

Do not create these folders/files until there is actual source material to put in them.

#### 4.1 Research papers / sleep inertia literature

Status: missing.

Potential source file:

- `research/external-research/sleep-inertia/sleep-inertia-research.md`

Potential raw/source folder:

- `research/external-research/sleep-inertia/raw/`

Look for research on:

- sleep inertia duration
- waking from deep sleep vs lighter sleep
- effects of light/audio on waking
- sleep stage and grogginess
- alarm timing
- circadian light exposure
- auditory stimulation during sleep
- limitations of consumer sleep-stage detection

Extract:

- what is scientifically plausible
- what is not proven
- what claims should be avoided
- what language can be used safely
- where Orisen needs real testing before making claims

Best use:

- Claim discipline.
- Product roadmap realism.
- Fundraising diligence.
- Avoiding irresponsible claims around sleep manipulation.

Weak use:

- Proving customer demand.
- Proving Orisen efficacy before Orisen-specific testing.

Next steps:

- Find review papers or credible sources on sleep inertia.
- Find papers on light/audio effects near waking.
- Find sources on sleep-stage-based smart alarms and their limitations.
- Add citations and summarize in careful claim-safe language.

#### 4.2 Market reports / surveys

Status: missing.

Potential source file:

- `research/external-research/market-reports/market-research-notes.md`

Potential raw/source folder:

- `research/external-research/market-reports/raw/`

Look for:

- sleep tech market size
- alarm clock market size
- smart sleep device market
- wearable sleep tracker market
- consumer frustration with sleep tracking
- demand for sleep improvement rather than tracking

Extract:

- category size
- growth direction
- buyer behavior
- investor-facing market framing
- survey-level consumer pain, if credible

Best use:

- Fundraising context.
- Investor narrative.
- Category framing.

Weak use:

- Proving Orisen's wedge.
- Proving willingness to pay for Orisen.
- Proving product-market fit.

Next steps:

- Gather credible market reports or survey summaries.
- Separate high-quality sources from fluffy market-report claims.
- Do not over-rely on market size to justify product strategy.

#### 4.3 Articles

Status: missing.

Potential source file:

- `research/external-research/articles-and-media/articles-and-media-notes.md`

Potential raw/source folder:

- `research/external-research/articles-and-media/raw/`

Look for:

- articles on waking up, oversleeping, sleep inertia, heavy sleepers, and sleep tech
- expert commentary in reputable publications
- sleep tracker critiques
- consumer sleep-tech trend coverage

Extract:

- public framing
- expert warnings
- recurring pain language
- claims that are common but potentially risky

Best use:

- Context.
- Messaging inspiration.
- Identifying common public beliefs and misconceptions.

Weak use:

- Scientific proof unless the article directly references strong sources.

Next steps:

- Save only sources worth citing later.
- Prefer primary research or expert commentary over generic SEO articles.

#### 4.4 Reddit / forum posts

Status: missing.

Potential source file:

- `research/external-research/reddit-forums/reddit-customer-language.md`

Potential raw/source folder:

- `research/external-research/reddit-forums/raw/`

Search communities such as:

- `r/GetOutOfBed`
- `r/sleep`
- `r/ADHD`
- `r/productivity`
- `r/GetMotivated`
- `r/college`
- `r/NightShift`
- `r/AskReddit`
- `r/BuyItForLife`
- `r/biohackers`

Search themes:

```text
sleep through alarms
can't wake up
turn off alarm in sleep
wake up but can't get out of bed
snooze for hours
sleep inertia
morning grogginess
alarm clock for heavy sleepers
sunrise alarm didn't work
Alarmy stopped working
```

Extract:

- exact phrases people use
- what they tried
- what failed
- how severe the consequences are
- whether they sound desperate enough to pay
- what they hate about existing solutions

Best use:

- Customer language.
- ICP pain refinement.
- Content ideas.
- Competitor/substitute failure modes.

Weak use:

- Statistical evidence.
- Market sizing.
- Medical conclusions.

Next steps:

- Save source links and short excerpts.
- Categorize by failure mode: sleep-through, snooze, turn-off-half-asleep, get-back-in-bed, phone trap, grogginess, partner disturbance.
- Avoid over-weighting extreme Reddit examples as representative of the whole market.

#### 4.5 Reviews of competing products

Status: missing.

Potential source file:

- `research/external-research/competitor-reviews/competitor-review-research.md`

Potential raw/source folder:

- `research/external-research/competitor-reviews/raw/`

Look at reviews for:

- Alarmy
- Sleep Cycle
- Hatch Restore
- Loftie
- Philips SmartSleep / sunrise lamps
- Pavlok Shock Clock
- Sonic Bomb alarm clock
- Clocky
- Apple/Android alarm complaints
- wearable sleep trackers like Oura, WHOOP, Fitbit, Apple Watch

Amazon review targets:

- Sonic Bomb
- sunrise alarm clocks
- Hatch
- Clocky
- vibrating alarms
- bed shaker alarms
- extra loud alarm clocks

Extract:

- why people bought it
- what they love
- what failed
- what they still complain about
- whether they mention sleeping through it
- whether they mention snoozing, turning it off, waking groggy, partner disturbance, phone dependence, or privacy concerns

Best use:

- Finding gaps in substitutes.
- Understanding what people already pay for.
- Finding language from real buyers.
- Positioning Orisen against existing solutions.

Weak use:

- Proving Orisen will win.
- Proving Orisen's efficacy.

Next steps:

- Collect reviews by product type.
- Separate positive purchase drivers from negative failure modes.
- Identify which competitors are “works but brutal” versus “pleasant but ineffective.”
- Look for repeated phrases and objections.

#### 4.6 Sleep clinic / expert commentary

Status: partially started through conversations, but not yet structured here.

Potential source file:

- `research/external-research/expert-commentary/expert-commentary.md`

Potential raw/source folder:

- `research/external-research/expert-commentary/raw/`

Best experts:

- behavioral sleep medicine specialists
- sleep technologists
- sleep clinic workers
- circadian rhythm researchers
- people who score sleep studies
- ADHD coaches or clinicians
- shift-work fatigue experts

Ask:

- who has the most severe wake-up problems?
- what causes people to fail at waking?
- what is realistic vs overclaimed about sleep-stage-based waking?
- what would be unsafe or irresponsible to claim?
- what would make this useful clinically or practically?

Best use:

- Claim discipline.
- Product risk discovery.
- Clinical/scientific realism.
- Identifying user segments that may require caution.

Weak use:

- Proving demand unless experts report repeated customer/patient demand.
- Making medical claims.

Next steps:

- Add structured notes from any expert calls.
- Record what the expert said, what it supports, what it does not prove, warnings, objections, and suggestions.
- Keep medical/clinical claims conservative.

## Evidence priority order

For near-term marketing and X posting, prioritize:

1. Direct customer discovery.
2. Prototype/pilot evidence.
3. Competitor reviews.
4. Reddit/forum customer language.
5. Claims-safe sleep inertia research.
6. Website/marketing traffic evidence.
7. Expert commentary.
8. Market reports and market sizing.

For fundraising, prioritize:

1. Prototype/pilot evidence.
2. Direct customer discovery.
3. Website/waitlist evidence.
4. Competitor reviews.
5. Sleep inertia and scientific claim discipline.
6. Market reports and category size.
7. Expert commentary.

For product strategy, prioritize:

1. Prototype/pilot failure modes.
2. Direct customer discovery.
3. Competitor review failure modes.
4. Expert commentary.
5. Research papers on sleep inertia and intervention plausibility.
6. Reddit/forum language.
7. Website/marketing metrics.
8. Market reports.

## Repo hygiene rules

- Do not duplicate full evidence across multiple files.
- Keep raw data near the source category.
- Keep synthesis near the source category.
- Point to source files from this roadmap.
- Add conservative claim interpretation to `validation/evidence-log.md` only when evidence is meaningful enough to affect claims.
- Update `product/claims-and-evidence.md` before using any stronger public claim.
- Do not convert anecdotal evidence, Reddit posts, or reviews into statistical claims.
- Do not treat market reports as proof of demand.
- Do not treat scientific plausibility as proof that Orisen works.

## Immediate next steps

Before moving to Orisen Marketing for X execution, update:

1. `product/target-customer.md`
2. `product/claims-and-evidence.md`

Use currently available evidence:

- summer 2024 customer interviews
- old MVP prototype/pilot evidence
- old MVP user feedback
- LinkedIn/waitlist evidence
- evidence weighting rules in this roadmap

Then, in Orisen Marketing, create or update:

- `marketing/positioning-and-messaging.md`
- `marketing/twitter-content-strategy.md`
- `marketing/customer-voice-log.md`
- `marketing/twitter-post-bank.md`
