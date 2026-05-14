# Context Map

## Purpose of this file

This file is the top-level document-routing map for the Orisen master docs repo.

Use it to decide which documents to read for a specific question, decision, or project after project/chat routing has been handled.

This file does not replace source-of-truth docs. It points ChatGPT projects and human readers to the right source-of-truth docs.

## Preferred entry point for new ChatGPT chats

For new ChatGPT chats, the preferred first file is:

- `ai-context/start-here.md`

`start-here.md` handles the boot sequence for new and refreshed chats, including:

- Project routing
- Existing-chat checks
- Chat-index checks
- Refresh-vs-new-chat decisions
- Handoff decisions
- Whether the current chat should exist
- Whether the request belongs in another ChatGPT project

After that routing check is complete, `start-here.md` sends the assistant back to this file to route into the correct source-of-truth docs.

## GitHub-first context rule

Use `HaseebTron/orisen-master-docs` on GitHub as the source of truth.

Do not assume ChatGPT Project source files are present or current.

For new serious Orisen chats, read the relevant baseline doc pack below from GitHub, then read additional task-specific docs only as needed.

## Default prompt for new chats

Use this prompt when manually starting a new Orisen chat:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

My question:
[insert question]
```

## Always read for important decisions

For any important Orisen decision, read:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

These define the current company state and how to interpret conflicts between docs.

## Project baseline doc packs

Use these baseline packs after `start-here.md` has handled project/chat routing.

The baseline pack replaces the need to rely on ChatGPT Project source files.

After reading the baseline pack, read any task-specific docs needed for the request.

### Orisen General

Use for company strategy, product direction, source-of-truth docs, claims, roadmap priority, cross-domain decisions, and project/workflow architecture.

Baseline docs:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/project-routing.md`
- `ai-context/context-map.md`
- `ai-context/repo-backlog.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `validation/evidence-log.md`

### Orisen Software

Use for firmware, app, cloud, Supabase, OTA, BLE onboarding, implementation slices, software architecture, and software debugging.

Baseline docs from this repo:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `software/software-context-map.md`

Then read relevant docs from the active software repo if needed, especially active slice docs, architecture docs, decisions, and coding rules.

Software docs describe implementation reality. They should not shrink the full product or company vision.

### Orisen Radar + ML

Use for radar module decisions, signal processing, vital signs, RRV, HRV, movement extraction, sleep-stage modeling, datasets, papers, and intervention-loop experiments.

Baseline docs:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `validation/evidence-log.md`
- `radar-ml/radar-ml-context-map.md`

Escalate to Orisen General before changing public claims around sleep-stage estimation, grogginess reduction, sleep inertia, or artificial sleep phase transitioning.

### Orisen Marketing + GTM

Use for website copy, positioning, messaging, social posts, customer language, waitlist growth, GTM experiments, and launch planning.

Baseline docs:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `validation/evidence-log.md`
- `marketing/marketing-context-map.md`
- `marketing/positioning-and-messaging.md`

Marketing docs must remain downstream from product direction and claims evidence.

### Orisen Fundraising

Use for investor narrative, pitch deck, outreach, traction framing, market story, fundraising strategy, investor FAQ, and investor-specific messaging.

Baseline docs:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `validation/evidence-log.md`
- `fundraising/investor-narrative.md`

Fundraising docs can be ambitious, but must not overclaim beyond product truth and evidence.

### Orisen Hardware

Use for physical product architecture, sensors, enclosure, manufacturing, power, audio, reliability, and hardware tradeoffs.

Baseline docs:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`

Then read hardware-specific docs when they exist, such as:

- `hardware/hardware-context-map.md`
- `hardware/hardware-overview.md`
- `hardware/sensor-decisions.md`
- `hardware/manufacturing-notes.md`

If a hardware context map does not exist yet, say so and recommend creating it only when hardware work becomes frequent enough.

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
- Radar + ML: `radar-ml/radar-ml-context-map.md`

If a folder context map does not exist yet, use the available docs in that folder and recommend creating the missing context map only if the workstream is active enough to justify it.

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

- `marketing/positioning-and-messaging.md`
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

### Radar + ML questions

Use for questions about radar module selection, signal extraction, vital signs, RRV, HRV, movement, sleep-stage modeling, papers, datasets, model validation, and artificial sleep phase transitioning.

Start with:

- `radar-ml/radar-ml-context-map.md`

Important radar/ML docs may include:

- `radar-ml/radar-module-decision.md`
- `radar-ml/vital-signs-pipeline.md`
- `radar-ml/sleep-stage-model.md`
- `radar-ml/intervention-loop.md`
- `radar-ml/research-notes.md`
- `radar-ml/technical-validation.md`

## Routing rules for ChatGPT projects

When using this repo as context after project/chat/refresh/handoff routing:

1. Read this file.
2. Read the relevant project baseline doc pack for the current project/task.
3. Read `ai-context/current-state.md` and `ai-context/source-of-truth-rules.md` for any important decision if they were not already included.
4. Route to the relevant folder context map.
5. Read the specific docs listed there for the task.
6. If docs conflict, apply `ai-context/source-of-truth-rules.md`.
7. If a needed doc does not exist, say so and recommend creating it only if needed.
8. Do not assume old notes or brainstorms are current truth unless promoted into source-of-truth docs.

## Current repo buildout status

The repo is still being built.

The first stable docs are:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `validation/evidence-log.md`

The current routing docs are:

- `ai-context/start-here.md`
- `ai-context/project-routing.md`
- `ai-context/chat-index.md`
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`
- `ai-context/repo-backlog.md`

Many folder-specific docs may not exist yet. When missing, create them deliberately rather than guessing that they already exist.
