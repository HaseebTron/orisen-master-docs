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

- **Current product identity**:
  - Orisen is a non-contact sleep intervention device for people who struggle to wake up.
  - It is designed to make waking up more reliable and less brutal.

- **Platform-capable architecture**:
  - Orisen is being built as a platform-capable ambient sleep device.
  - The hardware foundation should combine:
    - non-contact sensing
    - audio
    - light
    - compute
    - connectivity
    - local device control
    - app/cloud support where useful
  - The software defines the intervention layer.
  - Wake completion is the first software-defined intervention.
  - Future intervention layers may build on the same hardware/software foundation.

- **Core product direction**:
  - Orisen is not passive sleep tracking.
  - Orisen is active sleep intervention, starting with the morning wake-up problem.
  - Over time, Orisen should move toward ambient sleep intelligence: a system that senses context, adapts over time, and guides the night from wind-down to wake-up.

- **Closed-loop wake intervention**:
  - At the product level, the first loop is wake completion:
    - It senses whether the user is still in bed.
    - It responds based on whether the user actually completed the wake-up behavior.
    - It can keep the wake-up flow active until the user gets out of bed.
    - It can re-trigger if the user returns to bed during the wake window.
  - Over time, the product should use sensor data to make waking up feel less brutal, not just more forceful.

## What Orisen is not

- **Not just a smart alarm clock**:
  - Orisen is not only a louder alarm, sunrise lamp, or app-controlled bedside device.
  - The core product is not just alarm playback. It is wake completion.

- **Not primarily a sleep tracker**:
  - Orisen should not be positioned mainly around dashboards, sleep scores, or passive sleep data.
  - Sleep data is valuable only when it improves intervention.

- **Not a wearable**:
  - Orisen should avoid requiring the user to wear a ring, watch, band, headband, or other body-mounted sensor to get the core wake-up benefit.
  - Future wearable integrations may add useful context, but the core experience should remain non-contact.

- **Not a medical device in the current company direction**:
  - Orisen should not make clinical claims unless future evidence, regulatory strategy, and product scope support that.

- **Not a solved all-in-one sleep fixer today**:
  - Platform-capable does not mean Orisen already has all hardware required to solve every sleep problem.
  - Future interventions may require technical validation, new software, integrations, hardware changes, or different evidence.
  - Avoid treating every sleep issue as a simple software-only problem.

## Core customer problem

- **First customer problem**:
  - The first customer problem is wake-up failure.
  - The target user does not simply want a nicer alarm.
  - They have a repeated, painful problem where normal alarms and willpower are not enough.

- **The user may**:
  - Oversleep
  - Sleep through alarms
  - Dismiss alarms while still half-asleep
  - Turn alarms off and go back to bed
  - Wake up feeling heavy, groggy, or mentally foggy
  - Feel that mornings are unreliable, stressful, or out of control
  - Face real consequences when they fail to wake up on time

- **Customer focus rule**:
  - The product should focus first on users who feel this pain strongly.
  - Orisen should not be designed primarily for casual users who only want prettier sleep graphs or general wellness insights.

## The first wedge

- **Wedge**:
  - The first wedge is presence-based wake completion.
  - Internally, this can be referred to as the guaranteed wake completion wedge.

- **Core behavior**:
  - The alarm does not fully stop just because the user taps a button or dismisses an app notification.
  - The device uses presence detection to determine whether the user has physically left the bed.
  - If the user gets back into bed within the re-trigger window, the alarm can start again.
  - The final wake-up moment should work locally on the device and should not depend on the phone, app, cloud, or Wi-Fi.

- **Anti-bypass behavior**:
  - The product should not offer a normal snooze path as the default wake flow.
  - The device can have a normal OFF button for ordinary use, but during the alarm-critical window that OFF button should not fully disable the wake-completion flow.
  - If the user unplugs the device from wall power during the alarm-critical window, the device should continue operating on internal backup battery power rather than immediately shutting down.
  - The device is intended to be wall-mounted, such as with 3M Command Strip-style mounting, so the user cannot casually move it like a bedside clock or phone.
  - The mounting is intended to make casual removal inconvenient enough that the user cannot simply pick up or move the device while half-asleep.
  - The system should make the easiest completion path getting out of bed, not bypassing the device.

- **Planned control and override behavior**:
  - Before the wake window, the user should be able to skip, change, or disable an upcoming alarm normally through the app.
  - During the alarm-critical window, a full override should remain possible, but should require higher-friction deliberate action away from bed.
  - Possible override mechanisms include a physical recovery code, QR card, NFC card, or similar token stored away from the bed and entered or scanned through the app.

- **Claim boundary**:
  - The goal is to prevent half-asleep bypass without trapping the user.
  - Externally, claims should be worded carefully as “designed to ensure wake completion,” “presence-based wake completion,” or “helps make sure you actually get out of bed,” unless stronger claims are supported by evidence.

- **Why this wedge matters**:
  - This is the most validated early product wedge.
  - It directly attacks the real behavior problem: the user does not just need to hear an alarm, they need to actually leave the bed and stay out of bed.

## Engineering MVP

- **Role**:
  - The engineering MVP is not the full product vision.
  - The engineering MVP exists to prove the basic connected product loop.

- **The engineering MVP should prove**:
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

- **Boundary**:
  - The engineering MVP should prove that the system can function as a connected product.
  - It does not need to include every future sleep intervention feature.
  - It should not shrink the company vision or redefine Orisen as only an app-connected alarm.

## First customer-ready product

- **Role**:
  - The first customer-ready product should go beyond the engineering MVP.
  - It should include the validated wake-completion wedge, while also beginning to deliver the broader promise of less brutal mornings.

- **The first customer-ready product should include**:
  - Reliable local alarm execution
  - Presence-based wake completion
  - Re-trigger behavior if the user returns to bed
  - A simple and usable app experience
  - Planned schedule-change controls before the wake window
  - Higher-friction deliberate override behavior during alarm-critical windows
  - Gradual audio wake-up behavior
  - Gradual light wake-up behavior
  - Basic sleep/session logging where useful
  - Basic device reliability and OTA support
  - A basic version of sensor-informed wake intervention
  - Sleep-phase-aware wake intervention if technically feasible
  - Careful user-facing claims around reducing grogginess and sleep inertia

- **Boundary**:
  - The first customer-ready product does not need a perfect sleep-stage model.
  - It also does not need to prove full artificial sleep phase transitioning in a clinical or highly precise way.
  - It should begin moving the product beyond forcing the user out of bed toward helping the user wake up in a less painful state.

- **Less brutal mornings may come from**:
  - Wake completion
  - Gradual audio
  - Gradual light
  - Presence feedback
  - Sensor-informed timing or intervention where feasible
  - Early sleep-phase-aware behavior if the sensing pipeline supports it

- **Claim boundary**:
  - The first customer product should not overclaim that it eliminates grogginess or accurately controls sleep stages until real-world testing supports those claims.

## Product architecture: hardware foundation and software-defined interventions

- **Internal architecture model**:
  - Orisen is being built as a platform-capable ambient sleep device.
  - The hardware is the foundation.
  - The software defines the intervention.
  - Wake completion is the first application.

- **Hardware foundation**:
  - The planned device foundation includes:
    - non-contact sensing
    - radar-based presence and movement context where technically feasible
    - audio output
    - light output
    - local compute
    - local storage
    - connectivity
    - backup power for alarm-critical windows
    - app/cloud connection where useful

- **First software-defined intervention layer**:
  - The first intervention layer is wake completion.
  - It focuses on:
    - waking up reliably
    - detecting whether the user is still in bed
    - making alarm dismissal different from wake completion
    - re-triggering if the user returns to bed
    - making going back to sleep harder
    - working toward less brutal mornings through gradual audio/light and sensor-informed wake behavior

- **Future software-defined intervention layers may include**:
  - Wind-down support
  - Bedtime routines
  - White noise and sleep-supportive audio
  - Sleep-supportive lighting
  - Phone/app friction near bedtime or during protected sleep windows
  - Wearable and health-platform integrations for daytime context
  - Nighttime sleep-context sensing from non-contact radar
  - Personalized wake intervention timing
  - Adaptive audio and light intervention
  - Sleep-phase-aware wake intervention
  - Artificial sleep phase transitioning if validated
  - Sleep onset support
  - More advanced sleep history and insights when they improve intervention

- **Important boundary**:
  - The platform framing is a product architecture direction, not proof that Orisen can solve every sleep problem.
  - Some future interventions may require new hardware, different sensors, different placement, stronger algorithms, external integrations, or new validation.

## Long-term product direction

- **Long-term direction**:
  - The long-term product direction is ambient sleep intelligence.
  - Orisen should move from reliable wake completion toward personalized sleep intervention across more parts of the night.

- **Long-term product direction may include**:
  - More accurate non-contact sleep-state estimation
  - Radar-based vital sign and movement sensing
  - Body movement and orientation signals where technically feasible
  - Personalized wake intervention timing
  - Adaptive audio and light stimulation
  - Artificial sleep phase transitioning if validated
  - Reduced sleep inertia if validated
  - Better sleep onset support
  - White noise and bedtime routines
  - Long-term user adaptation
  - Sleep-supportive lighting
  - Wearable integrations and other connected sleep-context sources
  - More advanced sleep history and insights
  - Subscription features where value is clear
  - Multi-device and household support
  - Production-grade device fleet management

- **Direction boundary**:
  - The long-term direction is to move beyond measurement into intervention.
  - Orisen should help users change the outcome of their sleep and wake-up experience, not just observe it afterward.
  - Long-term items remain roadmap, hypothesis, or future direction until tested.

## Core product principles

### Solve a painful problem first

- **Rule**:
  - The product should stay focused on people with a strong wake-up problem.
  - Do not dilute the product into generic sleep wellness before the painful wake-up use case is solved.

### Reliability comes before intelligence

- **Rule**:
  - The device must wake the user up reliably.
  - AI, cloud intelligence, sleep-stage estimation, and personalization are valuable only if the core wake-up system works.
  - The final alarm moment should remain locally reliable.

### Local control matters

- **Rule**:
  - The device should not depend on the phone, app, cloud, or Wi-Fi to execute the final wake-up behavior.
  - The cloud and app can improve setup, personalization, updates, and intelligence, but the device should remain dependable on its own.

### Intervention matters more than tracking

- **Rule**:
  - Sleep tracking is useful only when it helps the product intervene better.
  - Orisen should not become a passive dashboard product.
  - The product should be judged by whether it improves the morning outcome.

### The hardware is the foundation, not the whole promise

- **Rule**:
  - The hardware should be designed to support multiple interventions over time.
  - The company should not assume every future sleep problem becomes software-only.
  - Future capabilities still need validation, and some may require hardware, sensing, placement, or integration changes.

### Override should preserve deliberate control

- **Rule**:
  - Orisen should prevent half-asleep bypass without removing legitimate user control.
  - Users should be able to change, skip, or disable upcoming alarms normally before the wake window.
  - During an alarm-critical window, a full override should still exist, but it should require deliberate action away from bed so the user is awake enough to make an intentional decision.

### Claims must match evidence

- **Rule**:
  - Product claims should be tied to what has actually been built and validated.
  - Ambitious future direction is allowed, but it must be separated from validated current capability.

### The first product should feel meaningfully different

- **Rule**:
  - The customer should understand why Orisen is different from a normal alarm within seconds.

- **Clearest difference**:
  - Orisen does not just make noise. It detects whether you actually got out of bed.

- **Longer-term difference**:
  - Orisen is being built to prepare your body for waking, not just alert you at a fixed time.

## What should not be overclaimed

- **Orisen should not overclaim**:
  - Grogginess elimination
  - Sleep inertia elimination
  - Sleep-stage accuracy
  - Artificial sleep phase transitioning
  - Clinical sleep improvement
  - Perfect light-sleep wake timing
  - Guaranteed better sleep quality
  - Medical treatment of sleep disorders
  - Real-time biological control beyond what has been validated
  - Fixing everything surrounding sleep
  - All future sleep issues being software-only

- **Avoid saying**:
  - "Eliminates grogginess"
  - "Eliminates sleep inertia"
  - "Wakes you in the perfect sleep stage"
  - "Controls your sleep stages"
  - "Clinically proven to reduce sleep inertia"
  - "Accurately detects sleep stages"
  - "Guarantees better sleep"
  - "Manipulates biology in real time"
  - "Fixes everything about sleep"
  - "All sleep problems can be solved through software"

- **Safer product phrasing**:
  - "Designed to make waking up more reliable"
  - "Built for people who struggle to get out of bed"
  - "Uses presence detection to help ensure wake completion"
  - "Working toward less brutal mornings through gradual, sensor-informed wake intervention"
  - "Being built as a platform-capable ambient sleep device"
  - "Wake completion is the first software-defined intervention"
  - "Future intervention layers may expand into other parts of sleep"
  - "Early versions will be tested and improved with real users"

## Difference from a smart alarm clock

- **Smart alarm clock**:
  - A smart alarm clock usually focuses on alarm scheduling, sounds, app controls, sunrise lighting, or basic convenience.

- **Orisen**:
  - Orisen differs because the core product is wake completion.

- **Category difference**:
  - A normal smart alarm asks:
    - Did the alarm go off?
  - Orisen asks:
    - Did the user actually get out of bed?
  - That difference changes the product category.

- **System difference**:
  - The product is not just an alarm output device.
  - It is a closed-loop wake-up system that senses whether the desired behavior happened and responds accordingly.

## Difference from a sleep tracker

- **Sleep tracker**:
  - A sleep tracker mainly measures and reports sleep.
  - It may tell the user how they slept, assign a score, or show trends.

- **Orisen**:
  - Orisen should not be primarily judged by how much data it displays.
  - Orisen should be judged by whether it changes the user’s morning outcome.

- **Intervention value**:
  - The product may use sleep data internally, but the main value is intervention:
    - Wake the user reliably
    - Help prevent going back to bed
    - Gradually prepare the user for waking
    - Eventually personalize wake intervention based on sensed sleep state

## Difference from a wearable

- **Wearables**:
  - Wearables require the user to wear something on the body.
  - That creates friction, charging requirements, comfort issues, and compliance problems.

- **Orisen**:
  - Orisen should remain non-contact for the core product experience.
  - The user should be able to receive the main wake-up benefit without wearing a device.

- **Why this matters**:
  - The target user already struggles with consistency.
  - The product should not depend on the user remembering to wear, charge, or tolerate another device every night.

## Product positioning summary

- **Current product identity**:
  - Orisen is a non-contact sleep intervention device for people who struggle to wake up.

- **First wedge**:
  - The first wedge is presence-based wake completion: the alarm does not fully stop just because the user taps a button, and it can re-trigger if they return to bed.

- **Architecture framing**:
  - Orisen is being built as a platform-capable ambient sleep device.
  - The hardware foundation supports sensing, audio, light, compute, connectivity, and app/cloud intelligence where useful.
  - Wake completion is the first software-defined intervention layer.

- **First customer-ready product**:
  - The first customer-ready product should also begin introducing gradual, sensor-informed, or sleep-phase-aware wake intervention aimed at making mornings feel less brutal.

- **Long-term direction**:
  - The long-term direction is ambient sleep intelligence: a personalized sleep intervention platform that moves beyond passive tracking toward active sleep-state guidance.
  - Orisen should be positioned around fixing painful mornings first, not around generic sleep tracking.
