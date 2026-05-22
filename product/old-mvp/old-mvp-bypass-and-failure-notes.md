# Old MVP Bypass and Failure Notes

## Purpose

This file captures detailed founder-reported clarification about old MVP bypass attempts, failure modes, radar behavior, enclosure behavior, unplug behavior, and design lessons.

This file is an addendum to `product/old-mvp.md` and should be used with:

- `product/old-mvp.md`
- `product/old-mvp-test-row-labels.md`
- `ai-context/claim-control/claim-control-log.md`
- `product/claims-and-evidence.md`

It preserves detailed notes without overloading the main old MVP file.

## Source and interpretation

Source:
- Founder-provided speech-to-text clarification in May 2026.
- Founder-provided follow-up clarification in May 2026.

Interpretation rules:
- Treat these as founder-reported historical notes.
- Use them to strengthen the old MVP anti-bypass and failure-mode record.
- Do not treat them as production reliability proof.
- Do not convert them into broad claims without supporting evidence from larger tests.

Name note:
- The founder used speech-to-text and referred to “Sippy.”
- Based on context, “Sippy” likely refers to Sabeeh.
- Confirm spelling/name later if needed.

## Summary

Founder reports that the old MVP was intentionally stress-tested by early pilot users for bypass attempts.

Reported behavior:

- Testers tried to bypass the device.
- Testers tried to unplug it.
- Testers tried to go back to bed.
- Unplug behavior worked because the device switched to battery.
- Return-to-bed behavior worked because the device continued or re-triggered.
- Radar did not fail in the reported test context.
- The clamp/enclosure did not cause meaningful issues.
- The device reportedly fell and cracked somewhat, but still worked.

Main discovered bug/design gap:

- Sabeeh likely found a way to wake up before the alarm and shut it off before the anti-dismiss alarm period started.
- Founder clarified that there was no pre-alarm protection window: the user could change or disable the alarm even seconds before alarm time.
- Design lesson: future versions need a pre-alarm lockout window where the alarm cannot be adjusted, dismissed, disabled, or weakened shortly before the scheduled alarm.

## Bypass attempts

Founder-reported behavior:

- All pilot users tried to bypass the device in some way.
- Sabeeh was especially active in testing bypass methods.
- Sabeeh likely discovered that if he woke up before the alarm, he could shut it off before the alarm period started, preventing the alarm from ringing.
- Founder clarified that because there was no lockout window, the device would allow alarm changes or disabling even seconds before the scheduled alarm.

Interpretation:

- This is valuable failure-mode evidence.
- It shows that users with severe wake-up problems may actively look for loopholes.
- Anti-bypass behavior needs to cover not only the alarm period, but also a pre-alarm window.

## Required design change: pre-alarm tamper lockout

Future device behavior should include a pre-alarm lockout window.

During this window, the user should not be able to:

- disable the upcoming alarm
- change the upcoming alarm to a later time
- reduce the alarm volume or duration below a safe threshold
- turn off wake-completion enforcement
- bypass the alarm through local controls

Open design decision:

- Exact lockout window length still needs to be chosen.
- Candidate values might be 10, 15, 30, or 60 minutes before the scheduled alarm.
- The final value should balance anti-bypass strength with legitimate user control.

Important product principle:

- Orisen is for people whose half-awake self cannot be trusted to make good wake-up decisions.
- The product must protect the user from their own predictable bypass behavior during the wake-up window.

## Unplug attempts and battery backup

Founder-reported behavior:

- Testers tried unplugging the device.
- The device continued working after unplugging because it switched to battery power.
- Battery/unplug behavior worked as intended in the reported pilot context.
- Founder later estimated that battery duration under unplugged alarm behavior was at least about 15 minutes, though exact runtime is not documented.

Interpretation:

- This strengthens evidence for the old MVP’s anti-bypass concept.
- It supports keeping battery backup as a core product requirement.
- It does not prove final battery duration, production power reliability, or regulatory-ready power design.

Design implication:

- Future Orisen versions should retain internal backup power.
- Backup power should be long enough to survive intentional unplugging during the wake-up period.
- The user should not be able to bypass the alarm by unplugging the device.

## Return-to-bed attempts

Founder-reported behavior:

- Testers intentionally tried to go back to bed.
- Going back to bed did not work as a bypass.
- The device continued or re-triggered when the user returned to bed.
- Founder does not currently remember the exact return-to-bed detection window.

Interpretation:

- This directly supports the wake-completion mechanism.
- It supports the claim that the old MVP could detect return-to-bed behavior and enforce wake completion in the reported pilot context.
- It does not prove broad robustness across all users, bedrooms, bedding, partners, or pets.

Design implication:

- Return-to-bed detection should remain a core feature.
- The future version should clearly define the return-to-bed window after alarm dismissal.
- The product should not consider wake-up complete merely because the user briefly exits bed.

## Radar behavior

Founder-reported behavior:

- Radar did not fail in the reported pilot context.
- Founder reports no known false positives or false negatives during the relevant tests.
- The system included a short debounce/stability delay, about 2 seconds, before treating in-bed or out-of-bed state changes as real.
- The purpose of this delay was to reduce false positives and false negatives.

Interpretation:

- This is useful evidence that a simple debounce/stability window helped the old MVP behave reliably in its test context.
- The strongest safe claim is that radar presence detection worked well in the old MVP pilot context.
- Do not claim measured radar accuracy without quantitative test logs.

Design implication:

- Future radar/presence logic should include state-debounce or confidence timing.
- Bed presence should not flip instantly on a single noisy signal.
- The firmware should likely use clear state transitions such as `IN_BED_CANDIDATE`, `IN_BED_CONFIRMED`, `OUT_OF_BED_CANDIDATE`, and `OUT_OF_BED_CONFIRMED`, or equivalent logic.

## Clamp and enclosure behavior

Founder-reported behavior:

- Clamp/enclosure did not create meaningful issues in the reported tests.
- Device reportedly fell and cracked somewhat, but still continued working.

Interpretation:

- This is encouraging for rough prototype durability.
- It does not prove production mechanical reliability.
- It does suggest that the basic headboard-mounted form factor did not immediately fail in the pilot context.

Design implication:

- Headboard mounting remains a plausible mechanical direction.
- Future versions need proper mechanical testing for clamp stability, drop, vibration, cable strain, user installation error, and bed/headboard variation.

## Alarm behavior details

Founder-reported details:

- Alarm sound was a random game sound.
- Alarm volume stayed at one volume.
- The old MVP did not ramp volume.
- Founder does not remember exactly how long the alarm rang before auto-stopping.
- Blue light was intended to help wake the user.
- Blue light gradually ramped up.
- The device did not log events.

Design implications:

- Future alarm should escalate volume instead of staying at one fixed volume.
- Future alarm should not auto-stop while the user is still in bed.
- Future device should log alarm start, alarm stop, dismiss attempts, alarm edits, power changes, presence transitions, and wake-completion state changes.
- Future light behavior should be specified as a proper ramp/intervention profile rather than only a simple blue-light output.

## High-friction physical override

Founder-reported behavior:

- During alarm behavior, the intended physical override was high-friction.
- The user would have to unscrew the front and unplug the battery.
- Founder intended this as a high-friction override so users would not use it as a snooze mechanism.

Interpretation:

- This supports the product principle that Orisen should be hard to bypass during the wake-up window.
- However, a production product needs a safer, clearer, and more responsible emergency override design than requiring disassembly.

Design implication:

- Future versions need an emergency override that is possible but intentionally high-friction, logged, and not usable as an easy snooze.
- Emergency override design should consider safety, liability, user trust, and edge cases.

## Dennis alarm failure day

Founder-reported clarification:

- Dennis’s alarm-failure day was likely because the alarm did not ring or something similar.
- Founder says to assume it was a bug and not strategically important.
- Exact root cause is not confirmed.

Interpretation:

- Treat this as a technical failure day, not a wake-completion behavior failure.
- Do not count this day as a successful alarm trial.
- Root cause remains unknown.

Open question:

- Was this caused by a software bug, power issue, UI/alarm-setting issue, audio module issue, or user setup issue?

## Hamza / Humza partial-failure days

Founder-reported clarification:

- Hamza was one of the earlier testers.
- Founder considers all Hamza days successful overall compared with baseline.
- Founder later clarified that on late-wake days, Hamza likely woke late because the alarm was not loud enough to wake him up.
- The prototype stayed at one volume and did not ramp volume.
- Some partial failures may also have involved the alarm duration being set too short, possibly around 15 minutes instead of 30 minutes.
- 2025-03-12 is the day where Hamza slept again.

Interpretation:

- Some Hamza/Humza failures should likely be interpreted as configuration/prototype-behavior limitations, not necessarily failure of the presence-detection concept.
- Still, they should remain documented as partial failures or technical limitations in strict row-level analysis.

Design implication:

- Alarm duration must be long enough to enforce wake completion.
- Volume ramping/escalation should be required.
- The alarm should not stop automatically while the user is still in bed.
- Wake-completion state should override fixed alarm-duration expiration.

## Sabeeh / “Sippy” bug days

Founder-reported clarification:

- Founder says 2025-07-09 was a success.
- The remaining days where Sabeeh overslept significantly were likely bug days.
- The suspected bug was a pre-alarm bypass: waking before the scheduled alarm and shutting it off before the alarm lockout/enforcement period began.
- The root design flaw was that there was no pre-alarm lockout window.

Interpretation:

- Sabeeh’s data is valuable because it exposes a real bypass edge case.
- These days should not be treated as clean evidence against the wake-completion mechanism without labeling them as bug/bypass days.
- They should also not be ignored, because users will exploit loopholes if they exist.

Design implication:

- Add a pre-alarm tamper lockout.
- Add event logging for alarm changes, dismissals, power changes, and local-control attempts near alarm time.
- In future pilots, classify each morning as successful, partial success, user bypass, technical failure, setup issue, or invalid test.

## Battery duration

Founder-reported clarification:

- Battery/unplug behavior worked fine in the old MVP pilot context.
- Founder estimates battery duration was at least about 15 minutes.
- Exact battery duration is not documented here.

Interpretation:

- This supports the concept of backup power as a functional anti-bypass feature.
- It does not provide a quantified runtime requirement or validated battery spec.

Open question:

- What was the actual battery runtime during alarm behavior?

## Evidence implications

This clarification strengthens support for:

- anti-bypass behavior as a real user need
- battery backup as a necessary product feature
- return-to-bed detection as central to the product
- pre-alarm tamper lockout as a required next-generation feature
- debounce/stability timing as useful for radar state changes
- wake completion as Orisen’s strongest validated wedge
- volume escalation/ramping as a required alarm behavior
- event logging as a required future validation and debugging feature

This clarification does not prove:

- production reliability
- broad bedroom robustness
- paid demand
- retention
- clinical efficacy
- reduced grogginess
- reduced sleep inertia
- sleep-stage-aware intervention
- artificial sleep phase transitioning
- radar-based sleep-stage estimation

## Recommended updates to future specs

Future product/software/firmware specs should include:

- pre-alarm tamper lockout window
- active-alarm anti-dismiss behavior
- post-alarm return-to-bed re-trigger window
- battery-backed alarm enforcement
- event logging for bypass attempts
- volume ramping/escalation
- no automatic alarm timeout while the user is still detected in bed
- radar state debounce/stability window
- explicit classification of pilot mornings by outcome type
- high-friction but safe emergency override behavior

## Related docs

- `product/old-mvp.md`
- `product/old-mvp-test-row-labels.md`
- `ai-context/claim-control/claim-control-log.md`
- `software/software-read-rules.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
