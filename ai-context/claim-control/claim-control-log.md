# Claim Control Log

## Purpose

This file tracks conservative, claim-relevant evidence entries for Orisen.

Use it when evidence affects what Orisen can safely claim in product, marketing, fundraising, radar/ML, hardware, software, or public-facing material.

This file should not duplicate all raw data. Raw data belongs in the relevant source folders.

## Relationship to source files

For raw evidence, go to the source folders:

- Customer interviews: `research/customer-interviews/`
- Old MVP / pilot evidence: `product/old-mvp/`
- Marketing traffic and waitlist evidence: `marketing/post-performance-log.md`
- Expert commentary: `research/expert-commentary/`
- External research: `research/external-research/`

For claim classification rules, use:

- `ai-context/claim-control/claim-control-system.md`

For final public claim boundaries, use:

- `product/claims-and-evidence.md`

## Evidence entry template

```markdown
### [YYYY-MM-DD] [Short evidence title]

- Evidence type:
- Source:
- What was tested or observed:
- What the user/customer/expert/source said or did:
- Claim supported:
- Claim not supported:
- Evidence category:
- Evidence strength:
- Confidence:
- Limitations:
- Related docs to update:
- Notes:
```

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

### Expert commentary signal

- Leila Jalali suggested artificial sleep phase transitioning sounds technically possible, but likely requires ongoing feedback-based intervention rather than a one-time shift.
- Leila Jalali cautioned that grogginess and sleep inertia are multi-cause and should not be claimed as solved by sleep-stage shifting alone.
- Benji Ozynski emphasized that Orisen's algorithm and intervention hypothesis must be tested empirically because sleep is unpredictable.
- Benji Ozynski suggested temperature and actigraphy as areas to investigate, and noted light may not affect users who wear sleep masks.
- Expert commentary is useful for claim discipline and validation design, but does not validate Orisen efficacy or market demand.

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
- PSG/actigraphy validation design
- Competitor review failure modes
- Reddit/forum customer language

## Evidence entries

### 2026-05-18 — Waitlist signups from one LinkedIn post and limited external sharing

- Evidence type: Website/waitlist and social post performance.
- Source: `marketing/post-performance-log.md`.
- What was tested or observed:
  - A single founder LinkedIn post and limited external sharing drove early attention to the Orisen website/waitlist.
  - Microsoft Clarity started after the site had already received about 68 visits and 29 signups.
  - Reported final known LinkedIn post metrics included about 23.4k impressions, 197 likes, 69 comments, 296 LinkedIn-reported link visits from the post, 13 sends, and 6 saves.
  - Waitlist result was 66 signups excluding the founder/test signup.
  - Estimated total website visits were about 415.
- Claim supported:
  - Orisen has an early signal of interest from a founder-led organic launch post.
  - The wake-up problem and/or early positioning were compelling enough for some visitors to join a waitlist.
  - Early/relevant launch traffic appears to have converted meaningfully better than later stale or curiosity traffic.
- Claim not supported:
  - This does not prove willingness to pay, broad-market demand, product-market fit, retention, product efficacy, reduced grogginess, sleep-stage intervention, or clinical validity.
- Evidence category: Early signal.
- Evidence strength: Level 1 to Level 2.
- Confidence: Medium for signups and broad interest; medium-low for exact conversion because traffic attribution and pre-Clarity visits are imperfect.
- Limitations:
  - Waitlist signup is not payment.
  - Traffic came through founder-led social context.
  - Attribution across LinkedIn, Clarity, direct visits, and external sharing is imperfect.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `marketing/positioning-and-messaging.md`
  - `fundraising/investor-narrative.md`

### 2026-05-18 — Old MVP demonstrated radar-based wake-completion loop

- Evidence type: Technical prototype evidence / old MVP evidence.
- Source: `product/old-mvp/old-mvp.md`.
- What was tested or observed:
  - The old MVP was a physical prototype inside a 3D printed case.
  - It used a development-board/module-based architecture rather than a custom PCB.
  - It included a main controller, radar module, audio module, high-power LED/light module, power/battery switching module, LCD screen, joystick, and headboard clamp.
  - It allowed the user to set an alarm locally.
  - It used radar to detect whether the user was in bed.
  - If the user remained in bed during alarm time, the alarm continued ringing.
  - If the user left bed, the alarm shut off.
  - If the user got back into bed, the alarm continued or re-triggered.
  - If unplugged, the device switched to battery power.
- Claim supported:
  - Orisen's core presence-based wake-completion behavior was physically prototyped.
  - The wake-completion wedge is not purely conceptual.
  - A non-contact radar-based prototype could detect in-bed/out-of-bed state well enough in the reported prototype context to drive wake-completion logic.
- Claim not supported:
  - This does not prove production reliability, broad robustness, paid demand, reduced grogginess, sleep-stage intervention, artificial sleep phase transitioning, or radar-based sleep-stage estimation.
- Evidence category: Built but not validated; technical prototype evidence; early validation of core wake-completion mechanism when combined with tester data.
- Evidence strength: Level 2.
- Confidence: Medium for prototype existence and reported behavior; lower for general reliability.
- Limitations:
  - Founder-reported.
  - No production-intent hardware.
  - No quantitative radar accuracy metrics.
  - No clinical or physiological measurement.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `product/product-overview.md`
  - `product/roadmap.md`

### 2026-05-18 — Old MVP pilot/test users showed early wake-completion signal

- Evidence type: Small prototype pilot / real-use morning test logs.
- Source:
  - `product/old-mvp/old-mvp.md`
  - `product/old-mvp/old-mvp-test-row-labels.md`
  - `product/old-mvp/old-mvp-bypass-and-failure-notes.md`
  - `product/old-mvp/old-mvp-user-feedback.md`
- Participants:
  - Founder
  - Hamza/Humza
  - Dennis
  - Sabeeh
- What was tested or observed:
  - A small group used the old MVP in real morning contexts.
  - Dennis's usual baseline was waking at 8:30 but not getting out of bed until 10:00.
  - On Dennis's successful logged days, wake-up and get-out-of-bed times matched or were very close to the alarm time.
  - Dennis wrote that he wanted to get back in bed but could not, so his only option was to take a shower, after which he woke up completely.
  - Hamza/Humza's usual baseline was alarm at 4:00, wake at 4:50, and get out of bed at 5:00.
  - Several Hamza/Humza logged days show wake-up and get-out-of-bed within a few minutes of alarm time.
  - Sabeeh's data included bug/failure days, including a pre-alarm shutoff loophole.
- Claim supported:
  - The old MVP showed early real-world signal for the presence-based wake-completion mechanism.
  - Preventing the user from staying in bed or returning to bed can force or strongly encourage getting out of bed closer to the alarm time.
  - The strongest outcome signal is wake completion / getting out of bed, not subjective sleep quality.
- Claim not supported:
  - This does not prove broad production reliability, paid demand, broad robustness, reduced grogginess, sleep-stage-aware intervention, or physiological outcomes.
- Evidence category: Early validation / small prototype pilot signal.
- Evidence strength: Level 2 to early Level 3 for wake completion.
- Confidence: Medium for directional wake-completion signal; lower for exact success rate because data is small and some rows are incomplete or bug-affected.
- Limitations:
  - Small convenience sample of founder and friends.
  - Self-reported data.
  - Not controlled.
  - Some rows incomplete.
  - Some days had failure, bugs, or sleeping again.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `product/product-overview.md`
  - `marketing/positioning-and-messaging.md`
  - `fundraising/investor-narrative.md`

### 2026-05-18 — Old MVP qualitative tester feedback showed wake-completion value and easier-wake-up pull

- Evidence type: Qualitative tester feedback / founder-reported user conversation notes.
- Source: `product/old-mvp/old-mvp-user-feedback.md`.
- What was tested or observed:
  - Testers expressed that the old MVP was much better at helping them wake up on time compared with their normal/default wake-up behavior.
  - Dennis said he would buy it “right now,” according to founder memory.
  - The discussed price at the time may have been around $100.
  - Testers expressed interest in artificial sleep phase transitioning / easier wake-up features because forced wake completion could still leave them groggy.
- Claim supported:
  - Early testers perceived meaningful wake-completion value.
  - One tester expressed early purchase intent.
  - There is early qualitative user pull for a roadmap layer beyond forced wake completion.
  - The old MVP revealed a two-layer product need: wake completion first, easier wake-up second.
- Claim not supported:
  - This does not prove broad willingness to pay, a $100 price point, product-market fit, reduced grogginess, artificial sleep phase transitioning, or sleep-stage detection.
- Evidence category:
  - Early validation / qualitative pilot feedback for wake-completion value.
  - Early signal for willingness to pay.
  - Hypothesis with early user pull for easier wake-up.
- Evidence strength:
  - Level 2 to early Level 3 for wake-completion value when combined with old MVP tables.
  - Level 1 to Level 2 for willingness-to-pay signal.
  - Level 1 to Level 2 for easier wake-up / artificial sleep phase transitioning demand.
- Confidence: Medium for directional qualitative learning; lower for exact price sensitivity.
- Limitations:
  - Founder-reported memory.
  - Small sample.
  - Testers were connected to the founder.
  - No actual payment, preorder, or deposit documented.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `product/product-overview.md`
  - `marketing/positioning-and-messaging.md`

### 2026-05-19 — Leila Jalali expert commentary on wake difficulty, sleep inertia, and sleep-stage intervention

- Evidence type: Expert commentary / sleep expert meeting notes.
- Source:
  - `research/expert-commentary/raw/leila-jalali-meeting-notes.md`
  - `research/expert-commentary/expert-commentary.md`
- What was observed or discussed:
  - Artificial sleep phase transitioning sounded technically possible, but likely requires continuous disturbance/intervention to keep a person in a lighter stage.
  - Disturbance may temporarily move a patient into a lighter sleep stage before they quickly shift back.
  - Grogginess cannot be eliminated simply by shifting sleep stage.
  - Sleep inertia is partly related to waking from deep sleep, but also influenced by sleep quality, REM, deep sleep, and sleep timing.
  - N1 and REM were described as better phases to wake from.
  - Sleep spindles and arousal difficulty were suggested as research topics.
- Claim supported:
  - Sleep-stage intervention is a technically plausible direction worth investigating.
  - A one-time sleep-stage shift is probably insufficient.
  - Grogginess and sleep inertia are multi-cause problems, so Orisen should keep claims careful.
  - Teens/young adults and shift workers are plausible segments to investigate further.
- Claim not supported:
  - This does not prove Orisen can perform artificial sleep phase transitioning, reduce grogginess, reduce sleep inertia, detect sleep stages, keep users in lighter sleep, or deliver clinical efficacy.
- Evidence category: Expert commentary / early external validation / claim-discipline input.
- Evidence strength: Level 1 to Level 2.
- Confidence: Medium for qualitative claim-discipline implications; low for off-the-cuff percentages and population-level segment conclusions.
- Limitations:
  - Founder-written notes, not transcript.
  - One expert / one clinic perspective.
  - Off-the-cuff estimates should not be treated as population-level statistics.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `product/target-customer.md`
  - `product/roadmap.md`
  - `research/external-research/research-papers/`
  - `radar-ml/radar-ml-context-map.md`

### 2026-05-19 — Benji Ozynski expert commentary on empirical validation, PSG pathway, and intervention uncertainty

- Evidence type: Expert commentary / sleep doctor meeting notes / potential research-validation lead.
- Source:
  - `research/expert-commentary/raw/benji-ozynski-meeting-notes.md`
  - `research/expert-commentary/benji-ozynski-synthesis.md`
  - `research/expert-commentary/expert-commentary.md`
- What was observed or discussed:
  - He emphasized that Orisen's algorithm and intervention hypothesis must be tested empirically.
  - He cautioned that even if the mechanism makes sense theoretically, it may not work in real life because sleep is unpredictable.
  - He suggested temperature may help with transitioning sleep phase.
  - He recommended looking into actigraphy watches as useful measurement tools.
  - He noted that many sleep-focused people wear masks to bed, so light-based intervention may not work for all users.
  - Founder notes say full overnight PSG analysis at his clinic was discussed at about $250.
  - Founder notes say he / the clinic were open to research-level validation and that he may be interested in deeper involvement.
- Claim supported:
  - Sleep-stage-aware intervention, grogginess reduction, and artificial sleep phase transitioning should be treated as empirical hypotheses.
  - PSG validation may be a possible future validation path if confirmed.
  - Actigraphy may be worth investigating for early measurement and validation design.
  - Temperature should be added to the intervention-research backlog.
  - Light should not be treated as the only reliable intervention channel.
- Claim not supported:
  - This does not prove Orisen efficacy, sleep-stage detection, reduced grogginess, reduced sleep inertia, clinical validation, formal partnership, formal advisor status, or market demand.
- Evidence category: Expert commentary / early external validation / claim-discipline input / validation-design input.
- Evidence strength: Level 1 to Level 2 for direction and claim discipline; potential Level 2 collaboration signal if reconfirmed in writing.
- Confidence: Medium for qualitative claim-discipline and validation-design usefulness; medium-low for collaboration/advisor signal until reconfirmed.
- Limitations:
  - Founder-written notes, not transcript.
  - Some content came from an AI-generated meeting summary and should be treated carefully.
  - Clinic validation opportunity, PSG price, and deeper involvement interest need written confirmation.
- Related docs to update:
  - `product/claims-and-evidence.md`
  - `product/target-customer.md`
  - `product/roadmap.md`
  - `research/external-research/research-papers/`
  - `radar-ml/radar-ml-context-map.md`

## Supported claim summary

### Strongest claim today

Orisen has early evidence that presence-based wake completion can help people get out of bed closer to their alarm time.

Use wording like:

> Orisen uses presence detection to help make sure you actually get out of bed.

Avoid wording like:

> Orisen guarantees you will never oversleep.

### Safe current product framing

Orisen is a non-contact sleep intervention device for people who struggle to wake up.

### Careful current framing

Orisen aims to make mornings less brutal through gradual audio, light, and future sensor-informed wake intervention.

### Roadmap / hypothesis framing

Orisen is exploring artificial sleep phase transitioning and sleep-phase-aware wake intervention, but these are not yet validated.

## Claims not yet supported

Do not strongly claim:

- Orisen eliminates grogginess.
- Orisen eliminates sleep inertia.
- Orisen accurately detects sleep stages.
- Orisen wakes users in the perfect sleep stage.
- Orisen controls sleep stages.
- Orisen is clinically proven.
- Orisen treats sleep disorders.
- Orisen improves sleep quality.
- Orisen has validated broad paid demand.

## Next evidence to add

- Research paper synthesis around sleep inertia, arousal threshold, sleep stages, light/audio/temperature intervention, and actigraphy/PSG validation.
- Reddit/forum synthesis around severe wake-up pain language.
- Competitor review synthesis around substitute failures.
- More direct customer interviews with severe wake-up sufferers.
- Better next-prototype logs with event-level wake-completion behavior.
- Written confirmation of any expert collaboration/advisor/research-validation opportunity.