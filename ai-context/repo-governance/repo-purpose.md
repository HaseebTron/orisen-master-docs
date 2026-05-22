# Repo Purpose

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md`
Downstream docs:
- `ai-context/repo-governance/repo-operating-model.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- Folder read-rules files
- Domain source-of-truth docs

## Purpose

This file defines why the Orisen master docs repo exists and what it should help Orisen do.

It should be read when planning repo cleanups, reorganizing docs, creating new source-of-truth files, deciding whether content belongs in the repo, or evaluating whether the repo is becoming bloated or unclear.

This file explains the repo's intent. It does not explain the full operating model or list the file structure. For the repo operating model, use `ai-context/repo-governance/repo-operating-model.md`. For structure logic, use `ai-context/repo-governance/repo-structure.md`. For the current file inventory, use `ai-context/repo-governance/repo-file-map.md`.

## What this repo is for

This repo is the source-of-truth memory system for Orisen.

It exists to help ChatGPT and the founder make better decisions by preserving:

- current company truth
- product direction
- customer focus
- validation and evidence boundaries
- claims discipline
- strategy decisions
- domain-specific context
- repo operating rules
- project routing rules
- handoff and context-loading rules

The repo should make future AI-assisted work more accurate, not just store more notes.

## What this repo should help with

The repo should help Orisen:

- prevent context loss across chats
- prevent old brainstorms from being mistaken for current truth
- keep product, marketing, fundraising, software, radar/ML, hardware, and business work aligned
- separate validated evidence from assumptions and future vision
- keep public claims grounded
- preserve important decisions and their reasoning
- make new ChatGPT chats useful quickly
- make repo cleanups safer and less subjective
- give Codex or ChatGPT enough context before changing files

## What this repo is not

This repo is not:

- a dumping ground for every thought
- a replacement for raw research archives
- a place to preserve every old draft as current truth
- a marketing copy library by default
- a fundraising deck workspace by default
- a code implementation repo
- a place where lower-level docs can redefine company direction

Old notes, brainstorms, chat outputs, and draft language should not become source-of-truth unless deliberately promoted through the source-of-truth rules.

## What good looks like

A good version of this repo is:

- easy for GPT to boot from
- clear about which docs are authoritative
- explicit about what is validated, assumed, planned, or future vision
- small enough that important context can be loaded without drowning the model
- organized by authority and task, not by random chronology
- stable at the top and more detailed downstream
- useful for source-of-truth decisions, not just storage
- easy to audit for contradictions
- easy to update when real decisions change

Good docs should make future work safer, clearer, and faster.

## What repo bloat looks like

Repo bloat means the repo contains too much material that is not clearly routed, governed, or useful.

Signs of bloat include:

- duplicate file trees listed in multiple docs
- old drafts presented as current truth
- multiple docs answering the same question differently
- long prose that does not clarify authority, evidence, or decisions
- folder docs that become mini-repos with their own conflicting structures
- marketing or fundraising language that quietly overclaims
- implementation docs that accidentally shrink the company vision
- raw notes rewritten into conclusions without evidence review
- too many context files that must be read before simple tasks

Bloat should be fixed by clarifying authority, archiving or routing content, and removing duplication. Do not fix bloat by deleting raw evidence or important historical context without a deliberate plan.

## Stable top, flexible bottom

The repo should have a stable top layer and flexible downstream layers.

Stable top-layer docs define:

- what Orisen is
- how source-of-truth works
- how GPT should reason
- how repo changes should happen
- how the repo is structured
- what files exist and where to find them

Downstream docs can change more often as Orisen learns, builds, tests, markets, and fundraises.

This avoids rewriting high-level repo purpose every time a folder or file changes.

## Upstream and downstream principle

Higher-level docs govern lower-level docs.

Lower-level docs should inherit from higher-level docs. They should not redefine company truth, product promise, claims, validation status, or roadmap priority by accident.

Default authority flow:

1. Company and AI-context docs
2. Product and validation docs
3. Domain strategy docs
4. Implementation docs
5. Marketing, fundraising, draft, or execution assets
6. Raw notes and old brainstorms

If a downstream doc conflicts with an upstream doc, do not average them together. Identify the conflict and apply `ai-context/source-of-truth-rules.md`.

## How GPT should use this repo

GPT should use this repo as a source-of-truth system, not as a pile of context.

Before major Orisen work, GPT should:

- start from `ai-context/start-here.md`
- load the relevant baseline docs from `ai-context/context-map.md`
- use `ai-context/source-of-truth-rules.md` to resolve conflicts
- use `ai-context/ai-operating-mode.md` to reason non-agreeably
- use `ai-context/doc-creation-rules.md` before creating or editing docs
- use `ai-context/repo-governance/repo-editing-rules.md` and `ai-context/repo-governance/repo-change-checklist.md` before repo edits
- use `ai-context/repo-governance/repo-operating-model.md` for broad repo audits, system explanations, and governance architecture reviews
- use `ai-context/repo-governance/repo-structure.md` for structural logic
- use `ai-context/repo-governance/repo-file-map.md` for the current file inventory

GPT should read only the docs needed for the task. Loading everything by default is not the goal.

## Cleanup principle

During repo cleanup, optimize for clarity, authority, and future usefulness.

Do not optimize only for neatness.

A cleanup should ask:

- Does this content support a current decision, evidence base, operating rule, or domain workflow?
- Is this current truth, assumption, archive, draft, or raw source material?
- Is this content duplicated elsewhere?
- Which file has authority over this topic?
- Would deleting, moving, or rewriting this content make future GPT work safer or riskier?
- Are downstream docs still consistent after the cleanup?

## What should not be added

Avoid adding:

- polished but unsupported claims
- broad strategy docs that duplicate `ai-context/current-state.md`
- file trees inside folder docs
- temporary chat outputs unless promoted deliberately
- raw notes rewritten as conclusions without evidence status
- documents that combine unrelated domains without a clear purpose
- docs that exist only because a topic seems interesting

Create a new doc only when it makes future reasoning, routing, or execution meaningfully better.

## Relationship to repo structure docs

This file defines the repo's intent.

Use:

- `ai-context/repo-governance/repo-operating-model.md` for the repo's governed source-of-truth operating model
- `ai-context/repo-governance/repo-structure.md` for structural philosophy and folder responsibilities
- `ai-context/repo-governance/repo-file-map.md` for the current file inventory
- `ai-context/repo-governance/repo-change-checklist.md` before changing the repo

Do not duplicate the file tree in this file.
