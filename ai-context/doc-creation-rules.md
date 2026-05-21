# Doc Creation Rules

## Purpose

This file defines how Orisen source-of-truth docs should be created, edited, and promoted.

The goal is to prevent polished but unsafe docs from contaminating downstream work.

A good Orisen doc should preserve the company truth hierarchy, separate facts from assumptions, and make future AI-assisted work more accurate.

## Core rule

Do not create a lower-level doc from the user's latest request alone.

Before drafting or editing a doc, identify the higher-level docs that govern it.

Then derive the new doc from:

1. current company truth
2. source-of-truth rules
3. repo purpose and structure rules, when the work affects repo organization
4. relevant product truth
5. validation and evidence
6. relevant domain docs
7. the user's requested change

The user's request is an input, not the authority.

## Repo governance docs

When creating, moving, renaming, deleting, reorganizing, or cleaning up durable repo docs, also use:

- `ai-context/repo-purpose.md` for why the repo exists and what good repo health means.
- `ai-context/repo-structure.md` for structural logic, folder responsibilities, and upstream/downstream rules.
- `ai-context/repo-file-map.md` for the central current file inventory.
- `ai-context/repo-change-checklist.md` for the operational checklist before repo changes.

Do not duplicate repo-wide or folder-level file trees inside folder docs, context maps, or domain docs. The central durable file inventory belongs in `ai-context/repo-file-map.md`.

## Required pre-draft check

Before creating or materially editing a source-of-truth doc, determine:

- what type of doc this is
- which higher-level docs govern it
- whether the doc is current truth, working strategy, implementation scope, evidence, or draft material
- what claims are validated
- what claims are assumptions
- what claims are planned but unvalidated
- what belongs in MVP scope
- what belongs in first customer-ready product scope
- what belongs in roadmap or long-term vision
- what should be excluded
- which downstream docs may depend on it

If the request conflicts with source-of-truth docs, flag the conflict before drafting.

## Repo editing rule

When ChatGPT directly edits GitHub files, also follow:

- `ai-context/repo-editing-rules.md`
- `ai-context/repo-change-checklist.md` for significant repo changes

Especially for multi-file source-of-truth changes, ChatGPT should state the intended edit scope before editing, keep edits in small logical batches, avoid broad direct edits to `main` when a local/Codex/branch workflow would be safer, and summarize what changed afterward.

## Document status labels

Important docs should include a short metadata block near the top when useful.

Recommended format:

```markdown
Status: Source of truth / Working strategy / Draft / Archive
Authority level: Company / Product / Validation / Domain strategy / Implementation / Messaging / Fundraising
Last reviewed: YYYY-MM-DD
Governing docs:
- `path/to/doc.md`
Downstream docs:
- `path/to/doc.md`
```

Use metadata for durable docs that downstream work depends on.

Do not overuse metadata for tiny notes, temporary drafts, or one-off working files.

## Doc types

### Company-level docs

Company-level docs define durable truth about Orisen.

They should be broad, stable, and careful.

They should not include excessive implementation detail.

They should clearly separate:

- current truth
- strategic direction
- validation status
- assumptions
- open questions

Examples:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`

### Repo governance docs

Repo governance docs define why the repo exists, how it should be organized, how its file inventory is tracked, and how changes should be planned.

They should keep repo purpose, structural logic, file inventory, and operational checklists separate.

Examples:

- `ai-context/repo-purpose.md`
- `ai-context/repo-structure.md`
- `ai-context/repo-file-map.md`
- `ai-context/repo-change-checklist.md`

`ai-context/repo-structure.md` should explain structural philosophy. `ai-context/repo-file-map.md` should list the current file inventory. Do not merge those jobs into one file.

### Product docs

Product docs define what Orisen is, who it serves, what it promises, what it excludes, and how the product evolves.

They should stay consistent with company truth and validation evidence.

They should separate:

- engineering MVP
- first customer-ready product
- roadmap
- long-term vision
- excluded directions
- claims that need evidence

### Validation and evidence docs

Validation docs define what is known from real evidence.

They should be conservative.

They should separate:

- observed evidence
- user quotes or qualitative signal
- quantitative signal
- interpretation
- confidence level
- limitations
- what this evidence does and does not support

Validation docs should override unsupported marketing, fundraising, or product claims.

### Marketing docs

Marketing docs translate product truth into customer-facing language.

They should not invent product capabilities or validation.

They should include:

- target customer
- customer pain
- approved claims
- disallowed claims
- tone
- messaging principles
- evidence boundaries

Marketing docs must remain downstream from product and claims evidence.

### Fundraising docs

Fundraising docs translate company truth into an investor narrative.

They can be ambitious, but they must separate:

- what is built
- what is validated
- what is being built
- what is planned
- what is future vision
- what remains an assumption

Fundraising docs must not imply clinical proof, technical performance, or market validation that does not exist.

### Software and implementation docs

Software docs define implementation reality and build sequence.

They do not define the full company vision by themselves.

MVP implementation scope should not shrink product positioning unless the product docs are deliberately updated.

If an implementation constraint affects product promise, claims, roadmap, or customer experience, escalate the decision to Orisen General.

### Radar, ML, and technical research docs

Radar and ML docs define technical approach, research interpretation, experiment design, validation needs, and feasibility.

They should be especially careful about:

- sleep-stage accuracy
- HRV/RRV extraction
- artificial sleep phase transitioning
- intervention-loop claims
- what a paper does and does not prove
- lab performance vs real-bedroom performance

Technical promise should not become public claim without validation and product review.

### Hardware docs

Hardware docs define physical architecture, components, manufacturability, reliability, sensing placement, audio/light design, and physical user experience.

They should escalate to Orisen General when decisions affect:

- customer promise
- price point
- reliability
- claims
- launch timeline
- product form factor

## Required sections for durable docs

For durable source-of-truth docs, include sections like:

- Purpose
- Scope
- Current truth
- What this does not mean
- Assumptions
- Evidence or source basis
- Open questions
- Downstream implications

Not every doc needs all sections, but the doc should make these distinctions clear.

## Assumption discipline

Label assumptions clearly.

Do not write assumptions as facts.

Examples of assumptions:

- which early customer segment will pay first
- what users will pay
- how much users value grogginess reduction
- what radar signal quality will be sufficient
- what level of sleep-stage accuracy is good enough
- which marketing channel will convert best

Assumptions can guide work, but they should not be treated as validated evidence.

## Claims discipline

When a doc contains claims that could later appear in marketing, fundraising, or product pages, classify them as one of:

- validated
- built but not validated
- being built
- planned
- hypothesis
- long-term vision
- unsafe or disallowed

Do not bury claims in polished prose where their evidence status becomes unclear.

## Promotion rule

Old notes, brainstorms, and chat outputs are not source-of-truth by default.

To promote a note into source-of-truth:

1. Compare it against current high-level docs.
2. Check evidence status.
3. Resolve conflicts.
4. Assign the doc a status and authority level.
5. Update any downstream docs that depend on the decision.

## Update rule

When a source-of-truth doc changes, consider whether related docs need updates.

Especially check:

- `ai-context/current-state.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `product/target-customer.md`
- `product/roadmap.md`
- validation and claim-control docs
- marketing docs
- fundraising docs
- software/radar/hardware context maps

For repo structure or repo-governance changes, especially check:

- `ai-context/repo-purpose.md`
- `ai-context/repo-structure.md`
- `ai-context/repo-file-map.md`
- `ai-context/repo-change-checklist.md`
- `ai-context/context-map.md`
- relevant folder context maps

Do not update every file automatically.

Update only files that become stale, incomplete, or contradictory.

## Output rule for ChatGPT

When asked to create or revise a doc, ChatGPT should usually provide:

- the exact file path
- the full markdown content when requested
- a brief note on governing docs used
- any conflicts or assumptions discovered
- suggested follow-up docs to update

If directly editing GitHub, ChatGPT should follow `ai-context/repo-editing-rules.md` and summarize what files were created, updated, or intentionally not touched.