# Old MVP Prototype

## Purpose

This file documents the old Orisen MVP/prototype.

Use it to preserve historical product, hardware, firmware, UX, validation, and pilot-test context from the earlier physical prototype.

This file is not the current product spec.

It records what the old prototype included, what it demonstrated, what appeared to work, what was limited, and what evidence it does or does not provide.

## Source and status

Source:
- Founder-provided description in May 2026.
- Founder-uploaded old MVP component notes from prior planning and build documentation.
- Founder-provided old MVP pilot/test notes for the founder, Hamza/Humza, Dennis, and Sabeeh.

Status:
- Historical prototype / old MVP.
- Useful for understanding what was already built and tested directionally.
- Not a current production architecture.
- Not a validated customer-ready product.

## High-level summary

The old MVP was a physical bedside/headboard-mounted alarm prototype built around a wired development-board architecture inside a 3D printed case.

It demonstrated the core wake-completion concept:

- user sets an alarm on the device
- alarm rings at the scheduled time
- radar detects whether the user is still in bed
- alarm continues if the user remains in bed
- alarm shuts off after the user leaves bed
- alarm re-triggers or continues if the user gets back in bed
- off button is disabled during the alarm period
- device switches to battery if unplugged during alarm behavior

The prototype was not a polished consumer product. It was a functional proof-of-concept with modules, wires, a breadboard/dev board, and a 3D printed enclosure.

The old MVP was tested by a small group of early users/friends. The pilot evidence is strongest for wake-completion behavior: when the alarm and anti-dismiss behavior worked correctly, users generally got out of bed much closer to the alarm time than their usual baseline. The evidence is still limited because the sample was small, the testers were connected to the founder, there were bugs, and the test was not a controlled study.

## Prototype generation

Working label:
- Old MVP
- MVP 2
- 2025 Jan-Apr prototype, based on uploaded notes

## Physical architecture

### Enclosure and mounting

- 3D printed case.
- Mounted to the bed headboard using a C-clamp.
- Designed to sit near the user's bed and observe presence without requiring a wearable or camera.

### Electronics construction

- No custom PCB.
- Development board and modules connected through a breadboard and soldered wires.
- Multiple separate modules handled sensing, audio, light, power, and control.

### Main electronics mentioned by founder

- Arduino Nano development board, described by founder as the main controller/brain.
- Audio module for sound output.
- High-power or high-voltage LED module for light output.
- Power module that interfaced with wall power and battery input and switched between them as needed.
- SparkFun module containing the Acconeer A121 radar chip.
- Small LCD screen for interface/display.
- Joystick on top of the device for local control.

### Notes from uploaded old MVP component documentation

The uploaded old MVP planning notes list a component table and supporting notes. Relevant listed components include:

| Component | Notes |
|---|---|
| Speaker | 4 ohm, 94 dB top-port speaker listed in old notes |
| RTC | DS3231 precision RTC listed in old notes |
| Power module | TPS61090 / PowerBoost-style eval board listed in old notes |
| Audio module | DFPlayer listed in old notes |
| Wall adapter | AC/DC wall mount adapter listed in old notes |
| Switch | 120 V 5 A SPDT switch listed in old notes |
| LED driver | 1 A buck LED driver listed in old notes |
| LED module | Blue LED module listed in old notes |
| Radar module | SparkFun Qwiic XM125 radar sensor listed in old notes |
| MOSFETs/resistors/capacitors | Supporting discrete components listed in old notes |

Important note:
- The founder's recent verbal description mentioned an Arduino Nano.
- The uploaded old notes also mention Arduino Uno R3 in one planning section.
- Treat this as a historical documentation discrepancy until the exact final board used in the physical prototype is confirmed.

## User interface

The old MVP had local on-device controls:

- joystick on top of the device
- small LCD screen
- local interface for setting an alarm

The device did not rely on a phone app for the described alarm-setting flow.

## Core behavior demonstrated

### Alarm setting

- User could set an alarm using the joystick and LCD interface.
- Device would ring at the scheduled alarm time.

### Presence-based wake completion

Founder-reported behavior:

- Device used radar to detect whether the user was in bed.
- If the user was in bed during alarm time, the alarm continued ringing.
- If the user left bed, the alarm shut off.
- If the user tried to get back into bed, the alarm continued or re-triggered.
- The off button worked outside the alarm time.
- During alarm time, the off button did not work as a way to bypass the wake-completion behavior.

### Unplug protection / battery backup

Founder-reported behavior:

- If the device was unplugged, it switched to battery power.
- This supported the anti-bypass behavior during alarm time.

### Audio and light output

The old MVP included:

- audio output
- high-power LED/light output

Detailed ramping, sound profile, brightness levels, and intervention sequencing are not fully documented yet.

## Radar and presence detection

Radar module:
- SparkFun Qwiic XM125 radar sensor / Acconeer A121-based module, based on founder description and old component notes.

Founder-reported performance:
- Presence detection was very accurate directionally.
- It worked even if the user was under a blanket.
- It accurately detected when the user left bed.
- It accurately detected when the user got back into bed.

Important claim boundary:
- This supports that the old prototype demonstrated radar-based bed presence detection for wake-completion behavior in the founder-reported context.
- It does not by itself prove production reliability, broad bedroom robustness, sleep-stage detection, breathing/heart-rate extraction, sleep inertia reduction, or customer willingness to pay.

## Pilot/test participants

Founder-provided participant summary:

| Name | Occupation at time | Relationship to founder | Notes |
|---|---|---|---|
| Founder | University student | Self | Tested own prototype. |
| Hamza / Humza | University student | Friend | During testing, he was in Ramadan and finals, sleeping about 4 hours/day. Founder reports that waking was extremely hard for him, but the device worked every time in the relevant test context, whereas he would often otherwise sleep through and wake up about an hour later or similar. |
| Dennis | University student | Friend | Logged multi-day morning data and comments. |
| Sabeeh | Working full time | Friend | Logged multiple dates. Founder reports a bug allowed alarm shutoff on some days; excluding those bug days, he woke on time. |

Important limitation:
- These testers were a small convenience sample connected to the founder.
- This is useful early prototype/pilot evidence, not broad market validation.

## Test log definitions

The old test sheets asked users to fill in a usual baseline and then daily entries while using the alarm.

Variables:

- Bed time: time the user went to sleep.
- Alarm time: alarm time set.
- Wake up time: time the user actually woke up.
- Get out of bed time: time or delay until the user got out of bed after waking.
- Sleepy rating:
  - 5: extremely sleepy, feel drunk
  - 4: very sleepy
  - 3: decently sleepy
  - 2: slightly sleepy
  - 1: not sleepy at all, feel great, like waking naturally
- Irritation rating:
  - 5: extremely irritated
  - 4: pretty irritated
  - 3: mild irritation
  - 2: not irritated whatsoever
  - 1: not irritated by the alarm and actually wants to leave bed
- Mood rating, about 15 minutes after waking:
  - 5: irritated / wanted more sleep
  - 4: mild irritation
  - 3: indifferent
  - 2: happy to have woken on time
  - 1: really happy
- Energy rating, about 15 minutes after waking:
  - 5: really lethargic
  - 4: mildly lethargic
  - 3: normal
  - 2: somewhat energetic
  - 1: really energetic

Note:
- Lower ratings are better for sleepy, irritation, mood, and energy in these test sheets.

## Dennis test log

### Dennis baseline and daily table

| Metric | Usual | Day 1 | Day 2 | Day 3 | Day 4 | Day 5 | Day 6 | Day 7 |
|---|---:|---:|---:|---:|---|---:|---:|---:|
| Bed time | 12:30 | 1:00 | 1:00 | 2:45 | Alarm did not go off | 2:00 | 1:30 | 1:30 |
| Alarm time | 8:30 | 8:30 | 8:30 | 9:30 |  | 9:30 | 9:30 | 9:30 |
| Wake up time | 8:30 | 8:30 | 8:30 | 9:30 |  | 9:30 | 9:30 | 9:20 |
| Get out of bed | 10:00 | 8:30 | 8:30 | 9:30 |  | 9:30 | 9:30 | 9:20 |
| Sleepy rating | 4 | 4 | 4 | 3 |  | 3 | 3 | 2 |
| Irritation rating | 4 | 4 | 4 | 4 |  | 3 | 3 | 3 |
| Mood rating | 4 | 3 | 3 | 3 |  | 3 | 3 | 3 |
| Energy rating | 5 | 3 | 3 | 3 |  | 3 | 3 | 3 |

### Dennis comments

- Dennis reported that he does not drink caffeine.
- Dennis wrote: "Every single day, I really want to get back in bed but I can’t. So my only option is to take a shower, which I’m not happy about doing. But after about a minute in the shower, I wake up completely."

### Dennis interpretation

What this suggests:
- Dennis's usual baseline was waking at 8:30 but not getting out of bed until 10:00.
- On logged successful alarm days, his get-out-of-bed time matched or was very close to the alarm/wake-up time.
- His comment directly supports the behavioral mechanism: the system prevented returning to bed, forcing a wake-completion routine.

Limitations:
- One tester.
- Self-reported data.
- One day had an alarm failure and should not be treated as a successful trial.
- This does not prove reduced sleepiness or improved mood; the strongest signal is get-out-of-bed behavior.

## Hamza / Humza test log

### Hamza context

Founder-provided context:
- Hamza was a university student.
- He was in Ramadan and finals during testing.
- He was sleeping about 4 hours per day.
- Founder reports that waking was extremely hard for him.
- Founder reports that the device worked every single time in the relevant testing context, whereas Hamza would usually often sleep through and wake up about an hour later or similar.

### Hamza baseline and daily table

| Metric | Usual | 2025-03-04 | 2025-03-05 | 2025-03-06 | 2025-03-10 | 2025-03-11 | 2025-03-12 | 2025-03-13 | 2025-03-14 | 2025-03-17 | 2025-03-18 | 2025-03-19 |
|---|---:|---:|---:|---|---|---:|---|---:|---|---:|---:|---|
| Bed time | 12:00 | 1:30 | ~1:30 | ~12:30 | ~12:00 | ~11:30 | 11:15 | 12:00 | 11:30 | 11:00 | 2:00 | 11:00 |
| Alarm time | 4:00 | 3:30 | 3:30 | 3:30 | 4:30 | 3:00 | 3:30 | 5:00 | 4:30 | 5:00 | 3:00 | 5:00 |
| Wake up time | 4:50 | 3:33 | 3:31 | 3:28 (blue light woke me up) | 6:00 (slept again) | 3:34 | 3:46 | 5:01 | 4:40 | 5:01 | 3:33 | 5:46 |
| Get out of bed | 5:00 | 3:34 | 3:32 | 3:31 | 6:01 | 3:35 | 5:30 (slept again) | 5:01 | 4:41 | 5:01 | 3:34 | 5:48 |
| Sleepy rating | 4 | 1 | 3 | 1 | 4 | 2 | 4 | 1 | 2 | 1 | 4 | 4 |
| Irritation rating | 5 | 1 | 4 | 1 | 4 | 3 | 4 | 2 | 3 | 2 | 4 | 4 |
| Mood rating | 5 | 3 | 4 | 1 | 5 | 3 | 4 | 2 | 3 | 2 | 4 | 4 |
| Energy rating | 4 | 3 | 3 | 1 | 5 | 3 | 5 | 2 | 2 | 2 | 5 | 4 |

### Hamza interpretation

What this suggests:
- Hamza's usual baseline was alarm at 4:00, wake at 4:50, get out of bed at 5:00.
- Several logged days show wake-up and get-out-of-bed within a few minutes of the alarm time.
- There were also failure or partial-failure days where he slept again or woke much later.
- One day specifically notes that blue light woke him up.

Limitations:
- Context was unusual and severe: Ramadan, finals, and about 4 hours/day of sleep.
- Data is self-reported and small sample.
- Some days show sleeping again, so the claim cannot be "worked every time" without qualification.
- This supports directional wake-completion value but also shows the need for stronger anti-return-to-bed and reliability design.

## Sabeeh test log

### Sabeeh context

Founder-provided context:
- Sabeeh was working full time.
- Founder reports Sabeeh found a bug that allowed him to shut off the alarm on some days.
- Founder reports that excluding bug days, Sabeeh woke on time.

### Sabeeh baseline and daily table

| Date | Bed time | Alarm time | Wake up time | Get out of bed | Sleepy rating | Irritation rating | Mood rating | Energy rating | Comments |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| Usual | 10:30 | 5:30 | 6:30 | 9:00 | 4 | 4 | 4 | 4 |  |
| 2025-07-09 | 1:00 AM | 10:30 AM | 10:30 AM | 12:00 PM | 2 | 3 | 3 | 4 |  |
| 2025-07-10 |  |  |  |  |  |  |  |  |  |
| 2025-07-11 |  |  |  |  |  |  |  |  |  |
| 2025-07-12 |  |  |  |  |  |  |  |  |  |
| 2025-07-13 |  |  |  |  |  |  |  |  |  |
| 2025-07-14 |  |  |  |  |  |  |  |  |  |
| 2025-07-15 |  |  |  |  |  |  |  |  |  |
| 2025-07-16 | 11:00 PM | 6:30 AM | 7:30 AM | 8:30 AM | 2 | 3 | 3 | 4 | I didn't wake up to the alarm. I think I slept through it. Volume was 3, duration 15. |
| 2025-07-17 |  |  |  |  |  |  |  |  |  |
| 2025-07-18 |  |  |  |  |  |  |  |  |  |
| 2025-07-19 |  |  |  |  |  |  |  |  |  |
| 2025-07-20 |  |  |  |  |  |  |  |  |  |
| 2025-07-21 |  |  |  |  |  |  |  |  |  |
| 2025-07-22 |  |  |  |  |  |  |  |  |  |
| 2025-07-23 |  |  |  |  |  |  |  |  |  |
| 2025-07-24 | 11:00 | 5:30 | 5:30 | 9:00 | 4 | 4 | 4 | 4 |  |
| 2025-07-25 | 10:30 | 5:30 | 6:00 | 10:00 | 4 | 3 | 3 | 2 |  |
| 2025-07-26 | 11:00 | 7:30 AM | 10:00 AM | 10:30 AM | 2 | 2 | 3 | 3 |  |
| 2025-07-27 |  |  |  |  |  |  |  |  | At parents house |
| 2025-07-28 |  |  |  |  |  |  |  |  |  |
| 2025-07-29 |  |  |  |  |  |  |  |  |  |
| 2025-07-30 | 11:00 | 5:30 | 7:30 | 7:40 |  |  |  |  |  |

### Sabeeh interpretation

What this suggests:
- Sabeeh's usual baseline was alarm at 5:30, wake at 6:30, and get out of bed at 9:00.
- The data shows mixed results and some clear failure/bug days.
- The founder reports that a bug allowed alarm shutoff on some days.
- Excluding bug days may show better wake performance, but the raw table itself should be treated cautiously until bug days are explicitly labeled.

Limitations:
- Several rows are blank.
- Bug days are not fully labeled in the table.
- Some logged days show wake-up or get-out-of-bed much later than alarm time.
- This is useful as failure-mode evidence as much as success evidence.

## Pilot-level interpretation

What the pilot data supports:

- The old MVP was used by multiple people, not only the founder.
- The presence-based wake-completion concept showed early promise in real morning contexts.
- Dennis's data strongly supports the behavioral mechanism: preventing the user from staying in bed or going back to bed can force immediate wake completion.
- Hamza's data supports value under severe wake-up conditions, but with some failures/partial failures.
- Sabeeh's data shows both usefulness and reliability/bug risks.
- The strongest validated dimension is getting the user out of bed closer to the alarm time, not improving mood, energy, grogginess, or overall sleep quality.

What the pilot data does not support:

- broad production reliability
- clinical efficacy
- reduced sleep inertia
- reduced grogginess
- better mood or energy as a proven outcome
- sleep-stage-aware intervention
- artificial sleep phase transitioning
- paid demand
- retention
- scalable customer readiness

## Current evidence interpretation

What the old MVP supports:

- Orisen's core wake-completion loop was physically prototyped.
- Non-contact radar presence detection was used in a real device form factor.
- The device could combine local alarm behavior, radar presence detection, audio/light output, local controls, and battery backup.
- The product direction is not purely conceptual; an earlier physical prototype existed.
- A small pilot/test group used the old MVP in real morning contexts.
- The strongest pilot signal is that presence-based wake completion can force or strongly encourage users to get out of bed closer to the alarm time.

What the old MVP does not yet support by itself:

- production reliability
- manufacturability
- regulatory readiness
- sleep-stage detection
- sleep-phase-aware intervention
- artificial sleep phase transitioning
- proven reduction in grogginess or sleep inertia
- willingness to pay
- repeat usage or retention beyond the small pilot context
- broad robustness across many users and bedrooms

## Known limitations

- Breadboard/dev-board/module-based build.
- No custom PCB.
- Many wired module interconnects.
- 3D printed enclosure, not production enclosure.
- Local joystick/LCD interface rather than app-based setup.
- Historical documentation still has some uncertainty around exact controller board used.
- Small tester sample.
- Testers were founder and friends, not cold customers.
- Self-reported data.
- Some rows are incomplete.
- Some days had failures, bugs, or sleeping again.
- Sabeeh found a bug that allowed alarm shutoff on some days.
- No quantitative radar false-positive/false-negative metrics documented yet.
- No production reliability testing documented.
- No willingness-to-pay test documented.

## Open questions to fill in

Add more detail as the founder provides it:

- Which specific Sabeeh days were bug days?
- What exactly was the Sabeeh shutoff bug?
- What caused Dennis's alarm failure day?
- Did anyone successfully bypass the wake-completion mechanism besides known bug behavior?
- What were the known radar false positives/false negatives?
- How did it behave with blankets, pillows, different bed positions, multiple people, pets, or room movement?
- What audio/light behavior was implemented exactly?
- Was re-trigger behavior timed/windowed, or immediate?
- What battery duration was achieved?
- What enclosure and mounting issues appeared?
- What would be changed in the next version?
- Are there photos or videos of the old MVP and test setup?
- Are there exact tester quotes beyond Dennis's written comment?

## Related docs

- `validation/evidence-log.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `hardware/hardware-overview.md` if created later
- `radar-ml/radar-ml-context-map.md`
