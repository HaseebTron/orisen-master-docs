# Repo Structure

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md`
Downstream docs:
- `ai-context/repo-governance/repo-operating-model.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- `ai-context/context-map.md`
- Folder context maps
- Domain docs

## Purpose

This file explains the organizing logic of the Orisen master docs repo.

It defines how folders should be used, how upstream and downstream docs relate, and how to prevent file-structure duplication across the repo.

This file explains structure philosophy. It should not be treated as the constantly updated file inventory. For the repo operating model, use `ai-context/repo-governance/repo-operating-model.md`. For the current file and folder map, use `ai-context/repo-governance/repo-file-map.md`.

## Core structural principle

The repo should be organized by authority, task, and domain.

The highest-level docs should define company truth and AI operating rules. Domain folders should translate that truth into product, marketing, fundraising, software, radar/ML, hardware, or business-specific context.

Downstream docs should not redefine upstream truth. They should inherit from it.

## The stable top layer

The `ai-context/` folder is the repo's control layer.

It should contain durable rules for:

- project routing
- context loading
- current company state
- source-of-truth hierarchy
- AI operating behavior
- doc creation
- repo editing
- repo purpose
- repo structure
- repo file inventory
- repo change workflow
- decision logs and repo backlog
- claim-control rules

The top layer should be more stable than domain folders.

## Domain folders

Domain folders organize work by area.

Examples include:

- `product/`
- `marketing/`
- `fundraising/`
- `software/`
- `radar-ml/`
- `hardware/`
- `business/`

Domain folders should contain docs that are specific to that domain, while remaining downstream from company-level truth.

A domain folder should not become an isolated mini-repo with its own authority system.

## Folder responsibility rule

Each folder should have a clear responsibility.

A file belongs in a folder when that folder has authority over the file's main topic.

Examples:

- Product promise, target customer, roadmap, and product boundaries belong in `product/`.
- Claims, evidence, and validation boundaries may live in `product/` or `ai-context/claim-control/` depending on authority and usage.
- Messaging, positioning execution, customer language, and channel playbooks belong in `marketing/`.
- Investor narrative, fundraising strategy, outreach, and traction framing belong in `fundraising/`.
- Implementation context, software architecture, and links to active software repo docs belong in `software/`.
- Radar signal processing, sleep-stage modeling, experiments, and technical validation belong in `radar-ml/`.
- Physical product architecture, enclosure, power, audio, sensing placement, and manufacturing belong in `hardware/` when hardware docs exist.

When a topic affects multiple domains or company direction, handle the decision in `ai-context/` or Orisen General first, then propagate downstream.

## Upstream and downstream structure

Use this default authority flow:

1. `ai-context/current-state.md`
2. Other `ai-context/` operating and governance docs
3. Product and validation docs
4. Domain strategy docs
5. Implementation docs
6. Marketing, fundraising, draft, and execution docs
7. Raw notes, old brainstorms, and archives

Downstream docs should cite or reference governing upstream docs when useful.

If a downstream doc conflicts with an upstream doc, the downstream doc should be treated as stale, narrower, speculative, or in need of review unless the higher-level source-of-truth has been deliberately updated.

## Structure duplication rule

Do not duplicate repo or folder file trees across the repo.

The current repo-wide file inventory belongs in:

- `ai-context/repo-governance/repo-file-map.md`

Folder context maps and folder overview docs should not maintain their own complete file trees.

They may explain:

- the folder's purpose
- the folder's authority level
- which tasks the folder supports
- which upstream docs govern the folder
- which docs to read for a specific task
- where to find the current repo-wide file map

They should not maintain a separate folder inventory that can drift from the central file map.

## Why folder docs should not list mini file trees

Mini file trees become stale quickly.

They create extra maintenance because every file rename, move, or deletion may require multiple updates. They also confuse GPT if different docs list different structures.

The repo should have one central file inventory so structure updates have one place to land.

## Context maps versus file maps

Context maps and file maps have different jobs.

A context map answers:

- What should GPT read for this kind of task?
- What is the minimal baseline?
- What additional docs are needed for deeper work?
- Which docs govern the task?

A file map answers:

- What files currently exist?
- Where are they located?
- What is each file's short purpose?
- Which docs are entry points?

Do not turn context maps into file inventories.

## Recommended folder-context-map behavior

A folder context map should usually include:

- purpose of the folder
- governing upstream docs
- minimal baseline for that domain
- full reference pack for broad work
- task-specific reading paths
- escalation rules to Orisen General
- note pointing to `ai-context/repo-governance/repo-file-map.md` for current structure

A folder context map should avoid:

- complete folder file trees
- duplicate explanations of repo-wide structure
- source-of-truth rules already defined in `ai-context/source-of-truth-rules.md`
- long lists of every file unless the list is a task-based reading path

## File naming and nesting principles

Use clear, durable, kebab-case markdown names.

Prefer names that describe the file's job, not temporary status.

Good examples:

- `repo-purpose.md`
- `repo-structure.md`
- `repo-file-map.md`
- `repo-change-checklist.md`
- `product-overview.md`
- `claims-and-evidence.md`
- `positioning-and-messaging.md`

Avoid names that are vague or likely to become stale, such as:

- `misc.md`
- `general-notes.md`
- `random.md`
- `new-stuff.md`
- `final.md`

Use nesting when it improves routing or authority clarity. Do not nest only to make the repo look organized.

## When to create a new folder

Create a new folder only when:

- the topic has recurring work
- the topic needs its own context map or stable docs
- mixing it into another folder would create confusion
- the folder has a clear authority boundary
- future GPT sessions would benefit from targeted context loading

Do not create a folder just because a topic exists.

## When to create a new doc

Create a new doc only when it has a distinct job.

Before creating a new doc, ask:

- Which higher-level docs govern it?
- What decision, context, evidence, workflow, or reading path does it preserve?
- Is the content already covered elsewhere?
- Will this doc make future work more accurate or just add more reading burden?
- Is this source-of-truth, working strategy, implementation detail, draft, or archive?

## Where structure changes should be recorded

When files are added, moved, renamed, or deleted, update:

- `ai-context/repo-governance/repo-file-map.md` if the file inventory changes
- `ai-context/context-map.md` if context-loading rules change
- relevant folder context maps if task reading paths change
- `ai-context/decision-log.md` if the change reflects a durable decision

Do not update every doc automatically. Update only docs that become stale, incomplete, or contradictory.

## What this file does not do

This file does not:

- list the current repo tree
- replace `ai-context/context-map.md`
- replace `ai-context/source-of-truth-rules.md`
- decide product, marketing, fundraising, software, radar/ML, hardware, or business truth
- act as a checklist for every repo edit

Use `ai-context/repo-governance/repo-operating-model.md` for the repo's governed source-of-truth operating model.

Use `ai-context/repo-governance/repo-change-checklist.md` for the operational checklist before changing the repo.
