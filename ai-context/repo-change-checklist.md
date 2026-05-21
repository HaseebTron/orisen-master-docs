# Repo Change Checklist

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-21
Governing docs:
- `ai-context/repo-purpose.md`
- `ai-context/repo-structure.md`
- `ai-context/repo-editing-rules.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/source-of-truth-rules.md`
Downstream docs:
- Repo edit sessions
- Repo cleanup sessions
- Repo integrity checks

## Purpose

This file is the operational checklist for planning or making changes to the Orisen master docs repo.

Use it when creating, editing, moving, deleting, reorganizing, or cleaning up durable repo docs.

This file does not replace `ai-context/repo-editing-rules.md`. It translates the repo rules into a practical checklist.

## When to use this checklist

Use this checklist for:

- creating a new durable doc
- materially editing a source-of-truth doc
- moving files or folders
- deleting files
- renaming files
- changing context-loading rules
- updating folder context maps
- cleaning up repo bloat
- updating repo structure
- preparing Codex or GPT to modify repo files
- doing a repo integrity check

For tiny wording fixes, use judgment. Do not overburden small changes.

## Standard repo-change context pack

Before significant repo changes, read:

- `ai-context/start-here.md`
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/context-map.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/repo-editing-rules.md`
- `ai-context/repo-purpose.md`
- `ai-context/repo-structure.md`
- `ai-context/repo-file-map.md`
- `ai-context/repo-change-checklist.md`

Then read task-specific docs only as needed.

## Add task-specific docs when needed

Read `ai-context/claim-control/claim-control-system.md` when the change affects:

- claims
- evidence
- validation
- marketing language
- fundraising language
- technical support for product claims
- sleep-stage, grogginess, sleep inertia, radar/ML, or intervention claims

Read domain context maps when the change affects that domain:

- `software/software-context-map.md`
- `marketing/marketing-context-map.md`
- `fundraising/fundraising-context-map.md`
- `radar-ml/radar-ml-context-map.md`
- `hardware/hardware-context-map.md` if it exists
- `business/business-context-map.md` if it exists
- `product/product-context-map.md` if it exists

If a needed context map does not exist, use available docs directly and recommend creating the context map only if the workstream is active enough.

## Pre-change questions

Before changing the repo, answer:

- What is the change type?
  - create
  - edit
  - move
  - rename
  - delete
  - archive
  - cleanup
  - context-routing update
- What problem is the change solving?
- Which higher-level docs govern this change?
- Is this current truth, working strategy, implementation detail, evidence, draft, or archive?
- Is this change downstream from existing source-of-truth, or does it change source-of-truth?
- Does this affect product promise, claims, roadmap, fundraising, marketing, software architecture, radar/ML, hardware, or business strategy?
- Could this make any existing doc stale or contradictory?
- Does this require updating `ai-context/repo-file-map.md`?
- Does this require updating `ai-context/context-map.md`?
- Does this require updating folder context maps?
- Does this require a decision-log entry?

## Pre-edit scope statement

Before direct GitHub edits, state:

- files to create
- files to update
- files to move, rename, delete, or archive
- files intentionally not touched
- whether direct GitHub editing is safe
- whether local Git, Codex, or branch/PR workflow would be safer

For broad, risky, or many-file changes, prefer local Git, Codex, or branch/PR workflow.

## Required planned repo-change summary format

Before significant direct repo edits, use this format so the user can clearly see what context was loaded and what will change:

```markdown
## Planned repo-change summary

Files read:
- `path/to/file.md`

Files to create:
- `path/to/new-file.md`
- None

Files to edit:
- `path/to/existing-file.md`
- None

Files to move/rename:
- `old/path.md` -> `new/path.md`
- None

Files to delete/archive:
- `path/to/file.md`
- None

Files intentionally not touched:
- `path/to/file.md`
- None

Editing method:
- Direct GitHub edit / Local Git / Codex / Branch/PR

Risk level:
- Low / Medium / High

Reason:
- Brief explanation
```

Use `None` under any category that does not apply.

For tiny one-file wording fixes, this format can be shortened, but the assistant should still make clear what file is being edited.

## Workflow choice

Direct GitHub editing is acceptable for:

- small markdown edits
- simple new governance docs
- narrow reference updates
- low-risk context-map updates
- clearly agreed changes touching a small number of files

Prefer local Git, Codex, or branch/PR workflow for:

- large repo-wide refactors
- many file moves or renames
- deleting or archiving many files
- major source-of-truth changes
- claims or fundraising rewrites
- changes that require diff review before landing
- changes where rollback safety matters

## Creation checklist

When creating a new doc:

- Confirm the doc has a distinct job.
- Confirm the file path and name follow repo structure rules.
- Identify governing docs.
- Identify downstream docs.
- Add metadata if the doc is durable.
- Avoid duplicating content already covered elsewhere.
- Clearly separate truth, assumptions, evidence, and open questions when relevant.
- Update `ai-context/repo-file-map.md`.
- Update `ai-context/context-map.md` only if context-loading rules change.

## Editing checklist

When editing an existing doc:

- Fetch the latest version before editing.
- Check whether the edit conflicts with higher-authority docs.
- Keep the edit scoped to the intended purpose.
- Avoid quietly changing product truth, claims, or roadmap priority unless that is the explicit task.
- Check whether downstream docs now need updates.
- Do not update every related file automatically.
- Update only files that become stale, incomplete, or contradictory.

## Move or rename checklist

When moving or renaming files:

- Confirm the new location better matches authority and folder responsibility.
- Preserve content unless rewriting is explicitly part of the task.
- Update links and references.
- Update `ai-context/repo-file-map.md`.
- Update `ai-context/context-map.md` if context-loading paths changed.
- Update folder context maps if reading paths changed.
- Consider using local Git or Codex for link-search and diff review.

## Delete or archive checklist

When deleting or archiving files:

- Confirm the file is not source-of-truth or required evidence.
- Confirm raw evidence is preserved unless the user explicitly asked otherwise and the governing docs support it.
- Confirm deletion will not remove important decision history.
- Prefer archiving over deleting when historical context may matter.
- Update `ai-context/repo-file-map.md`.
- Update context maps and links.
- Use local Git or Codex for broad cleanup.

## Anti-duplication checklist

Before adding structure information to any doc, ask:

- Is this a file tree or inventory?
- Does it belong in `ai-context/repo-file-map.md` instead?
- Is this explaining structure logic?
- Does it belong in `ai-context/repo-structure.md` instead?
- Is this explaining what to read for a task?
- Does it belong in `ai-context/context-map.md` or a folder context map instead?

Do not add complete folder file trees to folder context maps or domain docs.

## Claim and evidence checklist

If the change touches claims, evidence, validation, marketing, fundraising, radar/ML, or scientific support:

- Read `ai-context/claim-control/claim-control-system.md`.
- Separate validated from assumed or planned.
- Do not strengthen public claims unless evidence supports it.
- Check `product/claims-and-evidence.md` when product claims are involved.
- Update claim-control docs if a durable claim decision changes.

## Post-change summary

After repo edits, summarize:

- files created
- files updated
- files moved, renamed, deleted, or archived
- files intentionally not touched
- whether `repo-file-map.md` was updated
- whether context maps were updated
- any tool errors or partial failures
- follow-up review needed

Do not imply the user reviewed a diff unless they actually did.

## Required repo-change result format

After significant direct repo edits, use this format:

```markdown
## Repo-change result

Files created:
- `path/to/new-file.md`
- None

Files edited:
- `path/to/existing-file.md`
- None

Files moved/renamed:
- `old/path.md` -> `new/path.md`
- None

Files deleted/archived:
- `path/to/file.md`
- None

Files intentionally not touched:
- `path/to/file.md`
- None

`repo-file-map.md` updated:
- Yes / No / Not needed

Context maps updated:
- Yes / No / Not needed

Tool errors:
- None / Brief description

Follow-up review needed:
- None / Brief description
```

Use `None` or `Not needed` where appropriate.

For tiny one-file wording fixes, this format can be shortened, but the assistant should still clearly state what changed and whether any tool errors occurred.

## Post-change consistency check

After meaningful changes, check:

- Do new docs have clear governing docs?
- Are downstream docs still consistent?
- Are there duplicated file trees?
- Did `repo-file-map.md` stay current?
- Did `context-map.md` stay accurate?
- Are claims still safe?
- Did the change create any authority ambiguity?

## Important principle

The goal of repo changes is not to make the repo look bigger or cleaner.

The goal is to make future Orisen reasoning more accurate, grounded, and easy to continue.