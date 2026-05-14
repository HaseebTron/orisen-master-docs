# Start Here

## Purpose of this file

This is the first file to read when starting a new Orisen ChatGPT chat or when an existing Orisen chat may need a context refresh or handoff decision.

Its job is to route the chat before work begins or before major work continues.

It helps determine:

- Whether the current ChatGPT project is the right project for the request
- Whether the current chat should continue, refresh context, move projects, or hand off to a new chat
- Which source-of-truth docs should be read before answering

This file is a boot sequence. It does not replace the source-of-truth docs.

## GitHub source-of-truth rule

Use `HaseebTron/orisen-master-docs` on GitHub as the source of truth.

Do not assume ChatGPT Project source files are present or current.

At the start of a new Orisen chat, read the baseline docs required for the current project and task from GitHub.

After the baseline docs are read, read additional task-specific docs only as needed.

## Purpose of prompting ChatGPT to read this file

Prompting ChatGPT to read `start-here.md` should:

- Boot the chat properly before meaningful Orisen work
- Refresh stale context when needed
- Route the task to the right project and source-of-truth docs
- Prevent wrong-context work
- Detect when a chat is long, mixed, unfocused, or contaminated
- Decide whether to continue, refresh, move projects, or hand off to a new chat

## Default new-chat prompt

Use this prompt when manually starting a new Orisen chat:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

My question:
[insert question]
```

Project Instructions may also require this file to be read automatically at the start of every new chat.

## Default refresh prompt inside an existing chat

Use this prompt when an existing chat may be stale, long, unfocused, contaminated by mixed context, or drifting from its original purpose:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

Check whether this chat should continue after a context refresh, move to another project, or hand off to a new chat.

My current request:
[insert request]
```

## Small-task exception after boot

After a chat has completed the boot sequence and read the relevant baseline docs, answer small follow-up questions directly using the current chat context.

Do not rerun the full boot workflow for tiny wording fixes, simple explanations, small Git questions, formatting help, or next-step questions inside the same task.

Rerun the workflow only if the request affects source-of-truth docs, product direction, public claims, roadmap, architecture, fundraising narrative, project routing, or the chat may be stale, mixed, or contaminated.

## Mid-chat context expansion rule

After the initial boot sequence, the assistant may answer small follow-up questions using the current chat context.

If a later user request still belongs in the current project and chat, but requires source-of-truth docs that were not read earlier, do not rerun the full boot sequence by default.

Instead:

1. Briefly tell the user that the request needs additional source context.
2. Read `ai-context/context-map.md` if needed.
3. Read the relevant folder context map and task-specific docs from GitHub.
4. State which additional files were read.
5. Answer the user's request using the expanded context.

Use this for context expansion inside the same chat, not for stale, mixed, contaminated, or cross-domain chats.

If the new request changes the purpose of the chat, affects project routing, or suggests the chat is stale or contaminated, use the refresh or handoff workflow instead.

## Ongoing chat monitoring rule

During the chat, monitor whether the current request still fits the original purpose of the chat.

If the chat becomes long, stale, mixed, contaminated, or the user starts a new major task, reread `ai-context/start-here.md` and check whether to:

- Continue here
- Refresh context and continue here
- Move to another project
- Hand off to a new chat

Do not do major new work in a chat that should be handed off unless the user explicitly asks to continue here.

## Required boot sequence

When this file is read, follow this order before answering the user's main question:

1. Read `ai-context/project-routing.md`.
2. Read `ai-context/handoff-rules.md`.
3. Perform the project, chat, refresh, and handoff routing check.
4. Decide whether the current project/chat is the correct place for the request.
5. Decide whether the current chat should continue, refresh source context, move to another project, or hand off to a new chat.
6. If the request belongs in another project, tell the user before answering the main question.
7. If a handoff is recommended, follow `ai-context/handoff-rules.md` and provide the standard handoff prompt.
8. Read `ai-context/context-map.md`.
9. Follow `context-map.md` to the project baseline docs and relevant task-specific source-of-truth docs.
10. Answer the user's main question using the relevant docs.

## Project, chat, refresh, and handoff routing check

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

## If the current chat should refresh and continue

If the current request still fits the original purpose of the chat, but source context may be stale, continue in this chat after reading the relevant source-of-truth docs through `ai-context/context-map.md`.

Refreshing is appropriate when the same task is continuing and the main risk is stale source context, not contaminated conversation context.

## If a new chat is better

If the chat is long, mixed, contaminated by outdated context, or the request is a new major task, recommend a handoff to a new chat using `ai-context/handoff-rules.md`.

## Required source-of-truth routing

After the project/chat/refresh/handoff routing check is complete, read `ai-context/context-map.md` and follow its routing instructions.

For any important Orisen decision, also read:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

Then read the relevant project baseline doc pack, folder context map, and task-specific docs.

## Important principle

Routing comes before major work.

Use the lightest workflow that can answer the request safely.

Do not let a specialized project redefine company truth, product direction, customer promise, validation status, or public claims.

If a domain-specific task creates a product, positioning, validation, fundraising, or roadmap decision, escalate to Orisen General.

Refresh if stale.

Hand off if contaminated.
