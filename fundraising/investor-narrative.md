# Investor Narrative

## Purpose

This file defines the starter investor narrative for Orisen while separating what is built, validated, being built, planned, and still risky.

Use this file when working on pitch decks, teaser decks, investor emails, warm intros, fundraising strategy, and investor FAQ.

This file should stay consistent with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`

## Core investor story

Orisen is building toward ambient sleep intelligence: sleep technology that does not just track what happened, but helps guide sleep and wake outcomes.

The company is starting with the clearest wedge: reliable wake completion. Normal alarms stop when the user taps a button, even if the user is still in bed or returns to bed after dismissing the alarm. Orisen uses non-contact presence detection to check whether the user actually got out of bed and can re-trigger if they return.

Orisen is being built as a platform-capable ambient sleep device: one hardware foundation with sensing, audio, light, compute, connectivity, local control, and app/cloud support where useful. The hardware creates the bedroom interface; software defines the intervention.

Wake completion is the first software-defined sleep intervention. Future layers may expand into sensor-informed wake intervention, sleep onset support, bedtime routines, sleep-supportive audio and lighting, and broader ambient sleep intelligence as those capabilities are validated.

## What is strongest today

The strongest current wedge is presence-based wake completion.

This is the clearest difference from normal alarms, smart alarm clocks, and passive sleep trackers.

The current evidence supports the wake-completion wedge more strongly than it supports claims about reduced grogginess, sleep-stage accuracy, sleep inertia reduction, artificial sleep phase transitioning, or broad sleep improvement.

## What is being built

Current and near-term build direction includes:

- Local alarm execution
- App-based alarm setting
- Cloud/device sync
- Presence-based wake completion
- Re-trigger behavior if the user returns to bed
- Gradual audio and light wake-up
- Basic logging
- OTA update path
- Sensor-informed wake intervention where feasible

## What is planned or future-facing

Future-facing direction includes:

- Radar-based vital-sign and movement sensing
- Sleep-phase-aware wake intervention
- Artificial sleep phase transitioning
- Personalized wake timing
- Long-term adaptation
- Sleep onset support
- White noise and bedtime routines
- Subscription features where value is clear

These should be framed as roadmap or long-term direction unless evidence supports stronger claims.

## What is still risky or unproven

Important risks and open questions:

- Which early customer segment has the strongest willingness to pay
- How strong demand is beyond early interest and signups
- Required reliability standard for users to trust Orisen as a main alarm
- Radar signal quality in real bedrooms
- Sleep-stage estimation accuracy
- Whether sensor-informed intervention reduces perceived grogginess
- Whether future sleep-onset, bedtime, or sleep-quality interventions create measurable user value
- Price point
- Hardware cost and manufacturability
- Claims supported by evidence

## Claims boundary

Investor language can be ambitious, but it should not imply that unvalidated capabilities are already proven.

Avoid implying that Orisen currently:

- Eliminates grogginess
- Accurately detects sleep stages
- Controls sleep stages
- Clinically improves sleep inertia
- Guarantees better sleep
- Has proven artificial sleep phase transitioning
- Solves every sleep problem
- Turns all sleep problems into software-only problems
- Is a fully validated sleep platform

## Investor narrative structure

Use a vision-first, wedge-second structure:

1. Sleep tech is moving from passive tracking to active intervention.
2. Orisen is building toward ambient sleep intelligence: a non-contact system that helps guide sleep and wake outcomes.
3. The product is being built as a platform-capable ambient sleep device, where the hardware foundation creates the bedroom interface and software defines intervention behavior.
4. The first wedge is reliable wake completion because it is painful, clear, and easier to validate than broad sleep improvement.
5. Normal alarms only alert the user; Orisen checks whether the user actually got out of bed and can re-trigger if they return.
6. Early prototype evidence supports the wake-completion wedge, while broader intervention layers remain roadmap or hypothesis until validated.
7. Over time, Orisen may expand from wake reliability into additional sensor-informed and personalized sleep interventions.

## Evidence needed before strengthening the story

Before strengthening investor claims, update the relevant evidence and claim-control docs:

- `product/claims-and-evidence.md` for product claim boundaries and evidence summaries
- `ai-context/claim-control/claim-control-log.md` for durable claim-control decisions
- `marketing/post-performance-log.md` for marketing performance and waitlist evidence
- source-specific research folders for raw/source material and synthesis

This applies before strengthening claims around:

- User demand
- Willingness to pay
- Wake-up reliability outcomes
- Reduced grogginess
- Sleep inertia reduction
- Sleep-stage estimation
- Artificial sleep phase transitioning
- Sleep onset support
- Broader sleep improvement
- Pricing
- Pilot results

## Notes

- This is a starter investor narrative, not a finished pitch deck.
- The investor story should lead with the larger vision, then quickly land on the narrow first wedge.
- Update it as evidence, product progress, customer research, and fundraising feedback improve.
