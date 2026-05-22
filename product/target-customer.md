# Target Customer

## Purpose

This file defines Orisen's target customer assumptions, early beachhead hypotheses, excluded users, evidence basis, and validation work needed to narrow the first customer segment.

This file is a product source-of-truth doc. It should guide downstream marketing, fundraising, product, and validation work, but it should not contain channel-specific execution strategy.

This file should stay consistent with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`

## Authority and evidence boundary

Target-customer conclusions should be derived primarily from evidence and research, not from preferred marketing positioning.

Use evidence in this order:

1. Direct customer discovery and prototype/pilot evidence
2. Research synthesis and expert commentary
3. Claim-control and claims-and-evidence docs
4. Product framing docs
5. Marketing performance signals
6. Current company framing and process docs

Important boundaries:

- `product/claims-and-evidence.md` remains the final public-claim authority.
- `ai-context/claim-control/claim-control-log.md` remains the conservative evidence ledger.
- `ai-context/current-state.md` should be used as an alignment check, not as independent proof of the target customer.
- Marketing performance can show message resonance, but it should not decide the target customer by itself.
- External research can help identify who likely has the pain. It cannot prove who will buy Orisen.
- Orisen-specific buying evidence requires interviews, waitlist tagging, prototype pilots, deposits, preorders, pricing tests, retention, or actual sales.

## Current target customer summary

Orisen is most likely for people with a repeated, painful wake-up failure problem.

The clearest early target customer is not simply someone who uses an alarm. It is someone whose problem happens between alarm time and actual wake completion.

A strong early customer may:

- sleep through alarms
- dismiss alarms while half-asleep
- wake up but stay in bed
- turn alarms off and go back to sleep
- return to bed after initially getting up
- rely on many alarms or phone-alarm hacks
- feel that willpower-based solutions are not enough
- face real consequences when they fail to wake up on time

The first users should not be casual sleep-optimization users who only want sleep graphs, dashboards, or general wellness insights.

## Evidence snapshot

This snapshot is for internal product interpretation. Counts and percentages should not be copied into public marketing unless they are attributed, caveated, and allowed by `product/claims-and-evidence.md`.

| Evidence source | Relevant numbers/details | What it supports | What it does not prove |
|---|---|---|---|
| `research/customer-interviews/2024-alarm-clock-interviews.md` | 10 total responses. Age range 19 to 80. 8 of 10 were age 23 or younger. 5 university students, 1 student with part-time work, 2 full-time workers, 2 blank/unknown. Problem intensity split: 2 definite wake-up problems, 2 somewhat, 6 none or none/full survey. 7 of 10 mentioned camera discomfort. | Some people have repeated wake-up or get-out-of-bed problems. The pain is not universal. Getting out of bed can be distinct from hearing an alarm. Non-camera sensing is directionally supported. | Market size, final ICP, subgroup conclusions, willingness to pay, or public prevalence claims. |
| `product/old-mvp/old-mvp.md` | Old MVP was tested by founder and 3 connected testers: Hamza/Humza, Dennis, and Sabeeh. Dennis's usual baseline: wake 8:30, out of bed 10:00. On successful logged days, his out-of-bed time matched or was close to alarm/wake time. Hamza's usual baseline: alarm 4:00, wake 4:50, out of bed 5:00. Several logged days show waking and getting out of bed within a few minutes of alarm time, with some failures or partial failures. Sabeeh's baseline: alarm 5:30, wake 6:30, out of bed 9:00, with mixed results and bug/failure days. | Presence-based wake completion showed early promise in real morning contexts. The strongest signal is getting out of bed closer to alarm time. | Production reliability, broad customer demand, paid demand, reduced grogginess, improved energy, or product-market fit. |
| `product/old-mvp/old-mvp-user-feedback.md` | Founder-reported feedback: testers said the old MVP was much better at waking them on time than normal behavior. Dennis said he would buy it “right now,” likely around a roughly $100 discussed price point. Testers still wanted easier or less-groggy wake-up. | Early qualitative support for wake-completion value and one weak willingness-to-pay signal. Supports roadmap interest in easier wake-up. | Validated price point, broad willingness to pay, artificial sleep phase transitioning, or reduced sleep inertia. |
| `research/external-research/waking-up/synthesis.md` | Reviewed sources include Nature Scientific Reports / SleepCycle app-data study, snooze alarm / sleep inertia study, Talker Research / Avocado Green Mattress survey, MattressInquirer oversleeping survey, SleepJunkie survey inventory, and Trotti sleep inertia review as incomplete guardrail. Talker Research reports a 2,000-person U.S. online survey and 38% saying they are “bad” at mornings. The snooze/sleep-inertia experiment had only 10 participants. | Wake-up can be multi-step. Repeated snoozing, delayed bed exit, oversleeping, and missed obligations appear in processed external sources. Sleep inertia is relevant but claim-sensitive. | Orisen efficacy, Orisen demand, willingness to pay, final ICP, reduced grogginess, or reduced sleep inertia. |
| `research/expert-commentary/expert-commentary-synthesis.md` | Expert commentary supports investigating severe oversleepers, repeated snoozers, return-to-bed users, teens and young adults, young adults with rigid schedules, and shift workers. | Good source for segment hypotheses and caution around sleep inertia/grogginess claims. | Market demand, final ICP, or product efficacy. |
| `marketing/post-performance-log.md` | Early founder-led post and waitlist performance showed message resonance around the wake-up problem. | Useful weak signal that the problem framing can get attention. | Buyer segment, willingness to pay, product-market fit, or durable demand. |

## Primary ICP hypothesis

The current primary ICP hypothesis is:

> People who repeatedly fail between alarm time and actually being out of bed.

This is a behavioral ICP, not a demographic ICP.

Evidence basis:

- Customer interviews show some respondents explicitly described getting out of bed as the problem, while many respondents did not have meaningful wake-up pain.
- Old MVP evidence is strongest around reducing the gap between alarm time and out-of-bed time, especially in Dennis's logged data.
- External waking-up research supports the broader framing that alarm interaction, snoozing, and delayed bed exit are not the same as wake completion.

Interpretation:

- The strongest current evidence points to a behavior pattern more than to a final age, occupation, lifestyle, or identity segment.
- Demographic and lifestyle segments should be treated as beachhead hypotheses until stronger segment-specific evidence exists.
- The current evidence supports testing who has the pain. It does not yet prove who will buy.

## The wake-up failure pattern

The early evidence suggests that wake-up failure can include several different failure points.

### Alarm does not wake the user

The user may sleep through alarms or need many alarms before waking.

Possible indicators:

- sets many alarms
- needs loud alarms
- has tried placing the phone far away
- still wakes late despite basic alarm hacks

Evidence basis:

- In the 2024 interviews, one respondent reported usually taking 7 alarms.
- One respondent said they started sleeping through placing the phone far away.
- Old MVP logs include cases where users woke later than alarm time or slept through/failed to complete wake-up on some days.

### Alarm wakes the user, but wake completion fails

The user may technically wake up, but does not actually get out of bed.

Possible indicators:

- turns off the alarm while half-asleep
- stays in bed after waking
- loses time after the first alarm
- gets up briefly and returns to bed
- needs external friction to complete waking

Evidence basis:

- Customer interview language includes “Getting out of bed once awake,” “stay in bed,” and “Gets you out of bed effectively.”
- Dennis's old MVP baseline was waking at 8:30 but not getting out of bed until 10:00. On successful logged old MVP days, his out-of-bed time matched or was close to wake/alarm time.
- External waking-up synthesis supports the conceptual distinction between alarm activation, alarm dismissal/snooze, and actual wake completion.

### The user bypasses or weakens the alarm system

The user may create loopholes while tired, half-awake, or motivated to keep sleeping.

Possible indicators:

- disables alarms before they ring
- reduces alarm friction the night before or shortly before waking
- unplugs or moves alarm devices
- finds ways around alarm apps or phone settings
- treats snooze, dismiss, or schedule edits as escape paths

Evidence basis:

- Old MVP behavior included off-button disablement during the alarm period and battery backup if unplugged.
- Old MVP bypass/failure notes support the need to track unplugging, pre-alarm shutoff, return-to-bed, loopholes, and technical failure separately.
- Dennis wrote that he wanted to get back in bed every day but could not, so his only option was to take a shower.

### The user wakes, but the morning still feels brutal

Some users may complete waking but still feel heavy, foggy, or groggy.

Evidence basis:

- Old MVP user feedback says testers still wanted an easier or less-groggy wake-up after wake completion.
- The waking-up synthesis treats sleep inertia as relevant but claim-sensitive.
- The snooze/sleep-inertia experiment had only 10 participants, so it cannot support broad public claims.

Claim boundary:

- This is relevant target-customer pain.
- Orisen has not yet validated reduced grogginess, reduced sleep inertia, or sleep-stage-aware intervention outcomes.

## Strong early customer traits

A strong early customer likely has several of these traits:

- They frequently oversleep or almost oversleep.
- They struggle most weekdays or on recurring high-stakes mornings.
- They sleep through alarms or need multiple alarms.
- They dismiss alarms while half-asleep.
- They wake up but do not get out of bed.
- They return to bed after initially getting up.
- They have already tried basic workarounds.
- They feel embarrassed, frustrated, stressed, or out of control because of mornings.
- Being late causes real consequences.
- They want a system that makes wake completion harder to avoid.
- They would consider paying for reliable wake completion.

Evidence basis:

- Customer interviews support recurring pain for some respondents, including daily or most-day problems among problem-having respondents.
- Old MVP data supports wake-completion value most strongly for users with a large alarm-to-out-of-bed gap.
- External research supports wake-up difficulty as a meaningful problem area, but not Orisen-specific purchase intent.

Potential weak-fit traits:

- They wake up easily most days.
- They only want a nicer alarm sound.
- They mainly want motivation content.
- They only want sleep scores or passive sleep data.
- They are curious about sleep tech but do not have a painful wake-up problem.

Evidence basis:

- In the 2024 interviews, 6 of 10 respondents had no meaningful wake-up problem or did not complete a problem-positive survey path.
- This supports filtering out low-pain users instead of treating everyone who uses an alarm as the target customer.

## Beachhead segment hypotheses

These are early hypotheses, not final ICP decisions.

The stronger filter is still behavior:

> Does this person repeatedly fail between alarm time and actually being out of bed?

### Chronic oversleepers and alarm dismissers

This is currently the strongest behavioral beachhead hypothesis.

Why this segment may matter:

- Their pain maps directly to presence-based wake completion.
- They are more likely to understand why a normal alarm is not enough.
- They may have already tried multiple alarms, phone placement tricks, alarm apps, or willpower-based systems.
- They may experience immediate consequences from missed mornings.

Evidence basis:

- Customer interviews include multiple-alarm and phone-far-away failure examples.
- Old MVP data and user feedback most directly support the value of forcing or strongly encouraging bed exit.
- External waking-up synthesis supports repeated snoozing, delayed bed exit, oversleeping, and missed obligations as relevant problem themes.

Evidence status:

- Strongest current behavioral segment hypothesis.
- Not yet validated as a paid, scalable segment.

### Students and young adults with real consequences

Students and young adults are a plausible segment to investigate, especially when the wake-up problem affects classes, exams, work shifts, religious obligations, appointments, or other commitments.

Why this segment may matter:

- The 2024 interview sample was heavily skewed young: 8 of 10 respondents were age 23 or younger.
- The old MVP testers were mostly university students or founder-connected young users, with one full-time worker.
- Expert commentary supports investigating teens and young adults.
- Young adults may have irregular sleep schedules, screen-time-related issues, and rigid obligations.

Evidence status:

- Plausible and supported enough to investigate.
- Not proven as the final ICP.
- The existing young-user evidence is sample-skewed and founder-connected, so it cannot prove that young adults are the best buyers.

### Early-career professionals with rigid schedules

Early-career professionals with high consequences for lateness are a plausible segment.

Why this segment may matter:

- Being late can affect work reputation, income, performance reviews, or job security.
- The pain may be easier to monetize if the user connects wake-up reliability to work outcomes.
- The customer may have enough disposable income for a hardware solution.

Evidence basis:

- Customer interviews include 2 full-time workers, but the sample is too small to compare workers against students.
- Sabeeh was a full-time worker in the old MVP testing context, but his data was mixed and included bug/failure ambiguity.
- This segment is mostly logic-driven and needs more direct evidence.

Evidence status:

- Plausible hypothesis.
- Needs direct interviews, waitlist tagging, prototype tests, and willingness-to-pay evidence.

### Shift workers and inconsistent-schedule users

Shift workers and people with irregular schedules are a plausible segment to investigate.

Why this segment may matter:

- Irregular schedules can make waking harder.
- Consequences of being late can be high.
- Standard alarm routines may be less reliable when sleep timing changes often.

Evidence basis:

- Expert commentary supports investigating shift workers.
- External waking-up research supports the broader problem of morning difficulty and wake-up failure.
- Current Orisen-specific evidence does not yet strongly include shift workers.

Evidence status:

- Expert-informed hypothesis.
- Not strong enough to make shift workers the first ICP by default.

### Performance-focused users with actual wake-up pain

Biohackers, athletes, founders, and performance-focused users may be useful early adopters only when they also have real wake-up pain.

Why this segment may matter:

- They may be open to new sleep technology.
- They may understand closed-loop intervention faster than casual consumers.
- They may give detailed feedback.

Evidence basis:

- This segment is more of a reachability and early-adopter hypothesis than a direct evidence-backed target.
- There is not enough current evidence to prioritize performance-focused users above severe wake-up-pain users.

Evidence status:

- Useful exploratory segment.
- Should not be prioritized above high-pain wake-up sufferers unless evidence shows stronger pain, willingness to pay, and reachability.

## Who Orisen is not for first

Orisen should not be designed first for:

- casual sleep trackers
- people who only want sleep scores or dashboards
- people with mild interest but low pain
- users who mainly want a prettier alarm clock
- users who wake up reliably already
- users who only want motivation quotes or morning routine content
- users who are unwilling to pay for wake-up reliability
- users who primarily need clinical diagnosis or treatment
- medical users requiring regulated, clinical, diagnostic, or treatment claims

Evidence basis:

- In the 2024 interview sample, the wake-up problem was not universal.
- Product evidence is strongest for wake completion, not passive tracking, dashboards, diagnosis, or clinical treatment.
- `claims-and-evidence.md` does not support medical, diagnostic, clinical, sleep-stage, or sleep-inertia claims.

## Pain-level qualification criteria

A person is more likely to be an early target customer if they answer yes to several of these questions:

- Do they fail to wake up on time repeatedly?
- Do they wake up but stay in bed?
- Do they turn off alarms without fully remembering it?
- Do they go back to sleep after dismissing alarms?
- Do they return to bed after getting up?
- Do they need many alarms or escalating alarm hacks?
- Have standard alarms, phone alarms, and alarm apps failed them?
- Does being late create real consequences?
- Do they feel frustration, shame, stress, or loss of control around mornings?
- Would they pay for something that makes wake completion harder to avoid?
- Would they tolerate some friction during the wake window if it protected them from half-asleep bypass?

A person is less likely to be an early target customer if they answer yes to these questions:

- Do they wake up reliably with a normal phone alarm?
- Is their main interest sleep data rather than wake-up reliability?
- Are mornings only mildly annoying rather than painful?
- Are they unwilling to accept any anti-bypass friction?
- Are they looking for clinical sleep-disorder treatment rather than a consumer wake-up product?

## Safe customer claims

Safe or careful customer claims:

- Orisen is built for people who struggle to wake up.
- Orisen is for people whose real problem is getting out of bed, not just setting an alarm.
- Orisen is designed for users who need more than another phone alarm.
- Orisen's first target customer is pain-driven, not casual wellness-driven.
- Some early evidence suggests wake-completion failure is a meaningful problem for certain users.
- Students, young adults, shift workers, early-career professionals, and severe oversleepers are segments worth investigating.
- External waking-up research supports the broader problem framing around repeated snoozing, delayed bed exit, oversleeping, and missed obligations.

## Claims and assumptions to avoid

Do not claim yet:

- Students are definitively the ICP.
- Shift workers are definitively the ICP.
- Young adults are definitively the ICP.
- Biohackers are definitively the ICP.
- Most people need Orisen.
- Orisen has proven broad willingness to pay.
- Orisen has proven product-market fit.
- Orisen eliminates grogginess.
- Orisen reduces sleep inertia.
- Orisen fixes sleep disorders.
- Orisen wakes users in the perfect sleep stage.
- Orisen guarantees users will never oversleep.
- External sleep research proves Orisen works.
- Survey percentages prove buyer demand.

Avoid turning early evidence into hard market conclusions.

## Evidence basis

### Customer interviews

Source:

- `research/customer-interviews/2024-alarm-clock-interviews.md`

Relevant numbers:

- 10 total responses.
- Age range: 19 to 80.
- 8 of 10 respondents were age 23 or younger.
- Working status: 5 university students, 1 university student with part-time work, 2 full-time workers, 2 blank/unknown.
- Problem intensity: 2 definitely had wake-up problems, 2 somewhat had wake-up problems, 6 had none or did not complete a problem-positive path.
- Frequency among responses included 2 at 7/7 days, 2 at 5/7 days, 1 at 1/7 days, 1 weekdays/off, 3 never, 1 blank/unclear.
- 7 of 10 respondents mentioned camera discomfort.

Supported interpretations:

- Some people experience repeated wake-up and get-out-of-bed problems.
- The wake-up problem is not universal.
- Getting out of bed can be distinct from hearing the alarm.
- Multiple alarms and phone-placement hacks appeared as existing workarounds.
- Morning phone interaction may be an adjacent failure mode.
- Camera discomfort appeared multiple times, supporting the non-camera direction.

Limitations:

- Small convenience sample.
- Mostly younger respondents.
- Not statistically representative.
- Not enough data to make subgroup claims by age, student status, gender, occupation, ethnicity, religion, or living situation.
- Does not prove willingness to pay or product-market fit.

### Old MVP prototype and pilot evidence

Sources:

- `product/old-mvp/old-mvp.md`
- `product/old-mvp/old-mvp-test-row-labels.md`
- `product/old-mvp/old-mvp-bypass-and-failure-notes.md`
- `product/old-mvp/old-mvp-user-feedback.md`

Relevant numbers and details:

- Old MVP was tested by founder and 3 founder-connected testers.
- Dennis's baseline: wake at 8:30, out of bed at 10:00.
- On Dennis's successful logged days, out-of-bed time matched or was close to alarm/wake time.
- Hamza's baseline: alarm 4:00, wake 4:50, out of bed 5:00.
- Several Hamza days showed waking and getting out of bed within a few minutes of alarm time, but there were also failures or partial failures.
- Sabeeh's baseline: alarm 5:30, wake 6:30, out of bed 9:00.
- Sabeeh data was mixed and included bug/failure ambiguity.
- One tester, Dennis, said he would buy the device “right now,” likely around a roughly $100 discussed price point.

Supported interpretations:

- The old MVP supports the wake-completion wedge as the strongest early product direction.
- The strongest pilot signal is getting the user out of bed closer to alarm time.
- The product direction is not purely conceptual. A physical presence-based prototype existed and was used in real morning contexts.
- User feedback supports that wake completion is valuable but does not solve the entire morning experience.

Limitations:

- Small sample.
- Founder/friend-connected testers.
- Historical prototype, not production hardware.
- Self-reported data.
- Some rows incomplete.
- Some days had failures, bugs, or sleeping again.
- Does not prove broad demand, production reliability, retention, product-market fit, or paid conversion.

### External waking-up research

Source:

- `research/external-research/waking-up/synthesis.md`

Reviewed source categories:

- Nature Scientific Reports / SleepCycle app-data study on snooze alarm use.
- Snooze alarm / sleep inertia study with corrected DOI.
- Talker Research / Avocado Green Mattress morning struggles survey.
- MattressInquirer oversleeping survey article.
- SleepJunkie waking-up survey article, currently weak/inaccessible.
- Trotti sleep inertia / sleep drunkenness review, currently an incomplete guardrail source.

Relevant numbers and details:

- Talker Research reports a 2,000-person U.S. online survey and says 38% of respondents agreed they are “bad” at mornings.
- The snooze/sleep-inertia experimental portion had only 10 participants.
- MattressInquirer is more directly related to oversleeping and missed obligations but is weaker evidence because it uses an MTurk convenience sample, includes respondents as young as 15, lacks field dates, is self-reported, and is exploratory.
- Nature Scientific Reports / SleepCycle app-data study is the strongest processed external source for repeated snooze behavior, but its app-user dataset is self-selected and should not be treated as general-population prevalence.

Supported interpretations:

- Waking up can be framed as a multi-step process, not only an alarm-sound event.
- Repeated snoozing is a real behavior pattern in at least some measured or surveyed groups.
- Some people report delayed bed exit, oversleeping, repeated snoozing, and missed obligations.
- External research supports the need to distinguish alarm dismissal from actual wake completion.
- Sleep inertia and grogginess are relevant concepts, but require careful handling.

Limitations:

- External research does not prove Orisen works.
- External research does not prove willingness to pay.
- External research does not prove the final ICP.
- External research does not prove Orisen reduces grogginess or sleep inertia.
- Exact survey percentages should not be used prominently unless attributed, caveated, and approved through `product/claims-and-evidence.md`.

### Expert commentary

Source:

- `research/expert-commentary/expert-commentary-synthesis.md`

Supported investigation areas:

- severe oversleepers
- repeated snoozers
- return-to-bed users
- teens and young adults
- young adults with rigid schedules
- shift workers

Supported interpretations:

- These are plausible segments to investigate.
- Expert commentary supports caution around grogginess and sleep inertia because they are multi-cause.

Limitations:

- Expert commentary does not prove market demand.
- It does not prove a final ICP.
- It does not validate reduced grogginess, reduced sleep inertia, or artificial sleep phase transitioning.

### Competitor and substitute research

Source:

- `research/external-research/competitors-and-substitutes/synthesis.md`

Current status:

- The competitor/substitute synthesis is not yet developed enough to strongly influence target-customer conclusions.
- It should be revisited after structured review evidence is added.

Potential future use:

- Identify what people already try.
- Identify what existing products fail to solve.
- Identify language used in reviews by chronic snoozers, oversleepers, and alarm dismissers.

### Marketing performance signal

Source:

- `marketing/post-performance-log.md`

Supported interpretation:

- Early founder-led marketing performance and waitlist signups suggest message resonance around the wake-up problem.

Limitations:

- Waitlist signups do not prove willingness to pay.
- One post does not prove the final ICP.
- Marketing resonance should not override customer evidence or claim boundaries.

## Evidence needed to narrow the first segment

To narrow the first target customer segment, collect evidence on:

- Which segment has the strongest repeated wake-up pain.
- Which segment most clearly understands wake completion.
- Which segment has the highest willingness to pay.
- Which segment is easiest to reach without paid ads.
- Which segment is most likely to test a prototype.
- Which segment gives the clearest product feedback.
- Which segment has the strongest referral potential.
- Which segment tolerates anti-bypass friction without feeling punished.
- Which segment values wake completion versus less-groggy waking versus both.
- Which segment has the highest consequence from wake-up failure.
- Which segment keeps using the product after novelty fades.

Useful validation methods:

- customer interviews with severe oversleepers
- interviews with students and young adults who miss commitments
- interviews with early-career professionals with rigid schedules
- interviews with shift workers and irregular-schedule workers
- tagged waitlist survey responses
- willingness-to-pay tests
- preorder or deposit tests
- prototype pilots with event logs
- comparison of baseline wake time, alarm time, and out-of-bed time
- return-to-bed and bypass-attempt tracking
- subjective morning difficulty and grogginess tracking
- competitor review mining for repeated alarm failure language

## Open questions

- Who should be the first 100 users?
- Which behavior pattern predicts strongest demand: sleeping through alarms, dismissing alarms, staying in bed, returning to bed, or severe grogginess?
- Which demographic segment contains the most reachable high-pain users?
- Which segment should be targeted first for pilots?
- Which segment should be targeted first for paid preorders?
- Which segment best supports the fundraising narrative without distorting the product?
- What price point is acceptable for the first customer segment?
- How much anti-bypass friction will high-pain users tolerate?
- Do users care more about guaranteed wake completion, easier wake-up, or both?
- What evidence would justify prioritizing one segment over the others?

## Notes

- This file is still a target-customer hypothesis doc, not a final ICP decision.
- Update this file after customer interviews, pilot feedback, waitlist analysis, pricing tests, and competitor/substitute synthesis.
- Keep target-customer conclusions evidence-led.
- Do not use this file to define channel-specific marketing strategy.
- Downstream marketing docs may translate this customer truth into positioning, messaging, X content, and posting strategy, but those docs should not change the customer truth without new evidence.

## Appendix: Source weighting for this doc

This table records how strongly each upstream file should influence future updates to this file.

Sort order:

1. Use strength
2. Evidence value
3. Authority value

| File | Read? | Use strength | Evidence value | Authority value | Main use in this file | Caution |
|---|---:|---|---|---|---|---|
| `research/customer-interviews/2024-alarm-clock-interviews.md` | Yes | Very high | Very high | Medium | Best source for early customer pain patterns: repeated wake-up failure, getting out of bed, many alarms, phone failure mode, camera discomfort. | Small convenience sample. Do not make demographic or statistical conclusions. |
| `product/old-mvp/old-mvp.md` | Yes | Very high | High | Medium | Shows what customer behavior the prototype actually addressed: staying in bed, returning to bed, bypassing normal alarm shutoff. | Historical prototype, not current product spec or broad validation. |
| `product/old-mvp/old-mvp-user-feedback.md` | Yes | Very high | High | Medium | Shows testers valued wake completion and still wanted less brutal wake-ups. Good for understanding high-pain users. | Founder-reported, small sample, no broad willingness-to-pay proof. |
| `product/claims-and-evidence.md` | Yes | Very high | Medium | Very high | Final boundary for what can safely be concluded and said. Prevents overclaiming from source evidence. | Should constrain claims, but should not replace source evidence for customer detail. |
| `product/old-mvp/old-mvp-test-row-labels.md` | Yes | High | High | Medium-low | Useful for seeing whether the product changed bed-exit timing, not just alarm interaction. | Small, messy pilot data. Use directionally. |
| `product/old-mvp/old-mvp-bypass-and-failure-notes.md` | Yes | High | High | Medium-low | Useful for defining users with bypass behavior: unplugging, pre-alarm shutoff, loopholes, returning to bed. | More product/failure-mode focused than customer-segment focused. |
| `research/external-research/waking-up/synthesis.md` | Yes | High | Medium-high | Medium | Supports the broader problem frame: wake-up is not always a clean one-step event; snoozing, delayed bed exit, oversleeping, and missed obligations exist. | External research supports problem framing, not Orisen efficacy or customer willingness to pay. |
| `ai-context/claim-control/claim-control-log.md` | Yes | High | Medium-high | High | Useful evidence ledger summarizing what each evidence source supports and does not support. | Compressed summary. Good for safety, less good for nuance. |
| `ai-context/claim-control/claim-control-system.md` | Yes | High | Low | High | Defines how to classify evidence strength and avoid turning weak signals into facts. | Rules file, not customer evidence. |
| `ai-context/source-of-truth-rules.md` | Yes | High | Low | High | Tells how to resolve conflicts and separate assumptions from evidence. | Rules file, not evidence. |
| `research/expert-commentary/expert-commentary-synthesis.md` | Yes | Medium-high | Medium | Medium | Supports investigating young adults, rigid-schedule users, repeated snoozers, return-to-bed users, and shift workers. Adds caution around grogginess and sleep inertia. | Expert commentary does not prove ICP, market size, or efficacy. |
| `product/product-overview.md` | Yes | Medium-high | Low-medium | High | Keeps target customer aligned with the product wedge: wake completion, non-contact intervention, not passive tracking. | Product framing should not override evidence about who actually has pain. |
| `ai-context/current-state.md` | Yes | Medium | Low | Very high | Alignment check: make sure this file does not drift away from current company direction. | Do not treat it as evidence. It is partly a prior synthesis/decision doc. |
| `ai-context/ai-operating-mode.md` | Yes | Medium | Low | Medium | Keeps the assistant non-agreeable and evidence-disciplined. | Process file, not content. |
| `ai-context/doc-creation-rules.md` | Yes | Medium | Low | Medium | Helps structure the doc properly and label assumptions. | Process file, not evidence. |
| `product/product-read-rules.md` | Yes | Medium | Low | Medium | Helps choose which product docs to read. | Routing file, not content. |
| `marketing/post-performance-log.md` | Maybe | Medium-low | Medium-low | Low | Useful as an early signal that founder-led messaging around the wake-up problem resonated. | Marketing performance does not prove ICP, product-market fit, willingness to pay, or target market. |
| `product/product-questions-and-objections.md` | Maybe | Medium-low | Low-medium | Medium-low | Useful for edge-case customer objections around override, anti-bypass, and user trust. | Working question log, not target-customer evidence. |
| `research/external-research/competitors-and-substitutes/synthesis.md` | Maybe | Low for now | Low currently | Low | May eventually help identify what people already try and where alternatives fail. | Not synthesized yet, so it should not strongly influence this file right now. |
| `ai-context/repo-governance/repo-editing-rules.md` | Yes, before editing | Low content / high process | Low | Medium | Required for safe direct GitHub editing. | Not relevant to target-customer conclusions. |
