# Claim Control System

## Purpose

This file defines how Orisen evidence, validation, and claim safety should be organized before claims flow into `product/claims-and-evidence.md`.

Use this file when adding research, customer discovery, prototype data, expert notes, marketing traffic data, competitor/customer-language evidence, or when judging whether a product, marketing, fundraising, radar/ML, or technical claim is safe.

The goal is to keep source material separate from interpretation while preventing Orisen from overclaiming before evidence supports it.

## Core principle

Orisen docs should reason top down:

```text
Company/product truth
↓
Evidence and validation status
↓
Claim boundaries
↓
Marketing, fundraising, website, roadmap, and implementation docs
```

The user's latest message is input, not automatic source-of-truth.

## Evidence flow

Evidence should flow through three layers:

```text
Raw/source material
↓
Problem-area synthesis
↓
product/claims-and-evidence.md
```

Do not create extra abstraction layers unless the folder becomes too large or the claim is high-stakes.

For external research, organize primarily by Orisen problem area. Source type should be metadata inside each source entry, not the main folder structure.

## Raw/source material

Raw/source files preserve source material with minimal interpretation.

They can include:

- links
- source title
- source type
- why the source was saved
- short notes about what to inspect later
- copied snippets only when allowed and useful
- founder caveats about source quality
- raw tables, CSVs, rough meeting notes, screenshots, transcripts, or exported analytics

They should not contain final Orisen claims.

## Synthesis files

Synthesis files interpret a set of raw/source files inside that evidence category.

They should answer:

- what this evidence suggests
- what it does not prove
- what claims it can support
- what claims it cannot support
- how strong the evidence is
- what should be researched or tested next

Every meaningful interpretation should point back to the relevant raw/source file using readable Markdown links.

## Final claim-control file

`product/claims-and-evidence.md` is the final downstream claim-control file.

It should pull only the strongest, most decision-relevant conclusions from:

- `research/customer-interviews/`
- `product/old-mvp/`
- `marketing/post-performance-log.md`
- `research/expert-commentary/`
- `research/external-research/`
- `ai-context/claim-control/claim-control-log.md`

It should not duplicate all raw data.

## Evidence classification

Use these labels consistently.

### Validated

A claim is validated only when there is enough direct evidence from Orisen-specific users, tests, data, or transactions to support it.

Use carefully. Do not call something validated just because it is plausible, expert-supported, or common in the market.

### Early signal

A claim has an early signal when there is meaningful but limited evidence.

Examples:

- a small number of user interviews
- waitlist signups
- prototype tester comments
- one or a few strong behavioral examples
- expert interest or caution

Early signal is useful for direction, not proof.

### Built but not validated

Use when something exists technically or was prototyped, but has not been validated with enough real users or conditions.

### Planned

Use when something is on the roadmap but not built yet.

### Hypothesis

Use when something might be true and is worth testing, but evidence is not strong enough yet.

### Long-term vision

Use when something describes where Orisen may go eventually, not what the product can claim now.

### Unsupported or unsafe claim

Use when the claim should not be made because evidence is missing, the wording is too strong, or the claim may imply clinical, technical, or customer proof that does not exist.

## Evidence strength levels

Use these levels when helpful:

- Level 0: no evidence or only founder belief.
- Level 1: weak signal, anecdote, offhand comment, or small unstructured note.
- Level 2: meaningful early signal from user behavior, prototype use, expert commentary, or structured discovery.
- Level 3: stronger repeated evidence across multiple users, tests, or source types.
- Level 4: strong validation with repeatable data, clearer user behavior, or strong technical validation.
- Level 5: high-confidence validation from robust trials, paid demand, long-term retention, production reliability, or clinical-quality evidence where relevant.

Most current Orisen evidence is Level 1 to Level 3.

## Current highest-confidence evidence

The strongest current evidence supports presence-based wake completion as the first wedge.

This does not yet prove:

- production reliability
- broad-market demand
- willingness to pay at scale
- reduced grogginess
- reduced sleep inertia
- sleep-stage detection
- artificial sleep phase transitioning
- clinical efficacy

## Claim-review rule

Before strengthening a public claim, check:

1. Is this claim about what exists today, what is being built, or what is planned?
2. Is there direct Orisen-specific evidence?
3. Is the evidence user behavior, paid behavior, technical test data, expert commentary, or secondary research?
4. Does the wording imply clinical proof, exact accuracy, guaranteed outcome, or production reliability?
5. Would a reasonable customer or investor think the outcome is already proven?
6. Can the claim be rewritten as a safer current claim, careful aim, roadmap item, or hypothesis?

## Citation and linking convention

Inside Markdown files, prefer readable source links instead of full visible URLs.

Good:

```markdown
- Snooze use is common, but this source should be used cautiously for broad population claims. Source: [Scientific Reports snooze paper](raw/founder-sources.md)
```

Avoid:

```markdown
- Snooze use is common: https://very-long-url-example.com/...
```

For raw source lists, full links are acceptable because raw files are allowed to be messy and source-preserving.

## Repo hygiene rules

- Keep raw data near the source category.
- Keep interpretation outside the raw folder.
- Do not overwrite raw data with conclusions.
- Do not duplicate full evidence across multiple files.
- Use synthesis files before promoting claims into `product/claims-and-evidence.md`.
- Use `ai-context/claim-control/claim-control-log.md` for conservative evidence entries that materially affect claims.
- Do not turn anecdotes, Reddit posts, reviews, or market reports into statistical claims.
- Do not treat scientific plausibility as proof that Orisen works.
- Do not treat informal expert interest as a formal advisor, partner, or cofounder relationship.

## Complete evidence map

```text
orisen-master-docs/
├── product/
│   ├── claims-and-evidence.md
│   ├── target-customer.md
│   └── old-mvp/
│       ├── README.md
│       ├── old-mvp.md
│       ├── old-mvp-test-row-labels.md
│       ├── old-mvp-bypass-and-failure-notes.md
│       └── old-mvp-user-feedback.md
│
├── marketing/
│   └── post-performance-log.md
│
├── research/
│   ├── customer-interviews/
│   │   ├── raw/
│   │   └── 2024-alarm-clock-interviews.md
│   │
│   ├── expert-commentary/
│   │   ├── raw/
│   │   ├── expert-commentary.md
│   │   └── benji-ozynski-synthesis.md
│   │
│   └── external-research/
│       ├── README.md
│       ├── raw/
│       │   ├── founder-full-source-list.md
│       │   ├── founder-pitch-deck-source-shortlist.md
│       │   └── founder-source-categorization-map.md
│       ├── waking-up/
│       │   ├── raw/founder-sources.md
│       │   └── waking-up-synthesis.md
│       ├── going-to-sleep/
│       │   ├── raw/founder-sources.md
│       │   └── going-to-sleep-synthesis.md
│       ├── during-sleep/
│       │   ├── raw/founder-sources.md
│       │   └── during-sleep-synthesis.md
│       ├── sleep-tracking-and-validation/
│       │   ├── raw/founder-sources.md
│       │   └── sleep-tracking-and-validation-synthesis.md
│       ├── competitors-and-substitutes/
│       │   ├── raw/founder-sources.md
│       │   └── competitors-and-substitutes-synthesis.md
│       └── market-and-category/
│           ├── raw/founder-sources.md
│           └── market-and-category-synthesis.md
│
└── ai-context/
    └── claim-control/
        ├── claim-control-system.md
        ├── claim-control-roadmap.md
        └── claim-control-log.md
```

## Relationship to `product/claims-and-evidence.md`

This file defines the operating system for evidence and claim safety.

`product/claims-and-evidence.md` is the downstream public-claim authority.

When they appear to conflict, use this file for classification rules, then update `product/claims-and-evidence.md` to match the current evidence.