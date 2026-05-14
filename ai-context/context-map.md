# Context Map

## Purpose

This file is the top-level document-routing map for the Orisen master docs repo.

Use it after `ai-context/start-here.md` has handled project, chat, refresh, and handoff routing.

This file does not replace source-of-truth docs. It tells ChatGPT projects and human readers which docs to read for a specific task.

## Preferred entry point

For new Orisen ChatGPT chats, start with:

- `ai-context/start-here.md`

`start-here.md` handles:

- Project routing
- Refresh vs new-chat decisions
- Handoff decisions
- Whether the task belongs in another ChatGPT project

After that routing check, use this file to choose the minimal starting context and any additional task-specific docs.

## GitHub-first context rule

Use `HaseebTron/orisen-master-docs` on GitHub as the source of truth.

Do not assume ChatGPT Project source files are present or current.

For new substantive Orisen chats, read the relevant minimal baseline from GitHub first, then read additional task-specific docs only as needed.

## Context loading rule

Each project has two context levels:

- Minimal baseline: the default starting point for new substantive chats in that project.
- Full reference pack: the maximum recommended pack for broad or high-stakes tasks.

Default workflow:

1. Read the minimal baseline first.
2. Assess the user's task.
3. Read only the additional docs needed for that task.
4. Use the full reference pack only when the task broadly affects product direction, public claims, roadmap, architecture, fundraising, marketing, or cross-domain strategy.

Do not automatically load the full reference pack just because a chat is serious. Load it when the task needs that breadth.

For any important Orisen decision, always include:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

These define current company truth and how to handle conflicts.

## Project context packs

### Orisen General

Use for company strategy, product direction, source-of-truth docs, claims, roadmap priority, cross-domain decisions, and workflow architecture.

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/project-routing.md`
- `ai-context/context-map.md`

Full reference pack:

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

Minimal baseline from this repo:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `software/software-context-map.md`

Full reference pack from this repo:

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

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `radar-ml/radar-ml-context-map.md`

Full reference pack:

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

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `marketing/marketing-context-map.md`
- `marketing/positioning-and-messaging.md`

Full reference pack:

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

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `fundraising/fundraising-context-map.md`
- `fundraising/investor-narrative.md`

Full reference pack:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `validation/evidence-log.md`
- `fundraising/fundraising-context-map.md`
- `fundraising/investor-narrative.md`

Fundraising docs can be ambitious, but must not overclaim beyond product truth and evidence.

### Orisen Hardware

Use for physical product architecture, sensors, enclosure, manufacturing, power, audio, reliability, and hardware tradeoffs.

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

Full reference pack:

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

Start with the Orisen General minimal baseline, then read only the relevant additional docs. Use the Orisen General full reference pack only for broad strategic reviews or major source-of-truth decisions.

Relevant folder context maps may include:

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

- `product/product-context-map.md` if it exists

Important product docs may include:

- `product/product-overview.md`
- `product/mvp-scope.md`
- `product/target-customer.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`

If `product/product-context-map.md` does not exist yet, use the relevant product docs directly.

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

Fundraising can be ambitious, but must not overclaim beyond product truth and evidence.

### Business questions

Use for questions about business model, pricing, market analysis, competitors, GTM assumptions, partnerships, operations, and revenue strategy.

Start with:

- `business/business-context-map.md` if it exists

Important business docs may include:

- `business/business-model.md`
- `business/pricing.md`
- `business/competitors.md`
- `business/market-notes.md`

Business docs may contain assumptions. Separate assumptions from validated facts.

### Hardware questions

Use for questions about physical product architecture, sensors, enclosure, manufacturing, power, audio, reliability, and hardware tradeoffs.

Start with:

- `hardware/hardware-context-map.md` if it exists

Important hardware docs may include:

- `hardware/hardware-overview.md`
- `hardware/sensor-decisions.md`
- `hardware/manufacturing-notes.md`

If hardware docs do not exist yet, use the Orisen Hardware minimal baseline and only add product/roadmap context if needed.

### Software questions

Use for questions about firmware, app, cloud, repo structure, slices, OTA, BLE onboarding, Supabase, and implementation status.

Start with:

- `software/software-context-map.md`

Important implementation docs live in the Orisen Software repo. Follow `software/software-context-map.md` for the exact repo and default entry docs.

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
2. Read the relevant project minimal baseline.
3. Assess the user's task.
4. Read only the additional task-specific docs needed.
5. Use the full reference pack only when the task requires broad context.
6. Read `ai-context/current-state.md` and `ai-context/source-of-truth-rules.md` for any important decision if they were not already included.
7. If docs conflict, apply `ai-context/source-of-truth-rules.md`.
8. If a needed doc does not exist, say so and recommend creating it only if needed.
9. Do not assume old notes or brainstorms are current truth unless promoted into source-of-truth docs.

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
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`
- `ai-context/repo-backlog.md`

Many folder-specific docs may not exist yet. When missing, create them deliberately rather than guessing that they already exist.
