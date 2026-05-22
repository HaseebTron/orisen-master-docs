# Project Routing

Status: Source of truth
Authority level: Company / AI context / Project routing
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/start-here.md`
- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
Downstream docs:
- `ai-context/handoff-rules.md`
- `ai-context/context-map.md`
- `ai-context/chatgpt-project-instructions.md`

## Purpose of this file

This file explains which Orisen ChatGPT project should handle different kinds of work.

It exists to prevent asking the right question in the wrong project, duplicating decisions across chats, or letting one domain accidentally redefine another domain.

Read this file after `ai-context/start-here.md` and before doing the user's main task.

This file decides which project should handle a task; `ai-context/chatgpt-project-instructions.md` holds the copyable custom-instructions text for those projects.

## Core rule

Use the most focused project that can answer the question correctly.

Use `Orisen General` when the question affects company direction, product promise, customer focus, positioning, claims, fundraising strategy, roadmap priority, or multiple domains.

Use a domain project when the question is mainly execution work inside one area and does not require redefining the company or product truth.

When unsure, start in `Orisen General`.

## Recommended projects

The recommended Orisen project structure is:

- `Orisen General`
- `Orisen Software`
- `Orisen Radar + ML`
- `Orisen Marketing + GTM`
- `Orisen Fundraising`
- `Orisen Hardware` if hardware work becomes frequent enough to justify its own project

## Orisen General

Use this as the company-level decision brain.

Use this project for:

- Company strategy
- Product direction
- Product positioning
- Customer segment decisions
- What Orisen is or is not
- First customer-ready product decisions
- Long-term vision
- Cross-domain tradeoffs
- Claims and evidence questions
- Whether a feature belongs in the MVP, first customer product, or roadmap
- Deciding which docs should be created or updated
- Deciding which project should handle a task
- Reviewing conflicts between docs
- High-level planning across software, hardware, radar, marketing, fundraising, and business

Ask in Orisen General when the question sounds like:

- Should Orisen do this?
- Is this the right strategy?
- Does this fit the product vision?
- Are we overclaiming?
- What should be prioritized?
- Which project should I ask this in?
- Should this be in the MVP, first customer product, or future roadmap?
- What docs should I update after this decision?
- Does this conflict with current state?
- Should we split this into a new project or folder?

Do not use Orisen General for deep implementation unless the implementation affects company or product direction.

## Orisen Software

Use this project for firmware, app, backend, cloud, device logic, and code implementation.

Use this project for:

- ESP32 firmware
- App development
- Supabase
- BLE onboarding
- OTA
- Alarm sync
- Local alarm execution
- Wake completion state machine
- Git and code tasks
- Debugging logs
- Slice-by-slice implementation
- Code reviews
- PlatformIO
- Build errors
- App/cloud/device integration
- Software architecture

Ask in Orisen Software when the question sounds like:

- How do I implement this?
- Why is this firmware bug happening?
- What should Codex change in this file?
- What is the next software slice?
- Write a prompt for Codex.
- Review this git diff.
- What files should I commit?
- How should BLE onboarding work?
- How should the ESP32 store this setting?

Do not use Orisen Software to decide the company promise, marketing claims, or first customer-ready product vision.

Escalate to Orisen General if a software decision changes product scope, reliability promise, user promise, roadmap priority, or public claims.

## Orisen Radar + ML

Use this project for radar sensing, signal processing, vital signs, movement, datasets, sleep-stage estimation, and ML experimentation.

Use this project for:

- Radar module evaluation
- XM125 / A121 work
- V-LD3 / TI radar work
- RRV extraction
- HRV extraction
- Movement extraction
- Feature engineering
- Sleep-stage model design
- Research paper interpretation
- Dataset selection
- Model validation
- Sensor-informed wake intervention
- Artificial sleep phase transitioning experiments
- Closed-loop stimulation logic from a technical perspective

Ask in Orisen Radar + ML when the question sounds like:

- Can this radar measure the signal we need?
- How do I extract RRV?
- What inputs should the sleep-stage model use?
- Does this paper support my approach?
- How do I validate sleep-stage estimates?
- What is the technical path from radar data to intervention?
- What dataset should I use?
- How accurate does the model need to be?

Do not use Orisen Radar + ML to decide marketing claims, company positioning, fundraising claims, or customer-facing promises by itself.

Escalate to Orisen General if the answer affects what Orisen can claim publicly or what belongs in the first customer-ready product.

## Orisen Marketing + GTM

Use this project for messaging, website copy, content, growth, customer language, and launch execution.

Use this project for:

- Website copy
- Landing page sections
- LinkedIn posts
- X/Twitter posts
- TikTok or Instagram ideas
- Reddit research
- Waitlist growth
- Founder-led content
- Customer interviews from a messaging angle
- Customer language
- GTM experiments
- Launch planning
- Email capture strategy
- Positioning tests

Ask in Orisen Marketing + GTM when the question sounds like:

- How do I say this clearly?
- Write this LinkedIn post.
- Improve this landing page copy.
- What hook should I use?
- How do I explain Orisen to normal people?
- What content should I post?
- How do I get more waitlist signups?
- What customer pain should I lead with?

Do not use Orisen Marketing + GTM to invent product capabilities, validation, or technical claims.

Escalate to Orisen General if marketing wants to say something stronger than current evidence supports or if messaging changes the product positioning.

## Orisen Fundraising

Use this project for investor narrative, decks, outreach, traction framing, market story, and fundraising strategy.

Use this project for:

- Pitch deck
- Teaser deck
- Investor emails
- Angel outreach
- VC outreach
- Investor updates
- Fundraising narrative
- Traction framing
- Market sizing
- Competitive story
- Fundraising FAQ
- Objection handling
- Warm intro messages

Ask in Orisen Fundraising when the question sounds like:

- How do I pitch this to investors?
- Improve this investor email.
- What should go in the deck?
- How do I frame traction?
- What questions will investors ask?
- How should I explain the market?
- Is this a good pre-seed story?
- How do I ask for a warm intro?

Fundraising can be ambitious, but it must separate:

- What is validated
- What is built
- What is being built
- What is future vision
- What is still an assumption

Escalate to Orisen General if the fundraising story changes product positioning, target customer, public claims, or roadmap priority.

## Orisen Hardware

Use this project only when hardware work becomes active enough to deserve its own project.

Until then, hardware questions may be handled by Orisen General, Orisen Software, or Orisen Radar + ML depending on the task.

Use Orisen Hardware for:

- Enclosure
- Mounting
- Speaker system
- LED system
- PCB architecture
- Power system
- Battery backup
- Sensor placement
- Manufacturing
- DFM/DFA
- Reliability testing
- Mechanical and electrical tradeoffs

Ask in Orisen Hardware when the question sounds like:

- Where should the radar be placed?
- How should the device mount to the wall?
- What speaker should we use?
- How do we design the enclosure?
- What battery architecture makes sense?
- How do we make this manufacturable?
- What should be on the PCB?

Escalate to Orisen General if the hardware decision affects the product promise, customer experience, price point, claims, or launch timeline.

## When to use Orisen General instead of a domain project

Use Orisen General if the question involves more than one of these areas:

- Product
- Customer
- Marketing
- Fundraising
- Hardware
- Software
- Radar/ML
- Business model
- Claims
- Validation
- Roadmap

Use Orisen General if the question starts with or implies:

- Should we...
- Is it worth...
- What is the right strategy...
- Does this fit...
- What should we prioritize...
- Are we overclaiming...
- Is this validated...
- What should the product be...
- What docs should change...

Use the domain project if the question starts with or implies:

- Implement...
- Debug...
- Write copy for...
- Draft a post...
- Analyze this paper...
- Extract this signal...
- Review this code...
- Create a Codex prompt for...

## Escalation rules

Escalate from a domain project to Orisen General when:

- A decision changes product scope
- A decision changes customer promise
- A decision affects public claims
- A decision affects fundraising narrative
- A decision affects roadmap priority
- A decision creates conflict between docs
- A technical limitation forces a product strategy change
- Marketing wants to say something stronger than evidence supports
- Fundraising wants to imply something not yet built or validated

## New project creation rule

Do not create a new ChatGPT project just because a topic exists.

Create a new project only when:

- The topic has recurring work
- The work needs different context from other projects
- The work has enough docs or repo files to justify a separate brain
- Mixing it with another project would cause confusion
- The project needs its own working memory and workflow
