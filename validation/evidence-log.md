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
- A small old-MVP pilot/test group used the device in real morning contexts, with the strongest signal around getting users out of bed closer to the alarm time.
- Founder-reported tester feedback says users felt the old MVP was much better at waking them on time than their previous/default wake-up behavior.

### Early demand and messaging signal

- Orisen received 66 waitlist signups excluding the founder/test signup after one founder LinkedIn post and limited external sharing.
- Estimated total website visits were about 415, implying about 16% blended visitor-to-waitlist conversion.
- Current internal high-intent / relevant-traffic conversion estimate is about 22%.
- Later lower-intent incremental conversion from 2026-02-08 to 2026-05-18 was about 6%.
- The 22% number should be treated as a directional estimate for relevant early launch traffic, not as a universal site conversion rate.
- This is an early signal of problem/message resonance, not proof of willingness to pay, retention, product-market fit, or clinical/technical efficacy.
- Dennis expressed that he would buy the old MVP “right now,” likely around a roughly $100 discussed price point. This is an early one-person willingness-to-pay signal, not validated pricing.

### Needs more evidence

- Reduced grogginess
- Reduced sleep inertia
- Sleep-phase-aware wake intervention
- Artificial sleep phase transitioning
- Radar-based sleep-stage estimation
- Willingness to pay beyond one tester statement
- First customer segment
- Price point
- Reliability standard required for users to trust Orisen as a main alarm
- More exact old-MVP failure-mode labels and bug details

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

### 2026-05-18 — Old MVP qualitative tester feedback showed wake-completion value and easier-wake-up pull

- Evidence type: Qualitative tester feedback / founder-reported user conversation notes.
- Source:
  - Founder-provided memory and notes from old MVP tester conversations.
  - Related detailed doc: `product/old-mvp-user-feedback.md`.
- Participants:
  - Old MVP testers, including Dennis and other early tester/friends.
- What was tested or observed:
  - Testers used or discussed the old MVP after seeing how it affected their wake-up behavior.
  - Founder reports that testers expressed the old MVP was much better at helping them wake up on time compared with their normal/default wake-up behavior.
  - Founder reports that Dennis said he would buy it “right now” during the old MVP period.
  - Founder believes the discussed price at the time may have been around $100.
  - Founder reports that he mentioned artificial sleep phase transitioning and easier wake-up concepts to testers.
  - Testers expressed interest in those future features, especially Dennis.
  - The reason was that the old MVP could wake users and force wake completion, but could still leave them groggy or affected by sleep inertia.
- What the user/customer said or did:
  - Dennis expressed immediate purchase interest, according to founder memory.
  - Testers expressed that the old MVP was much better at waking them on time than before, according to founder memory.
  - Testers expressed pull for an easier/gentler wake-up feature direction because forced wake-up did not fully solve grogginess or sleep inertia.
- Claim supported:
  - Early testers perceived meaningful wake-completion value from the old MVP.
  - One tester expressed early purchase intent, likely around a roughly $100 discussed price point.
  - There is early qualitative user pull for the roadmap layer beyond forced wake completion: making wake-up feel less groggy or less brutal.
  - The old MVP revealed a two-layer product need: wake completion first, easier wake-up second.
- Claim not supported:
  - This does not prove broad willingness to pay.
  - This does not validate a $100 price point.
  - This does not prove paid demand, because no payment/preorder is documented.
  - This does not prove product-market fit.
  - This does not prove reduced grogginess or reduced sleep inertia.
  - This does not prove artificial sleep phase transitioning works.
  - This does not prove sleep-stage detection or sleep-stage-aware intervention.
  - This does not prove that cold customers would respond the same way as founder-connected testers.
- Evidence category:
  - Early validation / qualitative pilot feedback for wake-completion value.
  - Early signal for willingness to pay.
  - Hypothesis with early user pull for easier wake-up / artificial sleep phase transitioning.
- Evidence strength:
  - Level 2 to early Level 3 for wake-completion value when combined with old MVP tables.
  - Level 1 to Level 2 for willingness-to-pay signal.
  - Level 1 to Level 2 for easier wake-up / artificial sleep phase transitioning demand.
- Confidence: Medium for directional qualitative learning; lower for exact price sensitivity because the price was only discussed and not paid.
- Limitations:
  - Founder-reported memory rather than direct written quotes, except where written tester comments already exist elsewhere.
  - Small sample.
  - Testers were connected to the founder.
  - No actual purchase, preorder, or deposit documented.
  - The old MVP did not technically validate artificial sleep phase transitioning.
  - The old MVP could still leave users groggy, so grogginess reduction remains unvalidated.
- Related docs to update:
  - `product/old-mvp-user-feedback.md`
  - `product/claims-and-evidence.md`
  - `product/product-overview.md`
  - `marketing/positioning-and-messaging.md`
  - `fundraising/investor-narrative.md`
  - `validation/validation-roadmap.md` when created
- Notes:
  - Use this as support for the positioning hierarchy: lead with guaranteed wake completion, then explain easier wake-up / grogginess reduction as the next claim-sensitive layer.
  - Do not use this as proof that artificial sleep phase transitioning works.
  - Do not use this as proof that customers will pay $100 without further purchase evidence.

### 2026-05-18 — Old MVP pilot/test users showed early wake-completion signal

- Evidence type: Small prototype pilot / real-use morning test logs.
- Source:
  - Founder-provided old MVP pilot/test data for founder, Hamza/Humza, Dennis, and Sabeeh.
  - Uploaded tester instruction sheet defining bed time, alarm time, wake-up time, get-out-of-bed time, sleepy rating, irritation rating, mood rating, energy rating, and comments. fileciteturn42file0
- Related detailed doc: `product/old-mvp.md`.
- Participants:
  - Founder: university student, self-test.
  - Hamza/Humza: university student, friend; tested during Ramadan and finals while sleeping about 4 hours/day.
  - Dennis: university student, friend; logged multi-day morning data and written comments.
  - Sabeeh: working full time, friend; logged several dates and found a bug that allowed alarm shutoff on some days.
- What was tested or observed:
  - A small group used the old MVP in real morning contexts.
  - Dennis's usual baseline was waking at 8:30 but not getting out of bed until 10:00.
  - On Dennis's logged successful alarm days, wake-up and get-out-of-bed times matched or were very close to the alarm time.
  - Dennis wrote: "Every single day, I really want to get back in bed but I can’t. So my only option is to take a shower, which I’m not happy about doing. But after about a minute in the shower, I wake up completely."
  - Hamza/Humza's usual baseline was alarm at 4:00, wake at 4:50, and get out of bed at 5:00.
  - Several Hamza/Humza logged days show wake-up and get-out-of-bed within a few minutes of the alarm time, including one day where the blue light woke him up.
  - Some Hamza/Humza days show sleeping again or waking/getting out of bed much later.
  - Sabeeh's usual baseline was alarm at 5:30, wake at 6:30, and get out of bed at 9:00.
  - Sabeeh's data was mixed and included bug/failure days.
  - Founder reports that Sabeeh found a bug that allowed him to shut off the alarm on some days, and that excluding those bug days he woke on time.
- What the user/customer said or did:
  - Dennis's comment directly describes wanting to get back in bed but being unable to, then taking a shower and waking up completely after about a minute.
  - Hamza/Humza's table includes a note that blue light woke him up on one day.
  - Sabeeh wrote on one day that he did not wake up to the alarm and thought he slept through it, with volume 3 and duration 15.
- Claim supported:
  - The old MVP showed early real-world signal for the presence-based wake-completion mechanism.
  - Preventing the user from staying in bed or returning to bed can force or strongly encourage getting out of bed closer to the alarm time.
  - The strongest outcome signal from the old MVP is wake completion / getting out of bed, not subjective sleep quality.
  - The old MVP was used by multiple people beyond the founder.
  - Blue light may have contributed to waking in at least one logged case.
- Claim not supported:
  - This does not prove broad production reliability.
  - This does not prove paid demand or willingness to pay.
  - This does not prove retention or long-term behavior change.
  - This does not prove broad-market demand.
  - This does not prove clinical efficacy.
  - This does not prove reduced grogginess or reduced sleep inertia as a validated outcome.
  - This does not prove better mood or energy as a validated outcome.
  - This does not prove sleep-stage-aware intervention, artificial sleep phase transitioning, or radar-based sleep-stage estimation.
  - This does not prove that the device worked every time, because the logs include alarm failure, sleeping again, and bug/failure days.
- Evidence category: Early validation / small prototype pilot signal.
- Evidence strength: Level 2 to early Level 3 for the wake-completion mechanism; not Level 3+ for production reliability, broad robustness, paid demand, or physiological outcomes.
- Confidence: Medium for directional wake-completion signal; lower for exact success rate because some rows are incomplete, bug days are not fully labeled, and data is self-reported.
- Limitations:
  - Small sample size.
  - Convenience sample of founder and friends.
  - Self-reported data.
  - Not a controlled study.
  - Some rows are blank or incomplete.
  - Some days had alarm failure, sleeping again, or bugs.
  - Sabeeh's bug days need to be labeled precisely before computing success rate.
  - No payment or preorder evidence.
  - No production-intent device.
  - No clinical or physiological measurement.
- Related docs to update:
  - `product/old-mvp.md`
  - `product/claims-and-evidence.md`
  - `product/product-overview.md`
  - `product/roadmap.md`
  - `marketing/positioning-and-messaging.md`
  - `fundraising/investor-narrative.md`
- Notes:
  - This is one of the strongest pieces of evidence for Orisen's first wedge.
  - It should be used carefully as early prototype/pilot validation of wake completion, not as proof of product-market fit or production reliability.
  - Future analysis should label valid/invalid days and compute success metrics separately for each tester.

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
    - about 16% blended visitor-to-waitlist conversion using 66 signups / 415 estimated total website visits
    - about 22% current internal high-intent / relevant-traffic conversion estimate
    - about 6% later lower-intent incremental conversion estimate from 2026-02-08 to 2026-05-18
- Intermediate tracking notes:
  - By 2026-02-04 at about 6:45 PM, the post had about 4.1k impressions, 85 likes, 34 comments, 29 signups, and about 68 estimated website visits before Clarity was active.
  - By 2026-02-06 at about 2:00 AM, the post had about 10.5k impressions, 50 signups, about 222 estimated website visits, and about 23% estimated conversion.
  - By 2026-02-08, the founder estimated about 274 total website visits, using about 206 Clarity-recorded visits plus about 68 pre-Clarity visits, with 57 signups and about 21% estimated conversion.
  - From 2026-02-08 to 2026-05-18, signups increased from 57 to 66 while estimated visits increased from 274 to 415, implying about 6.4% incremental conversion.
- What the user/customer said or did:
  - Users signed up for the waitlist after viewing the website.
  - LinkedIn users engaged with the post through likes, comments, sends, saves, and link visits.
- Claim supported:
  - Orisen has an early signal of interest from a founder-led organic launch post.
  - The wake-up problem and/or Orisen's early positioning were compelling enough for some visitors to join a waitlist.
  - A single organic LinkedIn post can generate meaningful early awareness and waitlist interest for Orisen.
  - The website showed promising early visitor-to-waitlist conversion under founder-reported tracking assumptions.
  - Early/relevant launch traffic appears to have converted meaningfully better than later lower-intent or stale traffic.
- Claim not supported:
  - This does not prove willingness to pay.
  - This does not prove broad-market demand.
  - This does not prove product-market fit.
  - This does not prove retention or repeated usage.
  - This does not prove that Orisen reduces grogginess or sleep inertia.
  - This does not prove sleep-stage-aware intervention, artificial sleep phase transitioning, radar-based sleep-stage estimation, or clinical efficacy.
  - This does not prove that the LinkedIn post alone caused all signups, because there was limited external sharing and likely some direct/unknown traffic.
  - This does not prove that the website universally converts at 22% across all traffic sources and intent levels.
- Evidence category: Early signal.
- Evidence strength: Level 1 to Level 2.
- Confidence: Medium for signups, LinkedIn metrics, and broad direction of interest; medium-low for exact website conversion because total visits rely partly on a pre-Clarity estimate and different analytics tools do not measure traffic identically.
- Limitations:
  - Waitlist signup is not the same as payment, preorder, usage, or retention.
  - Traffic attribution is imperfect because LinkedIn, Microsoft Clarity, direct traffic, and external sharing are separate measurement sources.
  - The audience was likely influenced by the founder's network and may not represent broader cold-market demand.
  - The landing page and post may have selected for people interested in startups, hardware, or the founder rather than only people with severe wake-up pain.
  - No evidence here measures whether users would trust Orisen as their primary alarm or pay for it.
  - The 22% high-intent number is a directional internal estimate, not a universal conversion claim.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `fundraising/investor-narrative.md`
  - `marketing/positioning-and-messaging.md`
  - `product/target-customer.md` if signup source or customer profile details become available
- Notes:
  - This evidence can be used carefully in fundraising and marketing as an early demand/message-resonance signal.
  - It should not be described as product validation, paid demand, clinical evidence, or proof of broad product-market fit.
  - Use three conversion views: about 22% for internal high-intent/relevant traffic estimate, about 16% for conservative blended historical conversion, and about 6% for later lower-intent incremental conversion.

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
  - This is the blended historical conversion number, not the high-intent internal estimate.

### Relevant early launch traffic appears to have converted around 22% to waitlist

- Claim: Early/relevant launch traffic appears to have converted around 22% to the waitlist under current internal interpretation.
- Evidence category: Early signal.
- Evidence strength: Level 1 to Level 2.
- Evidence source: 2026-05-18 waitlist and LinkedIn launch evidence entry, including early conversion snapshots and LinkedIn-link-visit directional calculation.
- Limitations:
  - Directional internal estimate.
  - Not a universal site conversion rate.
  - Not cleanly attributable to one source.
  - Does not prove paid demand or willingness to pay.

### Orisen's presence-based wake-completion loop was physically prototyped

- Claim: Orisen's core wake-completion loop was physically prototyped using local alarm behavior, radar presence detection, audio/light output, local controls, and battery backup.
- Evidence category: Built but not validated; technical prototype evidence.
- Evidence strength: Level 2.
- Evidence source: 2026-05-18 old MVP prototype evidence entry and `product/old-mvp.md`.
- Limitations:
  - Does not prove production reliability, customer validation, willingness to pay, reduced grogginess, sleep-stage-aware intervention, or broad robustness.
  - External tester details and repeated real-use evidence still need to be documented.

### Orisen's old MVP showed early pilot signal for wake completion

- Claim: In a small old-MVP pilot/test group, the presence-based wake-completion mechanism showed early signal for getting users out of bed closer to the alarm time.
- Evidence category: Early validation / small prototype pilot signal.
- Evidence strength: Level 2 to early Level 3.
- Evidence source: 2026-05-18 old MVP pilot/test evidence entry and `product/old-mvp.md`.
- Limitations:
  - Small convenience sample of founder/friends.
  - Self-reported data.
  - Some rows incomplete.
  - Some days had failure, bugs, or sleeping again.
  - Does not prove production reliability, willingness to pay, broad robustness, sleep-stage-aware intervention, or physiological outcomes.

### One old MVP tester expressed immediate purchase intent

- Claim: One old MVP tester, Dennis, expressed that he would buy the device immediately, likely around a roughly $100 discussed price point.
- Evidence category: Early signal.
- Evidence strength: Level 1 to Level 2.
- Evidence source: 2026-05-18 old MVP qualitative tester feedback entry and `product/old-mvp-user-feedback.md`.
- Limitations:
  - Founder-reported memory.
  - One tester connected to founder.
  - No actual payment, preorder, or deposit documented.
  - Does not validate a $100 price point or broad willingness to pay.

### Old MVP testers expressed pull for easier wake-up beyond forced wake completion

- Claim: Old MVP testers wanted the wake-up experience to feel easier/less groggy in addition to being forced to wake up.
- Evidence category: Hypothesis with early user pull.
- Evidence strength: Level 1 to Level 2.
- Evidence source: 2026-05-18 old MVP qualitative tester feedback entry and `product/old-mvp-user-feedback.md`.
- Limitations:
  - Does not prove artificial sleep phase transitioning works.
  - Does not prove reduced grogginess or reduced sleep inertia.
  - Supports roadmap direction, not validated efficacy.

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
