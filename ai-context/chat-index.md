# Chat Index

## Purpose of this file

This file tracks meaningful ChatGPT chats across Orisen projects.

It helps decide:

- Whether a new question belongs in an existing chat
- Whether a new chat should be created
- Which project should handle a question
- What decisions have already been made
- Which docs or repo files were created or updated
- When a chat is becoming too long or unfocused

This file should be read during the `ai-context/start-here.md` boot sequence before the assistant answers the user's main question.

## Core rule

A chat should have one clear job.

If a chat starts covering a new slice, new domain, new asset, or major new decision, create a new chat and add an entry to this index if the chat is meaningful enough to track.

Do not track every tiny one-off question.

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

## Required routing process for new chats

When a new chat starts and the user asks the assistant to read `ai-context/start-here.md`, the assistant should:

1. Read this file.
2. Check whether an existing active chat already matches the user's task.
3. Check whether the current project is the correct project using `ai-context/project-routing.md`.
4. If an existing chat is better, recommend using that chat instead of creating a new one.
5. If another project is better, recommend the correct project before answering.
6. If the current chat should exist and is meaningful enough to track, update this file or provide the exact entry to add.
7. Only after routing is resolved should the assistant continue to `ai-context/context-map.md` and answer the main task.

## Response format for routing recommendation

Use this format when routing is non-obvious:

```markdown
## Chat routing recommendation

Best project:
- [Project name]

Best chat:
- Continue this chat / Start a new chat / Use existing chat: [chat title]

Reason:
- [Brief explanation]

Suggested first prompt:
- [Prompt to paste if another project or chat is better]
```

## Chat entry template

Use this template for meaningful chats:

```markdown
## [YYYY-MM-DD] [Project Name] - [Chat Title]

### Project

- Project:

### Chat title

- Title:

### Status

- Active / Completed / Superseded / Archived

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

No tracked chats yet.

Add new meaningful chats below this line.

---
