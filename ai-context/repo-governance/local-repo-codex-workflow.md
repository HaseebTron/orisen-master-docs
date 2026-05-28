# Local Repo + Codex Workflow

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-05-28
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

## Default solo-founder docs workflow for `orisen-master-docs`

For normal bounded docs edits in `HaseebTron/orisen-master-docs`, the default workflow is:

```text
local branch -> ChatGPT diff review -> local merge into main -> push main
```

This is a local docs workflow, not a GitHub pull-request requirement.

Use this sequence:

1. Start from local `main`.
2. Run `git pull origin main`.
3. Create a local task branch.
4. Make changes on the task branch.
5. Create the local branch commit or commits intended for review.
6. Run `git status --short` to confirm no uncommitted work is being left out of review.
7. Use `git diff main...HEAD` for ChatGPT review.
8. If ChatGPT approves, switch to `main`.
9. Run `git pull origin main` again.
10. Merge the task branch into local `main`.
11. Push `main` to GitHub.

Codex prompts still default to:

```text
Do not commit.
Do not push.
```

The founder must explicitly authorize any commit, merge, or push step.

## Optional GitHub PR workflow

A GitHub pull request is optional for normal bounded docs edits in `HaseebTron/orisen-master-docs`.

Use a GitHub PR when the change is broad, risky, likely to need a GitHub-hosted review record, or when the user explicitly wants a PR.

When a PR is used, push the task branch and use the GitHub PR review path before merge.

This rule applies only to `HaseebTron/orisen-master-docs`. Do not apply it to `HaseebTron/Orisen`; that repo follows its own implementation and code workflow.

## Assistant responsibility

When a task is large enough for local repo + Codex, ChatGPT should explicitly tell the user:

- that local repo + Codex is the safer workflow
- why direct ChatGPT GitHub editing is not ideal
- whether to use the same Codex session or start a new one
- what Codex intelligence level to use
- whether Codex should edit files or only inspect/report
- whether Codex should commit, push, or stop before committing
- what output the user should paste back into ChatGPT

## Codex-first command workflow

When the user's next action would normally be to manually run terminal, bash, PowerShell, Git, or repo-inspection commands, ChatGPT should usually give the user one copy-pasteable Codex prompt instead of asking the user to run the commands manually.

The Codex prompt should ask Codex to:

- run the needed commands in the local repo
- inspect the command output instead of merely relaying raw output
- report the exact results ChatGPT needs for the next decision
- edit files only if the prompt explicitly authorizes editing
- stop before commit or push unless the user explicitly asks for commit or push

Manual terminal commands should be reserved for tiny, safe, obvious one-liners, or for cases where Codex is unavailable or inappropriate.

The default workflow should reduce founder manual terminal burden while preserving review discipline: Codex performs the mechanical local work, ChatGPT reviews the reported results and diff, and the user remains in control of approvals, commits, pushes, and merges.

## Codex session routing instruction

Whenever ChatGPT gives the user a prompt to paste into Codex, ChatGPT must state above the prompt whether the user should paste it into:

- the existing Codex session
- a new Codex session

ChatGPT must briefly explain why.

Recommend the existing Codex session when:

- the task depends on current uncommitted diffs
- the task continues the same branch or local repo state
- the task needs Codex to preserve context from the immediately previous task
- the prompt refers to "current diff," "existing branch," "uncommitted changes," or "continue from the previous edit"

Recommend a new Codex session when:

- starting a new major task
- switching branches or workstreams
- the current Codex session may be stale, confused, or contaminated
- the task needs a clean review
- the task no longer depends on the current local state except what can be rediscovered through `git status` and file reads

If either option is acceptable, ChatGPT should still recommend one default and explain the tradeoff.

The session-routing note must appear before the Codex prompt, not after it.

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

## Mandatory source-context loading gate

When preparing a Codex prompt for Orisen repo-governance, source-of-truth docs, project routing, context loading, read-rules, repo boundaries, claims, product direction, roadmap, radar/ML strategy, marketing, or fundraising docs, the prompt must explicitly tell Codex which source-of-truth files to read before planning or editing.

Do not assume Codex will infer the right context from the repo, branch name, file names, or requested edit.

For source-of-truth or repo-governance edits, the Codex prompt must include a `Before planning or editing, read:` section listing the required boot, governance, and task-specific docs.

The prompt must require Codex to:

- summarize what it read
- identify the governing docs for the requested change
- state planned file changes before editing
- stop if the requested change conflicts with higher-authority docs

Git workflow safety steps are required, but they do not replace source-context loading.

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

For diff review:
- If Codex is stopping before an authorized commit, first show the working-tree diff with `git diff`.
- After the user authorizes the local branch commit or commits, use `git diff main...HEAD` for ChatGPT branch review before merge.
- If the review diff is too long for chat, write it to `$env:USERPROFILE\Downloads\task-review-diff.md`.
- Do not create temporary review files inside the repo.
- Do not stage temporary review files.
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

For the branch-level ChatGPT review before a local merge in `HaseebTron/orisen-master-docs`, use `git diff main...HEAD` after the local branch commit or commits exist.

## Diff sharing rule

For branch diff review before local merge, avoid asking for many tiny one-file diffs unless the user specifically wants that.

Preferred order:

1. Ask Codex to show the full branch diff:

   ```powershell
   git diff main...HEAD
   ```

2. If the diff is too long for chat, ask Codex to write the branch diff to a temporary file outside the repo, preferably the user's Downloads folder:

   ```powershell
   git diff main...HEAD > "$env:USERPROFILE\Downloads\task-review-diff.md"
   ```

3. The user should upload or paste that review file into ChatGPT.

4. Do not create temporary review files inside the repo unless there is a specific reason.

5. If a temporary review file is accidentally created inside the repo, it must not be staged and should be deleted before commit.

For targeted review, Codex may still output a single-file diff when ChatGPT asks for one specific file, but the default for multi-file review should be full diff or review-file export.

## ChatGPT review loop

For meaningful local repo edits, especially file moves, renames, reference updates, source-of-truth edits, governance edits, or claim-sensitive edits, Codex should stop after editing and show the diff summary.

For normal bounded docs edits in `HaseebTron/orisen-master-docs`, the user should paste the `git diff main...HEAD` branch diff or relevant diff summary into ChatGPT before local merge and `main` push.

Before commit, push, or merge, the user should paste the diff summary or relevant diff into ChatGPT for review unless the user explicitly chooses to skip ChatGPT review.

For pre-commit review, use the working-tree or staged diff. For the required branch review before local merge in `HaseebTron/orisen-master-docs`, use `git diff main...HEAD`.

ChatGPT should review for:

- missed old references
- accidental content deletion
- accidental meaning changes
- wrong source-of-truth hierarchy
- claim-safety issues
- files that should not have changed
- files that should have changed but were missed
- whether the edit stayed within the approved scope
- whether the change stayed minimal when minimal edits were requested

Codex should not commit, push, or merge until this review is complete unless the user explicitly chooses to skip ChatGPT review.

If the user skips ChatGPT review, ChatGPT should not later imply that it reviewed or approved the diff.

## Commit, merge, push, and cleanup

Codex must not commit, merge, or push unless the user explicitly asks.

Commit only after the staged review is clean:

```powershell
git commit -m "Short task description"
git status
```

For normal bounded docs edits in `HaseebTron/orisen-master-docs`, the default completion path after ChatGPT approves the branch diff is local merge into `main` and push `main`:

```powershell
git diff --check main...HEAD
git diff --stat main...HEAD
git diff main...HEAD
git checkout main
git pull origin main
git merge --no-ff branch-name -m "Merge task description"
git push origin main
git status
```

Push the task branch only when using the optional GitHub PR workflow or when the user explicitly asks:

```powershell
git push -u origin branch-name
```

After a task branch has been merged into `main` and pushed, delete the completed local branch unless the user wants to keep it.

Delete a remote branch only if one was created for a PR or explicit branch push.

```powershell
git branch -d branch-name
git status
```

If a remote branch exists and should be deleted:

```powershell
git push origin --delete branch-name
git status
```

Do not delete the branch before confirming that `main` is pushed and clean.

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
