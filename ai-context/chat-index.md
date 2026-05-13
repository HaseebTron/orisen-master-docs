# Chat Index

## Purpose of this file

This file tracks meaningful ChatGPT chats across Orisen projects.

It helps decide:

- Whether a new question belongs in an existing chat
- Whether a new chat should be created
- Which project should handle a question
- What decisions have already been made
- Which docs or repo files were created or updated
- When a chat is becoming too long, stale, contaminated, or unfocused
- Whether a chat should be marked as completed, handed off, superseded, or archived
- Whether the user has already confirmed the ChatGPT sidebar title for a tracked chat

This file should be read during the `ai-context/start-here.md` boot sequence before the assistant answers the user's main question.

## Core rule

A chat should have one clear job.

If a chat starts covering a new slice, new domain, new asset, or major new decision, create a new chat and add an entry to this index if the chat is meaningful enough to track.

Do not track every tiny one-off question.

## Official chat title rule

The official chat title is the title in this file.

The ChatGPT sidebar title is optional convenience metadata.

The assistant cannot reliably rename the ChatGPT sidebar title automatically.

When creating a new chat-index entry, the assistant should provide a suggested ChatGPT sidebar title for the user to manually rename the chat if desired.

If the user confirms that the sidebar chat has been renamed to the suggested title, record that confirmation in the relevant chat entry.

If the sidebar title is confirmed, future reads of `ai-context/start-here.md` should not keep reminding the user to rename that chat.

## Status labels

Use these statuses:

- `Active`: The chat is still the recommended place for that task.
- `Completed`: The task was completed and no further work is expected in that chat.
- `Handoff Recommended`: The task may continue, but a new chat is safer.
- `Superseded`: A newer chat has replaced this chat.
- `Archived`: The chat is kept for reference only.

## Sidebar title status labels

Use these values:

- `Unknown`: The sidebar title status has not been checked or recorded.
- `Not confirmed`: The assistant suggested a sidebar title, but the user has not confirmed renaming the chat.
- `Confirmed`: The user stated that the sidebar chat was renamed to the suggested title.
- `Not needed`: This chat does not need sidebar title tracking.

The assistant cannot independently verify the sidebar title. Confirmation means the user reported the rename.

## What counts as meaningful enough to track

Track chats that involve:

- A new software slice
- A meaningful debugging thread
- A new radar or ML experiment
- A major product or strategy decision
- A new marketing asset or campaign
- A new fundraising asset or outreach sequence
- A new source-of-truth doc
- A major cross-domain decision
- A decision likely to be referenced later

Do not normally track:

- Tiny wording fixes
- One-off clarifications
- Quick formatting questions
- Small Git questions
- Short tactical questions with no lasting decision

## Required routing process for new or refreshed chats

When a new chat starts or an existing chat asks the assistant to read `ai-context/start-here.md`, the assistant should:

1. Read this file.
2. Check whether an existing active chat already matches the user's task.
3. Check whether the current project is the correct project using `ai-context/project-routing.md`.
4. Check whether the current chat should continue, refresh source context, hand off, move projects, or use an existing indexed chat using `ai-context/handoff-rules.md`.
5. Check whether the relevant chat's sidebar title status is already confirmed.
6. If an existing chat is better, recommend using that chat instead of creating a new one.
7. If another project is better, recommend the correct project before answering.
8. If a new chat is safer, follow `ai-context/handoff-rules.md` and provide the standard handoff prompt.
9. If the current chat should exist and is meaningful enough to track, update this file or provide the exact entry to add.
10. Only after routing is resolved should the assistant continue to `ai-context/context-map.md` and answer the main task.

## Response format for routing recommendation

Use this format when routing is non-obvious:

```markdown
## Chat routing recommendation

Best project:
- [Project name]

Best chat:
- Continue this chat / Refresh and continue this chat / Start a new chat / Use existing chat: [chat title]

Sidebar title status:
- Confirmed / Not confirmed / Unknown / Not needed

Reason:
- [Brief explanation]

Suggested first prompt:
- [Prompt to paste if another project or chat is better]
```

## Chat entry template

Use this template for meaningful chats:

```markdown
## [YYYY-MM-DD] [Project Name] - [Official Index Title]

### Project

- Project:

### Official index title

- Title:

### Suggested ChatGPT sidebar title

- Title:

### Sidebar title status

- Status: Unknown / Not confirmed / Confirmed / Not needed
- Confirmed renamed by user: Yes / No / Unknown
- Confirmed sidebar title:

### Status

- Active / Completed / Handoff Recommended / Superseded / Archived

### Main purpose

- Short explanation of what this chat is for.

### Topics covered

- Topic 1
- Topic 2
- Topic 3

### Key decisions made

- Decision 1
- Decision 2
- Decision 3

### Files created or updated

- `path/to/file.md`
- `path/to/file.cpp`
- `path/to/file.ts`

### Current outcome

- What was accomplished?

### Follow-up needed

- What should happen next?

### Continue this chat if...

- Criteria for when this chat should be reused.

### Start a new chat instead if...

- Criteria for when a new chat is better.

### Related chats

- Related chat name or project, if any.
```

## Sidebar title confirmation workflow

If the user says they renamed the current chat to a specific title:

1. Compare the provided title exactly against the suggested ChatGPT sidebar title for the relevant chat entry.
2. If the title matches exactly, update the chat entry:
    - `Status: Confirmed`
    - `Confirmed renamed by user: Yes`
    - `Confirmed sidebar title: [matched title]`
3. If the title does not match exactly, do not mark it confirmed.
4. Tell the user the exact expected title.
5. If no relevant chat entry exists yet, create or suggest the chat entry first, then record the confirmation.

Once a sidebar title is confirmed, do not keep reminding the user to rename that chat during future `start-here.md` refreshes.

## When to update a chat entry

Update a chat entry when:

- A new meaningful chat is created.
- A chat status changes.
- A chat becomes too long or contaminated and should be marked `Handoff Recommended`.
- A new chat supersedes an older chat.
- A sidebar title is confirmed by the user.
- A meaningful decision is made.
- Meaningful files are created or updated.
- The current outcome or follow-up changes.

## Project-specific guidance

### Orisen General

Track chats about:

- Product direction
- Source-of-truth docs
- Strategy decisions
- Cross-domain decisions
- Project routing decisions

Start a new chat when:

- A new major source-of-truth doc is being created
- A new strategic decision is being made
- The topic shifts from one domain to another

### Orisen Software

Track chats by implementation slice or meaningful debug thread.

Recommended pattern:

- One chat per slice
- One follow-up debug chat if needed
- One review/commit chat if needed

Example chat titles:

- Slice 5 - Mobile App
- Slice 6 - BLE Setup and Onboarding
- Slice 7 - Device Claiming
- OTA Debug Follow-up

Start a new chat when:

- A slice is completed and committed
- A new slice begins
- The bug is unrelated to the active slice
- You need a clean code review

### Orisen Radar + ML

Track chats by research or experiment topic.

Example chat titles:

- XM125 RRV Extraction
- V-LD3 vs XM125 Sensor Decision
- Radar Sleep Stage Paper Review
- Sleep Stage Feature Pipeline
- Artificial Sleep Phase Transitioning Feasibility

Start a new chat when:

- Switching papers
- Switching radar modules
- Moving from research to implementation
- Moving from signal extraction to ML modeling

### Orisen Marketing + GTM

Track chats by asset or campaign.

Example chat titles:

- Homepage Rewrite
- LinkedIn Content Pillars
- Waitlist Conversion Copy
- Reddit Research
- Founder Story Posts

Start a new chat when:

- Starting a new marketing asset
- Switching platforms
- Moving from strategy to copywriting
- The asset has been finalized

### Orisen Fundraising

Track chats by deck, investor type, or outreach sequence.

Example chat titles:

- Teaser Deck V1
- Investor Email Sequence
- Angel Outreach
- Traction Slide
- Investor FAQ

Start a new chat when:

- A deck version is completed
- You switch investor segments
- You move from narrative to specific outreach
- You need a fresh investor-style review

### Orisen Hardware

Track chats by subsystem or decision.

Example chat titles:

- Speaker System Selection
- Radar Placement
- Wall Mount Design
- Battery Backup Architecture
- PCB Architecture Review

Start a new chat when:

- Switching hardware subsystems
- Moving from concept to detailed design
- A major hardware decision has been made and documented

## Existing tracked chats

| Date | Project | Official index title | Status | Sidebar title status | Purpose | Continue this chat if... |
|---|---|---|---|---|---|---|
| 2026-05-13 | Orisen General | Orisen General - Product Overview Source-of-Truth Draft | Completed | Confirmed | Create clean Orisen source-of-truth docs from existing context and draft inputs, especially the product/product overview direction. | The task is a small follow-up to the product overview doc. |
| 2026-05-13 | Orisen General | Orisen General - Chat Routing and Handoff Workflow | Active | Confirmed | Design and maintain the Orisen ChatGPT project routing, chat indexing, context refresh, handoff, and sidebar-title reminder workflow. | The task is about Orisen GPT project routing, chat indexing, context refresh, handoff rules, or source-of-truth workflow architecture. |

## Detailed tracked chat entries

## 2026-05-13 Orisen General - Product Overview Source-of-Truth Draft

### Project

- Project: Orisen General

### Official index title

- Title: Orisen General - Product Overview Source-of-Truth Draft

### Suggested ChatGPT sidebar title

- Title: Orisen General - Product Overview Source-of-Truth Draft

### Sidebar title status

- Status: Confirmed
- Confirmed renamed by user: Yes
- Confirmed sidebar title: Orisen General - Product Overview Source-of-Truth Draft

### Status

- Completed

### Main purpose

- Create clean Orisen source-of-truth docs from existing context and draft inputs, especially the product/product overview direction.

### Topics covered

- Orisen source-of-truth docs
- Product overview structure
- Distinction between engineering MVP, first customer-ready product, and long-term vision
- Careful claims around grogginess reduction, sleep-stage detection, and artificial sleep phase transitioning

### Key decisions made

- Product docs should not let MVP/software scope shrink the first customer-ready product vision.
- Product claims should stay careful around grogginess reduction, sleep-stage detection, and artificial sleep phase transitioning.
- Source-of-truth docs should distinguish engineering MVP, first customer-ready product, and long-term product direction.

### Files created or updated

- `product/product-overview.md`

### Current outcome

- Product overview source-of-truth doc was created or drafted.

### Follow-up needed

- Continue creating additional source-of-truth docs as needed.

### Continue this chat if...

- The task is a small follow-up to the product overview doc.

### Start a new chat instead if...

- A new source-of-truth doc, new strategic decision, or different Orisen domain is being started.

### Related chats

- Orisen General - Chat Routing and Handoff Workflow

## 2026-05-13 Orisen General - Chat Routing and Handoff Workflow

### Project

- Project: Orisen General

### Official index title

- Title: Orisen General - Chat Routing and Handoff Workflow

### Suggested ChatGPT sidebar title

- Title: Orisen General - Chat Routing and Handoff Workflow

### Sidebar title status

- Status: Confirmed
- Confirmed renamed by user: Yes
- Confirmed sidebar title: Orisen General - Chat Routing and Handoff Workflow

### Status

- Active

### Main purpose

- Design and maintain the Orisen ChatGPT project routing, chat indexing, context refresh, handoff, and sidebar-title reminder workflow.

### Topics covered

- `start-here.md` boot sequence
- `project-routing.md`
- `chat-index.md`
- `handoff-rules.md`
- Context refresh versus starting a new chat
- Sidebar title reminder and confirmation workflow
- Commit workflow for repo doc updates

### Key decisions made

- `ai-context/start-here.md` remains inside `ai-context/`, not the repo root.
- Project Instructions should stay lightweight and ask before reading `start-here.md`.
- `start-here.md` handles routing, refresh, handoff, chat-index, and title reminder workflow.
- `handoff-rules.md` handles handoff prompts and refresh-vs-new-chat decisions.
- `chat-index.md` is the official database for meaningful chats.
- The official chat title is the chat-index title; the ChatGPT sidebar title is optional convenience metadata.
- If the user confirms the sidebar title was renamed exactly, `chat-index.md` should record it and future refreshes should stop reminding them.
- Future related multi-file repo updates should be attempted as one commit unless tooling makes that impractical.

### Files created or updated

- `ai-context/start-here.md`
- `ai-context/project-routing.md`
- `ai-context/chat-index.md`
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`

### Current outcome

- Routing and handoff architecture is implemented and still being refined.

### Follow-up needed

- Continue refining the routing, refresh, handoff, and chat-index system as needed.

### Continue this chat if...

- The task is about Orisen GPT project routing, chat indexing, context refresh, handoff rules, or source-of-truth workflow architecture.

### Start a new chat instead if...

- The task moves into creating a new source-of-truth doc, software implementation, marketing asset, fundraising asset, radar/ML work, or hardware subsystem work.

### Related chats

- Orisen General - Product Overview Source-of-Truth Draft

---
