# Handoff Rules

Status: Source of truth
Authority level: Company / AI context / Handoff and refresh routing
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/start-here.md`
- `ai-context/project-routing.md`
- `ai-context/context-map.md`
Downstream docs:
- New-chat handoff prompts
- Chat refresh decisions
- Project move recommendations

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

## Proactive warning rule

The assistant must proactively warn the user when a refresh, new chat, or project move would reduce the risk of mistakes.

Do not wait for the user to ask whether the chat is too long.

A proactive warning is required before doing more major work if any of the following are true:

- The chat has completed a major repo migration, source-of-truth rewrite, evidence-architecture change, or project-structure decision.
- The chat has covered three or more distinct workstreams.
- The previous major task is complete and the user is about to start a new major task.
- The next task would require different baseline docs than the docs used for the current task.
- The next task belongs more naturally in a different Orisen project.
- The chat has become long enough that mixed prior context could affect judgment.
- The user asks “what next?”, “go ahead”, or “do it” after a major task has just finished and the correct place for the next task is not obvious.

If the risk is stale source context but the task is the same, recommend a refresh and continue.

If the risk is contaminated or mixed conversation context, recommend a new chat.

If the risk is project mismatch, recommend moving to the correct Orisen project.

## Required warning format

When recommending a refresh, new chat, or project move, the assistant must use a large, bold, all-caps heading so the user does not miss it.

Use one of these headings:

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

Then give:

- Reason
- Recommended project/chat
- Next action
- Exact prompt if a new chat or different project is recommended

For minor follow-ups, do not use the warning format.

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
# **HANDOFF RECOMMENDED**

Reason:
- [Brief explanation]

Recommended project:
- [Project name]

Prompt to paste in the new chat:
```text
[handoff prompt]
```
```

## Next-step response rule

When the user asks what to do next after a meaningful work item, include a small routing recommendation:

```markdown
Recommended place for the next task:
- Continue this chat / Refresh and continue / Start a new chat / Move to another project
```

If the recommendation is refresh, new chat, handoff, or project move, use the required large, bold, all-caps warning format.

## Important principle

Do not use handoff rules to avoid answering simple follow-up questions.

Use them when continuing in the same chat would create real risk: stale source context, mixed context, wrong project, long chat, new major task, or decision contamination.

When in doubt, warn the user early and briefly. The warning can be short, but it must be visible.
