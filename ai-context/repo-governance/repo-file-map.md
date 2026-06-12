# Repo File Map

Status: Source of truth
Authority level: Company / AI context / Repo governance
Last reviewed: 2026-06-12
Governing docs:
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/context-map.md`
Downstream docs:
- Folder read-rules files
- Repo cleanup tasks
- Repo integrity checks

## Purpose

This file is the central inventory of the Orisen master docs repo.

It lists the current folder and file structure at a practical level so that other docs do not need to duplicate file trees.

For the logic behind the structure, use `ai-context/repo-governance/repo-structure.md`. For what the repo is meant to do, use `ai-context/repo-governance/repo-purpose.md`.

## File map rule

This is the only durable place where the repo-wide file inventory should be maintained.

Folder read-rules files, folder overview docs, and domain docs should not maintain their own complete file trees. They should reference this file when the current structure matters.

## Maintenance rule

Update this file when:

- a durable file is created
- a durable file is deleted
- a durable file is renamed
- a durable file is moved
- a new folder is created
- a folder's purpose changes

Do not update this file for tiny temporary scratch files unless they become durable docs.

## Format rule

Use a nested bullet tree for the repo inventory.

Format:

```markdown
- **`folder/`**: Folder purpose.
  - `file.md`: File purpose.
  - **`subfolder/`**: Subfolder purpose.
    - `nested-file.md`: File purpose.
```

Conventions:

- Bold folder paths.
- Do not bold file paths.
- Use a colon and one-line plain-English summary after each folder or file.
- Use indentation to show what is inside what.
- Keep descriptions short.
- List every durable `.md` file in the repo, including raw and archive files.
- Raw files can have very short descriptions.
- Do not deeply summarize raw content here. The file map only identifies what exists and why it is stored.
- Link files only when it improves human navigation.
- Do not turn this file into a detailed task-routing map. That belongs in `ai-context/context-map.md` and folder read-rules files.

## Repo inventory

- `README.md`: Top-level repository overview.

- **`ai-context/`**: Controls source-of-truth behavior, AI operating mode, project routing, repo governance, context loading, claim control, decisions, and repo workflow.
  - `README.md`: AI context folder overview.
  - `start-here.md`: First file to read when starting or refreshing an Orisen ChatGPT chat.
  - `chatgpt-project-instructions.md`: ChatGPT project instruction reference.
  - `project-routing.md`: Explains which Orisen ChatGPT project should handle different kinds of work.
  - `handoff-rules.md`: Defines when to continue, refresh, move projects, or start a new chat.
  - `context-map.md`: Top-level document-routing map for choosing minimal and full context packs.
  - `current-state.md`: Current operating snapshot, build/evidence status, active priorities, and constraints.
  - `current-work.md`: Current work and active workstream notes.
  - `source-of-truth-rules.md`: Defines authority hierarchy and how to handle doc conflicts.
  - `ai-operating-mode.md`: Defines how GPT should reason when using Orisen docs.
  - `doc-creation-rules.md`: Defines how source-of-truth docs should be created, edited, and promoted.
  - `decision-log.md`: Durable decisions and rationale.
  - **`repo-governance/`**: Repo purpose, operating model, structure, file inventory, editing rules, local workflow rules, change checklist, and cleanup backlog.
    - `repo-purpose.md`: Defines why the repo exists and what good repo health means.
    - `repo-operating-model.md`: Explains how the repo works as a governed source-of-truth system.
    - `repo-structure.md`: Defines structural philosophy, folder responsibilities, and anti-duplication rules.
    - `repo-file-map.md`: Central current inventory of repo folders and durable files.
    - `repo-change-checklist.md`: Operational checklist for planning or making repo changes.
    - `repo-editing-rules.md`: Defines safe direct GitHub editing behavior.
    - `local-repo-codex-workflow.md`: Defines the local VS Code, Git, and Codex workflow for broader repo changes.
    - `cross-repo-boundaries.md`: Defines source-of-truth versus implementation repo boundaries.
    - `repo-backlog.md`: Backlog of repo buildout and cleanup work.
  - **`claim-control/`**: Controls claims, evidence, validation language, and claim-safety discipline.
    - `claim-control-system.md`: Rules for judging and controlling claims.
    - `claim-control-log.md`: Log of claim decisions and evidence status.
    - `claim-control-roadmap.md`: Roadmap for improving the claim-control system.

- **`product/`**: Defines product truth, product scope, customer promise, roadmap, target customer, and claims/evidence from a product perspective.
  - `product-read-rules.md`: Product-specific reading/routing rules.
  - `product-overview.md`: Highest product-specific authority for durable product direction and product-level truth.
  - `framing-and-narrative.md`: Product-level strategic narrative, category frame, and belief shift.
  - `claims-and-evidence.md`: Product claims and evidence boundaries.
  - `target-customer.md`: First target customer and customer focus.
  - `roadmap.md`: Roadmap and product sequencing.
  - `ai-powered-sleep-intervention-direction.md`: Brief supporting strategy note for the long-term AI-powered sleep intervention direction.
  - `product-questions-and-objections.md`: Product questions, objections, and response framing.
  - **`old-mvp/`**: Old MVP evidence, behavior notes, and failure/bypass learnings.
    - `README.md`: Old MVP folder overview.
    - `old-mvp.md`: Old MVP summary and learnings.
    - `old-mvp-bypass-and-failure-notes.md`: Old MVP bypass, failure, and user-behavior notes.

- **`research/`**: Stores customer interviews, expert commentary, external research, raw source material, source-by-source review, and research synthesis.
  - `research-read-rules.md`: Research-specific reading/routing rules.
  - `research-write-rules.md`: Research writing rules for research docs and synthesis files.
  - **`customer-interviews/`**: Customer interview synthesis and raw customer research.
    - `2024-alarm-clock-interviews.md`: Customer interviews from using the old MVP.
    - **`raw/`**: Raw customer interview and source material.
  - **`expert-commentary/`**: Expert commentary, expert synthesis, and raw meeting notes.
    - `README.md`: Expert commentary folder overview.
    - `expert-commentary-synthesis.md`: Consolidated synthesis of expert commentary across calls.
    - **`raw/`**: Raw expert meeting notes and source material.
      - `benji-ozynski-meeting-notes.md`: Raw notes from Dr Benji Ozynski expert conversation.
      - `leila-jalali-meeting-notes.md`: Raw notes from Leila Jalali expert conversation.
  - **`external-research/`**: External research sources, source-by-source review, and synthesis docs.
    - `README.md`: External research folder overview and usage notes.
    - **`raw/`**: Founder-provided source lists and source-categorization material.
      - `founder-full-source-list.md`: Full founder-provided external source list.
      - `founder-pitch-deck-source-shortlist.md`: Founder-provided pitch-deck source shortlist.
      - `founder-source-categorization-map.md`: Founder-provided map for categorizing external sources.
    - **`waking-up/`**: Waking-up, sleep inertia, grogginess, oversleeping, and alarm-failure research.
      - `synthesis.md`: Synthesis of waking-up research.
      - `raw-sources-reviewed.md`: Source-by-source review of waking-up raw sources.
      - **`raw/`**: Raw waking-up source material.
        - `founder-sources.md`: Founder-provided raw waking-up source list.
    - **`going-to-sleep/`**: Bedtime, circadian, falling-asleep, sound, and lighting research.
      - `synthesis.md`: Synthesis of going-to-sleep research.
      - **`raw/`**: Raw going-to-sleep source material.
        - `founder-sources.md`: Founder-provided raw going-to-sleep source list.
    - **`during-sleep/`**: During-sleep sensing, intervention, and sleep-state research.
      - `synthesis.md`: Synthesis of during-sleep research.
      - **`raw/`**: Raw during-sleep source material.
        - `founder-sources.md`: Founder-provided raw during-sleep source list.
    - **`sleep-tracking-and-validation/`**: Sleep tracking accuracy and validation-standard research.
      - `synthesis.md`: Synthesis of sleep tracking and validation research.
      - **`raw/`**: Raw sleep-tracking and validation source material.
        - `founder-sources.md`: Founder-provided raw sleep-tracking and validation source list.
    - **`competitors-and-substitutes/`**: Competitor, substitute, and alternative-solution research.
      - `synthesis.md`: Synthesis of competitor and substitute research.
      - **`raw/`**: Raw competitor and substitute source material.
        - `founder-sources.md`: Founder-provided raw competitor and substitute source list.
    - **`market-and-category/`**: Market, category, and industry-framing research.
      - `synthesis.md`: Synthesis of market and category research.
      - **`raw/`**: Raw market and category source material.
        - `founder-sources.md`: Founder-provided raw market and category source list.

- **`marketing/`**: Defines messaging, positioning, customer language, content strategy, channel playbooks, GTM experiments, launch execution, and marketing performance learnings.
  - `README.md`: Marketing folder overview.
  - `marketing-read-rules.md`: Marketing-specific reading/routing rules.
  - `marketing-write-rules.md`: Marketing writing rules for drafting and editing marketing docs.
  - `positioning-and-messaging.md`: Core marketing positioning and messaging.
  - `founder-voice.md`: Founder voice and cross-channel external communication style.
  - `post-performance-log.md`: Founder-led marketing post and campaign performance log.
  - **`x/`**: X/Twitter-specific content strategy, post drafts, profile notes, and reply guidance.
    - `playbook.md`: X/Twitter-specific content playbook.
    - `post-bank.md`: Draft and reusable X/Twitter post bank.
    - `posting-strategy.md`: X/Twitter posting strategy and execution guidance.
    - `profile-current-state.md`: Current X/Twitter profile state and profile notes.
    - `reply-strategy.md`: X/Twitter reply strategy and engagement guidance.
    - `style-guide.md`: X/Twitter-specific style guide.
  - Potential future files:
    - `customer-language.md`: Customer words, phrases, pain points, and message mining.
    - `content-pillars.md`: Core founder-led content themes.
    - `gtm.md`: Go-to-market strategy.
    - `linkedin-playbook.md`: LinkedIn-specific content and outreach playbook.
    - `tiktok-playbook.md`: TikTok-specific content playbook.
    - `instagram-playbook.md`: Instagram-specific content playbook.
    - `reddit-research.md`: Reddit research and community notes.

- **`fundraising/`**: Defines investor narrative, fundraising strategy, pitch framing, outreach, traction framing, and investor-specific communication.
  - `fundraising-read-rules.md`: Fundraising-specific reading/routing rules.
  - `investor-narrative.md`: Core investor narrative.
  - `investor-crm.md`: Investor CRM and investor relationship tracking.
  - `outreach-email-accounts.md`: Fundraising outreach email account setup and notes.
  - `founders-inc-application-guide.md`: General Founders, Inc application rubric and question-by-question guide.
  - Potential future files:
    - `pitch-deck-notes.md`: Pitch deck structure, slide notes, and investor-facing narrative details.
    - `traction.md`: Fundraising-focused traction framing.
    - `outreach-strategy.md`: Investor outreach and intro strategy.

- **`software/`**: Defines software context at the master-docs level and routes to active implementation docs in the software repo.
  - `README.md`: Software folder overview.
  - `software-read-rules.md`: Software-specific reading/routing rules and links to active software implementation docs.
  - `p1-overview.md`: Software project overview snapshot.
  - `p2-mvp-scope.md`: Software MVP scope snapshot.
  - Note: Detailed implementation docs may live in the active Orisen Software repo, not necessarily this master docs repo.

- **`radar-ml/`**: Defines radar module decisions, vital-sign extraction, sleep-stage modeling, intervention-loop research, datasets, technical validation, and research interpretation.
  - `radar-ml-read-rules.md`: Radar/ML-specific reading/routing rules.
  - **`v-ld3/`**: RFbeam V-LD3 technical research context.
    - `README.md`: Tiny index for V-LD3 radar context docs.
    - `vital-signs-demo-on-v-ld3.md`: V-LD3 compatibility notes for TI IWRL6432 Vital Signs testing.
    - `ti-vital-signs-output-and-waveform-access.md`: Stock TI output limits and waveform export path for HRV/RRV work.
  - **`radar-sleep-stage-literature/`**: Raw and reviewed literature artifacts for radar-based sleep-stage, sleep-state, and sleep/wake classification research.
    - **`raw/`**: Raw radar sleep-stage literature discovery and screening artifacts.
      - `discovery-pass-2026-06-12.md`: Raw high-recall radar sleep-stage literature discovery output.
      - `screening-pass-1-2026-06-12.md`: Raw working screening, deduplication, categorization, and priority pass.
      - `extraction-pass-1-2026-06-12.md`: Raw Extraction Pass 1 table and unresolved-details notes for screened P0 radar sleep-stage literature sources.
      - `primary-source-chase-pass-1-2026-06-12.md`: Raw Primary-Source Chase Pass 1 results for weak P0 radar sleep-stage literature rows.
  - Potential future files:
    - `radar-module-decision.md`: Radar module selection and tradeoff decisions.
    - `vital-signs-pipeline.md`: Vital-sign, RRV, HRV, and movement extraction strategy.
    - `sleep-stage-model.md`: Sleep-stage modeling approach.
    - `intervention-loop.md`: Sensor-informed wake intervention loop.
    - `research-notes.md`: Radar/ML research notes.
    - `technical-validation.md`: Technical validation plan and evidence requirements.

- **`hardware/`**: Defines physical product architecture, sensing placement, enclosure, power, audio/light, manufacturing, reliability, and hardware tradeoffs.
  - Potential future files:
    - `hardware-read-rules.md`: Hardware-specific reading/routing rules.
    - `hardware-overview.md`: Hardware architecture overview.
    - `sensor-decisions.md`: Sensor selection and placement decisions.
    - `manufacturing-notes.md`: Manufacturing, sourcing, and DFM notes.
  - Note: Hardware docs should be created when hardware work becomes frequent enough to justify stable context.

- **`business/`**: Defines business model, pricing, competitors, market assumptions, partnerships, operations, and revenue strategy.
  - Potential future files:
    - `business-read-rules.md`: Business-specific reading/routing rules.
    - `business-model.md`: Business model and revenue logic.
    - `pricing.md`: Pricing assumptions and strategy.
    - `competitors.md`: Competitor analysis.
    - `market-notes.md`: Market assumptions and notes.
  - Note: Business docs may contain assumptions and should clearly separate assumptions from validated facts.

## Entry-point docs

- **Default entry point**: `ai-context/start-here.md`
- **Top-level routing map**: `ai-context/context-map.md`
- **Repo governance entry points**: `ai-context/repo-governance/repo-purpose.md`, `ai-context/repo-governance/repo-operating-model.md`, `ai-context/repo-governance/repo-structure.md`, `ai-context/repo-governance/repo-file-map.md`, `ai-context/repo-governance/repo-change-checklist.md`
- **Source-of-truth authority entry points**: `ai-context/current-state.md`, `ai-context/source-of-truth-rules.md`, `ai-context/ai-operating-mode.md`
- **Doc and repo-edit workflow entry points**: `ai-context/doc-creation-rules.md`, `ai-context/repo-governance/repo-editing-rules.md`, `ai-context/repo-governance/local-repo-codex-workflow.md`
- **Claim-control entry point**: `ai-context/claim-control/claim-control-system.md`

## Notes for future updates

This file should stay useful but not overly detailed.

Do not turn it into a full duplicate of every folder's read-rules file. Its job is to show what exists and where to find it, not to define every task-specific reading path.
