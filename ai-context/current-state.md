# Orisen Current State

## Purpose of this file

This file defines the current source-of-truth understanding of Orisen at the company and product level.

It should be used to separate current decisions from old notes, MVP-only scope, future ideas, and unvalidated claims.

## What Orisen is

Orisen is a non-contact sleep intervention device designed to make waking up reliable and less brutal for people who struggle with oversleeping, sleeping through alarms, and severe sleep inertia.

Orisen is not primarily a sleep tracker and should not be positioned as a generic smart alarm clock.

The company direction is to build a connected sleep intervention system that uses sensing, local device control, light, audio, and eventually sleep-phase-aware intervention to help users wake up on time and feel less groggy.

## Who Orisen is for first

Orisen is for people with a strong, repeated, painful wake-up problem.

The first target users are not casual sleep-optimization users who only want sleep graphs. The first users should be people who already feel that normal alarms, phone alarms, and willpower-based solutions are not enough.

Priority early users may include:

- People who chronically oversleep
- People who sleep through alarms
- People with severe morning grogginess or sleep inertia
- Students and early-career professionals with high consequences for being late
- Shift workers or people with inconsistent schedules
- Biohackers or performance-focused users who are willing to try new sleep technology

The early customer profile should remain narrow and pain-driven.

## What problem Orisen solves first

Orisen first solves the wake-up reliability problem.

The most important initial problem is:

> The user needs to wake up on time and actually get out of bed, even when they are groggy, tired, or likely to dismiss normal alarms.

The second strategic problem is:

> The user wants waking up to feel less brutal, with less grogginess and sleep inertia.

Guaranteed wake completion is the most validated early wedge.

Grogginess reduction is strategically important to the product promise, customer story, and fundraising narrative, but it must be claimed carefully until validated with real users.

## Engineering MVP vs first customer product vs long-term vision

### Engineering MVP

The engineering MVP is focused on proving the connected product loop at a basic level.

The MVP should prove that:

- A user can set up the device
- The device can connect to the app/cloud
- The app can set an alarm
- The alarm can sync to the device
- The device can store the next alarm locally
- The device can ring locally at the correct time
- The device can use presence detection to determine whether the user got out of bed
- The alarm can re-trigger if the user returns to bed
- Basic gradual audio/light wake behavior can run
- Basic logging, syncing, and OTA paths can exist

The engineering MVP does not need to prove the full final product vision.

### First customer-ready product

The first customer-ready product should go beyond the engineering MVP.

It should include:

- Reliable local alarm execution
- Presence-based guaranteed wake completion
- Re-trigger behavior if the user goes back to bed
- Anti-bypass wake-completion behavior, including no normal snooze path, no simple in-bed shutoff, internal backup battery behavior if unplugged during alarm, and wall-mounted physical friction such as 3M Command Strip-style mounting
- A basic but usable app experience
- Gradual audio and light wake-up behavior
- A basic version of sleep-phase-aware or sensor-informed wake intervention
- Early artificial sleep phase transitioning if technically feasible
- Careful user-facing claims around reduced grogginess and sleep inertia

The first customer product does not need a perfect sleep-stage model.

However, it should begin delivering the strategic promise that Orisen is not just forcing the user out of bed, but also trying to prepare the user for waking in a less painful state.

### Long-term vision

The long-term vision is for Orisen to become a sleep intervention platform.

The long-term product should be able to:

- Sense sleep state non-contact
- Understand the user's sleep patterns over time
- Intervene using audio, light, and other non-invasive signals
- Help users wake up reliably
- Reduce sleep inertia
- Support better sleep onset and nighttime sleep behavior
- Personalize interventions over time
- Move beyond passive sleep tracking into active sleep-state guidance

The long-term company direction is sleep control and intervention, not just sleep measurement.

## What is currently validated

The most validated feature is presence-based guaranteed wake completion.

Current validation supports the idea that:

- Users with wake-up problems understand the value of a system that forces true wake completion
- A device that does not fully shut off until the user leaves bed is meaningfully different from normal alarms
- Re-triggering the alarm when the user returns to bed is central to solving the real behavior problem
- The wake-up reliability wedge is strong enough to anchor the early product

The current evidence should be treated as early validation, not proof of broad-market demand or clinical efficacy.

## What is planned but less validated

The following are planned or strategically important, but less validated than guaranteed wake completion:

- Sleep-phase-aware wake intervention
- Sensor-informed wake intervention
- Artificial sleep phase transitioning
- Reducing sleep inertia through sensor-driven audio/light stimulation
- Radar-based sleep-stage estimation
- Personalized intervention timing
- Long-term adaptation to each user
- Advanced sleep insights or dashboards
- Subscription features
- Sleep onset support
- White noise and bedtime routines
- Health platform integrations
- Multi-device households
- Production-scale fleet management

These should be framed as product direction or roadmap unless and until validated by testing.

## Claims that should be made carefully

Orisen can confidently claim that it is being built to solve wake-up reliability and reduce brutal mornings.

Orisen should be careful with claims such as:

- "Eliminates grogginess"
- "Wakes you in the perfect sleep stage"
- "Controls sleep stages"
- "Guarantees better sleep"
- "Clinically improves sleep inertia"
- "Accurately detects sleep stages"
- "Manipulates biology in real time"

Safer phrasing:

- "Designed to make waking up more reliable"
- "Built for people who oversleep or struggle to get out of bed"
- "Uses presence detection to help ensure you actually leave bed"
- "Aims to reduce grogginess through gradual, sensor-informed wake-up intervention"
- "Working toward sleep-phase-aware wake-up behavior"
- "Early versions will be tested and improved with real users"

The company should avoid overstating sleep-stage accuracy or grogginess reduction until there is evidence from real-world testing.

## Current company priority

The current priority is to prove a narrow, high-value customer promise:

> Orisen helps people who struggle with waking up actually get out of bed on time, while building toward less groggy mornings through sleep-phase-aware or sensor-informed wake intervention.

The near-term company focus should be:

- Finish the engineering MVP
- Prove the connected app-device-cloud loop
- Make guaranteed wake completion reliable
- Build a basic first version of gradual audio/light wake-up
- Begin testing sleep-phase-aware or sensor-informed wake intervention carefully
- Collect evidence from early users
- Use claims that match what has actually been validated
- Keep the product focused on painful wake-up problems, not generic sleep tracking

## Open questions

The main open questions are:

- Which early customer segment has the strongest willingness to pay?
- How strong is the real-world demand beyond early signups and interest?
- How reliably can radar detect the signals needed for sleep-phase-aware intervention?
- What level of sleep-stage accuracy is good enough to improve the wake-up experience?
- Can basic intervention reduce perceived grogginess in early user testing?
- What is the minimum acceptable version of artificial sleep phase transitioning for the first customer product?
- Which claims will be supported by early user data?
- What price point is acceptable for the first customer segment?
- What reliability standard is required before users trust the device as their main alarm?
- What parts of the product should remain local on-device versus cloud-assisted?
- What features are necessary for the first paid users versus later roadmap?

## Current positioning summary

Orisen is a non-contact sleep intervention device for people who struggle to wake up.

The first wedge is guaranteed wake completion: the alarm does not fully stop until the user physically gets out of bed, and it can re-trigger if they return.

The first customer-ready product should also include an early version of sleep-phase-aware or sensor-informed wake intervention aimed at reducing grogginess, but claims around sleep-stage control and sleep inertia reduction must remain careful until validated.

The company should position Orisen around fixing painful mornings, not around passive sleep tracking.
