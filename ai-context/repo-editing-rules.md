# Repo Editing Rules

## Purpose

This file defines how ChatGPT should perform direct GitHub edits to the Orisen master docs repo.

The goal is to reduce mechanical repo-editing mistakes, especially during multi-file source-of-truth changes.

These rules do not replace source-of-truth, doc-creation, claim-control, or repo-governance rules. They define the editing workflow used when applying changes to the repo.

## Related repo-governance docs

Use these docs together when planning or making repo changes:

- `ai-context/repo-purpose.md` defines why the repo exists and what good repo health means.
- `ai-context/repo-structure.md` defines the structural philosophy, folder responsibilities, and anti-duplication rules.
- `ai-context/repo-file-map.md` is the central inventory of the repo's current durable files and folders.
- `ai-context/repo-change-checklist.md` is the operational checklist for planning or making repo changes.

For significant repo changes, read `ai-context/repo-change-checklist.md` before editing.

## Core rule

Prefer small, bounded, reviewable repo edits.

Do not make large multi-file changes directly on GitHub without first stating the intended scope and confirming that direct editing is appropriate for the risk level.

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

For significant repo changes, use the required planned repo-change summary format from `ai-context/repo-change-checklist.md`.

For tiny one-file edits, this can be shortened, but the assistant should still make clear what file is being edited.

## Logical batch rule

For multi-file direct GitHub edits, edit in small logical batches.

Good batches:

- create new folder stubs
- update routing/context maps
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

- `ai-context/repo-file-map.md`

Folder context maps and domain docs should explain task-based reading paths, governing docs, and folder purpose. They should not maintain their own complete file inventories unless there is a specific, justified exception.

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
- whether `repo-file-map.md` was updated
- whether context maps were updated
- any tool errors or partial failures
- any follow-up review needed

For significant repo edits, use the required repo-change result format from `ai-context/repo-change-checklist.md`.

Do not imply that the user has reviewed a diff unless they actually have.

## Relationship to local Git and Codex

ChatGPT Orisen General is best for deciding what should change and why.

Local Git and Codex are better for applying larger repo changes safely because they allow:

- full diff review
- easier rollback
- cleaner commits
- repo-wide search and consistency checks
- branch/PR review before merge

Use the lightest workflow that is safe for the task.

## Relationship to doc creation, repo governance, and claim control

When creating or editing docs, still follow:

- `ai-context/doc-creation-rules.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/repo-purpose.md` for repo intent
- `ai-context/repo-structure.md` for repo structure logic
- `ai-context/repo-file-map.md` for the current file inventory
- `ai-context/repo-change-checklist.md` for the operational repo-change checklist
- `ai-context/claim-control/claim-control-system.md`, when claims, evidence, validation, marketing, fundraising, or scientific support are involved

These repo editing rules control editing mechanics. They do not decide company truth or claim safety by themselves.