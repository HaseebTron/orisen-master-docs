# Decision Log

## Purpose

This file records major Orisen source-of-truth, workflow, product, strategy, and documentation decisions.

It is not a replacement for detailed docs.

Use it to preserve the reasoning behind important decisions so future chats do not lose context or accidentally reverse decisions without noticing.

## How to use this file

Add an entry when a decision affects:

- company truth
- product direction
- target customer
- claims
- evidence standards
- roadmap
- ChatGPT workflow
- project routing
- source-of-truth hierarchy
- major documentation structure
- marketing or fundraising narrative
- cross-domain tradeoffs

Do not log tiny wording edits or temporary drafts.

## Entry format

```markdown
## YYYY-MM-DD — Decision title

Decision:
- [What was decided]

Reason:
- [Why this decision was made]

Impacted docs:
- `[file/path.md]`

Implications:
- [What downstream work should do differently]

Open questions:
- [Any unresolved questions]
```

## 2026-05-18 — Presence-based wake completion remains the first wedge

Decision:
- Orisen's first wedge is presence-based wake completion.
- The alarm should not fully stop until the user physically leaves bed, and it should be able to re-trigger if the user returns to bed.

Reason:
- The current source-of-truth identifies wake-up reliability as the first problem Orisen solves.
- Presence-based wake completion is the most validated early wedge.
- This wedge addresses the core behavioral failure mode of normal alarms: the user can dismiss the alarm while still in bed and go back to sleep.
- It creates a clear difference from phone alarms, generic smart alarms, and passive sleep trackers.

Impacted docs:
- `ai-context/current-state.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `marketing/positioning-and-messaging.md`
- `fundraising/investor-narrative.md`
- `software/p1-overview.md`
- `software/p2-mvp-scope.md`

Implications:
- Product, marketing, fundraising, and software docs should not weaken or bury the wake-completion wedge.
- Early product work should prioritize reliable local alarm execution, presence detection, leaving-bed confirmation, and re-trigger behavior.
- Marketing can confidently explain the wake-completion concept, but should avoid overstating broader claims like eliminating grogginess.

Open questions:
- What reliability standard is required before users trust Orisen as their main alarm?
- Which early customer segment values this wedge enough to pay first?

## 2026-05-18 — Orisen targets painful wake-up users first, not generic sleep optimization users

Decision:
- Orisen should focus first on users with a repeated, painful wake-up problem.
- The first users are not casual sleep-optimization users who mainly want dashboards, sleep scores, or general wellness insights.

Reason:
- The strongest early customer problem is not curiosity about sleep data. It is failing to wake up reliably, oversleeping, sleeping through alarms, going back to bed, and experiencing brutal mornings.
- A narrow pain-driven audience is more likely to understand the product's value than a broad wellness audience.
- This focus protects Orisen from becoming a generic sleep tracker or smart alarm clock.

Impacted docs:
- `ai-context/current-state.md`
- `product/target-customer.md`
- `product/product-overview.md`
- `marketing/positioning-and-messaging.md`
- `fundraising/investor-narrative.md`

Implications:
- Messaging should lead with painful mornings, oversleeping, sleep inertia, and actually getting out of bed.
- Product decisions should be evaluated against whether they help the painful wake-up user, not whether they make Orisen more appealing to casual sleep-data users.
- Future customer research should test which narrow subgroup has the strongest willingness to pay.

Open questions:
- Whether the first paid users are students, early-career professionals, shift workers, biohackers, or another pain-heavy segment.
- What price point this first audience will tolerate.

## 2026-05-18 — Orisen is non-contact and should not become a wearable-first product

Decision:
- Orisen should remain a non-contact sleep intervention device rather than a wearable-first product.

Reason:
- Non-contact sensing is central to the product category and differentiation.
- A wearable-first approach would move Orisen closer to sleep trackers and biometric wearables instead of a dedicated wake-up intervention system.
- The source-of-truth direction emphasizes a wall-mounted or room-based device that uses sensing, local control, audio, and light without requiring the user to wear something to bed.

Impacted docs:
- `ai-context/current-state.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `radar-ml/radar-ml-context-map.md`
- `hardware/hardware-context-map.md` when created
- `marketing/positioning-and-messaging.md`

Implications:
- Radar, sensor placement, hardware architecture, and UX decisions should preserve the non-contact premise where technically feasible.
- Marketing should not frame Orisen as another wearable or sleep tracker.
- Wearables may be used as comparison points, research tools, or validation aids, but should not redefine the core product unless company-level docs are deliberately updated.

Open questions:
- Which radar/sensing approach is reliable enough for the first customer-ready product?
- Whether any temporary external sensor is useful for validation without becoming part of the product promise.

## 2026-05-18 — Orisen should be hardware-led, not app-only

Decision:
- Orisen should remain a hardware-led product rather than an app-only alarm or coaching product.

Reason:
- The core wake-completion wedge depends on detecting whether the user physically leaves bed.
- The product promise depends on local device behavior at the final wake-up moment, not phone-only behavior.
- A phone app alone cannot reliably enforce the central behavior loop without becoming easy to dismiss, disable, or ignore.
- Hardware also enables non-contact sensing, audio/light intervention, and future sensor-informed wake behavior.

Impacted docs:
- `ai-context/current-state.md`
- `product/product-overview.md`
- `product/roadmap.md`
- `software/software-context-map.md`
- `fundraising/investor-narrative.md`

Implications:
- The app is important, but it is not the product by itself.
- Software work should support the device loop: setup, alarm scheduling, sync, status, logging, and updates.
- Fundraising and product docs should be clear that Orisen's defensibility and user promise come from the integrated device system, not just app UX.

Open questions:
- What minimum hardware quality is required for early paid pilots?
- How much hardware complexity can be deferred without weakening the first customer-ready product?

## 2026-05-18 — Engineering MVP should not shrink the first customer-ready product vision

Decision:
- The engineering MVP is a build milestone, not the full product vision.
- Software and MVP scope docs should not redefine Orisen as only local alarm execution, app sync, or wake completion.
- The first customer-ready product should go beyond the engineering MVP where needed to deliver a credible wake-up intervention experience.

Reason:
- The current company truth separates engineering MVP, first customer-ready product, and long-term vision.
- The engineering MVP proves the connected app-device-cloud loop and reliable wake completion.
- The first customer-ready product should also begin delivering the strategic promise of making mornings less brutal through gradual, sensor-informed, or sleep-phase-aware wake behavior if technically feasible.
- Without this distinction, implementation docs could accidentally shrink company strategy.

Impacted docs:
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/roadmap.md`
- `software/p1-overview.md`
- `software/p2-mvp-scope.md`
- `software/software-context-map.md`

Implications:
- MVP implementation docs should be read as implementation reality, not final product positioning.
- If software constraints force a product change, the decision must be escalated to Orisen General and reflected in higher-authority docs.
- Public-facing language should not imply features are built or validated before they are, but should preserve the strategic direction toward wake intervention.

Open questions:
- What is the minimum acceptable version of sensor-informed or sleep-phase-aware wake intervention for the first customer-ready product?
- Which parts can be deferred without making Orisen feel like a normal alarm?

## 2026-05-18 — Grogginess reduction and sleep-phase-aware intervention are strategic but claim-sensitive

Decision:
- Reducing brutal mornings, grogginess, and sleep inertia remains strategically important to Orisen.
- Claims around grogginess reduction, sleep-stage estimation, and artificial sleep phase transitioning must remain careful until validated by relevant testing.

Reason:
- The company direction is sleep intervention, not passive tracking.
- However, the evidence standard requires Orisen to separate validated wake-completion behavior from planned or experimental sleep-phase-aware intervention.
- Overclaiming physiological or sleep-stage outcomes would create marketing, fundraising, credibility, and regulatory risk.

Impacted docs:
- `ai-context/current-state.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `radar-ml/radar-ml-context-map.md`
- `marketing/positioning-and-messaging.md`
- `fundraising/investor-narrative.md`

Implications:
- Safer phrasing should be used until stronger evidence exists, such as "aims to reduce grogginess" or "working toward sensor-informed wake intervention."
- Radar/ML research can guide the technical path but does not automatically validate Orisen's customer-facing claims.
- Evidence must be logged in claim-control docs before public claims are strengthened.

Open questions:
- What real-world test would support a stronger claim about reduced grogginess?
- What level of sleep-stage or sensor accuracy is good enough to improve the wake-up experience?

## 2026-05-16 — AI operating mode added

Decision:
- ChatGPT should act as a non-agreeable, high-context company reasoning partner when working on Orisen.
- The AI should reason from high-level source-of-truth docs downward and treat the user's latest message as a proposal, not as source-of-truth.

Reason:
- Orisen's documentation workflow depends on high-level docs grounding lower-level docs.
- If ChatGPT passively agrees with the user or writes lower-level docs from the latest prompt alone, the documentation hierarchy can become contaminated.
- The company needs AI assistance that protects source-of-truth consistency, evidence discipline, product focus, and claims safety.

Impacted docs:
- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/start-here.md`
- `ai-context/context-map.md`
- `ai-context/source-of-truth-rules.md`

Implications:
- Future Orisen chats should not merely load docs and answer agreeably.
- They should challenge weak, overclaimed, stale, or contradictory requests.
- Lower-level docs should be drafted from higher-level docs, validation evidence, and relevant domain context.

Open questions:
- Whether older docs need metadata blocks added manually over time.
- Whether each folder should later receive a stricter context map and doc template.

## 2026-05-16 — Evidence standard added

Decision:
- Orisen should classify evidence and claims using a shared evidence standard, now enforced through claim-control and product evidence docs.

Reason:
- Orisen's product direction includes validated features, early signals, planned features, technical hypotheses, and long-term vision.
- Without a common evidence standard, marketing, fundraising, and product docs could overstate grogginess reduction, sleep-stage accuracy, or artificial sleep phase transitioning.

Impacted docs:
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `product/claims-and-evidence.md`
- marketing docs
- fundraising docs
- radar/ML docs

Implications:
- Claims should be classified as validated, early signal, built but not validated, planned, hypothesis, long-term vision, or unsupported.
- Public-facing claims should become stronger only when evidence becomes stronger.

Open questions:
- Whether current claim-control log entries should be reformatted to match the current claim-control system.
