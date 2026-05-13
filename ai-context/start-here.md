# Start Here

## Purpose of this file

This is the first file to read when starting a new Orisen ChatGPT chat.

Its job is to route the chat before work begins.

It helps determine:

- Whether the current ChatGPT project is the right project for the request
- Whether the question belongs in a new chat or an existing chat
- Whether the chat should be tracked in the chat index
- Which source-of-truth docs should be read before answering

This file is a boot sequence. It does not replace the source-of-truth docs.

## Default new-chat prompt

Use this prompt when starting a new Orisen chat:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

My question:
[insert question]
```

## Required boot sequence

When this file is read, follow this order before answering the user's main question:

1. Read `ai-context/project-routing.md`.
2. Read `ai-context/chat-index.md`.
3. Perform the project and chat routing check.
4. Decide whether the current project/chat is the correct place for the request.
5. If the request belongs in another project or existing chat, tell the user before answering the main question.
6. If the current chat should exist and is meaningful enough to track, update `ai-context/chat-index.md` or provide the exact index entry to add.
7. Read `ai-context/context-map.md`.
8. Follow `context-map.md` to the relevant source-of-truth docs for the task.
9. Answer the user's main question using the relevant docs.

## Project and chat routing check

Use this format before answering the main question when routing is non-obvious or when starting a new meaningful chat:

```markdown
## Project and chat routing check

Current project:
- [Project name if known, otherwise unknown]

User request:
- [One-sentence summary]

Best project:
- [Recommended project]

Best chat:
- Continue this chat / Start a new chat / Use existing chat: [chat title if known]

Routing decision:
- Correct project / Better handled in another project / Existing chat recommended / Current chat acceptable but not ideal

Reason:
- [Brief explanation]

Next action:
- [Answer here / Ask in another project / Continue existing chat / Create new chat]
```

## If the current project is wrong

If the request clearly belongs in another project, do not answer the user's main question yet.

Instead:

1. Say which project is better.
2. Explain briefly why.
3. Provide the exact prompt the user should paste in the correct project.

Use this format:

```markdown
This is better handled in: [Project name]

Reason:
- [Brief reason]

Prompt to paste there:
```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

My question:
[rewritten user question]
```
```

## If an existing chat is better

If `ai-context/chat-index.md` shows an active existing chat that clearly matches the request, recommend continuing that chat instead of creating a new one.

Do not create a new chat-index entry if the better action is to continue an existing chat.

## If the current chat should exist

If the current chat is in the right project and is meaningful enough to track, update `ai-context/chat-index.md` or provide the exact entry to add.

A chat is meaningful enough to track when it involves:

- A new software slice
- A new radar or ML experiment
- A major product or strategy decision
- A new marketing asset or campaign
- A new fundraising asset or outreach sequence
- A new source-of-truth doc
- A major cross-domain decision
- A meaningful implementation/debugging thread that may need to be found later

Do not track tiny one-off clarifications, small wording fixes, or quick questions unless the user explicitly asks.

## Required source-of-truth routing

After the project/chat routing check is complete, read `ai-context/context-map.md` and follow its routing instructions.

For any important Orisen decision, also read:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

Then read the relevant folder context map and task-specific docs.

## Important principle

Routing comes before work.

Do not let a specialized project redefine company truth, product direction, customer promise, validation status, or public claims.

If a domain-specific task creates a product, positioning, validation, fundraising, or roadmap decision, escalate to Orisen General.