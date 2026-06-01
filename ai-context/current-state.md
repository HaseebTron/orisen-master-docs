# Orisen Current State

## Purpose of this file

This file defines the current source-of-truth understanding of Orisen at the company and product level.

Use this file to separate current decisions from old notes, MVP-only scope, future ideas, and unvalidated claims.

## What Orisen is

- **Current product identity**:
  - Orisen is a non-contact sleep intervention device for people who struggle to wake up.
  - It is designed to make waking up more reliable and less brutal for people who oversleep, sleep through alarms, turn alarms off while half-asleep, or struggle with severe morning grogginess.

- **Product architecture direction**:
  - Orisen is being built as a platform-capable ambient sleep device.
  - The device should combine sensing, audio, light, compute, connectivity, local control, and app/cloud support where useful.
  - The hardware foundation is being designed to support multiple software-defined sleep interventions over time.
  - Wake completion is the first software-defined intervention layer.

- **Core product direction**:
  - Orisen is not primarily a sleep tracker.
  - Orisen should not be positioned as a generic smart alarm clock.
  - The company direction is active sleep intervention, starting with the morning wake-up problem and building toward broader ambient sleep intelligence over time.

- **Important claim boundary**:
  - Platform-capable does not mean Orisen already has all the hardware required to fix every sleep problem.
  - Ambient sleep intelligence is the long-term direction, not a proven current outcome.
  - Grogginess reduction, sleep inertia reduction, and sleep-phase-aware intervention must be claimed carefully until validated with real users.

## Who Orisen is for first

- **Primary early user**:
  - Orisen is for people with a strong, repeated, painful wake-up problem.
  - The first target users are not casual sleep-optimization users who only want sleep graphs.
  - The first users should be people who already feel that normal alarms, phone alarms, and willpower-based solutions are not enough.

- **Priority early users may include**:
  - People who chronically oversleep
  - People who sleep through alarms
  - People who dismiss alarms while still half-asleep
  - People who turn alarms off and go back to bed
  - People with severe morning grogginess or sleep inertia
  - Students and early-career professionals with high consequences for being late
  - Shift workers or people with inconsistent schedules
  - Biohackers or performance-focused users willing to try new sleep technology

- **Customer focus rule**:
  - The early customer profile should remain narrow and pain-driven.
  - Orisen should not dilute into generic sleep wellness before the painful wake-up use case is solved.

## What problem Orisen solves first

- **First problem**:
  - Orisen first solves the wake-up reliability problem.
  - The user needs to wake up on time and actually get out of bed, even when they are groggy, tired, or likely to dismiss normal alarms.

- **Second strategic problem**:
  - The user wants waking up to feel less brutal, with less grogginess and sleep inertia.
  - This is strategically important, but it must be claimed carefully until supported by real-world evidence.

- **Validated wedge**:
  - Guaranteed wake completion is the most validated early wedge.
  - The strongest current evidence supports presence-based wake completion, not broad sleep improvement or clinical sleep-inertia reduction.

## Engineering MVP vs first customer product vs long-term vision

### Engineering MVP

- **Purpose**:
  - The engineering MVP proves the basic connected product loop.
  - It does not need to prove the full final product vision.

- **The MVP should prove that**:
  - A user can set up the device.
  - The device can connect to the app/cloud.
  - The app can set an alarm.
  - The alarm can sync to the device.
  - The device can store the next alarm locally.
  - The device can ring locally at the correct time.
  - The device can use presence detection to determine whether the user got out of bed.
  - The alarm can re-trigger if the user returns to bed.
  - Basic gradual audio/light wake behavior can run.
  - Basic logging, syncing, and OTA paths can exist.

### First customer-ready product

- **Role**:
  - The first customer-ready product should go beyond the engineering MVP.
  - It should include the validated wake-completion wedge while beginning to deliver the broader promise of less brutal mornings.

- **It should include**:
  - Reliable local alarm execution
  - Presence-based guaranteed wake completion
  - Re-trigger behavior if the user goes back to bed
  - Anti-bypass wake-completion behavior
  - Easy planned schedule changes before the wake window
  - Higher-friction deliberate override behavior during alarm-critical windows
  - A basic but usable app experience
  - Gradual audio and light wake-up behavior
  - A basic version of sensor-informed wake intervention
  - Sleep-phase-aware wake intervention if technically feasible
  - Careful user-facing claims around reduced grogginess and sleep inertia

- **Boundary**:
  - The first customer product does not need a perfect sleep-stage model.
  - It also does not need to prove full artificial sleep phase transitioning in a clinical or highly precise way.
  - It should begin moving the product beyond forcing the user out of bed toward helping the user wake up in a less painful state.

### Long-term vision

- **End vision**:
  - The long-term vision is for Orisen to become an ambient sleep intelligence platform.
  - Internally, this can be understood as an intelligent intervention layer for sleep.

- **Architecture logic**:
  - The hardware is the foundation.
  - Software defines the intervention.
  - Wake completion is the first application.
  - Future software-defined intervention layers can build on the same sensing, audio, light, compute, connectivity, and app/cloud foundation.

- **Future direction may include**:
  - Better non-contact sleep-context sensing
  - Radar-based vital sign, movement, presence, and body-position signals where technically feasible
  - Wearable and health-platform integrations for daytime and recovery context
  - Personalized wake intervention timing
  - Adaptive audio and light stimulation
  - Sleep-phase-aware wake intervention
  - Artificial sleep phase transitioning if validated
  - Reduced sleep inertia if validated
  - Better sleep onset support
  - White noise and bedtime routines
  - Phone/app friction near bedtime or during protected sleep windows
  - Long-term user adaptation
  - Sleep-supportive lighting
  - More advanced sleep history and insights where they improve intervention
  - Subscription features where value is clear
  - Multi-device and household support
  - Production-grade device fleet management

- **Direction boundary**:
  - The long-term direction is to move beyond passive measurement into active intervention.
  - Orisen should help users change the outcome of their sleep and wake-up experience, not just observe it afterward.
  - Future features remain roadmap or hypothesis until tested.

## What is currently validated

- **Strongest current evidence**:
  - The most validated feature is presence-based guaranteed wake completion.

- **Current validation supports the idea that**:
  - Users with wake-up problems understand the value of a system that forces true wake completion.
  - A device that does not fully shut off until the user leaves bed is meaningfully different from normal alarms.
  - Re-triggering the alarm when the user returns to bed is central to solving the real behavior problem.
  - The wake-up reliability wedge is strong enough to anchor the early product.

- **Evidence boundary**:
  - The current evidence should be treated as early validation, not proof of broad-market demand, production reliability, clinical efficacy, sleep-stage accuracy, or broad sleep improvement.

## What is planned but less validated

- **Planned or strategically important**:
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
  - Phone/app friction features
  - Multi-device households
  - Production-scale fleet management
  - Broader ambient sleep intelligence beyond the wake-up wedge

- **Framing rule**:
  - These should be framed as product direction, roadmap, hypothesis, or long-term vision unless and until validated by testing.

## Claims that should be made carefully

- **Confident but careful**:
  - Orisen can confidently claim that it is being built to solve wake-up reliability and reduce brutal mornings.
  - Stronger outcome claims must match what has actually been validated.

- **Claims to avoid**:
  - "Eliminates grogginess"
  - "Eliminates sleep inertia"
  - "Wakes you in the perfect sleep stage"
  - "Controls sleep stages"
  - "Guarantees better sleep"
  - "Clinically improves sleep inertia"
  - "Accurately detects sleep stages"
  - "Manipulates biology in real time"
  - "Fixes everything about sleep"
  - "All sleep issues become software-only problems"

- **Safer phrasing**:
  - "Designed to make waking up more reliable"
  - "Built for people who oversleep or struggle to get out of bed"
  - "Uses presence detection to help ensure you actually leave bed"
  - "Working toward less brutal mornings through gradual, sensor-informed wake intervention"
  - "Being built as a platform-capable ambient sleep device"
  - "The first intervention layer is reliable wake completion"
  - "Future software-defined intervention layers may expand into other parts of sleep"
  - "Early versions will be tested and improved with real users"

## Current company priority

- **Priority promise**:
  - Orisen helps people who struggle with waking up actually get out of bed on time, while building toward less brutal mornings through sensor-informed wake intervention.

- **Near-term focus**:
  - Finish the engineering MVP.
  - Prove the connected app-device-cloud loop.
  - Make guaranteed wake completion reliable.
  - Build a basic first version of gradual audio/light wake-up.
  - Begin testing sleep-phase-aware or sensor-informed wake intervention carefully.
  - Collect evidence from early users.
  - Use claims that match what has actually been validated.
  - Keep the product focused on painful wake-up problems, not generic sleep tracking.

## Open questions

- **Product and customer questions**:
  - Which early customer segment has the strongest willingness to pay?
  - How strong is the real-world demand beyond early signups and interest?
  - What reliability standard is required before users trust the device as their main alarm?
  - What features are necessary for the first paid users versus later roadmap?
  - What parts of the product should remain local on-device versus cloud-assisted?

- **Sensing and intervention questions**:
  - How reliably can radar detect the signals needed for sleep-phase-aware intervention?
  - What level of sleep-stage accuracy is good enough to improve the wake-up experience?
  - Can basic intervention reduce perceived grogginess in early user testing?
  - What is the minimum acceptable version of artificial sleep phase transitioning for the first customer product?
  - Which claims will be supported by early user data?

- **Platform questions**:
  - Which future sleep interventions can be supported by the planned hardware foundation?
  - Which future interventions require new hardware, new placement, or different sensors?
  - Which wearable integrations create enough value to justify the complexity?
  - Which phone/app friction features are useful without feeling invasive?
  - What is the right path from wake completion device to ambient sleep intelligence platform?

## Current positioning summary

- **Current positioning**:
  - Orisen is a non-contact sleep intervention device for people who struggle to wake up.

- **First wedge**:
  - The first wedge is guaranteed wake completion: the alarm does not fully stop until the user physically gets out of bed, and it can re-trigger if they return.

- **Architecture framing**:
  - Orisen is being built as a platform-capable ambient sleep device.
  - The hardware foundation supports sensing, audio, light, compute, connectivity, and app/cloud intelligence where useful.
  - Wake completion is the first software-defined intervention layer.

- **Long-term direction**:
  - Orisen should expand from reliable wake completion into ambient sleep intelligence: a broader intervention layer that guides the night from wind-down to wake-up.
  - The company should position Orisen around fixing painful mornings first, not around passive sleep tracking or generic sleep wellness.
