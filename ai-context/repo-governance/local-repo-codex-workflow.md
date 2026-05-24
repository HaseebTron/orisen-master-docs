# Local Repo + Codex Workflow

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/repo-governance/repo-operating-model.md`
- `ai-context/repo-governance/repo-editing-rules.md`
- `ai-context/repo-governance/repo-change-checklist.md`
- `ai-context/repo-governance/repo-file-map.md`

## Purpose

This file defines how to use a local clone of the Orisen master docs repo with VS Code, Git, and Codex.

Use it when repo work is too broad, risky, or reference-heavy for direct ChatGPT GitHub edits.

## When to use local repo + Codex

Use local repo + Codex instead of direct ChatGPT GitHub editing when the task involves:

- moving, renaming, or deleting multiple files
- reorganizing folders
- repo-wide search and replace
- reference-heavy path updates
- large markdown refactors
- many context-map updates
- broad repo cleanup
- governance-file restructuring
- changes where the user should review a diff before merge
- changes where rollback safety matters
- changes that the ChatGPT GitHub connector may partially block

Direct ChatGPT GitHub editing is still acceptable for small markdown edits, one-file wording fixes, simple stub docs, and narrow low-risk reference updates.

## Assistant responsibility

When a task is large enough for local repo + Codex, ChatGPT should explicitly tell the user:

- that local repo + Codex is the safer workflow
- why direct ChatGPT GitHub editing is not ideal
- whether to use the same Codex session or start a new one
- what Codex intelligence level to use
- whether Codex should edit files or only inspect/report
- whether Codex should commit, push, or stop before committing
- what output the user should paste back into ChatGPT

## Mandatory prompt requirements

Whenever ChatGPT gives the user a Codex prompt for local repo work, the prompt must include:

- check current branch
- run `git status`
- stop if there are uncommitted changes
- switch to `main`
- pull latest `main` from origin
- create a task branch for meaningful repo edits
- confirm the working tree is clean before editing
- state whether Codex may edit or only inspect
- state `Do not commit. Do not push.` unless the user explicitly asked for commit/push

ChatGPT should not assume the user's local repo is current.

## Reusable Codex prompt preamble

Use this preamble when giving the user a Codex prompt for local repo work:

```text
Before editing anything:
1. Check the current git branch:
   `git branch --show-current`
2. Check the working tree:
   `git status`
3. If there are uncommitted changes, stop and report them. Do not stash, overwrite, or discard anything automatically.
4. Switch to main:
   `git checkout main`
5. Pull the latest main:
   `git pull origin main`
6. Create a task branch:
   `git checkout -b type/short-task-name`
7. Confirm the working tree is clean.
8. Only then begin the requested edits.

Do not commit.
Do not push.
Stop after editing and show the full diff.
```

For very small local edits where a branch is intentionally not needed, ChatGPT must say that explicitly and explain why.

## Codex session guidance

Use the same Codex session when the work continues the same branch and task, Codex already has useful context, or the next step is review/inspection.

Start a new Codex session when switching branches, switching tasks, needing a clean context window, or recovering from a confused previous session.

## Codex intelligence level rule

Use high intelligence / best reasoning mode for Codex when moving, renaming, deleting, reorganizing files, editing source-of-truth/governance docs, updating references, reviewing staged diffs, or checking for accidental meaning changes.

Lower/faster modes are acceptable only for narrow mechanical checks or very small low-risk edits.

## Local setup and branch rule

Before local work, confirm the repo is clean and current:

```powershell
git status
git branch --show-current
git pull origin main
```

Do not do meaningful repo restructuring directly on `main`.

Create a task branch:

```powershell
git checkout main
git pull origin main
git checkout -b type/short-task-name
```

## Prompt style for Codex

ChatGPT should give the user one copy-pasteable Codex prompt whenever possible.

A good Codex prompt should include repo name, branch, exact task, scope, out-of-scope items, required searches, whether Codex can edit, whether Codex can commit or push, and required final report fields.

For long terminal-output tasks, prefer asking Codex to run commands and report results instead of asking the user to manually run many terminal commands.

When Codex is allowed to edit, the prompt should usually say:

```text
Do not commit.
Do not push.
Stop after editing and reporting.
```

When Codex is only reviewing, the prompt should say:

```text
Review only.
Do not edit files.
Do not commit.
Do not push.
```

## Reference search workflow

For moves, renames, deletes, archives, folder changes, or doc-system replacements, search before and after the change.

Search for exact old full paths, old filenames, old folder paths, and obvious human-readable names if relevant.

Use `rg` locally when available:

```powershell
rg "old/path.md|old-filename.md|old-folder/" .
```

Open and edit only files with live references. Historical references may remain only if intentionally preserved and reported.

## Staging and review workflow

After Codex edits, stage changes only when the diff looks directionally correct:

```powershell
git add -A
git status --short
git diff --cached --name-status
git diff --cached --stat
```

For staged diff review, ask Codex to run:

```powershell
git diff --cached --check
git diff --cached --name-status
git diff --cached --stat
```

For file moves, staging helps Git recognize renames instead of showing large delete/add diffs.

Before commit, review staged files, rename detection, diff stat, whitespace/conflict-marker checks, reference-search results, and Codex's summary of whether meaning changed accidentally.

## Commit, push, merge, and cleanup

Commit only after the staged review is clean:

```powershell
git commit -m "Short task description"
git status
```

Push the branch:

```powershell
git push -u origin branch-name
```

If merging locally after review:

```powershell
git checkout main
git pull origin main
git merge --no-ff branch-name -m "Merge task description"
git push origin main
git status
```

After merge, delete branches if appropriate:

```powershell
git branch -d branch-name
git push origin --delete branch-name
```

## Guardrails

- Do not let Codex commit or push unless the user explicitly asks.
- Do not mix unrelated tasks in one branch.
- Do not skip reference search for path-breaking changes.
- Do not claim the user reviewed a diff unless they actually did.

## Related docs

Use:

- `ai-context/repo-governance/repo-operating-model.md` for system-level repo governance logic
- `ai-context/repo-governance/repo-editing-rules.md` for overall editing rules
- `ai-context/repo-governance/repo-change-checklist.md` for operational repo-change checks
- `ai-context/repo-governance/repo-file-map.md` for the current file inventory
- `ai-context/repo-governance/repo-structure.md` for folder and structure logic
