# Orisen Current State

## Purpose of this file

This file is Orisen's current operating snapshot and status doc.

Use it to understand what is currently true operationally: current build focus, evidence status, active priorities, constraints, and open questions.

This file is not the highest durable product-direction authority.

For durable product identity, product direction, product architecture, first customer-ready product definition, product principles, and long-term product truth, use:

- `product/product-overview.md`

For related product authority, use:

- `product/roadmap.md` for sequencing and scope
- `product/claims-and-evidence.md` for validation status and claim boundaries
- `product/target-customer.md` for first-customer and beachhead decisions

## Authority boundary

This file governs:

- current operating status
- current build and implementation snapshot at the company level
- current evidence snapshot
- active priorities
- active constraints
- source-of-truth alignment checks

This file does not govern:

- full durable product doctrine
- long-term product architecture by itself
- final customer promise by itself
- roadmap sequencing by itself
- public claim permission by itself
- first-customer or beachhead decisions by itself

If this file appears to conflict with `product/product-overview.md` on durable product identity, direction, architecture, or long-term product truth, treat `product/product-overview.md` as the product authority and update this file so the operating snapshot is aligned.

Do not use current build status to reduce Orisen to only what is currently implemented.

## Current operating snapshot

- **Current product identity, in brief**:
  - Orisen is a non-contact sleep intervention device for people who struggle to wake up.
  - Durable product identity and product direction live in `product/product-overview.md`.

- **Current first wedge**:
  - The first wedge remains presence-based wake completion.
  - The alarm should not fully stop merely because the user taps a button or dismisses an app notification.
  - The product should detect whether the user physically got out of bed and can re-trigger if the user returns to bed during the wake window.

- **Current customer focus, in brief**:
  - Orisen is currently focused on people with painful wake-up failure: oversleeping, sleeping through alarms, dismissing alarms while half-asleep, returning to bed, or struggling to actually get out of bed.
  - Detailed customer, ICP, and beachhead truth lives in `product/target-customer.md`.

- **Current product direction, by reference**:
  - Orisen is not primarily a sleep tracker.
  - Orisen should not be reduced to a generic smart alarm clock.
  - Orisen is being built toward active sleep intervention, starting with the wake-up problem and moving toward broader ambient sleep intelligence over time.
  - The durable version of this direction is in `product/product-overview.md`.

## Current build and evidence snapshot

- **Near-term build focus**:
  - Finish the engineering MVP.
  - Prove the connected app-device-cloud loop.
  - Make local alarm execution and wake completion reliable.
  - Build a basic first version of gradual audio/light wake behavior.
  - Keep implementation scope from accidentally redefining the full product direction.

- **Strongest current evidence**:
  - Presence-based guaranteed wake completion remains the strongest current evidence and the most validated early wedge.
  - The current evidence supports wake-up reliability and true bed-exit behavior more strongly than it supports broad sleep improvement, clinical sleep-inertia reduction, sleep-stage accuracy, or validated grogginess reduction.

- **Evidence boundary**:
  - Current evidence should be treated as early validation, not proof of broad-market demand, production reliability, clinical efficacy, sleep-stage accuracy, broad sleep improvement, or product-market fit.
  - Product and public claims must follow `product/claims-and-evidence.md` and the claim-control docs.

## Current active priorities

- Finish the engineering MVP.
- Prove the connected app-device-cloud loop.
- Make guaranteed wake completion reliable.
- Preserve local device reliability for the alarm-critical moment.
- Build a basic first version of gradual audio/light wake behavior.
- Begin testing sensor-informed or sleep-phase-aware wake intervention carefully where technically feasible.
- Collect evidence from early users.
- Keep claims matched to what has actually been validated.
- Keep the product focused on painful wake-up problems, not generic sleep tracking.

## Current constraints

- **Product direction constraint**:
  - Product direction should remain grounded in `product/product-overview.md`.
  - This status doc should not become a roadmap, a full product doctrine file, or a duplicate product overview.

- **MVP constraint**:
  - The engineering MVP proves the connected product loop.
  - The MVP does not define the whole company vision or full first customer-ready product.
  - Implementation docs can describe build reality, but they do not shrink durable product truth unless product source-of-truth docs are deliberately updated.

- **Claims constraint**:
  - Orisen can confidently say it is being built to solve wake-up reliability and work toward less brutal mornings.
  - Stronger outcome claims must match evidence.
  - Grogginess reduction, sleep inertia reduction, sleep-stage-aware intervention, artificial sleep phase transitioning, vital-sign accuracy, sleep-stage accuracy, and broad sleep improvement remain claim-sensitive until validated.

- **Customer focus constraint**:
  - The early customer profile should remain narrow and pain-driven.
  - Orisen should not dilute into generic sleep wellness before the painful wake-up use case is solved.
  - First-customer and beachhead decisions should follow `product/target-customer.md`.

## Open questions

- Which early customer segment has the strongest willingness to pay?
- How strong is real-world demand beyond early signups and interest?
- What reliability standard is required before users trust Orisen as their main alarm?
- Which features are necessary for the first paid users versus later roadmap?
- What parts of the product should remain local on-device versus cloud-assisted?
- How reliably can radar detect the signals needed for sensor-informed or sleep-phase-aware wake intervention?
- What level of sleep-stage accuracy is useful enough to improve the wake-up experience?
- Can early intervention reduce perceived grogginess in real user testing?
- Which claims will be supported by early user data?
- What is the right path from wake completion device to broader ambient sleep intelligence?

## Current positioning summary

- **Operating summary**:
  - Orisen is currently focused on reliable wake completion for people with painful wake-up problems.
  - The strongest current evidence is presence-based wake completion.
  - The near-term work is to finish the engineering MVP, prove reliability, and collect stronger evidence.

- **Product truth reference**:
  - Use `product/product-overview.md` for durable product direction.
  - Use `product/roadmap.md` for sequencing and scope.
  - Use `product/claims-and-evidence.md` for claim boundaries.
  - Use `product/target-customer.md` for first-customer and beachhead decisions.
