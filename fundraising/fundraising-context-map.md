# Fundraising Context Map

## Purpose of this file

This file is the routing map for the `fundraising/` folder.

Use it to decide which fundraising docs to read for investor narrative, pitch deck, outreach, traction framing, market story, investor FAQ, fundraising strategy, and investor-specific messaging.

This file does not replace fundraising source-of-truth docs. It points readers and ChatGPT projects to the right fundraising docs.

## File inventory rule

This file does not maintain this folder's file inventory.

For the current repo-wide file map, see:

- `ai-context/repo-file-map.md`

This context map should define task-based reading paths, not duplicate folder structure or current/planned file inventories.

## Always read first

For important fundraising work, start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `fundraising/investor-narrative.md`

Fundraising can be ambitious, but it must stay downstream from product truth, evidence, roadmap reality, and claims boundaries.

## Fundraising folder role

The `fundraising/` folder defines:

- Investor narrative
- Pitch deck structure and messaging
- Traction framing
- Fundraising outreach
- Warm intro messages
- Investor-specific positioning
- Investor FAQ
- Fundraising risks and open questions
- Market story and wedge framing

Fundraising docs should explain the size and ambition of Orisen without implying that unvalidated capabilities are already proven.

## Mid-chat context expansion

If a fundraising chat later asks a more specific fundraising question than the initial baseline docs covered, expand context inside the same chat instead of rerunning the full boot workflow.

Before answering, read this context map and the most relevant task-specific docs below.

State which extra files were read when the context expansion is meaningful.

If a fundraising question changes product truth, public claims, roadmap, or target customer strategy, escalate to Orisen General.

## Fundraising docs and when to use them

### Investor narrative

Use for questions like:

- What is the investor story?
- How should Orisen be framed to investors?
- What is the wedge?
- How should the long-term vision be explained?
- What is built versus planned versus risky?

Read:

- `fundraising/investor-narrative.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `ai-context/claim-control/claim-control-system.md`

### Pitch deck

Use for questions like:

- What should the deck structure be?
- What should each slide say?
- How should the problem, solution, traction, market, product, and ask be framed?
- How do we make the deck clear without overclaiming?

Read:

- `fundraising/pitch-deck-notes.md` if it exists
- `fundraising/investor-narrative.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `business/business-context-map.md` if market, pricing, or business model matters

### Traction framing

Use for questions like:

- How should waitlist traction be framed?
- What traction is credible?
- What does current user interest prove or not prove?
- How should conversion, signups, posts, or pilots be presented?

Read:

- `fundraising/traction.md` if it exists
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`
- `fundraising/investor-narrative.md`
- `marketing/marketing-context-map.md` if the traction came from marketing activity

Important rule:

Do not inflate traction. Separate interest, signup intent, pilot usage, retention, willingness to pay, and revenue.

### Investor outreach

Use for questions like:

- What should I email an investor?
- How should I ask for an intro?
- How should I follow up?
- How should I tailor the message to angels, VCs, operators, or sleep/hardware people?

Read:

- `fundraising/outreach-strategy.md` if it exists
- `fundraising/investor-narrative.md`
- `marketing/positioning-and-messaging.md`
- `ai-context/claim-control/claim-control-system.md` if mentioning traction or validation
- `ai-context/claim-control/claim-control-log.md` if prior claim decisions matter

### Investor FAQ and objections

Use for questions like:

- How should I answer investor objections?
- What are the biggest risks?
- How should I explain radar/ML feasibility?
- How should I explain why this is not just an alarm clock?
- How should I discuss hardware risk?

Read:

- `fundraising/investor-faq.md` if it exists
- `fundraising/investor-narrative.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `radar-ml/radar-ml-context-map.md` if radar/ML feasibility matters
- `software/software-context-map.md` if software progress matters
- `hardware/hardware-context-map.md` if hardware readiness matters

### Market and business story

Use for questions like:

- What market is Orisen in?
- How should the market opportunity be framed?
- Is this sleep tech, consumer AI hardware, wellness, or something else?
- What is the pricing or business model story?

Read:

- `business/business-context-map.md` if it exists
- `fundraising/investor-narrative.md`
- `product/product-overview.md`
- `product/target-customer.md`

If a referenced doc does not exist yet, use the available upstream docs and recommend creating the missing doc only if the task requires it.

## Fundraising interpretation rules

- Fundraising is downstream from product truth and claims evidence.
- Do not imply that roadmap items are already built.
- Do not imply that unvalidated claims are proven.
- Do not overstate clinical, medical, or sleep-stage claims.
- Do not reduce Orisen to just a smart alarm clock.
- The strongest wedge is presence-based wake completion.
- The long-term vision is active sleep intervention, but it must be framed carefully until evidence improves.
- Investor language can be ambitious, but the built/validated/planned/risky distinction must stay clear.

## Default fundraising framing

Unless a newer source-of-truth file says otherwise, Orisen fundraising should frame the company as:

A consumer sleep hardware company building a non-contact sleep intervention device, starting with the painful wedge of wake-up reliability through presence-based wake completion, and expanding toward sensor-informed, personalized sleep intervention over time.
