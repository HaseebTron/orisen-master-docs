# Claim Control Roadmap

## Purpose

This file tracks what evidence categories Orisen should eventually fill out and where each category lives.

It is not the evidence itself. It is a claim-control and evidence to-do list.

Use this file to answer:

- What evidence do we already have?
- Where does each evidence type live?
- What evidence is missing?
- What should be collected next?
- What claims can each evidence category support or not support?

## Relationship to other files

- Use `ai-context/claim-control/claim-control-system.md` for evidence organization, classification, and claim-safety rules.
- Use `ai-context/claim-control/claim-control-log.md` for conservative claim-relevant evidence entries.
- Use `product/claims-and-evidence.md` for final public claim boundaries.
- Use `product/target-customer.md` for ICP and target-customer synthesis.
- Use `research/`, `product/`, and `marketing/` folders for detailed source material and synthesis.

## Current evidence categories

### 1. Direct customer discovery

Status: partially filled.

Current source files:

- `research/customer-interviews/raw/2024-alarm-clock-responses.csv`
- `research/customer-interviews/2024-alarm-clock-interviews.md`

Purpose:

- Understand customer pain before product framing becomes too leading.
- Extract customer language.
- Identify possible ICP traits.
- Identify who is not the first customer.

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
- Capture exact quotes and raw language for marketing.
- Track whether people have paid for any alarm/sleep solution before.

### 2. Prototype / pilot evidence

Status: partially filled and currently strongest for wake-completion wedge.

Current source files:

- `product/old-mvp/README.md`
- `product/old-mvp/old-mvp.md`
- `product/old-mvp/old-mvp-test-row-labels.md`
- `product/old-mvp/old-mvp-bypass-and-failure-notes.md`
- `product/old-mvp/old-mvp-user-feedback.md`
- `ai-context/claim-control/claim-control-log.md`

Purpose:

- Validate whether the core wake-completion behavior works in real mornings.
- Learn failure modes and bypass behavior.
- Separate technical prototype success from production validation.

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
- Run next prototype tests with explicit event logging.
- Record bypass attempts, alarm edits, power changes, return-to-bed behavior, and wake-completion state transitions.
- Test with non-friend users when feasible.
- Separate strict on-time success from practical improvement versus baseline.
- Measure whether users keep using it after novelty fades.

### 3. Traffic from website / marketing

Status: partially filled.

Current source files:

- `marketing/post-performance-log.md`
- `ai-context/claim-control/claim-control-log.md`

Purpose:

- Measure message resonance and early demand signal.
- Learn which messages and channels drive relevant traffic.
- Track conversion quality over time.

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

### 4. Expert commentary

Status: partially filled.

Current source files:

- `research/expert-commentary/README.md`
- `research/expert-commentary/raw/leila-jalali-meeting-notes.md`
- `research/expert-commentary/raw/benji-ozynski-meeting-notes.md`
- `research/expert-commentary/expert-commentary.md`
- `research/expert-commentary/benji-ozynski-synthesis.md`

Purpose:

- Capture sleep-expert and domain-expert meeting notes.
- Use experts for claim discipline, technical plausibility, validation design, roadmap realism, and ICP hypotheses.
- Keep expert calls separate from secondary external research.

Current evidence:

- Leila Jalali expert commentary on sleep-stage intervention, sleep inertia, grogginess, wake-up difficulty, age patterns, shift workers, and sleep spindles.
- Benji Ozynski expert commentary on empirical testing, sleep unpredictability, temperature, actigraphy, sleep-mask/light limitations, PSG validation, and possible research/advisor collaboration.
- Strongest use is claim discipline, validation design, and roadmap realism.
- Does not validate Orisen efficacy or market demand.

Best use:

- Claim discipline.
- Product risk discovery.
- Clinical/scientific realism.
- Validation design.
- Identifying user segments that may require caution.

Weak use:

- Proving demand unless experts report repeated customer/patient demand.
- Making medical claims.
- Hard prevalence or segmentation claims.
- Claiming a formal partnership before it is confirmed.

Next steps:

- Add structured notes from any additional expert calls.
- Record what each expert said, what it supports, what it does not prove, warnings, objections, and suggestions.
- Keep medical/clinical claims conservative.
- Use expert commentary to guide literature review topics, especially sleep inertia, spindles, arousal threshold, delayed sleep phase, temperature, actigraphy, and PSG validation.
- Follow up with Dr Benji about PSG validation, exact cost, data access, protocol support, advisor interest, and whether clinic involvement can be formally confirmed.

### 5. External market / literature / community evidence

Status: mostly missing.

Purpose:

- Pressure-test Orisen against broader reality.
- Understand existing solutions and why they fail.
- Extract raw public customer language.
- Protect the company from overclaiming scientific/clinical outcomes.
- Support market/category framing for fundraising.

This category should not be used to prove Orisen works. It should be used to triangulate market pain, customer language, scientific plausibility, competitor gaps, and claim risk.

#### 5.1 Research papers

Look for research on:

- sleep inertia duration
- waking from deep sleep vs lighter sleep
- effects of light/audio on waking
- sleep stage and grogginess
- alarm timing
- circadian light exposure
- auditory stimulation during sleep
- temperature as a sleep/wake intervention variable
- actigraphy as a sleep/wake measurement tool
- limitations of consumer sleep-stage detection
- sleep spindles and arousal threshold

Best use:

- Claim discipline.
- Product roadmap realism.
- Fundraising diligence.
- Avoiding irresponsible claims around sleep manipulation.

Weak use:

- Proving customer demand.
- Proving Orisen efficacy before Orisen-specific testing.

#### 5.2 Articles and media

Look for:

- articles on waking up, oversleeping, sleep inertia, heavy sleepers, and sleep tech
- expert commentary in reputable publications
- sleep tracker critiques
- consumer sleep-tech trend coverage

Best use:

- Context.
- Messaging inspiration.
- Identifying common public beliefs and misconceptions.

Weak use:

- Scientific proof unless the article directly references strong sources.

#### 5.3 Reddit / forum posts

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

Best use:

- Customer language.
- ICP pain refinement.
- Content ideas.
- Competitor/substitute failure modes.

Weak use:

- Statistical evidence.
- Market sizing.
- Medical conclusions.

#### 5.4 Competitor product reviews

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

Best use:

- Finding gaps in substitutes.
- Understanding what people already pay for.
- Finding language from real buyers.
- Positioning Orisen against existing solutions.

Weak use:

- Proving Orisen will win.
- Proving Orisen's efficacy.

#### 5.5 Market and category

Look for:

- sleep tech market size
- alarm clock market size
- smart sleep device market
- wearable sleep tracker market
- consumer frustration with sleep tracking
- demand for sleep improvement rather than tracking

Best use:

- Fundraising context.
- Investor narrative.
- Category framing.

Weak use:

- Proving Orisen's wedge.
- Proving willingness to pay for Orisen.
- Proving product-market fit.

## Evidence priority order

For near-term marketing and X posting, prioritize:

1. Direct customer discovery.
2. Prototype/pilot evidence.
3. Competitor reviews.
4. Reddit/forum customer language.
5. Claims-safe sleep inertia / waking-up research papers.
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
8. PSG validation pathway and expert/advisor collaboration if confirmed.

For product strategy, prioritize:

1. Prototype/pilot failure modes.
2. Direct customer discovery.
3. Competitor review failure modes.
4. Expert commentary.
5. Research papers on sleep inertia and intervention plausibility.
6. PSG/actigraphy validation design.
7. Reddit/forum language.
8. Website/marketing metrics.
9. Market reports.

## Immediate next steps

Before moving deeply into Orisen Marketing for X execution, update or review:

1. `product/target-customer.md`
2. `product/claims-and-evidence.md`
3. `marketing/positioning-and-messaging.md`
4. `marketing/twitter-content-strategy.md` or equivalent X strategy file

Use currently available evidence:

- summer 2024 customer interviews
- old MVP prototype/pilot evidence
- old MVP user feedback
- LinkedIn/waitlist evidence
- Leila Jalali expert commentary
- Benji Ozynski expert commentary
- claim-control rules in `ai-context/claim-control/claim-control-system.md`