# Start Here

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
- `validation/evidence-standard.md` when judging claims, evidence, validation, marketing, fundraising, radar/ML, or product truth

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
11. If the task judges validation, claims, marketing, fundraising, scientific/technical support, or evidence strength, read `validation/evidence-standard.md`.
12. Follow `context-map.md` to the correct minimal or full baseline pack and any task-specific docs.
13. Provide the context loaded summary.
14. Answer the user's main question using the relevant docs.

## Small-task exception after boot

After a chat has completed the boot sequence and read the relevant baseline docs, answer small follow-up questions directly using the current chat context.

Do not rerun the full boot workflow for:

- tiny wording fixes
- simple explanations
- small Git questions
- formatting help
- next-step questions inside the same task
- minor clarifications that do not affect source-of-truth decisions

Rerun or expand context only if the request affects source-of-truth docs, product direction, public claims, roadmap, architecture, fundraising narrative, project routing, or the chat may be stale, mixed, or contaminated.

## Mid-chat context expansion rule

After initial boot, do not rerun the full boot sequence by default when the user asks a related follow-up that still belongs in the same project and chat.

If the new request needs source-of-truth docs that were not read earlier:

1. Briefly tell the user that the request needs additional source context.
2. Read `ai-context/context-map.md` if needed.
3. Read the relevant folder context map and task-specific docs from GitHub.
4. Read `ai-context/ai-operating-mode.md`, `ai-context/doc-creation-rules.md`, or `validation/evidence-standard.md` if the request needs them and they were not already read.
5. State which additional files were read.
6. Answer using the expanded context.

Use this for context expansion inside the same chat, not for stale, mixed, contaminated, or cross-domain chats.

If the request changes the purpose of the chat, affects project routing, or suggests the chat is stale or contaminated, use the refresh or handoff workflow instead.

## Mid-chat context expansion examples

Examples:

- In an Orisen Software chat, if the user moves from OTA to BLE onboarding, read `software/software-context-map.md` and the BLE slice/spec docs from the software repo. Do not rerun the full boot sequence unless the chat is stale or contaminated.
- In an Orisen Marketing + GTM chat, if the user asks whether a claim is safe, read `product/claims-and-evidence.md`, `validation/evidence-log.md`, and `validation/evidence-standard.md`.
- In an Orisen Fundraising chat, if the user asks how to frame traction, read `fundraising/fundraising-context-map.md`, `fundraising/investor-narrative.md`, `validation/evidence-log.md`, and `validation/evidence-standard.md`.
- In Orisen Radar + ML, if the user asks whether a paper supports a product claim, read the relevant radar/ML docs plus `product/claims-and-evidence.md`, `validation/evidence-log.md`, and `validation/evidence-standard.md`.
- In Orisen General, if the user shifts from project structure to fundraising strategy, expand context by reading fundraising docs. Do not recommend a new chat unless the current chat is long, mixed, or contaminated.

## Handoff trigger

During the chat, monitor whether the current request still fits the original purpose of the chat.

Reread `ai-context/start-here.md` and check for refresh, project move, or handoff when:

- the chat becomes long, stale, mixed, or contaminated
- the user starts a new major task
- a new software slice starts
- a new radar/ML experiment starts
- a new marketing asset or campaign starts
- a new fundraising asset or outreach sequence starts
- the request no longer fits the current project

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

For tiny follow-up questions after the chat has already booted, do not repeat the context loaded summary unless additional files are read.

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

Refresh if stale.

Hand off if contaminated.
