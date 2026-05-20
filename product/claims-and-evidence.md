# Claims and Evidence

## Purpose of this file

This file defines which Orisen product claims are currently safe, which claims require caution, and which claims should not be made until stronger evidence exists.

Use this file when writing or reviewing product, marketing, fundraising, website, pitch deck, customer interview, investor outreach, or sales language.

This file should stay consistent with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/claim-control/claim-control-roadmap.md`

## Evidence inputs

This file is the downstream claim authority for Orisen. It should synthesize claim-relevant evidence from the repo, but it should not duplicate all raw evidence.

Primary upstream evidence inputs:

- `research/customer-interviews/`
  - Direct customer discovery, raw interview data, customer pain themes, and interview limitations.
- `product/old-mvp/`
  - Old physical MVP build notes, pilot behavior, wake-completion behavior, bypass attempts, failure modes, and qualitative user feedback.
- `marketing/post-performance-log.md`
  - LinkedIn post performance, waitlist conversion, website traffic, Microsoft Clarity notes, and campaign learnings.
- `research/expert-commentary/`
  - Sleep-expert meeting notes, expert synthesis, validation suggestions, claim warnings, and roadmap realism.
- `research/external-research/`
  - Problem-first external research, including waking-up, going-to-sleep, during-sleep, sleep-tracking/validation, competitors/substitutes, and market/category sources.
- `ai-context/claim-control/claim-control-log.md`
  - Conservative evidence entries and claim-support tracking when evidence is important enough to affect allowed claims.

Use this file to answer:

- What can Orisen safely claim today?
- What can Orisen claim carefully?
- What is only a roadmap hypothesis?
- What is unsupported and should not be said?
- What upstream evidence supports each claim?
- What upstream evidence does not prove?

Important rule:

- Raw files preserve what sources, users, experts, or tests said.
- Synthesis files explain what those sources mean.
- This file defines what Orisen is allowed to claim.

When updating this file, read the relevant upstream evidence first and link back to the synthesis or source files where useful.

## Relationship to the claim-control system

`ai-context/claim-control/claim-control-system.md` is the authority for how Orisen classifies evidence and claim strength.

This file applies that claim-control system to Orisen's product claims.

When this file and `ai-context/claim-control/claim-control-system.md` appear to conflict, use `ai-context/claim-control/claim-control-system.md` for evidence classification and update this file to match it.

## Core rule

Do not let the product story move faster than the evidence.

Orisen can be ambitious, but external claims must clearly separate:

- What is currently validated
- What is built but not validated
- What is being built
- What is planned
- What is a hypothesis
- What is long-term vision
- What is unsupported or unsafe

If a claim is not clearly supported, weaken the wording.

## Current evidence status

### Strongest validated wedge

The strongest validated wedge is presence-based wake completion.

Current evidence supports the idea that:

- People with painful wake-up problems understand the value of a system that helps force real wake completion.
- A device that does not fully stop until the user physically leaves bed is meaningfully different from a normal alarm.
- Re-triggering the alarm if the user returns to bed addresses a real user behavior problem.
- Wake-up reliability is the strongest early product anchor.

Primary source areas:

- `product/old-mvp/`
- `research/customer-interviews/`
- `marketing/post-performance-log.md`
- `ai-context/claim-control/claim-control-log.md`

This evidence should still be treated as early validation, not broad-market proof.

### Strategically important but less validated

The following are strategically important, but not yet validated enough for strong public claims:

- Reduced grogginess
- Reduced sleep inertia
- Sleep-phase-aware wake intervention
- Sensor-informed wake intervention
- Artificial sleep phase transitioning
- Radar-based sleep-stage estimation
- Personalized wake timing
- Long-term sleep-state intervention

Primary source areas:

- `research/expert-commentary/`
- `research/external-research/`
- `product/old-mvp/old-mvp-user-feedback.md`

These can be described as product direction, roadmap, hypothesis, or active testing, but should not be presented as proven outcomes.

## Claim categories

### Safe current claims

These claims are generally safe if used honestly and without exaggeration:

- Orisen is a non-contact sleep intervention device.
- Orisen is built for people who struggle to wake up.
- Orisen is designed to make waking up more reliable.
- Orisen uses presence detection to help determine whether the user actually got out of bed.
- Orisen is designed so the final wake-up behavior can run locally on the device.
- Orisen is not primarily a sleep tracker.
- Orisen is not a wearable.
- Orisen is designed around wake-up intervention, not passive sleep data.
- The first wedge is presence-based wake completion.

### Safe but careful claims

These claims can be used, but should be worded carefully:

- Orisen helps make sure you actually get out of bed.
- Orisen is designed to reduce the chance of dismissing an alarm and going back to sleep.
- Orisen aims to make mornings feel less brutal.
- Orisen uses gradual audio and light to support the wake-up process.
- Orisen is working toward sensor-informed wake intervention.
- Orisen is working toward sleep-phase-aware wake-up behavior.
- Orisen aims to reduce grogginess through gradual, sensor-informed intervention.

These should not imply clinical proof, perfect reliability, or guaranteed physiological outcomes.

### Planned or roadmap claims

These claims should be framed as roadmap, development direction, or future product capability:

- Orisen will improve sleep-phase-aware wake intervention over time.
- Orisen is building toward artificial sleep phase transitioning.
- Orisen is building toward radar-based sleep-state estimation.
- Orisen is building toward personalized wake intervention.
- Orisen may eventually support bedtime routines, white noise, sleep onset support, and long-term user adaptation.

Use phrasing like:

- “building toward”
- “working toward”
- “planned”
- “roadmap”
- “future versions”
- “designed to eventually support”

### Claims that require validation before stronger use

Do not make these claims strongly until supported by real-world user testing, technical validation, or clinical-quality evidence where relevant:

- Orisen reduces grogginess.
- Orisen reduces sleep inertia.
- Orisen detects sleep stages accurately.
- Orisen wakes users in a lighter sleep stage.
- Orisen moves users from deep sleep toward lighter sleep.
- Orisen improves morning alertness.
- Orisen improves sleep quality.
- Orisen personalizes wake-up timing based on sleep state.

Until validated, these should be softened as aims, hypotheses, or development goals.

### Claims to avoid for now

Avoid these claims unless future evidence and regulatory strategy clearly support them:

- “Eliminates grogginess”
- “Wakes you in the perfect sleep stage”
- “Controls your sleep stages”
- “Clinically proven”
- “Clinically improves sleep inertia”
- “Guarantees better sleep”
- “Accurately detects sleep stages”
- “Manipulates biology in real time”
- “Treats sleep disorders”
- “Medical-grade sleep intervention”

These are too strong for the current evidence base.

## Recommended language

### For the product

Use:

> Orisen is a non-contact sleep intervention device for people who struggle to wake up.

Avoid:

> Orisen is a medical-grade sleep-stage control device.

### For the first wedge

Use:

> Orisen uses presence detection to help ensure wake completion by checking whether you actually got out of bed.

Avoid:

> Orisen guarantees you will never oversleep again.

### For wake-up reliability

Use:

> Orisen is designed to make waking up more reliable than a normal alarm by responding to whether you actually leave bed.

Avoid:

> Orisen guarantees perfect wake-up reliability.

### For grogginess reduction

Use:

> Orisen aims to make mornings feel less brutal through gradual audio, light, and future sensor-informed intervention.

Avoid:

> Orisen eliminates grogginess.

### For sleep-phase-aware intervention

Use:

> Orisen is building toward sleep-phase-aware wake intervention that uses sensor data to guide the wake-up process.

Avoid:

> Orisen accurately detects your sleep stage and wakes you at the perfect time.

### For artificial sleep phase transitioning

Use:

> Orisen is exploring artificial sleep phase transitioning as a future direction for preparing users for wake-up.

Avoid:

> Orisen controls your sleep stages in real time.

## Evidence classification

Use `ai-context/claim-control/claim-control-system.md` when reviewing the evidence status of a claim.

Important claim classifications include:

- Validated
- Early signal
- Built but not validated
- Planned
- Hypothesis
- Long-term vision
- Unsupported or unsafe claim

Do not create a separate evidence scale in this file.

This file should describe the product-specific claim implications of the claim-control system.

## Current claim status table

| Claim | Current status | Safe wording |
|---|---|---|
| Orisen is non-contact | Safe current claim | “Non-contact sleep intervention device” |
| Orisen is for people who struggle to wake up | Safe current claim | “Built for people who struggle to wake up” |
| Orisen is not primarily a sleep tracker | Safe current claim | “Not a passive sleep tracker” |
| Orisen uses presence-based wake completion | Strongest validated wedge | “Uses presence detection to help ensure wake completion” |
| Orisen prevents going back to bed | Careful claim | “Designed to reduce the chance of dismissing the alarm and going back to bed” |
| Orisen guarantees wake-up | Careful claim | Use internally with caution; externally prefer “designed to make waking up more reliable” |
| Orisen reduces grogginess | Needs validation | “Aims to make mornings feel less brutal” |
| Orisen reduces sleep inertia | Needs validation | “Aims to reduce sleep inertia through gradual, sensor-informed intervention” |
| Orisen detects sleep stages | Needs technical validation | “Working toward sleep-phase-aware wake-up behavior” |
| Orisen performs artificial sleep phase transitioning | Planned or exploratory | “Exploring artificial sleep phase transitioning as a future direction” |
| Orisen improves sleep quality | Not validated | Avoid unless future evidence supports it |
| Orisen is clinically proven | Not supported | Do not use |

## How to review marketing and fundraising claims

When reviewing public language, ask:

1. Is this claim about what exists today, what is being built, or what is planned?
2. Is there evidence for this claim?
3. Would a reasonable customer or investor think this is already proven?
4. Does the wording imply clinical proof or technical precision that does not exist yet?
5. Can the claim be made more accurately without weakening the story too much?

If the claim is unsupported, rewrite it instead of deleting the ambition entirely.

## Relationship to marketing and fundraising

Marketing and fundraising may be more emotionally compelling than internal product docs, but they must not claim more than the evidence supports.

Marketing can emphasize:

- Painful mornings
- Oversleeping
- Sleeping through alarms
- Getting out of bed
- A system that responds to whether the user actually left bed
- The ambition to make mornings less brutal

Fundraising can emphasize:

- The validated wake-completion wedge
- The larger sleep intervention vision
- The distinction from sleep trackers and wearables
- The roadmap toward sensor-informed and sleep-phase-aware intervention

Both should avoid implying that grogginess reduction, sleep-stage detection, or artificial sleep phase transitioning are already fully proven.

## What to update as evidence improves

Update this file when:

- A claim becomes validated by user testing.
- A claim is disproven or weakened by testing.
- Technical validation changes what can safely be said.
- Product scope changes the first customer-ready product.
- Marketing or fundraising needs stronger language and evidence exists to support it.
- A future regulatory or clinical strategy changes allowable claims.

When evidence improves, update the relevant raw/source files and synthesis docs first. If the evidence materially changes claim strength, update `ai-context/claim-control/claim-control-log.md`. Then update this file before updating marketing, fundraising, pitch, website, or customer-facing docs.

## Current summary

Orisen can currently claim that it is a non-contact sleep intervention device for people who struggle to wake up, with a strongest validated wedge around presence-based wake completion.

Orisen can carefully say it aims to make mornings feel less brutal through gradual audio, light, and future sensor-informed wake intervention.

Orisen should not yet strongly claim that it eliminates grogginess, accurately detects sleep stages, performs proven artificial sleep phase transitioning, or clinically improves sleep inertia.
