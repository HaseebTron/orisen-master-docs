# Research Context Map

## Purpose

This file is the routing map for the `research/` folder.

Use it to decide which research docs to read for customer interviews, external research, expert commentary, market/category research, competitor research, sleep science research, source review, and evidence interpretation.

This file does not replace product, claim-control, marketing, fundraising, radar/ML, or business source-of-truth docs. It points readers and ChatGPT projects to the right research inputs.

## File inventory rule

This file does not maintain this folder's file inventory.

For the current repo-wide file map, see:

- `ai-context/repo-file-map.md`

This context map should define task-based reading paths, not duplicate folder structure or current/planned file inventories.

## Always read first for important research work

For research work that may affect product truth, claims, roadmap, marketing, fundraising, or technical strategy, start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`

Then read the relevant research docs for the specific task.

## Research folder role

The `research/` folder stores and routes research inputs such as:

- Customer interviews and user research
- Raw survey responses and raw notes
- Expert commentary and meeting notes
- External research sources
- Processed source notes
- Research synthesis docs
- Competitor and substitute research
- Market and category research
- Waking-up research
- Going-to-sleep research
- During-sleep research
- Sleep tracking and validation research

Research docs should inform source-of-truth decisions, but raw research does not automatically become product truth or public claim support.

## Raw vs synthesis rule

Research files fall into different evidence levels:

- Raw notes and raw source lists preserve source material.
- Processed notes summarize or organize source material.
- Synthesis docs interpret patterns across sources.
- Product, claim-control, marketing, fundraising, and roadmap docs decide how research becomes operating truth.

Do not treat raw notes, single expert comments, or isolated sources as company truth by themselves.

Do not rewrite or delete raw research unless the user explicitly asks and repo-governance rules support it.

## Research docs and when to use them

### Customer interviews and survey responses

Use for questions like:

- What did early users say?
- What pain points were validated by interviews?
- What does the old alarm-clock feedback support?
- What customer language should marketing use?
- What does user evidence prove or not prove?

Read:

- `research/customer-interviews/2024-alarm-clock-interviews.md` if it exists
- relevant raw files under `research/customer-interviews/raw/` when exact source material matters
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`
- `marketing/marketing-context-map.md` if messaging or customer language matters

### Expert commentary

Use for questions like:

- What did sleep experts, operators, or advisors say?
- What expert feedback should affect product direction?
- What expert comments support or limit claims?
- How should expert feedback be incorporated into fundraising or product strategy?

Read:

- `research/expert-commentary/expert-commentary.md` if it exists
- relevant expert synthesis docs if they exist
- relevant raw meeting notes under `research/expert-commentary/raw/` when exact source material matters
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`

### External research source review

Use for questions like:

- What sources do we have on waking up, sleep inertia, sleep tracking, or competitors?
- What do external sources actually support?
- Which sources belong in a pitch deck or claims review?
- Which sources are weak, indirect, or only background context?

Read:

- `research/external-research/README.md` if it exists
- relevant processed source notes if they exist
- relevant synthesis docs under `research/external-research/`
- relevant raw source lists under `research/external-research/**/raw/` when source traceability matters
- `ai-context/claim-control/claim-control-system.md`

### Waking-up research

Use for questions like:

- What research supports the waking-up problem?
- What research supports sleep inertia or grogginess framing?
- What sources support painful mornings, oversleeping, alarm failure, or waking difficulty?

Read:

- `research/external-research/waking-up/waking-up-synthesis.md` if it exists
- `research/external-research/waking-up/processed-source-notes.md` if it exists
- relevant raw waking-up sources if exact source traceability matters
- `product/claims-and-evidence.md`
- `marketing/positioning-and-messaging.md` if messaging matters

### Going-to-sleep research

Use for questions like:

- What research supports bedtime, circadian, or falling-asleep features?
- How should Orisen treat going-to-sleep as roadmap versus current wedge?
- What sources support sleep-supportive lighting or sound before sleep?

Read:

- `research/external-research/going-to-sleep/going-to-sleep-synthesis.md` if it exists
- relevant raw going-to-sleep sources if exact source traceability matters
- `product/roadmap.md`
- `product/claims-and-evidence.md`

### During-sleep research

Use for questions like:

- What research supports during-sleep sensing or intervention?
- What sources support sleep-stage-aware intervention?
- What evidence is needed before stronger during-sleep claims?

Read:

- `research/external-research/during-sleep/during-sleep-synthesis.md` if it exists
- relevant raw during-sleep sources if exact source traceability matters
- `radar-ml/radar-ml-context-map.md`
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`

### Sleep tracking and validation research

Use for questions like:

- What sources support sleep tracking accuracy limits?
- What validation standard is needed for sleep-stage claims?
- How should Orisen discuss sleep-stage detection carefully?

Read:

- `research/external-research/sleep-tracking-and-validation/sleep-tracking-and-validation-synthesis.md` if it exists
- relevant raw sleep-tracking and validation sources if exact source traceability matters
- `radar-ml/radar-ml-context-map.md`
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`

### Competitors and substitutes

Use for questions like:

- What competitors and substitutes exist?
- How should Orisen be differentiated?
- What market alternatives should be mentioned in fundraising or positioning?

Read:

- `research/external-research/competitors-and-substitutes/competitors-and-substitutes-synthesis.md` if it exists
- relevant raw competitor sources if exact source traceability matters
- `marketing/positioning-and-messaging.md`
- `fundraising/fundraising-context-map.md` if investor framing matters

### Market and category research

Use for questions like:

- What category is Orisen in?
- What market framing is supported by external research?
- How should market/category research inform fundraising or business strategy?

Read:

- `research/external-research/market-and-category/market-and-category-synthesis.md` if it exists
- relevant raw market/category sources if exact source traceability matters
- `fundraising/fundraising-context-map.md`
- `business/business-context-map.md` if it exists

## Claims and evidence boundary

Research can support claims only after the claim-control system interprets the evidence strength.

Before using research in public claims, fundraising claims, technical claims, or marketing copy, read:

- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/claim-control/claim-control-log.md`

If a source is indirect, preliminary, based on another product, based on a lab context, or not specific to Orisen, weaken the claim.

## Escalation to Orisen General

Escalate to Orisen General when research interpretation changes or may change:

- Product truth
- Customer promise
- Public claims
- Roadmap priority
- Fundraising narrative
- Market/category positioning
- Target customer strategy
- Technical feasibility framing

## Research interpretation rules

- Research is input, not automatic source-of-truth.
- Raw notes should be preserved.
- Synthesis docs can summarize patterns but should not overstate certainty.
- Expert commentary is useful but not proof by itself.
- External papers and sources must be checked for applicability to Orisen.
- Claims should be routed through claim-control before becoming public language.
- Customer research should influence marketing language, product priority, and validation confidence, but limitations must stay visible.
