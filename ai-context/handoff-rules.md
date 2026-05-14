# Handoff Rules

## Purpose of this file

This file defines when an Orisen ChatGPT chat should continue, refresh its source context, move to another project, or hand off to a new chat.

It also defines the standard handoff prompt format.

Read this file during the `ai-context/start-here.md` boot sequence after reading:

- `ai-context/project-routing.md`

This file does not replace source-of-truth docs. It only decides whether the current chat is still a safe place to continue the work.

## Core rule

Refresh if the same task is continuing but source context may be stale.

Start a new chat if the chat has become long, mixed, contaminated, or the user is starting a new major task.

Move to another project if the request belongs in a more appropriate Orisen ChatGPT project.

## Decision options

When this file is read, choose one of these actions:

1. Continue in this chat after refreshing source context.
2. Continue in this chat without a full refresh.
3. Recommend starting a new chat in the same project.
4. Recommend moving to another Orisen project.

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

## Handoff prompt format

When recommending a new chat, provide a handoff prompt in this format:

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

This is a continuation from a previous Orisen chat.

Previous project:
- [Project name]

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
- If another project is better, tell me before doing the work.
```

## Handoff response format

When recommending a handoff, use this concise format:

```markdown
## Handoff recommended

Reason:
- [Brief explanation]

Recommended project:
- [Project name]

Prompt to paste in the new chat:
```text
[handoff prompt]
```
```

## Important principle

Do not use handoff rules to avoid answering simple follow-up questions.

Use them when continuing in the same chat would create real risk: stale source context, mixed context, wrong project, long chat, new major task, or decision contamination.
