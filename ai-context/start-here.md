# Start Here

## Purpose of this file

This is the first file to read when starting a new Orisen ChatGPT chat or when an existing Orisen chat may need a context refresh or handoff decision.

Its job is to route the chat before work begins or before major work continues.

It helps determine:

- Whether the current ChatGPT project is the right project for the request
- Whether the question belongs in a new chat or an existing chat
- Whether the current chat should continue, refresh context, or hand off to a new chat
- Whether the chat should be tracked in the chat index
- What the official chat-index title should be
- What the user should manually rename the ChatGPT sidebar chat to, if desired
- Which source-of-truth docs should be read before answering

This file is a boot sequence. It does not replace the source-of-truth docs.

## Purpose of prompting ChatGPT to read this file

The following is the purpose of prompting the reading of `start-here.md`, in ChatGPT chats:

- **Give correct context**
    - **Boot the chat properly**: make GPT read the workflow rules before doing meaningful Orisen work.
    - **Refresh stale context**: if the chat is still on the same task but docs/context may be stale, reread the relevant source docs before answering.
    - **Route to source-of-truth docs**: after project/chat routing, read `context-map.md`, then the relevant docs like `current-state.md`, `source-of-truth-rules.md`, product docs, software docs, etc.
    - **Prevent wrong-context work**: stop GPT from answering in the wrong project, with stale assumptions, or with a chat that should have been restarted.
- **Detect if this is the right place to discuss a topic**
    - **Check the right project**: decide whether the question belongs in Orisen General, Software, Radar + ML, Marketing, Fundraising, Hardware, etc.
    - **Check the right chat**: decide whether this should continue here, move to an existing indexed chat, or start a new chat.
- **Help user to move to a diff chat**
    - **Detect contamination**: if the chat is long, mixed, unfocused, or has outdated context, decide whether a new chat is safer.
    - **Handle handoff decisions**: if a new chat is better, generate the standard handoff prompt using the repo rules.
- **Tracking chats**
    - **Use `chat-index.md`**: check existing tracked chats and update or suggest an entry when a chat is meaningful enough to track.
    - **Name the chat**: decide the official `chat-index.md` title and remind you what to manually rename the ChatGPT sidebar chat to.
- **Remind User to rename chat to the right name in accordance to the database.**

## Default new-chat prompt

Use this prompt when starting a new Orisen chat:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

My question:
[insert question]
```

## Default refresh prompt inside an existing chat

Use this prompt when an existing chat may be stale, long, unfocused, contaminated by mixed context, or drifting from its original purpose:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

Check whether this chat should continue after a context refresh, move to another project, continue in an existing indexed chat, or hand off to a new chat.

My current request:
[insert request]
```

## Refresh-only output format

If the user only asks to read `ai-context/start-here.md` and does not provide a new question or task, treat it as a refresh/status check for the current chat.

Do not output the full project/chat routing block unless there is a routing problem, handoff recommendation, wrong-project issue, or other important warning.

Use this concise format:

```markdown
## Context refresh complete

I ran the routing/refresh workflow.

Docs read:
- `ai-context/start-here.md`
- `ai-context/project-routing.md`
- `ai-context/chat-index.md`
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`

Current chat status: **[Still correct / Refresh recommended / Handoff recommended / Wrong project / Existing chat recommended]**

Recommended action: **[Continue here / Start a new chat / Move to another project / Continue an existing indexed chat]**

Chat length status: **[Beginning / Still safe / Mid-way / Getting long / Nearly maxed / Start a new chat recommended]**

Suggested sidebar title: **[Title]**

Sidebar title confirmation: **[CONFIRMED / NOT CONFIRMED / UNKNOWN / NOT NEEDED]**

If you have a new task, paste it now and I will route it before answering.
```

Use rough chat length labels only. Do not claim an exact percentage of context usage.

If the sidebar title is already confirmed in `ai-context/chat-index.md`, use `Sidebar title confirmation: **CONFIRMED**` and do not remind the user to rename the chat.

If the sidebar title is not confirmed, use `Sidebar title confirmation: **NOT CONFIRMED**` and include a short reminder to manually rename the current ChatGPT sidebar chat to the suggested title.

## Required boot sequence

When this file is read, follow this order before answering the user's main question:

1. Read `ai-context/project-routing.md`.
2. Read `ai-context/chat-index.md`.
3. Read `ai-context/handoff-rules.md`.
4. Perform the project, chat, refresh, and handoff routing check.
5. Decide whether the current project/chat is the correct place for the request.
6. Decide whether the current chat should continue, refresh source context, move to another project, continue in an existing indexed chat, or hand off to a new chat.
7. Decide the official chat-index title for the current or recommended chat if the chat is meaningful enough to track.
8. Check whether the sidebar title has already been confirmed in `ai-context/chat-index.md`.
9. Tell the user the suggested ChatGPT sidebar title to manually rename the chat to, if relevant and not already confirmed.
10. If the user says they renamed the chat, compare the provided title exactly against the suggested sidebar title.
11. If the title matches exactly, update `ai-context/chat-index.md` to mark the sidebar title as confirmed.
12. If the title does not match exactly, tell the user the expected title.
13. If the request belongs in another project or existing chat, tell the user before answering the main question.
14. If a handoff is recommended, follow `ai-context/handoff-rules.md` and provide the standard handoff prompt.
15. If the current chat should exist and is meaningful enough to track, update `ai-context/chat-index.md` or provide the exact index entry to add.
16. Read `ai-context/context-map.md`.
17. Follow `context-map.md` to the relevant source-of-truth docs for the task.
18. Answer the user's main question using the relevant docs.

## Project, chat, refresh, and handoff routing check

Use this format before answering the main question when routing is non-obvious, when starting a new meaningful chat, or when this file is read inside an existing chat:

```markdown
## Project/chat routing check

Current project:
- [Project name if known, otherwise unknown]

User request:
- [One-sentence summary]

Best project:
- [Recommended project]

Best chat:
- Continue this chat / Refresh and continue this chat / Start a new chat / Use existing chat: [chat title if known]

Official chat-index title:
- [Title that should be used in ai-context/chat-index.md]

Suggested ChatGPT sidebar title:
- [Title the user should manually rename the sidebar chat to, if desired]

Sidebar title status:
- Confirmed / Not confirmed / Unknown / Not needed

Routing decision:
- Correct project / Better handled in another project / Existing chat recommended / Refresh current chat / Handoff recommended / Current chat acceptable but not ideal

Reason:
- [Brief explanation]

Next action:
- [Answer here / Refresh docs then answer / Ask in another project / Continue existing chat / Create new chat with handoff]
```

## Chat title reminder rule

The assistant cannot reliably rename the ChatGPT sidebar title automatically.

When this file is read and the current or recommended chat is meaningful enough to track, the assistant should check `ai-context/chat-index.md` for sidebar title status.

If the sidebar title is already confirmed, do not remind the user to rename the chat again.

If the sidebar title is not confirmed, the assistant should provide:

- The official chat-index title
- The suggested ChatGPT sidebar title
- A short reminder that the user may manually rename the ChatGPT sidebar chat to match

Use this format:

```markdown
Suggested sidebar title:
- [Title]
```

The official title in `ai-context/chat-index.md` is the source of truth. The sidebar title is only a convenience for the user.

Do not interrupt tiny one-off questions only to suggest a title. Use this title reminder for meaningful chats, handoffs, refreshed major work, or new indexed work.

## Sidebar title confirmation rule

If the user says they renamed the chat to a specific title, compare the user's provided title exactly against the suggested ChatGPT sidebar title.

If the title matches exactly:

1. Acknowledge the match.
2. Update `ai-context/chat-index.md` for the relevant chat entry.
3. Set `Confirmed renamed by user` to `Yes`.
4. Set `Confirmed sidebar title` to the matched title.
5. Do not remind the user to rename this chat again in future `start-here.md` refreshes.

If the title does not match exactly:

1. Tell the user it does not exactly match.
2. Show the expected title.
3. Do not mark the sidebar title as confirmed.

If the relevant chat entry does not exist yet, create or suggest the entry first, then record the sidebar title confirmation.

## If the current project is wrong

If the request clearly belongs in another project, do not answer the user's main question yet.

Instead:

1. Say which project is better.
2. Explain briefly why.
3. Provide the exact prompt the user should paste in the correct project.
4. Include the suggested ChatGPT sidebar title for the recommended chat if it is meaningful enough to track and not already confirmed.

Use this format:

```markdown
This is better handled in: [Project name]

Reason:
- [Brief reason]

Suggested sidebar title:
- [Title]

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

If the existing indexed chat has an official title, tell the user that title so they can find the chat. Only remind them to rename the sidebar chat if the sidebar title has not already been confirmed.

## If the current chat should refresh and continue

If the current request still fits the original purpose of the chat, but source context may be stale, continue in this chat after reading the relevant source-of-truth docs through `ai-context/context-map.md`.

Refreshing is appropriate when the same task is continuing and the main risk is stale source context, not contaminated conversation context.

If the refreshed chat is meaningful enough to track, remind the user of the suggested sidebar title only if it has not already been confirmed.

## If a new chat is better

If the chat is long, mixed, contaminated by outdated context, or the request is a new major task, recommend a handoff to a new chat using `ai-context/handoff-rules.md`.

Do not do major new work in a chat that should be handed off unless the user explicitly asks to continue here.

The handoff recommendation should include the recommended official chat-index title and the suggested ChatGPT sidebar title, unless the sidebar title for that chat has already been confirmed.

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

After the project/chat/refresh/handoff routing check is complete, read `ai-context/context-map.md` and follow its routing instructions.

For any important Orisen decision, also read:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`

Then read the relevant folder context map and task-specific docs.

## Important principle

Routing comes before work.

Do not let a specialized project redefine company truth, product direction, customer promise, validation status, or public claims.

If a domain-specific task creates a product, positioning, validation, fundraising, or roadmap decision, escalate to Orisen General.

Refresh if stale.

Hand off if contaminated.
