# Product Context Map

## Purpose of this file

This file is the routing map for the `product/` folder.

Use it to decide which product docs to read for a specific product question, product decision, customer promise, feature priority, or roadmap discussion.

This file does not replace product source-of-truth docs. It points readers and ChatGPT projects to the right product docs.

## File inventory rule

This file does not maintain this folder's file inventory.

For the current repo-wide file map, see:

- `ai-context/repo-file-map.md`

This context map should define task-based reading paths, not duplicate folder structure or current/planned file inventories.

## Always read first

For important product work, start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`

These define the current company state, interpretation rules, and core product definition.

## Product folder role

The `product/` folder defines:

- What Orisen is as a product
- What Orisen is not
- The first customer problem
- The first wedge
- The difference between engineering MVP, first customer-ready product, and long-term vision
- Target customer and beachhead segments
- Product claims and evidence boundaries
- Feature priorities and roadmap logic
- Product principles and tradeoffs

Product docs should guide marketing, fundraising, business strategy, and customer-facing claims.

## Product docs and when to use them

### Product definition and category

Use for questions like:

- What is Orisen?
- Is Orisen a smart alarm clock, sleep tracker, wearable, or something else?
- How should the product category be described?
- What makes Orisen different?

Read:

- `product/product-overview.md`
- `ai-context/current-state.md`

### MVP vs first customer product

Use for questions like:

- What is in the engineering MVP?
- What should be in the first customer-ready product?
- What is later roadmap?
- Are we over-scoping or under-scoping the first version?

Read:

- `product/product-overview.md`
- `product/mvp-scope.md` if it exists
- `software/` implementation docs if the question depends on build status

Important rule:

The engineering MVP does not define the whole product vision. The first customer-ready product should go beyond the MVP where needed to deliver a credible customer promise.

### Target customer and beachhead

Use for questions like:

- Who is Orisen for first?
- Which customer segment should we target?
- Should we focus on students, professionals, shift workers, biohackers, or another segment?
- Which users have the strongest pain and willingness to pay?

Read:

- `product/target-customer.md`
- `ai-context/current-state.md`
- `product/product-overview.md`
- `marketing/customer-language.md` if it exists

### Claims, evidence, and validation

Use for questions like:

- Can we claim Orisen reduces grogginess?
- Can we claim sleep-stage detection works?
- Can we say guaranteed wake-up?
- What claims are safe for marketing or fundraising?
- What is validated versus planned?

Read:

- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`

Important rule:

If a claim is not supported by evidence, weaken the wording. Do not let marketing or fundraising imply more than the product, claims, and claim-control docs support.

### Roadmap and feature priority

Use for questions like:

- What should we build next?
- Which features belong in v1?
- What can wait?
- How should sleep-phase-aware intervention be sequenced?
- What tradeoffs should we make between reliability, intelligence, app polish, and hardware capability?

Read:

- `product/roadmap.md`
- `product/product-overview.md`
- `product/mvp-scope.md` if it exists
- `software/software-context-map.md` if implementation reality matters
- `hardware/hardware-context-map.md` if hardware constraints matter

### User experience and product behavior

Use for questions like:

- What should the wake-up flow feel like?
- How should the alarm escalate?
- How should the app explain Orisen?
- How should the product handle returning to bed?
- How should gradual audio/light behavior work?

Read:

- `product/product-overview.md`
- `product/user-experience.md` if it exists
- `software/` docs if behavior is already implemented

If a referenced doc does not exist yet, use the available upstream docs and recommend creating the missing doc only if the task requires it.

## Product interpretation rules

- Product docs are downstream from `ai-context/current-state.md`.
- Product docs are upstream of marketing, fundraising, and business docs.
- Product docs should not overclaim what has been validated.
- MVP scope should not shrink the first customer-ready product vision.
- Long-term vision should not be confused with what exists today.
- If product docs conflict with software docs, software docs usually define implementation reality, while product docs define desired product direction.
- If product docs conflict with claims/evidence docs, evidence wins for public claims.

## Default product framing

Unless a newer source-of-truth file says otherwise, Orisen should be framed as:

A non-contact sleep intervention device for people who struggle to wake up, with a first wedge around presence-based wake completion and a strategic direction toward gradual, sensor-informed, sleep-phase-aware wake intervention to make mornings less brutal.