# Repo Operating Model

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md`
Downstream docs:
- `ai-context/context-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- `ai-context/repo-governance/repo-editing-rules.md`
- `ai-context/repo-governance/local-repo-codex-workflow.md`
- Folder read-rules files

## Purpose

This file explains how the Orisen master docs repo carries out the intent defined in `ai-context/repo-governance/repo-purpose.md`.

`repo-purpose.md` explains why the repo exists. This file explains how the repo actually works as a system.

It is mainly for the founder and future ChatGPT chats to understand the repo's operating logic without needing to mentally combine every governance file from scratch.

## Core idea

The repo works by turning scattered startup context into a governed source-of-truth system.

It does this through five connected mechanisms:

1. smart booting
2. smart reading
3. source-of-truth authority
4. safe derivation of downstream docs
5. safe repo editing

No single file does all of this. The operating model is the combination of `start-here.md`, `context-map.md`, source-of-truth rules, doc creation rules, repo-governance docs, folder read-rules files, and domain docs.

## Smart booting

Smart booting means a new ChatGPT chat starts from a stable entry point instead of guessing from memory.

Default boot path:

1. Read `ai-context/start-here.md`.
2. Confirm the correct ChatGPT project and chat context.
3. Use `ai-context/context-map.md` to choose the right reading path.
4. Load only the docs needed for the task.

The goal is not to read everything by default. The goal is to load enough context to avoid bad reasoning without drowning the model.

## Smart reading

Smart reading means choosing docs based on task type.

`ai-context/context-map.md` is the main routing layer for this.

It separates:

- minimal baselines
- full reference packs
- task-specific docs
- escalation rules

Folder read-rules files extend this behavior inside specific domains like product, research, marketing, fundraising, software, and radar/ML.

A read-rules file should answer: What should GPT read for this task?

It should not become a duplicate file inventory. The current file inventory belongs in `ai-context/repo-governance/repo-file-map.md`.

## Source-of-truth authority

The repo prevents confusion by treating some docs as higher-authority than others.

Default authority flow:

1. company and AI-context docs
2. product and validation docs
3. domain strategy docs
4. implementation docs
5. marketing, fundraising, draft, and execution assets
6. raw notes, old brainstorms, and archives

If a lower-level doc conflicts with a higher-level doc, do not average the two together.

Instead:

- identify the conflict
- decide which doc has authority
- mark the downstream doc as stale, narrower, speculative, or in need of update
- update source-of-truth only deliberately

This is what prevents old ideas, draft copy, or implementation details from accidentally redefining the company.

## Safe derivation of new docs

New docs should be derived from upstream truth, not only from the latest user request.

Before creating or materially editing a source-of-truth doc, identify:

- what type of doc it is
- which upstream docs govern it
- what truth it inherits
- what claims are validated
- what claims are assumptions
- what is MVP scope versus future vision
- which downstream docs may depend on it

The user's request is an input, not the sole authority.

Good derivation flows downward:

- company truth informs product truth
- product truth informs marketing and fundraising language
- validation evidence informs claims
- implementation docs inform build reality but do not shrink the whole company vision unless deliberately promoted upward

## Smart editing

Smart editing means repo changes are made with context, scope, and review discipline.

Before repo edits, ChatGPT should disclose:

- what files it read
- what files it will create or edit
- what files it will move, rename, delete, or archive
- what files it will intentionally not touch
- editing method
- risk level
- reason for the change

Small low-risk edits can be done directly through ChatGPT GitHub editing.

Broad, risky, or reference-heavy edits should use local repo + Codex, because local Git allows better search, diff review, branch safety, and rollback.

## Reference safety

When a change can stale references, the repo uses reference search.

Reference search is required before:

- moving files or folders
- renaming files or folders
- deleting or archiving files or folders
- replacing doc systems
- changing official routing or context paths

Search for old paths, filenames, folder paths, and obvious human-readable names.

Then update live references, preserve intentional historical references, and report what changed.

## File map versus routing rules

The repo uses two different map types.

`repo-file-map.md` answers:

- What files exist?
- Where are they?
- What is each file's short purpose?

`context-map.md` and folder read-rules files answer:

- What should GPT read for a task?
- What is the minimal baseline?
- What deeper docs are needed for broad or high-stakes work?

Do not merge these jobs.

A file map is inventory. Routing/read-rules docs define task routing.

## Repo structure logic

The repo is organized by authority, task, and domain.

`ai-context/` is the control layer.

Domain folders translate company-level truth into product, research, marketing, fundraising, software, radar/ML, hardware, and business work.

`ai-context/repo-governance/` contains docs about maintaining the repo itself.

`ai-context/claim-control/` contains docs about claims, evidence, validation language, and claim safety.

Folder nesting should exist only when it improves routing or authority clarity.

## Human readability

This repo is not only for GPT. It should also help the founder understand what is true, where information lives, and why the structure exists.

Good human readability means:

- entry points are obvious
- file names describe jobs
- maps are easy to skim
- duplicated structure is avoided
- raw evidence stays separate from synthesis
- current truth is not mixed with old drafts
- cleanup decisions are explainable

## What this file should not do

This file should not replace:

- `repo-purpose.md` for why the repo exists
- `repo-structure.md` for structural philosophy
- `repo-file-map.md` for current file inventory
- `context-map.md` for task-specific reading paths
- `repo-editing-rules.md` for editing mechanics
- `doc-creation-rules.md` for detailed doc-creation rules
- `source-of-truth-rules.md` for conflict resolution and authority hierarchy

This file is an operating model, not a duplicate of every rule.

## When to read this file

Read this file when:

- auditing the repo's logic
- explaining how the repo works to the founder
- deciding whether the repo structure still matches its purpose
- planning broad cleanup
- teaching a new ChatGPT chat how the repo fits together
- checking whether a proposed new doc or folder fits the overall system

For normal narrow tasks, this file is optional.
