# Old MVP Test Row Labels

## Purpose

This file labels the old MVP pilot/test rows so future analysis does not misread the raw tables.

Use this file with:

- `product/old-mvp.md`
- `product/old-mvp-bypass-and-failure-notes.md`
- `validation/evidence-log.md`

This file preserves both:

- the founder's overall interpretation that the old MVP was a resounding success for helping testers wake up on time compared with their usual oversleeping patterns
- the conservative row-level interpretation needed for credible evidence and claims discipline

## Source

Source:
- Founder-provided clarification in May 2026.
- Founder noted that speech-to-text was used, so wording should be interpreted carefully.

## Classification labels

Use these labels for old MVP pilot rows:

- `Success`: alarm/wake-completion behavior worked well enough that the user woke/got out of bed close to the alarm time relative to baseline.
- `Partial success`: device helped or partially worked, but the user woke late, got out of bed late, slept again, or the outcome was mixed.
- `Technical failure`: issue caused by alarm not ringing, alarm duration too short, volume too low, missing volume ramp, or another prototype/configuration limitation.
- `Bypass/bug`: user exploited a loophole or bug, especially pre-alarm shutoff/tampering.
- `Invalid/no data`: row is blank, away from setup, or not enough data.

## Founder-level interpretation

Founder interpretation:

- Across the pilot users, the old MVP was a strong success compared with their usual oversleeping behavior.
- The device helped users wake up on time or much closer to their alarm than usual.
- The strongest evidence is around wake completion: getting the user out of bed and preventing return-to-bed behavior.
- The pilot data should not be used as proof of grogginess reduction, sleep-stage intervention, production reliability, or willingness to pay.

Conservative interpretation:

- Keep raw row labels honest.
- Preserve bug/failure days instead of hiding them.
- Treat bug/failure days as important product-learning evidence, not as invalidating the whole wedge.
- The old MVP supports early prototype/pilot validation of wake completion, not broad production validation.

## Dennis row labels

Founder clarification:

- Dennis's alarm-failure day should be treated as a bug/technical failure.
- Founder assumes it was not important strategically, likely the alarm did not ring or something similar.
- All other Dennis days should be treated as successful wake-completion days.

| Day | Raw outcome | Label | Notes |
|---|---|---|---|
| Day 1 | Alarm 8:30, wake 8:30, out of bed 8:30 | Success | Strong improvement versus usual out-of-bed time of 10:00. |
| Day 2 | Alarm 8:30, wake 8:30, out of bed 8:30 | Success | Strong improvement versus usual out-of-bed time of 10:00. |
| Day 3 | Alarm 9:30, wake 9:30, out of bed 9:30 | Success | Strong wake-completion result. |
| Day 4 | Alarm did not go off | Technical failure | Treat as bug/alarm failure, not as wake-completion failure. |
| Day 5 | Alarm 9:30, wake 9:30, out of bed 9:30 | Success | Strong wake-completion result. |
| Day 6 | Alarm 9:30, wake 9:30, out of bed 9:30 | Success | Strong wake-completion result. |
| Day 7 | Alarm 9:30, wake 9:20, out of bed 9:20 | Success | Woke and got out of bed before alarm time or around target wake window. |

Dennis interpretation:

- Dennis is the cleanest tester signal in the old MVP data.
- His usual baseline was waking at 8:30 but not getting out of bed until 10:00.
- During successful old MVP days, he got out of bed at or near the alarm time.
- His written comment strongly supports the anti-return-to-bed mechanism.

## Hamza / Humza row labels

Founder clarification:

- Founder considers all Hamza days a success at the overall behavioral level.
- Hamza was one of the earlier testers.
- Founder believes late wake days were mostly because the alarm was not loud enough, did not ramp volume, or rang for too short a duration.
- 2025-03-12 is the day where Hamza slept again.
- The prototype stayed at one volume and did not ramp volume at that point.

Conservative handling:

- Mark days close to alarm time as `Success`.
- Mark days where wake/get-out-of-bed were much later as `Technical failure` or `Partial success`, depending on what the row shows.
- Preserve founder interpretation that these were prototype configuration limitations rather than failure of the wake-completion concept.

| Date | Raw outcome | Label | Notes |
|---|---|---|---|
| 2025-03-04 | Alarm 3:30, wake 3:33, out of bed 3:34 | Success | Strong result. |
| 2025-03-05 | Alarm 3:30, wake 3:31, out of bed 3:32 | Success | Strong result. |
| 2025-03-06 | Alarm 3:30, wake 3:28, out of bed 3:31; note says blue light woke him up | Success | Strong result; useful blue-light signal. |
| 2025-03-10 | Alarm 4:30, wake 6:00, out of bed 6:01; slept again | Partial success / technical limitation | Raw row is late. Founder context suggests early prototype limitations. Do not count as clean success in quantified analysis. |
| 2025-03-11 | Alarm 3:00, wake 3:34, out of bed 3:35 | Success / delayed success | Woke later than alarm but still much closer than usual severe oversleeping pattern. Label cautiously if computing strict on-time rate. |
| 2025-03-12 | Alarm 3:30, wake 3:46, out of bed 5:30; slept again | Partial success / slept again | Founder specifically identifies this as slept-again day. Important return-to-bed/follow-through issue. |
| 2025-03-13 | Alarm 5:00, wake 5:01, out of bed 5:01 | Success | Strong result. |
| 2025-03-14 | Alarm 4:30, wake 4:40, out of bed 4:41 | Success / slightly delayed | Strong practical result, slightly after alarm. |
| 2025-03-17 | Alarm 5:00, wake 5:01, out of bed 5:01 | Success | Strong result. |
| 2025-03-18 | Alarm 3:00, wake 3:33, out of bed 3:34 | Success / delayed success | Delayed but still likely materially better than baseline. Label cautiously for strict on-time calculations. |
| 2025-03-19 | Alarm 5:00, wake 5:46, out of bed 5:48 | Technical limitation / delayed success | Founder context suggests volume/duration limitations. Do not count as clean success in strict analysis. |

Hamza interpretation:

- Hamza is valuable because he tested under very hard conditions: Ramadan, finals, and about 4 hours/day of sleep.
- Several days were very strong successes.
- The weaker days likely reveal prototype limitations: no volume ramp, low volume, too-short duration, or alarm stopping too early.
- Product lesson: the alarm must escalate and cannot time out while the user is still in bed.

## Sabeeh row labels

Founder clarification:

- Founder says 2025-07-09 was a success.
- The remaining days where Sabeeh overslept were bug days.
- The suspected bug was pre-alarm bypass: Sabeeh could wake up shortly before the alarm and turn it off because there was no pre-alarm lockout window.
- Founder notes that if the user tried to change or shut off the alarm seconds before alarm time, the old MVP allowed it.

Conservative handling:

- Treat 2025-07-09 as success.
- Treat the significant oversleep days as `Bypass/bug` unless there is evidence they were normal clean trials.
- Treat blank rows as `Invalid/no data`.

| Date | Raw outcome | Label | Notes |
|---|---|---|---|
| 2025-07-09 | Alarm 10:30, wake 10:30, out of bed 12:00 | Success / delayed get-out-of-bed | Founder labels as success. Conservative note: out-of-bed was much later, so this is not clean wake-completion success unless context explains why. |
| 2025-07-10 | Blank | Invalid/no data | No data. |
| 2025-07-11 | Blank | Invalid/no data | No data. |
| 2025-07-12 | Blank | Invalid/no data | No data. |
| 2025-07-13 | Blank | Invalid/no data | No data. |
| 2025-07-14 | Blank | Invalid/no data | No data. |
| 2025-07-15 | Blank | Invalid/no data | No data. |
| 2025-07-16 | Alarm 6:30, wake 7:30, out of bed 8:30; user said he likely slept through it, volume 3, duration 15 | Technical failure / underpowered alarm | Could be volume/duration issue rather than pre-alarm bypass. Do not count as clean success. |
| 2025-07-17 | Blank | Invalid/no data | No data. |
| 2025-07-18 | Blank | Invalid/no data | No data. |
| 2025-07-19 | Blank | Invalid/no data | No data. |
| 2025-07-20 | Blank | Invalid/no data | No data. |
| 2025-07-21 | Blank | Invalid/no data | No data. |
| 2025-07-22 | Blank | Invalid/no data | No data. |
| 2025-07-23 | Blank | Invalid/no data | No data. |
| 2025-07-24 | Alarm 5:30, wake 5:30, out of bed 9:00 | Bypass/bug or partial failure | Woke at alarm but did not complete wake until much later. Founder says oversleep days were bug days. |
| 2025-07-25 | Alarm 5:30, wake 6:00, out of bed 10:00 | Bypass/bug or partial failure | Significant delayed wake-completion. Founder says oversleep days were bug days. |
| 2025-07-26 | Alarm 7:30, wake 10:00, out of bed 10:30 | Bypass/bug or technical failure | Significant oversleep. Label as bug/failure. |
| 2025-07-27 | At parents house | Invalid/no data | Not a valid home/setup trial. |
| 2025-07-28 | Blank | Invalid/no data | No data. |
| 2025-07-29 | Blank | Invalid/no data | No data. |
| 2025-07-30 | Alarm 5:30, wake 7:30, out of bed 7:40 | Bypass/bug or technical failure | Founder says remaining overslept days were bug days. |

Sabeeh interpretation:

- Sabeeh is most useful as bypass/failure-mode evidence.
- His behavior revealed the need for a pre-alarm tamper lockout window.
- The raw data should not be used to claim clean success across Sabeeh days.
- The data is still useful because it shows how a motivated sleepy user can exploit loopholes.

## Old MVP behavior details

Founder-provided behavior details:

| Question | Answer |
|---|---|
| Exact pre-alarm bug Sabeeh found | If he woke up shortly before alarm time and turned the alarm off, it would no longer ring. |
| How long before alarm could he shut it off? | There was no pre-alarm protection window. Even seconds before alarm time, the user could change/disable the alarm. |
| How long did alarm ring before auto-stopping? | Founder does not remember. |
| Did it ramp volume? | No. It stayed at one volume. |
| What sound did it play? | A random game sound. |
| What did blue light do? | Blue light was intended to help the user wake up. |
| Was light always on, flashing, ramping, or manual? | It gradually ramped up. |
| Return-to-bed detection window | Founder does not remember. |
| Battery duration when unplugged | At least about 15 minutes, according to founder memory. |
| Did the device log anything? | No. |
| User override during alarm | High-friction physical override: user would need to unscrew the front and unplug the battery. Founder intended this as a high-friction override so users would not use it as a snooze mechanism. |

## Product lessons from row labels

- Future Orisen should have a pre-alarm tamper lockout window.
- Future Orisen should not allow alarm disable, delay, or weakening shortly before wake time.
- Future Orisen should use volume escalation/ramping.
- Future Orisen should not auto-stop while the user is still in bed.
- Future Orisen should log alarm events, bypass attempts, power changes, alarm edits, and wake-completion state transitions.
- Future pilots should label every morning as success, partial success, bypass/bug, technical failure, invalid/no data, or setup issue.
- Future pilot analysis should separate strict on-time success from practical improvement versus baseline.

## Evidence boundary

This file strengthens support for:

- early prototype/pilot validation of wake completion
- anti-bypass product need
- pre-alarm lockout as a required product behavior
- volume escalation as a required product behavior
- battery backup as an anti-bypass requirement
- event logging as necessary for future evidence quality

This file does not prove:

- broad market demand
- willingness to pay
- production reliability
- clinical efficacy
- reduced grogginess
- reduced sleep inertia
- sleep-stage-aware intervention
- artificial sleep phase transitioning
- radar-based sleep-stage estimation
