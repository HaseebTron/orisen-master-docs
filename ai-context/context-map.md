# Context Map

## Purpose of this file

This file is the top-level routing map for the Orisen master docs repo.

Use it to decide which documents to read for a specific question, decision, or project.

This file does not replace source-of-truth docs. It points ChatGPT projects and human readers to the right source-of-truth docs.

## Always read first

For any important Orisen decision, start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

These define the current company state and how to interpret conflicts between docs.

## Global routing

### Company-level strategy questions

Use when the question affects product, market, business model, fundraising, positioning, or multiple teams.

Start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

Then route to the relevant folder context map:

- Product: `product/product-context-map.md`
- Marketing: `marketing/marketing-context-map.md`
- Fundraising: `fundraising/fundraising-context-map.md`
- Business: `business/business-context-map.md`
- Hardware: `hardware/hardware-context-map.md`
- Software: `software/software-context-map.md`

If a folder context map does not exist yet, use the available docs in that folder and recommend creating the missing context map.

### Product questions

Use for questions about what Orisen is, what it should build, what the customer promise is, what the product should not become, and what belongs in the first customer-ready product.

Start with:

- `product/product-context-map.md`

Important product docs may include:

- `product/product-overview.md`
- `product/mvp-scope.md`
- `product/target-customer.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`

### Marketing questions

Use for questions about positioning, messaging, customer language, founder-led content, content strategy, launch, GTM, waitlist growth, and platform-specific plans.

Start with:

- `marketing/marketing-context-map.md`

Important marketing docs may include:

- `marketing/marketing-strategy.md`
- `marketing/customer-language.md`
- `marketing/content-pillars.md`
- `marketing/gtm.md`
- `marketing/linkedin-playbook.md`
- `marketing/x-playbook.md`
- `marketing/tiktok-playbook.md`
- `marketing/instagram-playbook.md`
- `marketing/reddit-research.md`

Marketing docs must remain downstream from product direction and claims evidence.

### Fundraising questions

Use for questions about investor narrative, pitch deck, outreach, traction framing, market story, fundraising strategy, and investor-specific messaging.

Start with:

- `fundraising/fundraising-context-map.md`

Important fundraising docs may include:

- `fundraising/investor-narrative.md`
- `fundraising/pitch-deck-notes.md`
- `fundraising/traction.md`
- `fundraising/outreach-strategy.md`

Fundraising docs can be ambitious, but must not overclaim beyond product truth and evidence.

### Business questions

Use for questions about business model, pricing, market analysis, competitors, GTM assumptions, partnerships, operations, and revenue strategy.

Start with:

- `business/business-context-map.md`

Important business docs may include:

- `business/business-model.md`
- `business/pricing.md`
- `business/competitors.md`
- `business/market-notes.md`

Business docs may contain assumptions. Separate assumptions from validated facts.

### Hardware questions

Use for questions about physical product architecture, sensors, enclosure, manufacturing, power, audio, reliability, and hardware tradeoffs.

Start with:

- `hardware/hardware-context-map.md`

Important hardware docs may include:

- `hardware/hardware-overview.md`
- `hardware/sensor-decisions.md`
- `hardware/manufacturing-notes.md`

### Software questions

Use for questions about firmware, app, cloud, repo structure, slices, OTA, BLE onboarding, Supabase, and implementation status.

Start with:

- `software/software-context-map.md`

Important software docs may include:

- `software/README.md`
- copied docs from `orisen-software/docs/`

Software docs describe implementation reality. They should not shrink the full product or company vision.

## Routing rules for ChatGPT projects

When using this repo as context:

1. Read this file first.
2. Read `ai-context/current-state.md` and `ai-context/source-of-truth-rules.md` for any important decision.
3. Route to the relevant folder context map.
4. Read the specific docs listed there for the task.
5. If docs conflict, apply `ai-context/source-of-truth-rules.md`.
6. If a needed doc does not exist, say so and recommend creating it.
7. Do not assume old notes or brainstorms are current truth unless promoted into source-of-truth docs.

## Default prompt for new chats

Use this repo as the source of truth for Orisen. Start by reading `ai-context/context-map.md`, then follow its routing instructions for my task. If the task affects major product, marketing, fundraising, business, software, or hardware decisions, also read `ai-context/current-state.md` and `ai-context/source-of-truth-rules.md` before answering.

## Current repo buildout status

The repo is still being built.

The first stable docs are:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`

Many folder-specific docs may not exist yet. When missing, create them deliberately rather than guessing that they already exist.
