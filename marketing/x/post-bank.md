# X Post Bank

Status: Working asset bank
Authority level: Channel-specific marketing execution
Last reviewed: 2026-05-29
Governing docs:
- `marketing/x/playbook.md`
- `marketing/x/posting-strategy.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/framing-and-narrative.md`
- `marketing/positioning-and-messaging.md`
Downstream docs:
- `marketing/x/posting-calendar.md`
- Published X posts
- X reply drafts
- X campaign tests

## File structure

- **Purpose**: defines what this post bank is for and what it is not for.
- **Usage rules**: defines how to use drafts, hooks, and examples without treating them as approved forever.
- **Post ideas**: stores reusable raw post ideas, grouped by strategic content motion and topic.
- **Claim-safety reminder**: reminds the writer to check claim boundaries before posting.
- **Hook bank**: stores reusable hooks and recurring opening lines for X posts.
- **Post drafts**: stores draft X posts grouped by post type or campaign.
- **Reply drafts**: stores reusable reply patterns and examples for relevant X conversations.
- **CTA variants**: stores reusable calls to action for waitlist, DMs, customer discovery, expert feedback, and interviews.
- **Draft status labels**: defines how to mark drafts as ready, needs review, posted, retired, or claim-sensitive.
- **Maintenance rules**: defines when to add, update, retire, or move drafts.

## Purpose

This file stores reusable X writing assets for Orisen.

Use this file for:

- finished or near-finished X post drafts
- reusable hooks
- reusable reply examples
- CTA variants
- draft labels and notes
- posts that can later be scheduled in `marketing/x/posting-calendar.md`

This file is not:

- the X operating playbook
- the X posting strategy
- the product source of truth
- the public claim authority
- a performance log
- a place to invent new product claims

## Usage rules

To be written later.

Placeholder intent:

- This section should explain how to use, edit, reuse, and retire post drafts.
- It should explain how drafts move from this file into `marketing/x/posting-calendar.md`.
- It should keep this file useful as an asset bank, not a strategy doc.

## Post ideas

Use this section for raw post ideas before they become finished drafts.

These ideas should stay downstream from `marketing/x/posting-strategy.md`, `marketing/x/voice.md`, and the current product/claim boundaries.

### 1. Build Orisen in public

Purpose:

- show that Orisen is real and actively being built
- build founder trust
- make the product feel tangible
- attract useful builders, operators, experts, and early users

Good topics:

- **prototype progress**
  - App-device-cloud loop progress
    - post about getting the app to save an alarm and the device reading it from Supabase
    - post about the moment Orisen became more than a standalone prototype and started becoming a connected product
    - post about why local device execution matters even when the app/cloud exists
  - Wake-completion flow progress
    - post about testing the logic where the alarm does not fully stop until the user is out of bed
    - post about re-triggering the alarm when the user returns to bed
    - post about why the hard part is not making a louder alarm, but deciding when the device should trust that waking is complete
  - OTA / reliability foundation
    - post about adding the foundation for firmware updates because sleep hardware has to improve after shipping
    - post about why a wake-up device cannot be treated like a toy app where bugs are only annoying
  - Current build stage
    - post about moving from proof-of-concept behavior into a real MVP system
    - post about the difference between a demo that works once and a product that has to work every morning

- **product decisions**
  - Wake completion before sleep optimization
    - post about why Orisen starts with the gap between alarm dismissal and actually leaving bed
    - post about choosing the most painful morning failure instead of building another sleep dashboard
  - Non-contact sensing
    - post about choosing non-contact sensing because people should not need to wear something to make their alarm work
    - post about avoiding cameras because a bedroom sleep device has to earn trust
  - Local-first alarm behavior
    - post about why the device must ring locally even if Wi-Fi or the cloud fails
    - post about treating alarm reliability as a product requirement, not a nice-to-have
  - No easy in-bed shutoff
    - post about designing around half-awake behavior instead of trusting willpower
    - post about why a normal snooze path can work against the exact user Orisen is for

- **hardware/software tradeoffs**
  - Cloud vs local control
    - post about what belongs on-device versus what can live in the app/cloud
    - post about why the cloud can help coordinate, but the device has to own the alarm moment
  - Wall-mounted device constraints
    - post about why physical placement matters for anti-bypass behavior
    - post about designing friction into the device so the easiest path is getting out of bed
  - Audio/light behavior
    - post about building gradual audio/light as part of the wake-up flow, not just adding a nicer alarm sound
    - post about the tradeoff between being effective and not making the product feel unbearable
  - Sensor-informed future
    - post about building the base system first before making stronger claims about sleep-phase-aware intervention
    - post about separating the validated wake-completion wedge from the more experimental less-brutal-wake-up direction

- **reliability constraints**
  - Alarm-critical windows
    - post about why edits, overrides, and updates need stricter rules near the alarm time
    - post about not wanting a firmware update or cloud issue to interfere with the morning wake-up
  - Offline operation
    - post about why a sleep device should not fail just because the internet is down
    - post about local alarm storage as a core reliability decision
  - Backup behavior
    - post about thinking through what should happen if the device is unplugged during an alarm
    - post about wake-up hardware needing anti-bypass design because the user may not be fully rational in the morning
  - Trust requirement
    - post about how a wake-up device only matters if users can trust it more than they trust themselves
    - post about the product standard being different when failure means someone misses class, work, prayer, or an important obligation

- **lessons from the old MVP**
  - What early testers understood quickly
    - post about people instantly understanding the value of an alarm that cares whether you actually got out of bed
    - post about how the old MVP validated the wake-completion wedge more than any generic sleep feature
  - What the old MVP did not prove
    - post about being careful not to claim sleep-stage or grogginess improvements before testing them properly
    - post about the difference between early signal and proof
  - What changed in the new build
    - post about moving from a rough prototype into a connected system with app, device, cloud, local storage, and update paths
    - post about making the product more real before over-polishing the marketing

- **what broke or changed**
  - Scope changes
    - post about cutting generic sleep-tracking language and focusing harder on painful wake-up failures
    - post about narrowing from “better sleep device” to “wake-completion system first”
  - Technical changes
    - post about replacing hardcoded behavior with real app/cloud syncing
    - post about discovering that reliability logic matters more than flashy features in the early MVP
  - Messaging changes
    - post about realizing the sharper problem is not waking up, but completing the wake-up
    - post about moving away from generic wellness language because it hides the real pain

- **what is harder than expected**
  - Designing for half-awake behavior
    - post about how users are not fully rational when the product matters most
    - post about why the device has to assume the morning version of the user will try to bypass it
  - Defining wake completion
    - post about the challenge of deciding when “out of bed” is real enough to stop the alarm
    - post about avoiding false confidence while still making the product usable
  - Balancing intensity and trust
    - post about making the wake-up hard to avoid without making the product feel punishing
    - post about the line between useful friction and annoying friction
  - Building a simple product that is not simplistic
    - post about how the user-facing promise is simple, but the system behind it has many reliability edge cases
    - post about why “just make an alarm that keeps going” is much harder once you care about real mornings

### 2. Make the wake-up problem specific

Purpose:

- make high-pain users feel seen
- surface replies, DMs, and customer language
- avoid drifting into generic sleep wellness

Good topics:

- **sleeping through alarms**
- **turning alarms off half-asleep**
- **waking up but not getting out of bed**
- **going back to bed after initially getting up**
- **losing time between alarm time and being out of bed**
- **not trusting yourself in the morning**

### 3. Reframe the problem

Purpose:

- shift people from “I need more discipline” or “I need a louder alarm” to “waking up is a completion problem”
- make Orisen's wedge easier to understand
- build the tracking-to-intervention narrative carefully

Good topics:

- **normal alarms stop too early**
- **alarm success is not wake completion**
- **trackers tell you what happened but do not change the morning**
- **the morning failure happens after the alarm rings**
- **systems should be designed around half-awake behavior**

### 4. Learn from users and experts

Purpose:

- use X for customer discovery
- learn real language
- find high-pain users
- sharpen product assumptions before overbuilding the post bank

Good topics:

- **what usually fails in the morning**
- **what users have tried already**
- **what feels too extreme**
- **what feels useful**
- **what people would tolerate from a wake-up device**
- **what experts think about validation or claim boundaries**

## Claim-safety reminder

To be written later.

Placeholder intent:

- This section should remind the writer to check `product/claims-and-evidence.md` before publishing claim-sensitive posts.
- It should explain that drafts in this file are not automatically approved public claims.
- It should preserve the distinction between hooks, draft language, and approved claim language.

## Hook bank

To be written later.

Placeholder intent:

- This section should store reusable X hooks and recurring opening lines.
- Hook-making guidance should live in `marketing/x/posting-strategy.md`.
- Finished or reusable hooks can live here.

## Post drafts

To be written later.

Placeholder intent:

- This section should store actual X post drafts.
- Drafts should be grouped by post type, campaign, or publishing need.
- Drafts should include status labels when useful.

## Reply drafts

To be written later.

Placeholder intent:

- This section should store reusable X reply examples.
- Reply strategy should live in `marketing/x/playbook.md` or `marketing/x/posting-strategy.md`.
- Finished reply examples can live here.

## CTA variants

To be written later.

Placeholder intent:

- This section should store reusable CTAs for waitlist growth, DMs, interviews, expert feedback, and product feedback.
- CTAs should stay specific to high-pain users when used for customer discovery or waitlist growth.

## Draft status labels

To be written later.

Placeholder intent:

- This section should define simple labels for draft readiness and review status.
- Example labels may include ready, needs edit, needs claim review, posted, retired, or do not use.

## Maintenance rules

To be written later.

Placeholder intent:

- This section should define when to add, edit, retire, or move drafts.
- It should prevent this file from becoming cluttered with stale posts.
