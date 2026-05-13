# Handoff Rules

## Purpose of this file

This file defines when an Orisen ChatGPT chat should continue, refresh its source context, move to another project, or hand off to a new chat.

It also defines the standard handoff prompt format.

Read this file during the `ai-context/start-here.md` boot sequence after reading:

- `ai-context/project-routing.md`
- `ai-context/chat-index.md`

This file does not replace source-of-truth docs. It only decides whether the current chat is still a safe place to continue the work.

## Core rule

Refresh if the same task is continuing but context may be stale.

Start a new chat if the chat has become long, mixed, contaminated, or the user is starting a new major task.

Move to another project if the request belongs in a more appropriate Orisen ChatGPT project.

## Decision options

When this file is read, choose one of these actions:

1. Continue in this chat after refreshing source context.
2. Continue in this chat without a full refresh.
3. Recommend starting a new chat in the same project.
4. Recommend moving to another Orisen project.
5. Recommend continuing an existing indexed chat.

## When to refresh source context and continue

Refresh source context and continue in the current chat when:

- The current request still fits the original purpose of the chat.
- The same task is continuing.
- The chat is not badly mixed across domains.
- The user may have updated source docs since the last context read.
- The answer depends on current source-of-truth docs.
- The assistant may be relying on stale assumptions.
- A decision affects product, claims, marketing, fundraising, roadmap, software architecture, or cross-domain strategy.

Refreshing means reading `ai-context/start-here.md` and following its routing path to the relevant docs.

## When to recommend a new chat

Recommend starting a new chat when:

- A new major task starts.
- A new software slice starts.
- A new radar or ML experiment starts.
- A new marketing asset or campaign starts.
- A new fundraising asset or outreach sequence starts.
- The previous task is complete.
- The chat is long enough that a clean handoff would reduce mistakes.
- The chat has shifted across multiple domains.
- The chat contains mixed or outdated context that may contaminate the answer.
- The user wants a clean review.
- The current request no longer fits the initial purpose of the chat.

A new chat is usually better than a refresh when the problem is not stale docs, but contaminated conversation context.

## When to move to another project

Recommend moving to another Orisen project when `ai-context/project-routing.md` indicates that another project is clearly better for the task.

Examples:

- A code implementation task belongs in Orisen Software.
- A radar signal-processing task belongs in Orisen Radar + ML.
- A landing page copy task belongs in Orisen Marketing + GTM.
- A pitch deck/outreach task belongs in Orisen Fundraising.
- A company/product/claims/roadmap decision belongs in Orisen General.

If the request belongs in another project, do not answer the main question yet. Provide the exact prompt to paste in the better project.

## When to continue an existing indexed chat

Recommend continuing an existing chat when `ai-context/chat-index.md` shows an active chat with the same project, same task, and same working context.

Do not create a new chat-index entry if an existing chat is clearly better.

## Status labels for chat-index.md

Use these statuses in `ai-context/chat-index.md`:

- `Active`: The chat is still the recommended place for that task.
- `Completed`: The task was completed and no further work is expected in that chat.
- `Handoff Recommended`: The task may continue, but a new chat is safer.
- `Superseded`: A newer chat has replaced this chat.
- `Archived`: The chat is kept for reference only.

## When to mark Handoff Recommended

Mark a chat as `Handoff Recommended` when:

- The chat has become long or unfocused.
- A clean handoff would reduce mistakes.
- The task is not fully complete, but the current chat is no longer ideal.
- The chat contains useful context but also enough clutter to create risk.

## When to mark Superseded

Mark a chat as `Superseded` when:

- A new chat has taken over the task.
- A better project/chat now exists for the work.
- The old chat should no longer be used for active work.

When possible, include the title of the replacement chat in the `Current outcome` or `Follow-up needed` section.

## Official chat title rule

The official chat title is the title in `ai-context/chat-index.md`.

The ChatGPT sidebar title is optional convenience metadata.

The assistant cannot reliably rename the ChatGPT sidebar title automatically.

When creating a new chat-index entry, the assistant should provide a suggested sidebar title for the user to manually rename the chat if desired.

## Handoff prompt format

When recommending a new chat, provide a handoff prompt in this format:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

This is a continuation from a previous Orisen chat.

Previous project:
- [Project name]

Previous chat/index title:
- [Official chat-index title]

Why this new chat exists:
- [New major task / chat too long / topic shift / cleaner review / moved project / other reason]

What was completed:
- [Concise summary]

Important decisions:
- [Decision 1]
- [Decision 2]

Files created or updated:
- `[file/path]`

Current status:
- [Clean / in progress / blocked / needs review / unknown]

Current task:
- [What I want help with now]

Before answering:
- Confirm whether this is the correct project/chat for the task.
- If another project or existing chat is better, tell me before doing the work.
```

## Handoff response format

When recommending a handoff, use this concise format:

```markdown
## Handoff recommended

Reason:
- [Brief explanation]

Recommended project:
- [Project name]

Recommended chat/index title:
- [Title]

Suggested ChatGPT sidebar title:
- [Title]

Prompt to paste in the new chat:
```text
[handoff prompt]
```

Chat-index update:
- [Update made / Exact update to make / Not needed]
```

## Updating chat-index.md

If GitHub write access is available and the chat is meaningful enough to track, update `ai-context/chat-index.md` when:

- A new meaningful chat is created.
- A chat status changes to `Completed`, `Handoff Recommended`, `Superseded`, or `Archived`.
- A replacement chat supersedes an older chat.
- A major decision or file update should be discoverable later.

If direct updating is not possible, provide the exact markdown entry or edit for the user to paste.

## Important principle

Do not use handoff rules to avoid answering simple follow-up questions.

Use them when continuing in the same chat would create real risk: stale source context, mixed context, wrong project, long chat, new major task, or decision contamination.