# Repo Editing Rules

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-operating-model.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/source-of-truth-rules.md`
Downstream docs:
- Repo edit sessions
- Repo cleanup sessions
- Direct GitHub editing workflows
- Local repo + Codex workflow decisions

## Purpose

This file defines how ChatGPT should perform direct GitHub edits to the Orisen master docs repo.

The goal is to reduce mechanical repo-editing mistakes, especially during multi-file source-of-truth changes.

These rules do not replace source-of-truth, doc-creation, claim-control, or repo-governance rules. They define the editing workflow used when applying changes to the repo.

## Related repo-governance docs

Use these docs together when planning or making repo changes:

- `ai-context/repo-governance/repo-purpose.md` defines why the repo exists and what good repo health means.
- `ai-context/repo-governance/repo-operating-model.md` explains how the repo works as a governed source-of-truth system.
- `ai-context/repo-governance/repo-structure.md` defines the structural philosophy, folder responsibilities, and anti-duplication rules.
- `ai-context/repo-governance/repo-file-map.md` is the central inventory of the repo's current durable files and folders.
- `ai-context/repo-governance/repo-change-checklist.md` is the operational checklist for planning or making repo changes.
- `ai-context/repo-governance/local-repo-codex-workflow.md` defines when and how to use local VS Code, Git, and Codex for broader repo changes.

For significant repo changes, read `ai-context/repo-governance/repo-change-checklist.md` before editing.

For broad repo audits, repo logic reviews, AI/context system reviews, or governance architecture reviews, read `ai-context/repo-governance/repo-operating-model.md`.

For broad, risky, or reference-heavy local work, read `ai-context/repo-governance/local-repo-codex-workflow.md` before telling the user how to use Codex or VS Code.

## Mandatory pre-edit disclosure rule

Before creating, editing, moving, renaming, deleting, or archiving any repo file, ChatGPT must tell the user what it read and what it is about to change.

This applies even when the user has already approved the general task.

Before the first write action in a repo-editing task, ChatGPT must state:

- files read before editing
- files to create
- files to edit
- files to move or rename
- files to delete or archive
- files intentionally not touched, when relevant
- editing method
- risk level
- reason for the change

For significant repo changes, use the exact planned repo-change summary format from `ai-context/repo-governance/repo-change-checklist.md`.

For tiny one-file edits, a shortened version is acceptable, but it must still clearly state the file read and the file being edited before the edit happens.

Do not perform the write first and explain afterward.

## Mandatory reference search rule

Before any change that can break or stale file/folder references, ChatGPT must run a repo reference search.

Reference search is required before:

- moving, renaming, deleting, or archiving a file
- moving, renaming, deleting, or archiving a folder
- replacing an old doc system or folder with a new one
- changing official file paths, folder paths, or “read this doc” references inside routing, inventory, or context-map docs

Reference search is not required for edits that do not change paths or references, such as wording cleanup, formatting cleanup, or adding descriptions.

Required searches:

- exact old full path
- old filename
- old folder path, if a folder is affected
- obvious human-readable names, if relevant

Open only the files returned by search.

For each hit, decide whether to:

- update the reference
- preserve it as intentional historical context
- remove it if it is stale

After the edit, report:

- searches performed
- files that referenced the old path/name
- files updated
- references intentionally preserved

Do not manually read every Markdown file unless repo search is unavailable or insufficient.

## Core rule

Prefer small, bounded, reviewable repo edits.

Do not make large multi-file changes directly on GitHub without first stating the intended scope and confirming that direct editing is appropriate for the risk level.

If the change is broad, risky, or reference-heavy, ChatGPT should tell the user that local repo + Codex is safer and should use `ai-context/repo-governance/local-repo-codex-workflow.md` for the workflow.

## Direct GitHub editing is appropriate for

Direct GitHub edits are acceptable for:

- small markdown edits
- creating simple stub files
- fixing links or metadata
- updating a narrow set of related docs
- making low-risk structural additions
- applying a clearly agreed plan

## Direct GitHub editing is not ideal for

Prefer a local Git, Codex, or branch/PR workflow for:

- large repo-wide refactors
- changes touching many source-of-truth files
- major product, claims, marketing, fundraising, roadmap, or architecture revisions
- edits where the user should inspect a full diff before changes land
- changes involving many deletes, renames, or moves
- work where rollback safety matters
- changes where unrelated files might be affected

When recommending local Git/Codex, tell the user whether to continue the same Codex session or start a new one, what Codex intelligence level to use, whether Codex should edit or only inspect/report, and whether Codex should stop before commit/push.

## Pre-edit scope statement

Before direct GitHub edits, ChatGPT should briefly state:

- files read
- files it plans to create
- files it plans to update
- files it plans to move, rename, delete, or archive
- files it will intentionally not touch, when relevant
- editing method
- risk level
- whether the change is small enough for direct GitHub editing
- whether a local/Codex/branch workflow would be safer

For significant repo changes, use the required planned repo-change summary format from `ai-context/repo-governance/repo-change-checklist.md`.

For tiny one-file edits, this can be shortened, but the assistant should still make clear what file is being edited.

## Logical batch rule

For multi-file direct GitHub edits, edit in small logical batches.

Good batches:

- create new folder stubs
- update routing/read-rules files
- update claim-control references
- update final summary/check

Avoid mixing unrelated changes in the same batch.

Do not edit more than about 3 to 5 files in one direct GitHub pass unless the edits are mechanical, low-risk, and clearly connected.

## Main branch caution

If editing directly on `main`, keep changes narrow and reversible.

For broad or high-risk work, prefer:

- local Git workflow
- Codex local workflow
- branch and pull request workflow

Do not treat direct `main` edits as the default for large changes.

## Raw/archive preservation rule

Do not delete, heavily rewrite, or reorganize raw/archive files unless the user explicitly asks and the governing docs support it.

For raw research, customer notes, old MVP evidence, exported analytics, or founder-provided source lists:

- preserve the original material
- add routing maps or synthesis files around it
- avoid rewriting raw source material into conclusions
- do not duplicate large raw files across folders unless a deliberate processing pass requires it

## Structure duplication rule

Do not duplicate repo-wide or folder-level file trees across multiple docs.

The central file inventory belongs in:

- `ai-context/repo-governance/repo-file-map.md`

Folder read-rules files and domain docs should explain task-based reading paths, governing docs, and folder purpose. They should not maintain their own complete file inventories unless there is a specific, justified exception.

## Mid-edit error rule

If a tool error happens during repo editing:

1. Stop.
2. State what changed successfully.
3. State what failed.
4. Do not continue silently.
5. Resume only after the next safe edit step is clear.

## Post-edit summary rule

After direct GitHub edits, summarize:

- files created
- files updated
- files moved, renamed, deleted, or archived
- files intentionally not touched
- whether `ai-context/repo-governance/repo-file-map.md` was updated
- whether routing/read-rules files were updated
- any tool errors or partial failures
- any follow-up review needed

For significant repo edits, use the required repo-change result format from `ai-context/repo-governance/repo-change-checklist.md`.

Do not imply that the user has reviewed a diff unless they actually have.

## Relationship to local Git and Codex

ChatGPT Orisen General is best for deciding what should change and why.

Local Git and Codex are better for applying larger repo changes safely because they allow:

- full diff review
- easier rollback
- cleaner commits
- repo-wide search and consistency checks
- branch/PR review before merge

Use `ai-context/repo-governance/local-repo-codex-workflow.md` when giving the user local repo + Codex instructions.

Use the lightest workflow that is safe for the task.

## Relationship to doc creation, repo governance, and claim control

When creating or editing docs, still follow:

- `ai-context/doc-creation-rules.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/repo-governance/repo-purpose.md` for repo intent
- `ai-context/repo-governance/repo-operating-model.md` for the repo's governed source-of-truth operating model
- `ai-context/repo-governance/repo-structure.md` for repo structure logic
- `ai-context/repo-governance/repo-file-map.md` for the current file inventory
- `ai-context/repo-governance/repo-change-checklist.md` for the operational repo-change checklist
- `ai-context/repo-governance/local-repo-codex-workflow.md` for local repo + Codex workflow
- `ai-context/claim-control/claim-control-system.md`, when claims, evidence, validation, marketing, fundraising, or scientific support are involved

These repo editing rules control editing mechanics. They do not decide company truth or claim safety by themselves.
