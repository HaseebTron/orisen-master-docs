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
- Core AI operating behavior

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
- `ai-context/ai-operating-mode.md`

These define current company truth, how to handle conflicts, and how ChatGPT should reason from the docs.

For source-of-truth doc creation or revision, also include:

- `ai-context/doc-creation-rules.md`

For direct GitHub file edits or repo-edit planning, also include:

- `ai-context/repo-governance/repo-editing-rules.md`

For repo structure, repo cleanup, file moves, file inventory, folder organization, or repo-governance work, also include:

- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`

For evidence, validation, product claims, marketing claims, fundraising claims, or technical claim support, also include:

- `ai-context/claim-control/claim-control-system.md`

## Project context packs

### Orisen General

Use for company strategy, product direction, source-of-truth docs, claims, roadmap priority, cross-domain decisions, and workflow architecture.

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/project-routing.md`
- `ai-context/context-map.md`

Full reference pack:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/repo-governance/repo-editing-rules.md`
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- `ai-context/project-routing.md`
- `ai-context/context-map.md`
- `ai-context/repo-governance/repo-backlog.md`
- `ai-context/decision-log.md`
- `product/product-context-map.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `research/research-context-map.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/claim-control/claim-control-system.md`

### Orisen Software

Use for firmware, app, cloud, Supabase, OTA, BLE onboarding, implementation slices, software architecture, and software debugging.

Minimal baseline from this repo:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `software/software-context-map.md`

Full reference pack from this repo:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `software/software-context-map.md`

Then read relevant docs from the active software repo if needed, especially active slice docs, architecture docs, decisions, and coding rules.

Software docs describe implementation reality. They should not shrink the full product or company vision.

If software work creates or changes source-of-truth docs, read `ai-context/doc-creation-rules.md`.

If software work directly edits GitHub files or plans repo edits, read `ai-context/repo-governance/repo-editing-rules.md`.

If software work changes repo structure, docs, context maps, or file organization, read the repo-governance docs:

- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`

If software work affects product claims, validation, reliability promises, or public-facing capability statements, read `ai-context/claim-control/claim-control-system.md`.

### Orisen Radar + ML

Use for radar module decisions, signal processing, vital signs, RRV, HRV, movement extraction, sleep-stage modeling, datasets, papers, and intervention-loop experiments.

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `radar-ml/radar-ml-context-map.md`

Full reference pack:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `research/research-context-map.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/claim-control/claim-control-system.md`
- `radar-ml/radar-ml-context-map.md`

Escalate to Orisen General before changing public claims around sleep-stage estimation, grogginess reduction, sleep inertia, or artificial sleep phase transitioning.

### Orisen Marketing + GTM

Use for website copy, positioning, messaging, social posts, customer language, waitlist growth, GTM experiments, and launch planning.

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `marketing/marketing-context-map.md`
- `marketing/positioning-and-messaging.md`

Full reference pack:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `research/research-context-map.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/claim-control/claim-control-system.md`
- `marketing/marketing-context-map.md`
- `marketing/positioning-and-messaging.md`

Marketing docs must remain downstream from product direction and claims evidence.

Use `ai-context/claim-control/claim-control-system.md` before strengthening public claims.

### Orisen Fundraising

Use for investor narrative, pitch deck, outreach, traction framing, market story, fundraising strategy, investor FAQ, and investor-specific messaging.

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `fundraising/fundraising-context-map.md`
- `fundraising/investor-narrative.md`

Full reference pack:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `research/research-context-map.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/claim-control/claim-control-system.md`
- `fundraising/fundraising-context-map.md`
- `fundraising/investor-narrative.md`

Fundraising docs can be ambitious, but must not overclaim beyond product truth and evidence.

Use `ai-context/claim-control/claim-control-system.md` before framing traction, validation, technical proof, clinical support, or customer demand.

### Orisen Hardware

Use for physical product architecture, sensors, enclosure, manufacturing, power, audio, reliability, and hardware tradeoffs.

Minimal baseline:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`

Full reference pack:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/roadmap.md`
- `research/research-context-map.md`

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
- Research: `research/research-context-map.md`
- Marketing: `marketing/marketing-context-map.md`
- Fundraising: `fundraising/fundraising-context-map.md`
- Business: `business/business-context-map.md`
- Hardware: `hardware/hardware-context-map.md`
- Software: `software/software-context-map.md`
- Radar + ML: `radar-ml/radar-ml-context-map.md`

If a folder context map does not exist yet, use the available docs in that folder and recommend creating the missing context map only if the workstream is active enough to justify it.

### Repo governance, structure, and cleanup questions

Use when the question affects repo purpose, repo organization, source-of-truth structure, file moves, file naming, folder responsibilities, context maps, repo cleanup, or repo integrity.

Start with:

- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/repo-governance/repo-editing-rules.md`

Also include the Orisen General minimal baseline.

For repo edits, remember:

- `ai-context/repo-governance/repo-purpose.md` explains why the repo exists.
- `ai-context/repo-governance/repo-structure.md` explains structural logic and folder responsibilities.
- `ai-context/repo-governance/repo-file-map.md` is the only durable repo-wide file inventory.
- `ai-context/repo-governance/repo-change-checklist.md` is the operational checklist before changing files.

Folder context maps and domain docs should not maintain their own complete file trees. They should reference `ai-context/repo-governance/repo-file-map.md` when the current structure matters.

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

For product claims or validation status, also read:

- `ai-context/claim-control/claim-control-system.md`

For product questions based on research or customer evidence, also read:

- `research/research-context-map.md`

### Research questions

Use for questions about customer interviews, raw research, expert commentary, external research, source review, research synthesis, market/category sources, competitor sources, waking-up research, going-to-sleep research, during-sleep research, sleep tracking and validation research, and evidence interpretation.

Start with:

- `research/research-context-map.md`

Important research areas may include:

- `research/customer-interviews/`
- `research/expert-commentary/`
- `research/external-research/`

Research is input, not automatic source-of-truth. If research affects public claims, product truth, marketing, fundraising, roadmap, or technical feasibility framing, also read:

- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`

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

For public claims, also read:

- `ai-context/claim-control/claim-control-system.md`

For customer language or research-backed messaging, also read:

- `research/research-context-map.md`

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

For validation, traction, market, or technical claims, also read:

- `ai-context/claim-control/claim-control-system.md`

For investor claims based on customer, expert, market, competitor, or external research, also read:

- `research/research-context-map.md`

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

For market, category, competitor, or substitute research, also read:

- `research/research-context-map.md`

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

For claims, evidence, papers, and validation status, also read:

- `ai-context/claim-control/claim-control-system.md`
- `research/research-context-map.md`

## Routing rules for ChatGPT projects

When using this repo as context after project/chat/refresh/handoff routing:

1. Read this file.
2. Read the relevant project minimal baseline.
3. Assess the user's task.
4. Read only the additional task-specific docs needed.
5. Use the full reference pack only when the task requires broad context.
6. Read `ai-context/current-state.md`, `ai-context/source-of-truth-rules.md`, and `ai-context/ai-operating-mode.md` for any important decision if they were not already included.
7. Read `ai-context/doc-creation-rules.md` for source-of-truth doc creation, editing, review, or promotion.
8. Read `ai-context/repo-governance/repo-editing-rules.md` for direct GitHub file edits or repo-edit planning.
9. Read the repo-governance docs for repo structure, cleanup, file organization, or context-map work.
10. Read `ai-context/claim-control/claim-control-system.md` for validation, claims, evidence strength, marketing, fundraising, or technical support questions.
11. If docs conflict, apply `ai-context/source-of-truth-rules.md`.
12. If a needed doc does not exist, say so and recommend creating it only if needed.
13. Do not assume old notes or brainstorms are current truth unless promoted into source-of-truth docs.

## Current repo buildout status

The repo is still being built.

The first stable docs are:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/repo-governance/repo-editing-rules.md`
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- `product/product-context-map.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- `research/research-context-map.md`
- `ai-context/claim-control/claim-control-log.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-roadmap.md`

The current routing and workflow docs are:

- `ai-context/start-here.md`
- `ai-context/project-routing.md`
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`
- `ai-context/repo-governance/repo-backlog.md`
- `ai-context/decision-log.md`

The current repo-governance docs are:

- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`

Many folder-specific docs may not exist yet. When missing, create them deliberately rather than guessing that they already exist.
