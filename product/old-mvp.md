# Old MVP Prototype

## Purpose

This file documents the old Orisen MVP/prototype.

Use it to preserve historical product, hardware, firmware, UX, and validation context from the earlier physical prototype.

This file is not the current product spec.

It records what the old prototype included, what it demonstrated, what appeared to work, what was limited, and what evidence it does or does not provide.

## Source and status

Source:
- Founder-provided description in May 2026.
- Founder-uploaded old MVP component notes from prior planning and build documentation.

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

The founder did not yet provide detailed behavior for ramping, patterns, brightness levels, volume profiles, or intervention sequencing.

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

## Current evidence interpretation

What the old MVP supports:

- Orisen's core wake-completion loop was physically prototyped.
- Non-contact radar presence detection was used in a real device form factor.
- The device could combine local alarm behavior, radar presence detection, audio/light output, local controls, and battery backup.
- The product direction is not purely conceptual; an earlier physical prototype existed.

What the old MVP does not yet support by itself:

- customer validation unless tester details, usage sessions, and user feedback are documented
- production reliability
- manufacturability
- regulatory readiness
- sleep-stage detection
- sleep-phase-aware intervention
- artificial sleep phase transitioning
- reduction in grogginess or sleep inertia
- willingness to pay
- repeat usage or retention

## Known limitations

- Breadboard/dev-board/module-based build.
- No custom PCB.
- Many wired module interconnects.
- 3D printed enclosure, not production enclosure.
- Local joystick/LCD interface rather than app-based setup.
- Historical documentation still has some uncertainty around exact controller board used.
- No documented tester count yet.
- No documented number of nights/mornings tested yet.
- No documented raw tester quotes yet.
- No documented failure cases yet.
- No documented environmental limits yet.

## Open questions to fill in

Add more detail as the founder provides it:

- How many people tested the old MVP?
- Who tested it: founder only, friends, family, students, external users?
- How many nights/mornings was it tested?
- Was it tested during real sleep/wake conditions or mainly demos?
- What specific user feedback was received?
- Were there any quotes?
- Did anyone fail to bypass it?
- Did anyone successfully bypass it?
- What were the known radar false positives/false negatives?
- How did it behave with blankets, pillows, different bed positions, multiple people, pets, or room movement?
- What audio/light behavior was implemented exactly?
- Was re-trigger behavior timed/windowed, or immediate?
- What battery duration was achieved?
- What enclosure and mounting issues appeared?
- What would be changed in the next version?

## Related docs

- `validation/evidence-log.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `hardware/hardware-overview.md` if created later
- `radar-ml/radar-ml-context-map.md`
