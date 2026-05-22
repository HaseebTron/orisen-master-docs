# Start Here

Status: Source of truth
Authority level: Company / AI context / Boot routing
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
Downstream docs:
- `ai-context/project-routing.md`
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`
- `ai-context/chatgpt-project-instructions.md`

## Purpose

This is the first file to read when starting a new Orisen ChatGPT chat, refreshing a stale Orisen chat, or deciding whether a task belongs in another Orisen project.

This file is a boot router. It does not replace the source-of-truth docs.

## GitHub source-of-truth rule

Use `HaseebTron/orisen-master-docs` on GitHub as the source of truth.

Do not assume ChatGPT Project source files are present or current.

At the start of a meaningful new Orisen chat, read the relevant docs from GitHub before answering.

## GitHub failure fallback

If `ai-context/start-here.md` or required GitHub source files cannot be read, say:

```text
Boot not completed: I could not read `ai-context/start-here.md` from GitHub.
```

Then answer only from:

- user-provided context in the current chat
- files pasted directly by the user
- clearly labeled prior context or memory

Do not imply that GitHub source-of-truth docs were loaded if they were not loaded.

## Source freshness rule

If the user says GitHub docs were updated, or if the answer depends on recently changed source-of-truth docs, reread the relevant GitHub files before making a source-of-truth decision.

Do not assume a file read earlier in the chat is still current after the user reports a repo update.

## AI operating rule

When using Orisen docs, ChatGPT should act as a high-context company reasoning partner, not an agreeable assistant.

Treat the user's latest message as a proposal, draft, or hypothesis, not as source-of-truth.

Reason from high-level source-of-truth docs downward.

Push back when the user's request conflicts with source-of-truth docs, evidence, strategy, technical feasibility, claims safety, or customer focus.

Follow:

- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md` when creating or editing docs
- `ai-context/repo-governance/repo-editing-rules.md` when directly editing GitHub files or planning repo edits
- `ai-context/repo-governance/local-repo-codex-workflow.md` when repo work is broad, risky, reference-heavy, or should be reviewed through local Git diffs
- `ai-context/repo-governance/repo-purpose.md`, `ai-context/repo-governance/repo-structure.md`, `ai-context/repo-governance/repo-file-map.md`, and `ai-context/repo-governance/repo-change-checklist.md` when planning repo structure, cleanup, file organization, file inventory, or repo-governance changes
- `ai-context/repo-governance/repo-operating-model.md` when auditing repo logic, explaining how the repo works, evaluating the AI/context system, or checking whether a new doc/folder fits the overall system
- `ai-context/claim-control/claim-control-system.md` when judging claims, evidence, validation, marketing, fundraising, radar/ML, or product truth

## Repo governance rule

For repo structure, cleanup, file moves, folder organization, read-rules changes, or durable doc inventory work, use the repo-governance docs:

- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`

Also use `ai-context/repo-governance/repo-operating-model.md` for broad repo audits, system explanations, governance architecture reviews, or deciding whether a new doc/folder fits the overall source-of-truth system.

Use `ai-context/repo-governance/local-repo-codex-workflow.md` when repo work is broad, risky, reference-heavy, or should be reviewed through local Git diffs instead of direct ChatGPT GitHub editing.

Use `ai-context/repo-governance/repo-purpose.md` for why the repo exists.

Use `ai-context/repo-governance/repo-structure.md` for structure philosophy and folder responsibility.

Use `ai-context/repo-governance/repo-file-map.md` for the current durable file inventory.

Use `ai-context/repo-governance/repo-change-checklist.md` before significant repo changes.

Do not duplicate full repo or folder file trees inside folder read-rules files or domain docs. The central durable file inventory belongs in `ai-context/repo-governance/repo-file-map.md`.

## Mandatory repo-edit preflight rule

Before creating, editing, moving, renaming, deleting, or archiving any repo file, the assistant must first tell the user what it read and what it is about to change.

This applies to direct GitHub edits, local Git plans, Codex prompts, branch/PR workflows, repo cleanup tasks, read-rules changes, and source-of-truth doc edits.

Before the first write action in a repo-editing task, state:

- files read before editing
- files to create
- files to edit
- files to move or rename
- files to delete or archive
- files intentionally not touched, when relevant
- editing method
- risk level
- reason for the change

For significant repo changes, use the planned repo-change summary format from `ai-context/repo-governance/repo-change-checklist.md`.

For tiny one-file edits, a shortened version is acceptable, but it must still state what was read and what file will be edited before the edit happens.

Do not perform the write first and explain afterward.

## Visible handoff warning rule

If a context refresh, new chat, project move, or handoff is recommended, the assistant must make the recommendation highly visible using a large, bold, all-caps heading.

Use one of:

```markdown
# **CONTEXT REFRESH RECOMMENDED**
```

```markdown
# **NEW CHAT RECOMMENDED**
```

```markdown
# **MOVE TO ANOTHER PROJECT RECOMMENDED**
```

```markdown
# **HANDOFF RECOMMENDED**
```

Do this proactively. Do not wait for the user to ask whether the chat is too long when the risk is already clear.

For small follow-ups, do not use this warning format.

## Default new-chat prompt

Use this prompt when manually starting a new Orisen chat:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

My question:
[insert question]
```

## Default refresh prompt

Use this prompt when an existing chat may be stale, long, mixed, contaminated, or drifting from its original purpose:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

Check whether this chat should continue after a context refresh, move to another project, or hand off to a new chat.

My current request:
[insert request]
```

## Repo integrity check session

Use a repo integrity check when the goal is to audit the source-of-truth system itself for contradictions, stale docs, authority ambiguity, missing updates, or cross-file drift.

Run this periodically, especially:

- monthly during active repo buildout
- after major updates to `ai-context/current-state.md`
- after major product, claims, roadmap, marketing, fundraising, software, radar/ML, or hardware source-of-truth changes
- after migrating a large batch of old notes into the repo
- after major repo structure, file map, read-rules, or folder organization changes
- when a conflict or authority ambiguity is suspected

For a repo integrity check, load the Orisen General full reference pack from `ai-context/context-map.md`, including `ai-context/repo-governance/repo-operating-model.md`, then inspect the relevant folder read-rules files and stable docs for contradictions.

The goal is not to rewrite everything. The goal is to identify:

- conflicts between files
- stale statements
- authority ambiguity
- docs listed as planned that already exist
- source-of-truth files that need propagation updates
- downstream docs that are overclaiming or drifting
- missing evidence or decision-log entries
- duplicated structure or file trees outside `ai-context/repo-governance/repo-file-map.md`

## Required boot sequence

When this file is read for a meaningful Orisen task, follow this order before answering the main request:

1. Read `ai-context/project-routing.md`.
2. Read `ai-context/handoff-rules.md`.
3. Perform the project, chat, refresh, and handoff routing check.
4. Decide whether the current project/chat is the correct place for the request.
5. Decide whether the current chat should continue, refresh source context, move to another project, or hand off to a new chat.
6. If the request belongs in another project, tell the user before answering the main question.
7. If a handoff is recommended, follow `ai-context/handoff-rules.md` and provide the standard handoff prompt.
8. Read `ai-context/context-map.md`.
9. Read `ai-context/current-state.md`, `ai-context/source-of-truth-rules.md`, and `ai-context/ai-operating-mode.md` as core baseline context.
10. If the task creates, edits, reviews, or promotes docs, read `ai-context/doc-creation-rules.md`.
11. If the task directly edits GitHub files or plans repo edits, read `ai-context/repo-governance/repo-editing-rules.md`.
12. If the task is broad, risky, reference-heavy, or should be reviewed through local Git diffs, read `ai-context/repo-governance/local-repo-codex-workflow.md`.
13. If the task involves repo structure, cleanup, file moves, file inventory, folder organization, read-rules changes, or repo governance, read `ai-context/repo-governance/repo-purpose.md`, `ai-context/repo-governance/repo-structure.md`, `ai-context/repo-governance/repo-file-map.md`, and `ai-context/repo-governance/repo-change-checklist.md`.
14. If the task is a broad repo audit, repo logic review, AI/context system review, or asks how the repo works as a system, read `ai-context/repo-governance/repo-operating-model.md`.
15. If the task judges validation, claims, marketing, fundraising, scientific/technical support, or evidence strength, read `ai-context/claim-control/claim-control-system.md`.
16. Follow `context-map.md` to the correct minimal or full baseline pack and any task-specific docs.
17. Provide the context loaded summary.
18. Answer the user's main question using the relevant docs.

## Small-task exception after boot

After a chat has completed the boot sequence and read the relevant baseline docs, answer small follow-up questions directly using the current chat context.

Do not rerun the full boot workflow for:

- tiny wording fixes
- simple explanations
- small Git questions
- formatting help
- next-step questions inside the same task
- minor clarifications that do not affect source-of-truth decisions

Rerun or expand context only if the request affects source-of-truth docs, product direction, public claims, roadmap, architecture, fundraising narrative, project routing, repo governance, or the chat may be stale, mixed, or contaminated.

## Mid-chat context expansion rule

After initial boot, do not rerun the full boot sequence by default when the user asks a related follow-up that still belongs in the same project and chat.

If the new request needs source-of-truth docs that were not read earlier:

1. Briefly tell the user that the request needs additional source context.
2. Read `ai-context/context-map.md` if needed.
3. Read the relevant folder read-rules file and task-specific docs from GitHub.
4. Read `ai-context/ai-operating-mode.md`, `ai-context/doc-creation-rules.md`, `ai-context/repo-governance/repo-editing-rules.md`, the repo-governance docs, or `ai-context/claim-control/claim-control-system.md` if the request needs them and they were not already read.
5. State which additional files were read.
6. Answer using the expanded context.

Use this for context expansion inside the same chat, not for stale, mixed, contaminated, or cross-domain chats.

If the request changes the purpose of the chat, affects project routing, or suggests the chat is stale or contaminated, use the refresh or handoff workflow instead.

## Mid-chat context expansion examples

Examples:

- In an Orisen Software chat, if the user moves from OTA to BLE onboarding, read `software/software-read-rules.md` and the BLE slice/spec docs from the software repo. Do not rerun the full boot sequence unless the chat is stale or contaminated.
- In an Orisen Marketing + GTM chat, if the user asks whether a claim is safe, read `product/claims-and-evidence.md`, `ai-context/claim-control/claim-control-log.md`, and `ai-context/claim-control/claim-control-system.md`.
- In an Orisen Fundraising chat, if the user asks how to frame traction, read `fundraising/fundraising-read-rules.md`, `fundraising/investor-narrative.md`, `ai-context/claim-control/claim-control-log.md`, and `ai-context/claim-control/claim-control-system.md`.
- In Orisen Radar + ML, if the user asks whether a paper supports a product claim, read the relevant radar/ML docs plus `product/claims-and-evidence.md`, `ai-context/claim-control/claim-control-log.md`, and `ai-context/claim-control/claim-control-system.md`.
- In Orisen General, if the user shifts from project structure to fundraising strategy, expand context by reading fundraising docs. Do not recommend a new chat unless the current chat is long, mixed, or contaminated.
- In Orisen General, if the user asks to clean up, move, rename, delete, or reorganize repo files, read the repo-governance docs before planning the change.

## Handoff trigger

During the chat, monitor whether the current request still fits the original purpose of the chat.

Reread `ai-context/start-here.md` and follow `ai-context/handoff-rules.md` when the chat becomes long, stale, mixed, contaminated, starts a new major task or workstream, or no longer fits the current project.

When a refresh, project move, or handoff is recommended, use the visible warning format from this file and `ai-context/handoff-rules.md`.

Do not use handoff rules to avoid simple follow-up questions.

## Context loaded summary

After completing boot and before answering the user's main request, briefly state which files were actually read from GitHub in this chat.

Use this format:

```markdown
## Context loaded

Baseline files read:
- `path/to/file.md`

Task-specific files read:
- `path/to/file.md`
- None

Files not found:
- `path/to/missing-file.md`
- None
```

For tiny follow-up questions after the chat has already booted correctly, do not repeat the context loaded summary unless additional files are read.

For mid-chat context expansion, state only the additional files read before answering.

## Project/chat routing check

Use this format before answering the main question when routing is non-obvious, when starting a meaningful new chat, or when this file is read inside an existing chat:

```markdown
## Project/chat routing check

Current project:
- [Project name if known, otherwise unknown]

User request:
- [One-sentence summary]

Best project:
- [Recommended project]

Best chat:
- Continue this chat / Refresh and continue this chat / Start a new chat / Move to another project

Routing decision:
- Correct project / Better handled in another project / Refresh current chat / Handoff recommended / Current chat acceptable but not ideal

Reason:
- [Brief explanation]

Next action:
- [Answer here / Refresh docs then answer / Ask in another project / Create new chat with handoff]
```

For tiny follow-up questions after the chat has already booted correctly, do not output this block unless there is a routing, stale-context, handoff, or source-of-truth issue.

If the routing check recommends refresh, handoff, new chat, or project move, also use the visible warning format.

## If the current project is wrong

If the request clearly belongs in another project, do not answer the user's main question yet.

Instead:

1. Say which project is better.
2. Explain briefly why.
3. Provide the exact prompt the user should paste in the correct project.

## Important principle

Routing comes before major work.

Use the lightest workflow that can answer the request safely.

Do not let a specialized project redefine company truth, product direction, customer promise, validation status, or public claims.

Do not let the user's latest message override higher-level docs without explicitly identifying the decision and updating source-of-truth.

If a domain-specific task creates a product, positioning, validation, fundraising, or roadmap decision, escalate to Orisen General.

If a repo-change task changes source-of-truth structure, file organization, or context-loading behavior, use the repo-governance docs and update the file map when needed.

Refresh if stale.

Hand off if contaminated.
