# Evidence Log

## Purpose

This file tracks real evidence for Orisen claims, product decisions, customer assumptions, technical validation, and fundraising or marketing statements.

Use this file to separate what is validated from what is assumed, planned, or still unproven.

Do not invent evidence. Add only real user feedback, pilot results, website/signup data, technical test results, or other documented observations.

This file is the evidence record.

`validation/evidence-standard.md` is the authority for how evidence should be classified and interpreted.

## Evidence classification rule

Classify evidence using `validation/evidence-standard.md`.

Important categories include:

- Validated
- Early signal
- Built but not validated
- Planned
- Hypothesis
- Long-term vision
- Unsupported or unsafe claim

Also record evidence strength where helpful, using the evidence-strength levels defined in `validation/evidence-standard.md`.

If evidence does not clearly support a claim, treat the claim as an assumption, roadmap item, hypothesis, or unsupported claim.

## Current evidence summary

### Strongest current evidence

- Presence-based wake completion is currently the strongest validated wedge.
- Current evidence should still be treated as early validation, not broad-market proof.
- The old MVP physically demonstrated the wake-completion loop using local alarm behavior, radar-based presence detection, audio/light output, local controls, and battery backup.

### Early demand and messaging signal

- Orisen received 66 waitlist signups excluding the founder/test signup after one founder LinkedIn post and limited external sharing.
- Estimated total website visits were about 415, implying about 16% visitor-to-waitlist conversion.
- This is an early signal of problem/message resonance, not proof of willingness to pay, retention, product-market fit, or clinical/technical efficacy.

### Needs more evidence

- Reduced grogginess
- Reduced sleep inertia
- Sleep-phase-aware wake intervention
- Artificial sleep phase transitioning
- Radar-based sleep-stage estimation
- Willingness to pay
- First customer segment
- Price point
- Reliability standard required for users to trust Orisen as a main alarm
- Old MVP tester count, real usage sessions, failure modes, and user quotes

## Evidence entries

Add entries below as evidence is collected.

### Entry template

```markdown
### [YYYY-MM-DD] [Short evidence title]

- Evidence type:
- Source:
- What was tested or observed:
- What the user/customer said or did:
- Claim supported:
- Claim not supported:
- Evidence category:
- Evidence strength:
- Confidence:
- Limitations:
- Related docs to update:
- Notes:
```

## User interview evidence

Add customer interview evidence here.

## Pilot evidence

Add pilot user evidence here.

## Website and waitlist evidence

Add website, waitlist, conversion, and signup evidence here.

### 2026-05-18 — Waitlist signups from one LinkedIn post and limited external sharing

- Evidence type: Website/waitlist and social post performance.
- Source: Founder-reported LinkedIn analytics, Microsoft Clarity tracking, waitlist signup count, and founder estimate for pre-Clarity visits.
- Date range: 2026-02-04 to 2026-05-18.
- Traffic source:
  - One LinkedIn post by the founder, posted on 2026-02-04 at about 2:15 PM.
  - Limited external sharing from a friend, Hammad, who shared the website link with friends.
  - No paid traffic reported.
- What was tested or observed:
  - A single founder LinkedIn post and limited external sharing drove early attention to the Orisen website/waitlist.
  - Microsoft Clarity started on 2026-02-04 at about 6:30 PM, after the site had already received about 68 visits and 29 signups.
  - Final known LinkedIn post metrics reported by the founder:
    - 23.4k impressions
    - 197 likes
    - 69 comments
    - 296 LinkedIn-reported visits/clicks to the link from that post
    - 13 sends
    - 6 saves
  - Website visit tracking:
    - 347 Microsoft Clarity-recorded visits after setup
    - about 68 estimated website visits before Clarity setup
    - about 415 estimated total website visits
  - Waitlist result:
    - 66 waitlist signups excluding the founder/test signup
    - about 16% estimated visitor-to-waitlist conversion using 66 signups / 415 estimated total website visits
- Intermediate tracking notes:
  - By 2026-02-04 at about 6:45 PM, the post had about 4.1k impressions, 85 likes, 34 comments, 29 signups, and about 68 estimated website visits before Clarity was active.
  - By 2026-02-08, the founder estimated about 274 total website visits, using about 206 Clarity-recorded visits plus about 68 pre-Clarity visits.
- What the user/customer said or did:
  - Users signed up for the waitlist after viewing the website.
  - LinkedIn users engaged with the post through likes, comments, sends, saves, and link visits.
- Claim supported:
  - Orisen has an early signal of interest from a founder-led organic launch post.
  - The wake-up problem and/or Orisen's early positioning were compelling enough for some visitors to join a waitlist.
  - A single organic LinkedIn post can generate meaningful early awareness and waitlist interest for Orisen.
  - The website showed promising early visitor-to-waitlist conversion under founder-reported tracking assumptions.
- Claim not supported:
  - This does not prove willingness to pay.
  - This does not prove broad-market demand.
  - This does not prove product-market fit.
  - This does not prove retention or repeated usage.
  - This does not prove that Orisen reduces grogginess or sleep inertia.
  - This does not prove sleep-stage-aware intervention, artificial sleep phase transitioning, radar-based sleep-stage estimation, or clinical efficacy.
  - This does not prove that the LinkedIn post alone caused all signups, because there was limited external sharing and likely some direct/unknown traffic.
- Evidence category: Early signal.
- Evidence strength: Level 1 to Level 2.
- Confidence: Medium for signups, LinkedIn metrics, and broad direction of interest; medium-low for exact website conversion because total visits rely partly on a pre-Clarity estimate and different analytics tools do not measure traffic identically.
- Limitations:
  - Waitlist signup is not the same as payment, preorder, usage, or retention.
  - Traffic attribution is imperfect because LinkedIn, Microsoft Clarity, direct traffic, and external sharing are separate measurement sources.
  - The audience was likely influenced by the founder's network and may not represent broader cold-market demand.
  - The landing page and post may have selected for people interested in startups, hardware, or the founder rather than only people with severe wake-up pain.
  - No evidence here measures whether users would trust Orisen as their primary alarm or pay for it.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `fundraising/investor-narrative.md`
  - `marketing/positioning-and-messaging.md`
  - `product/target-customer.md` if signup source or customer profile details become available
- Notes:
  - This evidence can be used carefully in fundraising and marketing as an early demand/message-resonance signal.
  - It should not be described as product validation, paid demand, clinical evidence, or proof of broad product-market fit.

## Technical validation evidence

Add radar, firmware, app, hardware, and intervention test evidence here.

### 2026-05-18 — Old MVP demonstrated radar-based wake-completion loop

- Evidence type: Technical prototype evidence / old MVP evidence.
- Source:
  - Founder-provided description in May 2026.
  - Uploaded old MVP component notes covering the 2025 Jan-Apr MVP 2 build, including component table, radar module notes, audio module notes, power/UPS notes, LED notes, and circuit planning. fileciteturn40file0
- Related detailed doc: `product/old-mvp.md`.
- What was tested or observed:
  - The old MVP was a physical prototype inside a 3D printed case.
  - It used a development-board/module-based architecture rather than a custom PCB.
  - It included a main controller, radar module, audio module, high-power LED/light module, power/battery switching module, LCD screen, joystick, and headboard clamp.
  - It allowed the user to set an alarm locally using the joystick and LCD.
  - It rang at the scheduled alarm time.
  - It used radar to detect whether the user was in bed.
  - If the user remained in bed during alarm time, the alarm continued ringing.
  - If the user left bed, the alarm shut off.
  - If the user got back into bed, the alarm continued or re-triggered.
  - The off button worked outside alarm time but did not work during the alarm period.
  - If unplugged, the device switched to battery power.
  - Founder reported that presence detection was very accurate directionally, including when the user was under a blanket, when the user left bed, and when the user got back into bed.
- What the user/customer said or did:
  - No external tester count, usage count, or user quotes have been documented yet.
  - Current evidence is founder-reported technical/prototype evidence, not yet logged customer validation.
- Claim supported:
  - Orisen's core presence-based wake-completion behavior was physically prototyped.
  - The wake-completion wedge is not purely conceptual.
  - A non-contact radar-based prototype could detect in-bed/out-of-bed state well enough in the reported prototype context to drive alarm continuation/shutoff/re-trigger behavior.
  - The old MVP combined alarm scheduling, local control, radar presence detection, audio/light output, anti-dismiss behavior, and backup power in one physical prototype.
- Claim not supported:
  - This does not prove production reliability.
  - This does not prove the system works across many bedrooms, bed types, sleeping positions, users, pets, partners, blankets, or environmental conditions.
  - This does not prove willingness to pay.
  - This does not prove customer retention or repeated use.
  - This does not prove reduced grogginess or reduced sleep inertia.
  - This does not prove sleep-stage-aware intervention.
  - This does not prove artificial sleep phase transitioning.
  - This does not prove radar-based sleep-stage estimation, breathing extraction, heart-rate extraction, HRV, or RRV.
  - This does not prove manufacturability, regulatory readiness, or consumer-ready reliability.
- Evidence category: Built but not validated; technical prototype evidence; early validation of core wake-completion mechanism if later tester details confirm real-use testing.
- Evidence strength: Level 2 for technical prototype existence and functional demonstration; not yet Level 3 because external tester details, repeated usage, and failure modes are not documented.
- Confidence: Medium for prototype existence and reported behavior; medium-low for general reliability until tester count, testing conditions, and failure cases are documented.
- Limitations:
  - Founder-reported rather than independently documented in this file.
  - No tester count documented yet.
  - No number of mornings/nights documented yet.
  - No raw user quotes documented yet.
  - No failure cases documented yet.
  - No quantitative radar accuracy metrics documented yet.
  - Hardware was a breadboard/module prototype, not a production-intent architecture.
  - Historical notes have a possible controller discrepancy: founder recently described Arduino Nano, while uploaded planning notes mention Arduino Uno R3 in one section.
- Related docs to update:
  - `product/old-mvp.md`
  - `product/claims-and-evidence.md`
  - `product/product-overview.md`
  - `product/roadmap.md`
  - `hardware/hardware-overview.md` if created later
  - `radar-ml/radar-ml-context-map.md` if radar validation details are added
- Notes:
  - This is currently the strongest evidence that the presence-based wake-completion loop has been physically built.
  - This should be used carefully: it supports prototype feasibility, not production reliability or customer validation by itself.

## Claims supported by current evidence

Add supported claims here as evidence improves.

For each supported claim, include:

- the claim
- the evidence category
- the evidence strength
- the evidence source
- limitations

### Orisen showed early organic waitlist interest after one founder LinkedIn post

- Claim: Orisen received meaningful early interest from a single organic founder LinkedIn post and limited external sharing.
- Evidence category: Early signal.
- Evidence strength: Level 1 to Level 2.
- Evidence source: 2026-05-18 waitlist and LinkedIn launch evidence entry.
- Limitations:
  - Does not prove willingness to pay, retention, broad-market demand, product-market fit, or product efficacy.
  - Traffic attribution and exact conversion are imperfect.

### Orisen's landing page/waitlist showed promising early conversion

- Claim: Orisen's early landing page converted about 16% of estimated visitors into waitlist signups under founder-reported tracking assumptions.
- Evidence category: Early signal.
- Evidence strength: Level 1 to Level 2.
- Evidence source: 2026-05-18 waitlist and LinkedIn launch evidence entry.
- Limitations:
  - Estimated total visits rely partly on a pre-Clarity estimate.
  - Waitlist conversion does not prove payment intent or product value after use.

### Orisen's presence-based wake-completion loop was physically prototyped

- Claim: Orisen's core wake-completion loop was physically prototyped using local alarm behavior, radar presence detection, audio/light output, local controls, and battery backup.
- Evidence category: Built but not validated; technical prototype evidence.
- Evidence strength: Level 2.
- Evidence source: 2026-05-18 old MVP prototype evidence entry and `product/old-mvp.md`.
- Limitations:
  - Does not prove production reliability, customer validation, willingness to pay, reduced grogginess, sleep-stage-aware intervention, or broad robustness.
  - External tester details and repeated real-use evidence still need to be documented.

## Claims not yet supported

Add claims here that should remain careful, weakened, or avoided until better evidence exists.

Examples that currently need caution:

- Orisen reduces grogginess.
- Orisen reduces sleep inertia.
- Orisen accurately detects sleep stages.
- Orisen performs proven artificial sleep phase transitioning.
- Orisen improves sleep quality.
- Orisen is clinically proven.
- Orisen has proven willingness to pay.
- Orisen has achieved product-market fit.
- Orisen has proven broad-market demand.
- Orisen has proven production reliability.
- Orisen has proven broad bedroom robustness across many users and environments.

## Notes

- Update this file before strengthening marketing, fundraising, website, or pitch claims.
- If a claim is not clearly supported here, treat it as an assumption, roadmap item, hypothesis, or unsupported claim.
- Do not treat waitlist signups as proof of willingness to pay unless payment, preorder, or strong purchase-intent evidence exists.
- Do not treat a built feature as customer validation unless users have tested it in a relevant context.
