# Repo File Map

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-21
Governing docs:
- `ai-context/repo-purpose.md`
- `ai-context/repo-structure.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/context-map.md`
Downstream docs:
- Folder context maps
- Repo cleanup tasks
- Repo integrity checks

## Purpose

This file is the central inventory of the Orisen master docs repo.

It lists the current folder and file structure at a practical level so that other docs do not need to duplicate file trees.

For the logic behind the structure, use `ai-context/repo-structure.md`. For what the repo is meant to do, use `ai-context/repo-purpose.md`.

## File map rule

This is the only durable place where the repo-wide file inventory should be maintained.

Folder context maps, folder overview docs, and domain docs should not maintain their own complete file trees. They should reference this file when the current structure matters.

## Maintenance rule

Update this file when:

- a durable file is created
- a durable file is deleted
- a durable file is renamed
- a durable file is moved
- a new folder is created
- a folder's purpose changes

Do not update this file for tiny temporary scratch files unless they become durable docs.

## Current top-level structure

```text
ai-context/
product/
marketing/
fundraising/
software/
radar-ml/
hardware/
business/
```

Some folders may be partially built or planned. If a listed folder does not yet contain stable docs, treat it as a planned or emerging domain until populated.

## `ai-context/`

Purpose:
- Controls source-of-truth behavior, AI operating mode, project routing, repo governance, context loading, claim control, decisions, and repo workflow.

Key files:

- `ai-context/start-here.md`
  - First file to read when starting or refreshing an Orisen ChatGPT chat.

- `ai-context/project-routing.md`
  - Explains which Orisen ChatGPT project should handle different kinds of work.

- `ai-context/handoff-rules.md`
  - Defines when to continue, refresh, move projects, or start a new chat.

- `ai-context/context-map.md`
  - Top-level document-routing map for choosing minimal and full context packs.

- `ai-context/current-state.md`
  - Highest-level current company and product truth.

- `ai-context/source-of-truth-rules.md`
  - Defines authority hierarchy and how to handle doc conflicts.

- `ai-context/ai-operating-mode.md`
  - Defines how GPT should reason when using Orisen docs.

- `ai-context/doc-creation-rules.md`
  - Defines how source-of-truth docs should be created, edited, and promoted.

- `ai-context/repo-editing-rules.md`
  - Defines safe direct GitHub editing behavior.

- `ai-context/repo-purpose.md`
  - Defines why the repo exists and what good repo health means.

- `ai-context/repo-structure.md`
  - Defines structural philosophy, folder responsibilities, and anti-duplication rules.

- `ai-context/repo-file-map.md`
  - Central current inventory of repo folders and durable files.

- `ai-context/repo-change-checklist.md`
  - Operational checklist for planning or making repo changes.

- `ai-context/repo-backlog.md`
  - Backlog of repo buildout and cleanup work.

- `ai-context/decision-log.md`
  - Durable decisions and rationale.

## `ai-context/claim-control/`

Purpose:
- Controls claims, evidence, validation language, and claim-safety discipline across product, marketing, fundraising, radar/ML, and public-facing work.

Known key files:

- `ai-context/claim-control/claim-control-system.md`
  - Rules for judging and controlling claims.

- `ai-context/claim-control/claim-control-log.md`
  - Log of claim decisions and evidence status.

- `ai-context/claim-control/claim-control-roadmap.md`
  - Roadmap for improving claim-control system.

## `product/`

Purpose:
- Defines product truth, product scope, customer promise, roadmap, target customer, and claims/evidence from a product perspective.

Known key files:

- `product/product-context-map.md`
  - Product-specific context-loading map.

- `product/product-overview.md`
  - Product direction and product-level truth.

- `product/claims-and-evidence.md`
  - Product claims and evidence boundaries.

- `product/target-customer.md`
  - First target customer and customer focus.

- `product/roadmap.md`
  - Roadmap and product sequencing.

## `marketing/`

Purpose:
- Defines messaging, positioning, customer language, content strategy, channel playbooks, GTM experiments, and launch execution.

Known key files:

- `marketing/marketing-context-map.md`
  - Marketing-specific context-loading map.

- `marketing/positioning-and-messaging.md`
  - Core marketing positioning and messaging.

Potential future files:

- `marketing/customer-language.md`
- `marketing/content-pillars.md`
- `marketing/gtm.md`
- `marketing/linkedin-playbook.md`
- `marketing/x-playbook.md`
- `marketing/tiktok-playbook.md`
- `marketing/instagram-playbook.md`
- `marketing/reddit-research.md`

## `fundraising/`

Purpose:
- Defines investor narrative, fundraising strategy, pitch framing, outreach, traction framing, and investor-specific communication.

Known key files:

- `fundraising/fundraising-context-map.md`
  - Fundraising-specific context-loading map.

- `fundraising/investor-narrative.md`
  - Core investor narrative.

Potential future files:

- `fundraising/pitch-deck-notes.md`
- `fundraising/traction.md`
- `fundraising/outreach-strategy.md`

## `software/`

Purpose:
- Defines software context at the master-docs level and routes to active implementation docs in the software repo.

Known key files:

- `software/software-context-map.md`
  - Software-specific context-loading map and links to active software implementation docs.

Potential or external implementation docs may live in the active Orisen Software repo, not necessarily this master docs repo.

## `radar-ml/`

Purpose:
- Defines radar module decisions, vital-sign extraction, sleep-stage modeling, intervention-loop research, datasets, technical validation, and research interpretation.

Known key files:

- `radar-ml/radar-ml-context-map.md`
  - Radar/ML-specific context-loading map.

Potential future files:

- `radar-ml/radar-module-decision.md`
- `radar-ml/vital-signs-pipeline.md`
- `radar-ml/sleep-stage-model.md`
- `radar-ml/intervention-loop.md`
- `radar-ml/research-notes.md`
- `radar-ml/technical-validation.md`

## `hardware/`

Purpose:
- Defines physical product architecture, sensing placement, enclosure, power, audio/light, manufacturing, reliability, and hardware tradeoffs.

Potential future files:

- `hardware/hardware-context-map.md`
- `hardware/hardware-overview.md`
- `hardware/sensor-decisions.md`
- `hardware/manufacturing-notes.md`

Hardware docs should be created when hardware work becomes frequent enough to justify stable context.

## `business/`

Purpose:
- Defines business model, pricing, competitors, market assumptions, partnerships, operations, and revenue strategy.

Potential future files:

- `business/business-context-map.md`
- `business/business-model.md`
- `business/pricing.md`
- `business/competitors.md`
- `business/market-notes.md`

Business docs may contain assumptions and should clearly separate assumptions from validated facts.

## Entry-point docs

Default entry point:

- `ai-context/start-here.md`

Top-level routing map:

- `ai-context/context-map.md`

Repo governance entry points:

- `ai-context/repo-purpose.md`
- `ai-context/repo-structure.md`
- `ai-context/repo-file-map.md`
- `ai-context/repo-change-checklist.md`

Source-of-truth authority entry points:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`

Doc and repo-edit workflow entry points:

- `ai-context/doc-creation-rules.md`
- `ai-context/repo-editing-rules.md`

Claim-control entry point:

- `ai-context/claim-control/claim-control-system.md`

## Notes for future updates

This file should stay useful but not overly detailed.

Do not turn it into a full duplicate of every folder's context map. Its job is to show what exists and where to find it, not to define every task-specific reading path.