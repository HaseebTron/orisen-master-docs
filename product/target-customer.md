# Target Customer

## Purpose

This file defines Orisen's target customer assumptions, early beachhead hypotheses, excluded users, and evidence needed to narrow the first customer segment.

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
- This file should separate evidence-backed patterns from hypotheses that still need validation.

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

## Primary ICP hypothesis

The current primary ICP hypothesis is:

> People who repeatedly fail between alarm time and actually being out of bed.

This is a behavioral ICP, not a demographic ICP.

The strongest current evidence points to the behavior pattern more than to a final age, occupation, lifestyle, or identity segment.

Demographic and lifestyle segments should be treated as beachhead hypotheses until stronger segment-specific evidence exists.

## The wake-up failure pattern

The early evidence suggests that wake-up failure can include several different failure points.

### Alarm does not wake the user

The user may sleep through alarms or need many alarms before waking.

Possible indicators:

- sets many alarms
- needs loud alarms
- has tried placing the phone far away
- still wakes late despite basic alarm hacks

### Alarm wakes the user, but wake completion fails

The user may technically wake up, but does not actually get out of bed.

Possible indicators:

- turns off the alarm while half-asleep
- stays in bed after waking
- loses time after the first alarm
- gets up briefly and returns to bed
- needs external friction to complete waking

### The user bypasses or weakens the alarm system

The user may create loopholes while tired, half-awake, or motivated to keep sleeping.

Possible indicators:

- disables alarms before they ring
- reduces alarm friction the night before or shortly before waking
- unplugs or moves alarm devices
- finds ways around alarm apps or phone settings
- treats snooze, dismiss, or schedule edits as escape paths

### The user wakes, but the morning still feels brutal

Some users may complete waking but still feel heavy, foggy, or groggy.

This is relevant target-customer pain, but Orisen has not yet validated reduced grogginess, reduced sleep inertia, or sleep-stage-aware intervention outcomes.

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

Potential weak-fit traits:

- They wake up easily most days.
- They only want a nicer alarm sound.
- They mainly want motivation content.
- They only want sleep scores or passive sleep data.
- They are curious about sleep tech but do not have a painful wake-up problem.

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

Evidence status:

- Supported by customer discovery themes, old MVP behavior, old MVP user feedback, and waking-up research synthesis.
- Not yet validated as a paid, scalable segment.

### Students and young adults with real consequences

Students and young adults are a plausible segment to investigate, especially when the wake-up problem affects classes, exams, work shifts, religious obligations, appointments, or other commitments.

Why this segment may matter:

- Early customer interviews and prototype testing included younger users.
- Expert commentary suggests young people may be a high-pain group worth investigating.
- Irregular sleep schedules, screen time, and delayed sleep patterns may contribute to the problem.

Evidence status:

- Plausible and supported enough to investigate.
- Not proven as the final ICP.
- Do not claim that students or young adults are definitively the first market without stronger evidence.

### Early-career professionals with rigid schedules

Early-career professionals with high consequences for lateness are a plausible segment.

Why this segment may matter:

- Being late can affect work reputation, income, performance reviews, or job security.
- The pain may be easier to monetize if the user connects wake-up reliability to work outcomes.
- The customer may have enough disposable income for a hardware solution.

Evidence status:

- Plausible hypothesis based on pain/consequence logic.
- Needs direct interviews, waitlist tagging, prototype tests, and willingness-to-pay evidence.

### Shift workers and inconsistent-schedule users

Shift workers and people with irregular schedules are a plausible segment to investigate.

Why this segment may matter:

- Irregular schedules can make waking harder.
- Consequences of being late can be high.
- Standard alarm routines may be less reliable when sleep timing changes often.

Evidence status:

- Supported mainly as an expert-informed and logical segment hypothesis.
- Current direct Orisen evidence is not yet strong enough to make shift workers the first ICP by default.

### Performance-focused users with actual wake-up pain

Biohackers, athletes, founders, and performance-focused users may be useful early adopters only when they also have real wake-up pain.

Why this segment may matter:

- They may be open to new sleep technology.
- They may understand closed-loop intervention faster than casual consumers.
- They may give detailed feedback.

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

Avoid turning early evidence into hard market conclusions.

## Evidence basis

### Customer interviews

The 2024 alarm-clock customer interviews support several early patterns:

- Some people have repeated wake-up problems.
- For some people, getting out of bed is a distinct problem from hearing an alarm.
- Some users rely on multiple alarms or other basic hacks.
- Phone interaction can be part of the morning failure mode.
- Some respondents were uncomfortable with cameras in a bedroom device.

Limitations:

- Small convenience sample.
- Not statistically representative.
- Not enough data to make subgroup claims by age, student status, gender, occupation, ethnicity, religion, or living situation.
- Does not prove willingness to pay or product-market fit.

### Old MVP prototype and pilot evidence

The old MVP supports the wake-completion wedge as the strongest early product direction.

It demonstrated a physical presence-based wake-completion loop:

- alarm rings at the scheduled time
- radar detects whether the user is still in bed
- alarm continues or re-triggers if the user remains in bed or returns to bed
- alarm stops after the user leaves bed
- unplugging did not immediately bypass the device because of battery backup

The old MVP pilot and feedback suggest that some users valued being forced or strongly pushed to complete waking.

Limitations:

- Small sample.
- Founder/friend-connected testers.
- Historical prototype, not production hardware.
- Bugs and bypass cases existed.
- Does not prove broad demand, production reliability, or paid conversion.

### Old MVP bypass and failure evidence

Bypass and failure notes are especially useful for target-customer understanding because they show that some users may actively exploit loopholes when tired or half-awake.

Relevant patterns:

- trying to unplug the device
- trying to return to bed
- turning off or changing an alarm shortly before the alarm time
- needing pre-alarm lockout behavior
- needing escalation rather than a fixed-volume alarm
- needing logs to distinguish true success, partial success, bypass, and technical failure

This supports the view that Orisen's early customer may not simply need a louder alarm. They may need a system that protects their prior awake decision from their half-awake morning behavior.

### Expert commentary

Expert commentary supports investigating:

- severe oversleepers
- repeated snoozers
- return-to-bed users
- teens and young adults
- young adults with rigid schedules
- shift workers

Expert commentary also cautions that grogginess and sleep inertia are multi-cause and should not be treated as solved by wake completion, light, or sleep-stage shifting alone.

Limitations:

- Expert commentary does not prove market demand.
- It does not prove a final ICP.
- It does not validate reduced grogginess, reduced sleep inertia, or artificial sleep phase transitioning.

### External waking-up research

External waking-up research supports the broader problem frame that wake-up can involve repeated snoozing, delayed bed exit, oversleeping, missed obligations, and sleep inertia.

This research is useful for understanding the problem space.

Limitations:

- It does not prove Orisen works.
- It does not prove willingness to pay.
- It does not prove Orisen reduces grogginess or sleep inertia.
- It should not be used as a substitute for Orisen-specific validation.

### Competitor and substitute research

Competitor and substitute research may eventually help identify what users already try and what existing products fail to solve.

Current status:

- The competitor/substitute synthesis is not yet developed enough to strongly influence target-customer conclusions.
- It should be revisited after structured review evidence is added.

### Marketing performance signal

Early founder-led marketing performance and waitlist signups suggest early message resonance around the wake-up problem.

This is useful context, but weaker than direct customer and prototype evidence for defining the target customer.

Limitations:

- Waitlist signups do not prove willingness to pay.
- One post does not prove the final ICP.
- Marketing resonance should not override customer evidence or claim boundaries.

## Evidence needed to narrow the first segment

To narrow the first target customer segment, collect evidence on:

- Which segment has the strongest repeated wake-up pain
- Which segment most clearly understands wake completion
- Which segment has the highest willingness to pay
- Which segment is easiest to reach without paid ads
- Which segment is most likely to test a prototype
- Which segment gives the clearest product feedback
- Which segment has the strongest referral potential
- Which segment tolerates anti-bypass friction without feeling punished
- Which segment values wake completion versus less-groggy waking versus both
- Which segment has the highest consequence from wake-up failure
- Which segment keeps using the product after novelty fades

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
