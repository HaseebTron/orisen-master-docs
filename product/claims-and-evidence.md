# Claims and Evidence

## Purpose

This file is Orisen's final product and public-claim authority.

Use this file when writing or reviewing:

- product docs
- website copy
- pitch decks
- fundraising language
- social posts
- investor outreach
- customer messages
- app copy
- sales language
- interviews or public explanations

This file answers:

- what Orisen can safely claim today
- what Orisen can claim carefully
- what is only roadmap, hypothesis, or long-term vision
- what wording should be avoided
- what evidence supports each claim
- what the evidence does not prove
- what validation is needed before a stronger claim is allowed

## Authority and role boundary

This file defines final allowed public wording and claim boundaries.

It does not replace:

- [`ai-context/claim-control/claim-control-system.md`](../ai-context/claim-control/claim-control-system.md), which defines evidence categories, evidence-strength levels, and claim-review rules.
- [`ai-context/claim-control/claim-control-log.md`](../ai-context/claim-control/claim-control-log.md), which records conservative claim-relevant evidence entries.
- [`ai-context/claim-control/claim-control-roadmap.md`](../ai-context/claim-control/claim-control-roadmap.md), which tracks missing evidence and validation priorities.
- [`product/ai-powered-sleep-intervention-direction.md`](ai-powered-sleep-intervention-direction.md), which captures the focused long-term platform direction.
- Raw/source files and synthesis files, which preserve and interpret upstream evidence.

When these files overlap:

- Use the claim-control system for classification rules.
- Use the claim-control log for conservative evidence entries.
- Use the claim-control roadmap for missing evidence and validation planning.
- Use this file for final allowed product and public wording.
- Use the AI-powered sleep intervention direction note as supporting strategy context, not as authority to make stronger public claims than this file allows.

## Core rule

Do not let the product story move faster than the evidence.

Orisen can be ambitious, but every claim must separate:

- what is currently validated
- what is an early signal
- what has been built but not fully validated
- what is being built
- what is planned
- what is a hypothesis
- what is long-term vision
- what is unsupported or unsafe

If a claim is not clearly supported, weaken the wording.

If a claim could make a reasonable customer, investor, journalist, or partner think something is already proven, tested, clinically validated, or production-reliable when it is not, rewrite it.

## Evidence status summary

### Strongest current evidence

The strongest current evidence supports presence-based wake completion as Orisen's first wedge.

Current evidence supports a careful version of this idea:

- Some users have a real problem between alarm time, alarm dismissal, and actually being out of bed.
- The old MVP physically demonstrated a wake-completion loop using non-contact presence detection, local alarm behavior, audio/light output, local controls, and battery backup.
- A small old-MVP pilot/test group showed early real-world signal that presence-based wake completion can help users get out of bed closer to alarm time.
- Bypass attempts and failure modes from the old MVP are valuable product evidence because they show that anti-bypass design, local execution, lockout behavior, and backup power matter.

This is early validation, not broad-market proof.

Primary upstream docs:

- [`product/old-mvp/README.md`](old-mvp/README.md)
- [`product/old-mvp/old-mvp.md`](old-mvp/old-mvp.md)
- [`product/old-mvp/old-mvp-test-row-labels.md`](old-mvp/old-mvp-test-row-labels.md)
- [`product/old-mvp/old-mvp-bypass-and-failure-notes.md`](old-mvp/old-mvp-bypass-and-failure-notes.md)
- [`product/old-mvp/old-mvp-user-feedback.md`](old-mvp/old-mvp-user-feedback.md)
- [`ai-context/claim-control/claim-control-log.md`](../ai-context/claim-control/claim-control-log.md)

### Early but limited signals

Orisen also has early signals around:

- customer pain around waking up and getting out of bed
- non-camera sensing as a directionally important privacy boundary
- waitlist and message resonance from a founder-led LinkedIn post
- qualitative tester interest in buying the old MVP
- qualitative user pull for easier wake-up and less-groggy mornings
- expert commentary supporting claim discipline and future validation design
- external waking-up research supporting the problem framing around snoozing, delayed bed exit, oversleeping, and wake-completion friction

These signals are useful for direction. They do not prove product-market fit, broad paid demand, clinical efficacy, sleep-stage accuracy, or physiological outcomes.

Primary upstream docs:

- [`research/customer-interviews/2024-alarm-clock-interviews.md`](../research/customer-interviews/2024-alarm-clock-interviews.md)
- [`marketing/post-performance-log.md`](../marketing/post-performance-log.md)
- [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md)
- [`research/external-research/waking-up/synthesis.md`](../research/external-research/waking-up/synthesis.md)
- [`research/external-research/waking-up/raw-sources-reviewed.md`](../research/external-research/waking-up/raw-sources-reviewed.md)

### Not yet validated

The following are not yet validated enough for strong public claims:

- reduced grogginess
- reduced sleep inertia
- improved morning alertness
- improved cognitive performance after waking
- improved sleep quality
- accurate radar-based sleep-stage estimation
- accurate vital-sign sensing
- sleep-phase-aware wake timing
- waking users in a lighter sleep stage
- moving users from deep sleep toward lighter sleep
- artificial sleep phase transitioning
- personalized wake intervention based on sleep state
- validated voice intervention
- validated conversational sleep coaching
- AI sleep-agent capability
- autonomous sleep intervention or optimization
- production reliability
- broad willingness to pay
- product-market fit
- clinical efficacy

These may appear as careful product direction, roadmap, hypothesis, or long-term vision, but they should not be written as proven outcomes.

## Evidence classification

Use the classification labels from [`ai-context/claim-control/claim-control-system.md`](../ai-context/claim-control/claim-control-system.md):

- Validated
- Early signal
- Built but not validated
- Planned
- Hypothesis
- Long-term vision
- Unsupported or unsafe claim

Do not create a separate evidence scale in this file.

This file applies the claim-control system to Orisen's actual product and public claims.

## Claim matrix

### Product identity

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Product identity | Orisen is a non-contact sleep intervention device. | Safe current claim | "Orisen is a non-contact sleep intervention device for people who struggle to wake up." | N/A | "Medical-grade sleep intervention device." "Sleep-stage control device." | Product strategy and roadmap define Orisen as non-contact and intervention-first rather than passive tracking. | Does not prove efficacy, reliability, clinical value, or market demand. | No validation needed for identity wording, but downstream outcome claims still need evidence. | [`product/product-overview.md`](product-overview.md), [`marketing/positioning-and-messaging.md`](../marketing/positioning-and-messaging.md) |
| Product identity | Orisen is being built as a platform-capable ambient sleep device. | Safe internal/product architecture framing, careful investor use | "Orisen is being built as a platform-capable ambient sleep device, starting with wake completion." | "The hardware foundation creates the bedroom interface; software defines intervention behavior." | "Orisen fixes everything about sleep." "Orisen solves all sleep problems." "All sleep problems become software-only." "Proven sleep platform." "Sleep control platform." | Current-state, product overview, and investor narrative define platform-capable as an architecture direction: sensing, audio, light, compute, connectivity, local control, and app/cloud support where useful. | This is architecture and strategic direction, not proof that future interventions work, that broad sleep improvement is validated, or that every sleep problem can be solved through software. | Validate each future intervention layer with direct technical and user-outcome evidence before stronger product, public, or investor claims. | [`ai-context/current-state.md`](../ai-context/current-state.md), [`product/product-overview.md`](product-overview.md), [`fundraising/investor-narrative.md`](../fundraising/investor-narrative.md) |
| Product identity | Orisen is not primarily a sleep tracker. | Safe current claim | "Orisen is not primarily a sleep tracker. It is built around wake-up intervention." | "Tracking is only valuable when it improves intervention." | "Orisen gives medical-grade sleep analytics." "Orisen replaces PSG or clinical sleep tracking." | Product overview repeatedly separates Orisen from passive sleep dashboards and sleep scores. | Does not prove Orisen can intervene effectively or detect sleep stages accurately. | Future tracking claims need technical validation and user value validation. | [`product/product-overview.md`](product-overview.md) |
| Product identity | Orisen is not a wearable. | Safe current claim | "Orisen gives the core wake-up benefit without requiring a wearable." | N/A | "More accurate than wearables." "Replaces your Oura, WHOOP, Apple Watch, or Fitbit." | Product direction is wall-mounted or room-based non-contact sensing. | Does not prove better accuracy, better adherence, or better outcomes than wearables. | Comparative claims need direct testing against alternatives. | [`product/product-overview.md`](product-overview.md) |
| Product identity | Orisen is currently a consumer product direction, not a medical device. | Safe but legally sensitive claim | "Orisen is being built as a consumer wake-up product, not as a medical device." | "Avoid clinical intended-use claims unless regulatory strategy changes." | "Treats sleep disorders." "Medical-grade." "Clinically improves sleep inertia." | Product docs and expert commentary warn against medical claims. | Does not guarantee regulatory classification. Actual classification depends on claims, features, jurisdictions, and intended use. | Legal/regulatory review before any medical, clinical, diagnostic, or treatment language. | [`product/product-overview.md`](product-overview.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |

### AI-powered sleep intervention platform boundaries

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| AI sleep agents | Future AI sleep-agent support through Orisen. | Long-term vision / future architecture direction | "Future versions may let sleep software or AI agents use Orisen to sense context and act in the bedroom." | "AI sleep agent" means software that can use context, choose an intervention, act through Orisen's audio/light/voice/wake behavior, and adapt based on feedback. | "Orisen has autonomous AI sleep agents." "Orisen's AI fixes your sleep." "AI agents optimize your sleep automatically." | Current-state, product overview, roadmap, and AI direction docs define this as future platform direction. | Does not prove agent capability, decision quality, better sleep outcomes, safety, trust, retention, willingness to pay, or product-market fit. | Working agent prototype, user-permission and override rules, decision/outcome logs, user trust testing, and evidence that agent-driven interventions outperform static routines. | [`ai-context/current-state.md`](../ai-context/current-state.md), [`product/product-overview.md`](product-overview.md), [`product/roadmap.md`](roadmap.md), [`product/ai-powered-sleep-intervention-direction.md`](ai-powered-sleep-intervention-direction.md) |
| Voice intervention | Future voice intervention or conversational support. | Planned / future intervention channel, not validated | "Future versions may use intelligent voice interaction as one intervention channel." | "Voice should support wake completion, bedtime guidance, contextual prompts, explanation, or deliberate override only where useful and trusted." | "Orisen has a proven AI sleep coach." "Orisen talks you into perfect sleep." "Orisen replaces a sleep coach or clinician." | Roadmap and AI direction docs identify voice as a possible output/intervention channel. | Does not prove voice improves wake completion, bedtime behavior, user trust, tolerance, or sleep outcomes. | Prototype voice flows, opt-in/opt-out testing, annoyance/trust/comprehension measures, behavior-change evidence, and comparison against non-voice flows. | [`product/roadmap.md`](roadmap.md), [`product/ai-powered-sleep-intervention-direction.md`](ai-powered-sleep-intervention-direction.md) |
| Vital-sign sensing | Future vital-sign-related sensing. | Future technical direction / not validated for public accuracy claims | "Orisen is exploring non-contact sensing for future vital-sign-related signals." | "Distinguish raw technical capability from validated consumer or clinical accuracy." | "Orisen accurately tracks your vital signs." "Medical-grade heart-rate or breathing data." "Better than wearables for vital signs." "Replaces clinical monitoring." | Product and roadmap docs identify vital-sign-related sensing as possible future technical direction. | Does not prove accuracy, reliability across bedrooms/users/positions/bedding/pets/motion, clinical-grade performance, comparative accuracy, or improved outcomes. | Bench testing against reference sensors, real-bedroom validation across users and nights, error bounds, confidence reporting, and tests across placement, bedding, motion, and distance conditions. | [`product/product-overview.md`](product-overview.md), [`product/roadmap.md`](roadmap.md) |
| Sleep-stage sensing | Future sleep-state or sleep-stage estimation. | Future technical direction / not validated | "Orisen is researching non-contact sensing for future sleep-state estimation." | "Sleep-stage sensing may support personalized wake intervention, but it must not be assumed." | "Accurately detects sleep stages." "Wakes you in the perfect sleep stage." "Always wakes you from light sleep." "Controls sleep stages." "Replaces PSG." | Product, roadmap, expert, and sleep-tracking validation docs support this only as a direction to validate. | Does not prove accurate classification, real-bedroom reliability, correct wake timing, improved wake outcomes, or clinical sleep staging capability. | Labeled sleep-stage data, PSG or appropriate reference validation, real-bedroom testing, accuracy/error metrics with limitations, and outcome testing versus fixed timing. | [`product/roadmap.md`](roadmap.md), [`research/external-research/sleep-tracking-and-validation/synthesis.md`](../research/external-research/sleep-tracking-and-validation/synthesis.md) |
| Autonomous intervention | Future autonomous intervention within user-approved boundaries. | Future direction / hypothesis | "Future versions may autonomously adjust interventions within user-approved boundaries." | "Autonomy should mean controlled adaptation inside safe user-defined boundaries." | "Orisen autonomously optimizes your sleep." "Orisen fixes sleep automatically." "Set it and forget it, Orisen handles your sleep." "Orisen knows better than the user." | Product overview, roadmap, and AI direction docs include autonomy only as future direction. | Does not prove autonomous decisions work, improve sleep/wake outcomes, are safe, are trusted, are non-annoying, or improve retention and willingness to pay. | Defined autonomy boundaries, user permission model, override and failure-mode testing, decision/outcome logs, trust and annoyance testing, and outcome comparison against static/manual routines. | [`product/product-overview.md`](product-overview.md), [`product/roadmap.md`](roadmap.md) |

### Target customer

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Target customer | Orisen is built for people who struggle to wake up. | Safe current claim | "Built for people who struggle to wake up." | "The first customer should be pain-driven, not casual wellness-driven." | "Everyone needs Orisen." "For anyone who sleeps." | Product overview, target-customer doc, old MVP evidence, customer interviews, and waking-up research all support wake-up difficulty as the first problem area. | Does not prove exact ICP, first segment, willingness to pay, or broad demand. | More interviews, beta tests, preorders, and retention data by segment. | [`product/target-customer.md`](target-customer.md), [`research/customer-interviews/2024-alarm-clock-interviews.md`](../research/customer-interviews/2024-alarm-clock-interviews.md) |
| Target customer | The first ICP should be behavioral, not demographic. | Safe internal claim, careful public use | "Orisen is for people whose real problem is getting out of bed, not just setting an alarm." | "Prioritize chronic oversleepers, alarm dismissers, return-to-bed users, and high-consequence wake-up failures before demographic labels." | "Teens are definitively the ICP." "Students are proven as the first market." "Shift workers are the first market." | Expert commentary and target-customer docs identify plausible segments, but current evidence is stronger around behavior than demographics. | Does not prove a final beachhead. Does not support hard age, occupation, gender, or lifestyle conclusions. | Segment-specific interviews, pilots, conversion tests, and paid-intent tests. | [`product/target-customer.md`](target-customer.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |
| Target customer | Severe morning grogginess is a target pain, but not a proven solved outcome. | Careful claim | "Orisen is built for people who struggle with brutal mornings and is being developed toward less-groggy wake-ups." | "Grogginess is part of the customer pain, but reduction is not yet validated." | "Orisen eliminates grogginess." "Orisen fixes sleep inertia." | Users and experts support grogginess as relevant, but experts warn it is multi-cause and not solved by stage-shifting alone. | Does not prove Orisen reduces grogginess, sleep inertia, or improves alertness. | Direct user testing with subjective grogginess measures and ideally objective morning-function measures. | [`product/old-mvp/old-mvp-user-feedback.md`](old-mvp/old-mvp-user-feedback.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |

### Wake-completion wedge

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Wake completion | Presence-based wake completion is the strongest current wedge. | Strongest current evidence, early validation | "Orisen's first wedge is presence-based wake completion: it checks whether you actually got out of bed." | "Guaranteed wake completion wedge." | "Guaranteed to wake you up every time." "You will never oversleep again." | Old MVP physically demonstrated the loop, and small real-use tests showed early wake-completion signal. | Does not prove production reliability, broad robustness, or no-failure wake-ups. | Larger pilot with event logs, real bedrooms, non-friend users, failure-rate tracking, and repeat use over time. | [`product/old-mvp/old-mvp.md`](old-mvp/old-mvp.md), [`product/old-mvp/old-mvp-test-row-labels.md`](old-mvp/old-mvp-test-row-labels.md), [`ai-context/claim-control/claim-control-log.md`](../ai-context/claim-control/claim-control-log.md) |
| Wake completion | Normal alarms can stop before wake completion. | Safe problem-framing claim | "A normal alarm can stop when you tap a button. Orisen is built around whether you actually got out of bed." | "Alarm dismissal is not wake completion." | "Normal alarms do not work for anyone." "All alarm apps are useless." | Old MVP learning, customer interviews, and waking-up external research support the distinction between alarm interaction and actual bed exit. | Does not prove all users need Orisen or that Orisen solves the problem at scale. | More direct interviews and pilot logs showing the alarm-dismissal to bed-exit gap. | [`research/external-research/waking-up/synthesis.md`](../research/external-research/waking-up/synthesis.md), [`research/customer-interviews/2024-alarm-clock-interviews.md`](../research/customer-interviews/2024-alarm-clock-interviews.md) |
| Wake completion | Orisen uses presence detection to determine whether the user left bed. | Built in old MVP, current product direction | "Orisen uses presence detection to help determine whether you actually got out of bed." | "Radar-driven in-bed/out-of-bed state enables the wake-completion loop." | "Orisen detects presence perfectly." "Orisen knows your exact sleep state." | Old MVP used radar-based presence detection to drive alarm behavior. | Does not prove production radar accuracy, multi-bedroom robustness, edge-case performance, sleep-stage detection, or vital-sign accuracy. | Sensor validation in varied bedrooms, bed types, body positions, users, pets, room layouts, and mounting conditions. | [`product/old-mvp/old-mvp.md`](old-mvp/old-mvp.md), [`product/product-overview.md`](product-overview.md) |
| Wake completion | Re-trigger behavior if the user returns to bed is a core product behavior. | Built in old MVP, current product direction | "If you return to bed during the wake window, Orisen can re-trigger the alarm." | "Return-to-bed detection is part of wake completion, not a bonus feature." | "Orisen prevents all return-to-bed behavior." | Old MVP included return-to-bed alarm behavior, and tester feedback showed the urge to return to bed was real. | Does not prove it works for all users or cannot be bypassed. | Logged pilot tests with return-to-bed events, confirmation windows, false positives, and false negatives. | [`product/old-mvp/old-mvp.md`](old-mvp/old-mvp.md), [`product/old-mvp/old-mvp-user-feedback.md`](old-mvp/old-mvp-user-feedback.md) |
| Wake completion | Orisen is designed to make waking up more reliable. | Safe but careful claim | "Orisen is designed to make waking up more reliable by responding to whether you actually leave bed." | "Reliability means alarm execution plus wake completion, not just loud audio." | "Orisen guarantees perfect wake-up reliability." | Product direction and old MVP evidence support the design goal. | Does not prove production reliability, all-user reliability, or guaranteed outcomes. | Reliability testing over many nights, users, power states, Wi-Fi states, sensor edge cases, and alarm-critical scenarios. | [`product/product-overview.md`](product-overview.md), [`product/roadmap.md`](roadmap.md), [`product/old-mvp/`](old-mvp/) |

### Anti-bypass and local reliability

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Anti-bypass | The easiest completion path should be getting out of bed, not bypassing the device. | Product principle supported by old MVP failure modes | "Orisen is designed so the easiest path is getting out of bed." | "Prevent half-asleep bypass without trapping the user." | "Impossible to bypass." "You cannot turn it off." "No escape." | Old MVP bypass/failure notes show users may exploit off buttons, pre-alarm shutoff, unplugging, and other loopholes. | Does not prove final anti-bypass design is robust or user-safe. | Pilot tests that intentionally track bypass attempts and legitimate override use. | [`product/old-mvp/old-mvp-bypass-and-failure-notes.md`](old-mvp/old-mvp-bypass-and-failure-notes.md), [`product/product-overview.md`](product-overview.md) |
| Anti-bypass | A deliberate override path should exist. | Safe product principle | "Orisen should prevent half-asleep bypass while preserving deliberate control for legitimate exceptions." | "Higher-friction override away from bed during alarm-critical windows." | "The user cannot override it." "Traps you until you wake up." | Product overview defines the need to prevent casual bypass without removing user control. | Does not validate a specific override mechanism. | Usability and safety testing of recovery code, QR/NFC card, or other deliberate override methods. | [`product/product-overview.md`](product-overview.md) |
| Local reliability | Final alarm execution should run locally on the device. | Safe current product requirement | "The final wake-up behavior is designed to run locally on the device, without depending on Wi-Fi, cloud, or the phone at the alarm moment." | "Local alarm execution is non-negotiable for trust." | "The product can never fail." "Cloud-free forever." | Product overview and roadmap define local execution as core. Old MVP and engineering MVP direction reinforce this. | Does not prove production reliability or uptime. | Firmware tests, offline tests, power-loss tests, reboot tests, OTA-failure tests, and long-run reliability logs. | [`product/product-overview.md`](product-overview.md), [`product/roadmap.md`](roadmap.md) |

### Old MVP evidence

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Old MVP | The old MVP physically demonstrated the wake-completion loop. | Built but not production-validated | "An early physical prototype demonstrated the core presence-based wake-completion loop." | "The wedge was physically prototyped, not just imagined." | "Production-ready." "Fully validated." "Clinically tested." | Old MVP used a physical device with radar, audio, light, screen, controls, power switching, battery backup, and headboard clamp. | Does not prove manufacturability, production reliability, long-term reliability, or broad robustness. | Production-intent prototype, formal test plan, reliability logs, and real-bedroom pilots. | [`product/old-mvp/old-mvp.md`](old-mvp/old-mvp.md) |
| Old MVP | The small old-MVP pilot showed early wake-completion signal. | Early validation for wake completion | "In early prototype use, the strongest signal was helping users get out of bed closer to alarm time." | "Dennis is the cleanest wake-completion case; other users add directional evidence and failure-mode learning." | "Proven across users." "Validated success rate." "Works for everyone." | A small group used the device in real morning contexts, with the strongest signal around wake and bed-exit timing. | Does not prove exact success rate, broad-market efficacy, production reliability, or paid demand. | Larger pilot with clean baselines, event logs, non-friend users, repeated use, and explicit success criteria. | [`product/old-mvp/old-mvp-test-row-labels.md`](old-mvp/old-mvp-test-row-labels.md), [`ai-context/claim-control/claim-control-log.md`](../ai-context/claim-control/claim-control-log.md) |
| Old MVP | Tester feedback supports wake-completion value. | Early qualitative signal | "Early testers perceived meaningful value in the wake-completion behavior." | "One tester reportedly said he would buy it right now, but this is not paid demand." | "Customers are willing to pay." "Validated price point." "People will buy it." | Founder-reported tester feedback included strong perceived value and one purchase-intent comment. | Does not prove broad willingness to pay, actual purchase behavior, retention, or price. | Deposits, preorders, paid beta, or repeated purchase-intent interviews with cold users. | [`product/old-mvp/old-mvp-user-feedback.md`](old-mvp/old-mvp-user-feedback.md) |
| Old MVP | Old MVP evidence supports the need for an easier-wake-up layer. | Early signal for roadmap need | "Early testing suggested that forced wake completion is valuable, but users may still want the wake-up to feel less brutal." | "Wake completion first, easier wake-up second." | "Old MVP reduced grogginess." "Old MVP fixed sleep inertia." | User feedback indicated interest in artificial sleep phase transitioning or easier wake-up because forced wake completion could still leave users groggy. | Does not prove any grogginess reduction, sleep-inertia reduction, or sleep-stage intervention effect. | Pilot tests measuring subjective grogginess, morning functioning, and tolerance of gradual audio/light. | [`product/old-mvp/old-mvp-user-feedback.md`](old-mvp/old-mvp-user-feedback.md) |

### Customer discovery and demand signals

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Customer discovery | Some people experience repeated wake-up and get-out-of-bed problems. | Early signal | "Customer discovery suggests some people struggle not just with alarms, but with actually getting out of bed." | "Getting out of bed is a distinct pain from waking up for some users." | "Most people have this problem." "This proves the market." | Summer 2024 interviews support repeated wake-up and get-out-of-bed pain patterns, with limitations. | Does not prove market size, segment ranking, willingness to pay, or product-market fit. | More interviews with severe oversleepers, cold users, and people who have paid for wake-up solutions. | [`research/customer-interviews/2024-alarm-clock-interviews.md`](../research/customer-interviews/2024-alarm-clock-interviews.md) |
| Customer discovery | Non-camera sensing is directionally important. | Early signal | "Orisen avoids cameras and uses non-contact sensing instead." | "Camera discomfort appeared enough to support non-camera direction." | "Everyone rejects camera-based sleep products." | Customer interviews and product strategy support avoiding cameras. | Does not prove non-camera sensing alone drives purchase. | User testing around privacy concerns, trust, and willingness to place device in bedroom. | [`research/customer-interviews/2024-alarm-clock-interviews.md`](../research/customer-interviews/2024-alarm-clock-interviews.md), [`product/product-overview.md`](product-overview.md) |
| Demand signal | Waitlist signups show early interest and message resonance. | Early signal | "A founder-led LinkedIn post and limited sharing generated an early waitlist signal." | "66 signups excluding founder/test signup, with about 16% blended conversion and about 22% internal high-intent estimate." | "Validated demand." "Product-market fit." "People are ready to pay." | Post-performance log records LinkedIn metrics, website visits, waitlist signups, and conversion interpretation. | Does not prove paid demand, retention, efficacy, broad market demand, or willingness to pay. | Paid preorder test, beta conversion, waitlist survey, source attribution, and follow-up interviews. | [`marketing/post-performance-log.md`](../marketing/post-performance-log.md), [`ai-context/claim-control/claim-control-log.md`](../ai-context/claim-control/claim-control-log.md) |
| Demand signal | Orisen has an early founder-led organic launch signal. | Careful fundraising claim | "Early organic launch traffic showed promising message resonance around the wake-up problem." | "Use as early traction, not PMF." | "Our launch proved demand." "We have validated the market." | One LinkedIn post and limited external sharing drove signups and engagement. | Does not separate curiosity, friendship network, investor curiosity, or true buyer intent cleanly. | Cleaner campaign tracking, paid tests, preorders, and waitlist-to-interview conversion. | [`marketing/post-performance-log.md`](../marketing/post-performance-log.md) |

### Grogginess, sleep inertia, and easier wake-up

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Easier wake-up | Orisen aims to make mornings feel less brutal. | Careful claim | "Orisen aims to make mornings feel less brutal through gradual audio, light, and future sensor-informed intervention." | "Less brutal mornings are a roadmap/user-outcome goal, not yet proven." | "Orisen eliminates grogginess." "Wake up refreshed every time." | User feedback shows pull for easier wake-up. Product docs include gradual audio/light and future sensor-informed intervention. Experts warn outcomes need testing. | Does not prove reduced grogginess, reduced sleep inertia, improved mood, or improved alertness. | User studies with subjective wake-quality scores, grogginess scales, adherence, and repeated-use data. | [`product/old-mvp/old-mvp-user-feedback.md`](old-mvp/old-mvp-user-feedback.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |
| Grogginess | Orisen reduces grogginess. | Not yet validated | "Orisen is being built toward less-groggy mornings." "Orisen aims to reduce grogginess over time." | "Grogginess reduction is a hypothesis and product goal." | "Reduces grogginess." "Eliminates grogginess." "Wake up without grogginess." | Expert commentary says grogginess is relevant but multi-cause. Old MVP feedback indicates users still wanted an easier wake-up layer. | Does not prove Orisen reduces grogginess. | Direct Orisen-specific user testing, repeated mornings, subjective and objective morning-function measures. | [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md), [`product/old-mvp/old-mvp-user-feedback.md`](old-mvp/old-mvp-user-feedback.md) |
| Sleep inertia | Orisen reduces sleep inertia. | Unsupported for public use, hypothesis internally | "Orisen is exploring ways to make the sleep-to-wake transition less harsh." | "Sleep inertia reduction requires stronger evidence and careful clinical language." | "Clinically improves sleep inertia." "Treats sleep inertia." "Fixes sleep drunkenness." | Expert commentary and waking-up research show sleep inertia is relevant, but current evidence does not validate Orisen-specific improvement. | Does not prove clinical or physiological benefit. Does not prove Orisen treats any condition. | Strong direct testing with appropriate measures; clinical-quality evidence if clinical wording is desired. | [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md), [`research/external-research/waking-up/synthesis.md`](../research/external-research/waking-up/synthesis.md) |
| Gradual audio/light | Gradual audio and light can support the wake-up process. | Built/planned product direction, outcome not validated | "Orisen uses gradual audio and light to support the wake-up process." | "Audio and light are intervention channels to test, not proven outcome mechanisms yet." | "Light alone solves waking up." "Gradual light guarantees easier wake-ups." | Product roadmap includes gradual audio and light. Expert commentary cautions light may not work for users with sleep masks. | Does not prove improved grogginess, sleep-stage shift, or universal effectiveness. | A/B tests of audio/light patterns, user tolerance, sleep-mask cases, and morning outcomes. | [`product/roadmap.md`](roadmap.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |

### Sensor-informed and sleep-phase-aware intervention

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Sensor-informed intervention | Orisen is working toward sensor-informed wake intervention. | Planned/current product direction | "Orisen is working toward sensor-informed wake intervention that uses non-contact sensing to guide the wake-up process." | "Sensor-informed does not mean validated sleep-stage accuracy." | "Orisen knows exactly when you should wake up." | Product overview and roadmap include future sensor-informed intervention. | Does not prove sensors are accurate enough for sleep-stage guidance or that intervention improves outcomes. | Sensor validation, event logging, and user-outcome testing. | [`product/product-overview.md`](product-overview.md), [`product/roadmap.md`](roadmap.md) |
| Sleep-phase-aware intervention | Orisen is working toward sleep-phase-aware wake behavior. | Planned or hypothesis, careful public use | "Orisen is being built toward sleep-phase-aware wake intervention." | "Sleep-phase-aware is a future direction that must be validated." | "Wakes you in the perfect sleep stage." "Always wakes you from light sleep." | Product roadmap and expert commentary support this as a direction worth testing. | Does not prove current sleep-stage detection, timing accuracy, or improved waking outcomes. | PSG or appropriate validation against sleep stages, plus real-world outcome testing. | [`product/roadmap.md`](roadmap.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md), [`research/external-research/sleep-tracking-and-validation/synthesis.md`](../research/external-research/sleep-tracking-and-validation/synthesis.md) |
| Radar sleep-stage estimation | Orisen can accurately detect sleep stages. | Not validated | "Orisen is researching non-contact sensing for future sleep-state estimation." | "Radar/ML validation is required before accuracy claims." | "Accurately detects sleep stages." "Medical-grade sleep staging." "Replaces PSG." | Sleep-tracking/validation synthesis is not yet developed enough and explicitly does not prove Orisen's sleep-stage capability. | Does not prove accuracy, reliability, real-bedroom performance, or clinical validity. | PSG-labeled validation, actigraphy where appropriate, algorithm benchmarks, real-bedroom tests, and error-bound reporting. | [`research/external-research/sleep-tracking-and-validation/synthesis.md`](../research/external-research/sleep-tracking-and-validation/synthesis.md), [`product/roadmap.md`](roadmap.md) |
| Personalized wake timing | Orisen personalizes wake timing based on sleep state. | Planned/hypothesis | "Future versions may personalize wake intervention based on sensed sleep state." | "Personalization is a future direction." | "Orisen wakes you at the optimal time." "Orisen guarantees optimal wake timing." | Product roadmap includes personalization as a later roadmap item. | Does not prove sleep-state detection, correct timing, or improved outcomes. | Sleep-state validation plus user-outcome validation across repeated mornings. | [`product/roadmap.md`](roadmap.md) |

### Artificial sleep phase transitioning

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Artificial sleep phase transitioning | Artificial sleep phase transitioning is a future direction. | Hypothesis / long-term vision | "Orisen is exploring artificial sleep phase transitioning as a future direction for preparing users for wake-up." | "Technically plausible enough to investigate, not validated." | "Orisen controls your sleep stages." "Orisen moves you from deep sleep to light sleep." "Manipulates biology in real time." | Expert commentary suggests the concept is plausible but not simple and likely requires continuous feedback-based intervention. | Does not prove Orisen can do it, that users tolerate it, or that it improves grogginess or wake quality. | PSG-synchronized intervention studies, tolerance testing, real-user outcome testing, and clear safety boundaries. | [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md), [`product/roadmap.md`](roadmap.md) |
| Artificial sleep phase transitioning | A one-time sleep-stage shift is probably insufficient. | Internal claim-discipline insight | Avoid public unless explaining roadmap carefully: "Sleep intervention likely requires feedback over time, not a one-time cue." | "Closed-loop intervention is likely necessary." | "One cue shifts you into light sleep." | Expert commentary says disturbance may temporarily move a person lighter, but they may quickly return to the previous stage. | Does not prove Orisen can maintain or guide sleep state. | Controlled intervention tests with continuous sensing and outcome measurement. | [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |

### External research and problem framing

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| External research | Some wake-ups involve repeated snoozing, delayed bed exit, or oversleeping. | Careful problem-framing support | "External waking-up research supports the idea that some people struggle beyond the first alarm, including repeated snoozing, delayed bed exit, and oversleeping." | "Use external research for problem framing, not Orisen validation." | "Science proves Orisen works." "External research validates Orisen." | Waking-up synthesis reviewed snooze studies, survey sources, and sleep-inertia guardrails. | Does not prove Orisen efficacy, market demand, or improved outcomes. | Orisen-specific user testing and product data. | [`research/external-research/waking-up/synthesis.md`](../research/external-research/waking-up/synthesis.md), [`research/external-research/waking-up/raw-sources-reviewed.md`](../research/external-research/waking-up/raw-sources-reviewed.md) |
| External research | Snoozing is a meaningful behavior pattern in some datasets. | Careful problem-framing claim | "Some studies and surveys show repeated snoozing is a real behavior pattern in specific measured or surveyed groups." | "Use dataset caveats." | "Most people snooze." "Snoozing is always harmful." "Snoozing causes sleep inertia in everyone." | Waking-up synthesis says the strongest processed source is a SleepCycle app-data study, but not a general-population prevalence proof. | Does not prove snoozing is harmful for everyone or that Orisen reduces snoozing. | Direct Orisen user logs showing snooze-like behavior reduction or wake-completion improvement. | [`research/external-research/waking-up/synthesis.md`](../research/external-research/waking-up/synthesis.md) |
| External research | Sleep inertia is relevant but claim-sensitive. | Internal guardrail and careful problem framing | "Sleep inertia is relevant to wake-up difficulty, but Orisen has not validated sleep-inertia reduction." | "Treat sleep inertia as high-risk language." | "Orisen treats sleep inertia." "Orisen fixes sleep drunkenness." | Waking-up synthesis and expert commentary identify sleep inertia as relevant but not Orisen-validated. | Does not prove Orisen reduces or treats sleep inertia. | Direct validation with appropriate subjective and objective measures; clinical-quality evidence for clinical wording. | [`research/external-research/waking-up/synthesis.md`](../research/external-research/waking-up/synthesis.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |
| Market/category research | Market and category evidence can support context only. | Not yet synthesized enough for strong claims | "Sleep tech and alarm categories are relevant context for Orisen." | "Use market reports for context, not wedge validation." | "The market size proves Orisen demand." "Category growth proves PMF." | Market/category synthesis is draft and not yet synthesized. | Does not prove demand, willingness to pay, adoption, or efficacy. | Better source review, primary/reputable market sources, and Orisen-specific demand evidence. | [`research/external-research/market-and-category/synthesis.md`](../research/external-research/market-and-category/synthesis.md) |
| Competitors/substitutes | Competitor evidence can support positioning only after synthesis improves. | Not yet synthesized enough for strong claims | "Orisen should be positioned against alarms, apps, sunrise lamps, wearables, and other wake-up substitutes carefully." | "Competitor reviews can identify gaps, but do not prove Orisen wins." | "Competitors fail everyone." "Orisen is proven better than Alarmy/Hatch/Loftie/Oura/etc." | Competitor synthesis is draft and not yet synthesized. | Does not prove Orisen outperforms existing products. | Structured review synthesis and direct comparative user testing. | [`research/external-research/competitors-and-substitutes/synthesis.md`](../research/external-research/competitors-and-substitutes/synthesis.md) |

### Clinical, medical, and regulatory boundaries

| Claim family | Specific claim | Current status | Allowed public wording | Internal-only wording | Avoid wording | Evidence basis | What the evidence does not prove | Validation needed to upgrade | Upstream docs |
|---|---|---|---|---|---|---|---|---|---|
| Clinical claims | Orisen is clinically proven. | Unsupported and unsafe | Do not use. | N/A | "Clinically proven." "Clinical-grade." "Medical-grade." | No clinical trial or clinical validation exists. | N/A | Clinical-quality validation, regulatory review, and deliberate medical strategy. | [`ai-context/claim-control/claim-control-log.md`](../ai-context/claim-control/claim-control-log.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |
| Disorder claims | Orisen treats sleep disorders. | Unsupported and unsafe | Do not use. | "Stay in consumer wake-up framing unless strategy changes." | "Treats insomnia." "Treats hypersomnia." "Helps narcolepsy." "Treats sleep drunkenness." | Current product is not validated or positioned as a treatment. | N/A | Medical/regulatory strategy, clinician involvement, clinical evidence, and legal review. | [`product/product-overview.md`](product-overview.md), [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |
| Physiological control | Orisen controls sleep stages or manipulates biology. | Unsupported and unsafe | Do not use. | "Long-term intervention hypothesis only." | "Controls sleep stages." "Manipulates biology in real time." "Moves you into light sleep." | Expert commentary supports caution and testing, not current capability. | N/A | PSG-based intervention validation and safety/tolerance evidence. | [`research/expert-commentary/expert-commentary-synthesis.md`](../research/expert-commentary/expert-commentary-synthesis.md) |

## Approved wording library

### Product one-liner

Use:

> Orisen is a non-contact sleep intervention device for people who struggle to wake up.

Also acceptable:

> Orisen is built for people whose real problem is not setting an alarm, but actually getting out of bed.

Avoid:

> Orisen is a medical-grade sleep-stage control device.

> Orisen is a sleep tracker that fixes your sleep.

### Wake-completion wording

Use:

> Orisen uses presence detection to help determine whether you actually got out of bed.

Use:

> Orisen is designed around wake completion, not just alarm dismissal.

Use:

> A normal alarm can stop when you tap a button. Orisen is built around whether you actually left the bed.

Use carefully:

> Orisen helps make sure you actually get out of bed.

Avoid:

> Orisen guarantees you will never oversleep again.

> Orisen guarantees perfect wake-up reliability.

> Orisen is impossible to bypass.

### Reliability wording

Use:

> Orisen is designed to make waking up more reliable by responding to whether you actually leave bed.

Use:

> The final wake-up behavior is designed to run locally on the device, so the alarm-critical moment does not depend on Wi-Fi, the phone, or the cloud.

Avoid:

> Orisen can never fail.

> Orisen always wakes you up.

### Less-brutal-morning wording

Use:

> Orisen aims to make mornings feel less brutal through gradual audio, light, and future sensor-informed intervention.

Use:

> Orisen is being built toward less-groggy wake-ups, but that outcome still needs direct validation.

Avoid:

> Orisen eliminates grogginess.

> Orisen wakes you refreshed every time.

> Orisen fixes sleep inertia.

### Sleep-phase-aware wording

Use:

> Orisen is working toward sleep-phase-aware wake intervention that uses sensor data to guide the wake-up process.

Use:

> Future versions may personalize wake intervention based on sensed sleep state.

Avoid:

> Orisen wakes you in the perfect sleep stage.

> Orisen accurately detects your sleep stage.

> Orisen guarantees optimal wake timing.

### Artificial sleep phase transitioning wording

Use internally:

> Artificial sleep phase transitioning is a long-term hypothesis Orisen is exploring as a future direction.

Public use should be rare and careful. If used publicly, prefer:

> Orisen is exploring future ways to prepare users for wake-up using sensor-informed intervention.

Avoid:

> Orisen controls your sleep stages.

> Orisen moves you from deep sleep to light sleep.

> Orisen manipulates biology in real time.

### AI-powered platform wording

Use carefully:

> Orisen is being built as a hardware foundation for software-defined sleep interventions, starting with wake completion.

Use carefully for future-facing strategy:

> Future versions may let sleep software or AI agents use Orisen to sense context and act in the bedroom.

Avoid:

> Orisen has autonomous AI sleep agents.

> Orisen's AI fixes your sleep.

> AI agents optimize your sleep automatically.

### Voice intervention wording

Use:

> Future versions may use intelligent voice interaction as one intervention channel.

Use:

> Voice may support wake-up dialogue, bedtime guidance, contextual prompts, or deliberate override flows if users trust and value it.

Avoid:

> Orisen has a proven AI sleep coach.

> Orisen's voice assistant fixes your sleep.

> Orisen replaces a sleep coach or clinician.

### Vital-sign and sleep-stage sensing wording

Use:

> Orisen is exploring non-contact sensing for future vital-sign-related and sleep-state-related signals.

Use:

> These sensing directions require validation before accuracy claims are allowed.

Avoid:

> Orisen accurately tracks your vital signs.

> Orisen provides medical-grade heart-rate or breathing data.

> Orisen replaces wearables or PSG.

### Autonomous intervention wording

Use:

> Future versions may autonomously adjust interventions within user-approved boundaries.

Use:

> Autonomous behavior must remain permissioned, transparent, tested, and overrideable.

Avoid:

> Orisen autonomously optimizes your sleep.

> Set it and forget it, Orisen handles your sleep.

> Orisen knows better than the user.

### Investor-safe wording

Use:

> Orisen's strongest current evidence is around presence-based wake completion. The larger vision is sensor-informed sleep intervention, but sleep-stage-aware and grogginess-reduction claims still need validation.

Use:

> Early prototype use and waitlist response suggest a promising wedge around painful wake-up failure, but Orisen still needs stronger evidence around paid demand, retention, production reliability, and physiological outcomes.

Avoid:

> We have proven product-market fit.

> We have clinically validated sleep intervention.

> We can already control sleep stages.

## Avoid wording library

Avoid these claims unless future evidence, regulatory review, and claim-control review explicitly approve them:

- "Eliminates grogginess."
- "Fixes sleep inertia."
- "Clinically improves sleep inertia."
- "Clinically proven."
- "Medical-grade."
- "Treats sleep disorders."
- "Orisen has autonomous AI sleep agents."
- "Orisen's AI fixes your sleep."
- "Orisen has a proven AI sleep coach."
- "Orisen autonomously optimizes your sleep."
- "Orisen accurately tracks vital signs."
- "Medical-grade heart-rate or breathing data."
- "Wakes you in the perfect sleep stage."
- "Accurately detects sleep stages."
- "Controls your sleep stages."
- "Moves you from deep sleep to light sleep."
- "Manipulates biology in real time."
- "Guarantees better sleep."
- "Guarantees you will never oversleep again."
- "Impossible to bypass."
- "Proven product-market fit."
- "Validated demand."
- "Proven willingness to pay."
- "Better than wearables."
- "Replaces wearables."
- "Replaces PSG."

## Validation upgrade map

| Claim to upgrade | Current status | Minimum next evidence | Stronger evidence | Highest-confidence evidence |
|---|---|---|---|---|
| Presence-based wake completion helps users get out of bed closer to alarm time. | Early validation | Pilot with more users, clear baselines, and event logs. | Multi-week beta with non-friend users and repeat-use behavior. | Large real-world dataset with wake-completion rates, return-to-bed rates, bypass rates, and retention. |
| Orisen makes waking up more reliable. | Design claim, early evidence | Real-bedroom reliability tests across many nights and users. | Beta showing lower wake-completion failure versus user baseline. | Production fleet data with low failure rates and strong retention. |
| Orisen reduces return-to-bed behavior. | Early signal and product logic | Logs showing return-to-bed detection and re-trigger behavior. | Pilot showing reduced return-to-bed versus baseline. | Larger cohort with repeated use and persistent behavior change after novelty. |
| Orisen reduces grogginess. | Hypothesis | User-reported grogginess before/after pilot. | Repeated validated scales plus objective morning-function tasks. | Controlled study with meaningful subjective and objective improvements. |
| Orisen reduces sleep inertia. | Unsupported for public use | Internal exploratory testing with careful measures. | Controlled study using accepted sleep-inertia measures. | Clinical-quality validation if clinical language is desired. |
| Orisen accurately detects vital-sign-related signals. | Future technical direction / not validated | Bench testing against reference sensors. | Real-bedroom validation across users, nights, positions, bedding, motion, and placement conditions with error bounds. | Robust consumer or clinical validation with clear limits and appropriate regulatory review for medical wording. |
| Orisen detects sleep stages accurately. | Not validated | Algorithm tested against labeled sleep-stage data. | PSG-comparison validation with clear metrics and limitations. | Robust real-bedroom validation across users and nights with benchmarked accuracy. |
| Orisen performs sleep-phase-aware wake intervention. | Planned/hypothesis | Demonstrate sensor-informed intervention timing in pilot. | Show improved user outcomes versus fixed alarm timing. | Controlled study showing reliable improvement in wake outcomes. |
| Orisen performs artificial sleep phase transitioning. | Long-term hypothesis | Feasibility test with sensing and intervention logs. | PSG-synchronized study showing measurable stage movement or arousal-state effect. | Repeated controlled validation showing outcome improvement and user tolerance. |
| Orisen provides useful voice intervention. | Planned / not validated | Prototype voice flows and opt-in user testing. | Repeated tests showing voice improves wake completion, bedtime behavior, trust, or comprehension versus non-voice flows. | Real-world usage data showing durable behavior improvement, low annoyance, and clear user value. |
| Orisen provides AI sleep-agent capability. | Long-term vision / future architecture direction | Working agent prototype connected to device/app context with logs. | User tests showing safe, trusted, and useful agent decisions inside permissioned boundaries. | Repeated real-world evidence that agent-driven interventions outperform static or manual routines. |
| Orisen performs autonomous intervention. | Future direction / hypothesis | Defined autonomy boundaries, permission model, override rules, and failure-mode tests. | Pilot logs showing autonomous decisions, outcomes, overrides, and user trust. | Controlled or large real-world evidence showing outcome improvement without unacceptable safety, privacy, or annoyance costs. |
| Orisen has willingness to pay. | Early signal only | Structured interviews and price testing. | Deposits, preorders, or paid beta. | Paid retention, repeat purchase, referrals, and low refund rates. |
| Orisen has product-market fit. | Not validated | Strong pilot engagement and repeated usage. | Paid beta retention and referrals. | Sustained growth, retention, paid demand, and repeatable acquisition. |

## Review checklist for future claims

Before approving any public claim, ask:

1. Is this claim about what exists today, what was built in the old MVP, what is being built now, what is planned, or what is long-term vision?
2. Is the evidence Orisen-specific, or only external research?
3. Is the evidence user behavior, paid behavior, technical test data, expert commentary, or secondary research?
4. Would a reasonable reader think this is already proven?
5. Does the wording imply clinical proof?
6. Does the wording imply exact technical accuracy?
7. Does the wording imply guaranteed outcomes?
8. Does the wording imply production reliability?
9. Does the wording imply broad market demand or willingness to pay?
10. Can the claim be rewritten as a safer current claim, careful aim, roadmap item, or hypothesis?

If the answer is unclear, weaken the claim.

## Downstream use rules

### Website and customer-facing copy

Website copy may be emotional and direct, but it must not overclaim.

Good website themes:

- painful mornings
- oversleeping
- sleeping through alarms
- turning alarms off and going back to bed
- actually getting out of bed
- non-contact sensing
- not a wearable
- not a passive sleep tracker
- designed to make waking more reliable
- working toward less brutal mornings
- future software-defined intervention layers, when clearly framed as roadmap

Avoid website claims around:

- clinical sleep inertia improvement
- guaranteed wake-up
- perfect sleep-stage timing
- accurate sleep-stage detection
- accurate vital-sign detection
- validated AI sleep agents
- validated conversational sleep coaching
- autonomous sleep optimization
- artificial sleep phase transitioning as a current capability

### Fundraising language

Fundraising may discuss the larger vision, but must clearly separate wedge evidence from future ambition.

Safe fundraising structure:

1. Current validated wedge: presence-based wake completion.
2. Early evidence: old MVP, pilot/test users, customer interviews, waitlist response.
3. Product architecture direction: platform-capable non-wearable sleep intervention hardware.
4. Larger vision: software-defined sleep interventions, including possible future AI-assisted layers.
5. Validation gap: grogginess, sleep-stage detection, vital-sign sensing, voice intervention, AI-agent capability, autonomous intervention, and artificial sleep phase transitioning still need testing.

Avoid fundraising language that implies:

- clinical validation
- proven sleep-stage control
- proven sleep-inertia reduction
- validated vital-sign sensing
- validated AI sleep agents
- validated conversational coaching
- autonomous sleep optimization
- product-market fit
- paid demand at scale

### Social posts

Social posts can use sharper hooks, but the body must stay claim-safe.

Safe hook direction:

- "The problem is not always waking up. Sometimes it is staying out of bed."
- "A normal alarm stops when you tap it. Orisen is built around whether you actually got out of bed."
- "Sleep trackers tell you what happened. Orisen is being built to change what happens next morning."

Avoid hooks like:

- "We solved sleep inertia."
- "Never oversleep again."
- "We can control your sleep stages."
- "Our AI fixes sleep."
- "We built an autonomous sleep agent."

## Update rules

Update this file when:

- new user testing changes claim strength
- a claim is disproven, weakened, or made riskier by testing
- technical validation changes what can safely be said
- product scope changes the first customer-ready product
- marketing or fundraising needs stronger language and evidence exists to support it
- expert commentary or external research materially changes claim boundaries
- regulatory or clinical strategy changes allowable claims

Preferred update flow:

1. Preserve raw/source material in the relevant source folder.
2. Update `raw-sources-reviewed.md` or synthesis files where applicable.
3. Update [`ai-context/claim-control/claim-control-log.md`](../ai-context/claim-control/claim-control-log.md) if the evidence materially affects claims.
4. Update this file before updating website, fundraising, pitch, social, product, or customer-facing docs.

## Current summary

Orisen can currently claim that it is a non-contact sleep intervention device for people who struggle to wake up.

Orisen's strongest current evidence is presence-based wake completion: using presence detection to help determine whether the user actually got out of bed, with re-trigger behavior if they return to bed.

Orisen can carefully say it is designed to make waking up more reliable and is being built toward less brutal mornings through gradual audio, light, and future sensor-informed intervention.

Orisen may describe a long-term platform direction around software-defined sleep interventions and possible future AI-assisted layers, but wake completion remains the first concrete intervention layer.

Orisen should not yet strongly claim that it eliminates grogginess, reduces sleep inertia, accurately detects vital signs or sleep stages, wakes users in the perfect sleep stage, has validated voice coaching, has validated AI sleep agents, autonomously optimizes sleep, performs validated artificial sleep phase transitioning, improves sleep quality, replaces wearables or PSG, or has clinical proof.
