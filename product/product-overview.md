# Product Overview

## Purpose of this file

This file defines Orisen from the product perspective.

It explains what the product is, what it is not, which customer problem it solves first, how the engineering MVP differs from the first customer-ready product, and how the long-term product direction should be understood.

This file should stay consistent with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- Future validation and evidence docs
- Future product strategy docs

## What Orisen is

Orisen is a non-contact sleep intervention device for people who struggle to wake up.

It is designed to make waking up more reliable and less brutal by combining:

- Non-contact sensing
- Local alarm execution
- Presence-based wake completion
- Gradual audio and light stimulation
- App-based control
- Cloud-assisted intelligence where useful
- Future sensor-informed and sleep-phase-aware wake intervention

The core product direction is not passive sleep tracking.

The core product direction is active sleep intervention, starting with the morning wake-up problem.

At the product level, Orisen should be understood as a closed-loop wake intervention system:

- It senses whether the user is still in bed.
- It responds based on whether the user actually completed the wake-up behavior.
- Over time, it should use sensor data to make waking up feel less brutal, not just more forceful.

## What Orisen is not

Orisen is not just a smart alarm clock.

It is not only a louder alarm, sunrise lamp, or app-controlled bedside device.

Orisen is not primarily a sleep tracker.

It should not be positioned mainly around dashboards, sleep scores, or passive sleep data.

Orisen is not a wearable.

The product should avoid requiring the user to wear a ring, watch, band, headband, or other body-mounted sensor to get the core wake-up benefit.

Orisen is not a medical device in its current company direction.

It should not make clinical claims unless future evidence, regulatory strategy, and product scope support that.

## Core customer problem

The first customer problem is wake-up failure.

The target user does not simply want a nicer alarm. They have a repeated, painful problem where normal alarms and willpower are not enough.

The user may:

- Oversleep
- Sleep through alarms
- Dismiss alarms while still half-asleep
- Turn alarms off and go back to bed
- Wake up feeling heavy, groggy, or mentally foggy
- Feel that mornings are unreliable, stressful, or out of control
- Face real consequences when they fail to wake up on time

The product should focus first on users who feel this pain strongly.

Orisen should not be designed primarily for casual users who only want prettier sleep graphs or general wellness insights.

## The first wedge

The first wedge is presence-based wake completion.

The core behavior is:

- The alarm does not fully stop just because the user taps a button or dismisses an app notification.
- The device uses presence detection to determine whether the user has physically left the bed.
- If the user gets back into bed within the re-trigger window, the alarm can start again.
- The final wake-up moment should work locally on the device and should not depend on the phone, app, cloud, or Wi-Fi.

The intended anti-bypass behavior is part of the wake-completion wedge:

- The product should not offer a normal snooze path as the default wake flow.
- The user should not be able to fully shut off the alarm from bed through a simple button press.
- If the device is unplugged during the alarm, it should switch to internal backup battery power rather than immediately shutting down.
- The device is intended to be wall-mounted, such as with 3M Command Strip-style mounting, so the user cannot casually move it like a bedside clock or phone.
- The system should be designed to make the easiest completion path getting out of bed, not bypassing the device.

Internally, this can be referred to as the guaranteed wake completion wedge.

Externally, claims should be worded carefully as “designed to ensure wake completion,” “presence-based wake completion,” or “helps make sure you actually get out of bed,” unless stronger claims are supported by evidence.

This is the most validated early product wedge.

It directly attacks the real behavior problem: the user does not just need to hear an alarm, they need to actually leave the bed and stay out of bed.

## Engineering MVP

The engineering MVP is not the full product vision.

The engineering MVP exists to prove the basic connected product loop:

- User account creation
- Device setup and pairing
- App-based alarm setting
- Cloud storage of alarm settings
- Syncing alarm settings to the device
- Local alarm storage on the device
- Local alarm execution at the correct time
- Presence-based wake completion
- Re-trigger behavior if the user returns to bed
- Basic gradual audio and light wake-up
- Basic logging
- Basic OTA update path, if feasible

The engineering MVP should prove that the system can function as a connected product.

It does not need to include every future sleep intervention feature.

It should not shrink the company vision or redefine Orisen as only an app-connected alarm.

## First customer-ready product

The first customer-ready product should go beyond the engineering MVP.

It should include the validated wake-completion wedge, while also beginning to deliver the broader promise of less brutal mornings.

The first customer-ready product should include:

- Reliable local alarm execution
- Presence-based wake completion
- Re-trigger behavior if the user returns to bed
- A simple and usable app experience
- Gradual audio wake-up behavior
- Gradual light wake-up behavior
- Basic sleep/session logging where useful
- Basic device reliability and OTA support
- A basic version of sensor-informed wake intervention
- Sleep-phase-aware wake intervention if technically feasible
- Careful user-facing claims around reducing grogginess and sleep inertia

The first customer-ready product does not need a perfect sleep-stage model.

It also does not need to prove full artificial sleep phase transitioning in a clinical or highly precise way.

However, it should begin moving the product beyond “forcing the user out of bed” toward “helping the user wake up in a less painful state.”

This means the first customer product should aim to reduce the user’s perceived morning difficulty through a combination of:

- Wake completion
- Gradual audio
- Gradual light
- Presence feedback
- Sensor-informed timing or intervention where feasible
- Early sleep-phase-aware behavior if the sensing pipeline supports it

The first customer product should not overclaim that it eliminates grogginess or accurately controls sleep stages until real-world testing supports those claims.

## Long-term product direction

The long-term product direction is a non-contact sleep intervention platform.

Over time, Orisen should move from reliable wake completion toward personalized sleep-state intervention.

Long-term product direction may include:

- More accurate non-contact sleep-state estimation
- Radar-based vital sign and movement sensing
- Personalized wake intervention timing
- Adaptive audio and light stimulation
- Artificial sleep phase transitioning
- Reduced sleep inertia
- Better sleep onset support
- White noise and bedtime routines
- Long-term user adaptation
- Sleep-supportive lighting
- More advanced sleep history and insights
- Subscription features where value is clear
- Multi-device and household support
- Production-grade device fleet management

The long-term direction is to move beyond measurement into intervention.

Orisen should help users change the outcome of their sleep and wake-up experience, not just observe it afterward.

## Core product principles

### Solve a painful problem first

The product should stay focused on people with a strong wake-up problem.

Do not dilute the product into generic sleep wellness before the painful wake-up use case is solved.

### Reliability comes before intelligence

The device must wake the user up reliably.

AI, cloud intelligence, sleep-stage estimation, and personalization are valuable only if the core wake-up system works.

The final alarm moment should remain locally reliable.

### Local control matters

The device should not depend on the phone, app, cloud, or Wi-Fi to execute the final wake-up behavior.

The cloud and app can improve setup, personalization, updates, and intelligence, but the device should remain dependable on its own.

### Intervention matters more than tracking

Sleep tracking is useful only when it helps the product intervene better.

Orisen should not become a passive dashboard product.

The product should be judged by whether it improves the morning outcome.

### Claims must match evidence

Product claims should be tied to what has actually been built and validated.

Ambitious future direction is allowed, but it must be separated from validated current capability.

### The first product should feel meaningfully different

The customer should understand why Orisen is different from a normal alarm within seconds.

The clearest difference is:

> Orisen does not just make noise. It detects whether you actually got out of bed.

The longer-term difference is:

> Orisen is being built to prepare your body for waking, not just alert you at a fixed time.

## What should not be overclaimed

Orisen should not overclaim:

- Grogginess elimination
- Sleep-stage accuracy
- Artificial sleep phase transitioning
- Clinical sleep improvement
- Perfect light-sleep wake timing
- Guaranteed better sleep quality
- Medical treatment of sleep disorders
- Real-time biological control beyond what has been validated

Avoid saying:

- "Eliminates grogginess"
- "Wakes you in the perfect sleep stage"
- "Controls your sleep stages"
- "Clinically proven to reduce sleep inertia"
- "Accurately detects sleep stages"
- "Guarantees better sleep"
- "Manipulates biology in real time"

Safer product phrasing:

- "Designed to make waking up more reliable"
- "Built for people who struggle to get out of bed"
- "Uses presence detection to help ensure wake completion"
- "Aims to reduce grogginess through gradual, sensor-informed wake intervention"
- "Working toward sleep-phase-aware wake-up behavior"
- "Early versions will be tested and improved with real users"

## Difference from a smart alarm clock

A smart alarm clock usually focuses on alarm scheduling, sounds, app controls, sunrise lighting, or basic convenience.

Orisen differs because the core product is wake completion.

A normal smart alarm asks:

> Did the alarm go off?

Orisen asks:

> Did the user actually get out of bed?

That difference changes the product category.

The product is not just an alarm output device. It is a closed-loop wake-up system that senses whether the desired behavior happened and responds accordingly.

## Difference from a sleep tracker

A sleep tracker mainly measures and reports sleep.

It may tell the user how they slept, assign a score, or show trends.

Orisen should not be primarily judged by how much data it displays.

Orisen should be judged by whether it changes the user’s morning outcome.

The product may use sleep data internally, but the main value is intervention:

- Wake the user reliably
- Help prevent going back to bed
- Gradually prepare the user for waking
- Eventually personalize wake intervention based on sensed sleep state

## Difference from a wearable

Wearables require the user to wear something on the body.

That creates friction, charging requirements, comfort issues, and compliance problems.

Orisen should remain non-contact for the core product experience.

The user should be able to receive the main wake-up benefit without wearing a device.

This matters because the target user already struggles with consistency. The product should not depend on the user remembering to wear, charge, or tolerate another device every night.

## Product positioning summary

Orisen is a non-contact sleep intervention device for people who struggle to wake up.

The first wedge is presence-based wake completion: the alarm does not fully stop just because the user taps a button, and it can re-trigger if they return to bed.

The first customer-ready product should also begin introducing gradual, sensor-informed, or sleep-phase-aware wake intervention aimed at making mornings feel less brutal.

The long-term direction is a personalized sleep intervention platform that moves beyond passive tracking toward active sleep-state guidance.

Orisen should be positioned around fixing painful mornings, not around generic sleep tracking.
