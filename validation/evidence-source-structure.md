# Evidence Source Structure

## Purpose

This file defines how Orisen evidence should be organized before it flows into `product/claims-and-evidence.md`.

Use this file when adding new research, customer data, prototype data, expert notes, marketing traffic data, or competitor/customer-language evidence.

The goal is to keep raw/source material separate from interpretation while avoiding too many abstraction layers for the current startup stage.

## Core rule

Evidence should flow through three layers:

```text
Raw/source material
↓
Synthesis files
↓
product/claims-and-evidence.md
```

Do not create extra intermediate abstraction layers unless the folder becomes too large or the evidence is being used for a high-stakes claim.

## Complete evidence map

```text
orisen-master-docs/
├── product/
│   ├── claims-and-evidence.md
│   ├── target-customer.md
│   └── old-mvp/
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
│   │   │   └── 2024-alarm-clock-responses.csv
│   │   └── 2024-alarm-clock-interviews.md
│   │
│   ├── expert-commentary/
│   │   ├── raw/
│   │   │   ├── leila-jalali-meeting-notes.md
│   │   │   └── benji-ozynski-meeting-notes.md
│   │   ├── expert-commentary.md
│   │   └── benji-ozynski-synthesis.md
│   │
│   └── external-research/
│       ├── research-papers/
│       │   ├── raw/
│       │   └── research-papers-synthesis.md
│       ├── articles-and-media/
│       │   ├── raw/
│       │   └── articles-and-media-synthesis.md
│       ├── reddit-forums/
│       │   ├── raw/
│       │   └── reddit-forum-synthesis.md
│       ├── competitor-reviews/
│       │   ├── raw/
│       │   └── competitor-review-synthesis.md
│       └── market-and-category/
│           ├── raw/
│           └── market-and-category-synthesis.md
│
└── validation/
    ├── evidence-roadmap.md
    ├── evidence-log.md
    ├── evidence-standard.md
    └── evidence-source-structure.md
```

## Why expert commentary is separate from external research

Expert commentary should live under `research/expert-commentary/`, not inside `research/external-research/`.

Reason:

- Expert calls are primary founder-collected evidence.
- Research papers, articles, Reddit posts, competitor reviews, and market reports are external secondary sources.
- Mixing them blurs the difference between first-hand expert input and outside research.

## What market and category means

`research/external-research/market-and-category/` is for evidence that explains the broader market/category context.

Examples:

- sleep-tech market reports
- smart-alarm or alarm-clock market reports
- wearable sleep tracker market reports
- surveys about sleep problems or morning difficulty
- category articles about sleep technology adoption
- investor-category framing sources

Use it for fundraising/category framing, not as proof that Orisen's wedge is validated.

## What each layer should contain

### 1. Raw/source files

Raw/source files should preserve source material with minimal interpretation.

They can include:

- links
- source title
- source type
- why the source was saved
- short notes about what to inspect later
- copied snippets only when allowed and useful
- founder caveats about source quality

They should not contain final Orisen claims.

### 2. Synthesis files

Synthesis files should interpret a set of raw/source files inside that evidence category.

They should answer:

- what this evidence suggests
- what it does not prove
- what claims it can support
- what claims it cannot support
- how strong the evidence is
- what should be researched next

Every meaningful interpretation should point back to its raw/source file using normal Markdown links.

### 3. `product/claims-and-evidence.md`

This is the final downstream claim-control file.

It should pull only the strongest, most decision-relevant conclusions from:

- `research/customer-interviews/2024-alarm-clock-interviews.md`
- `product/old-mvp/` files
- `marketing/post-performance-log.md`
- `research/expert-commentary/` files
- `research/external-research/` synthesis files
- `validation/evidence-log.md`

It should not duplicate all raw data.

## Citation/linking convention

Inside Markdown files, prefer readable source links instead of full visible URLs.

Good:

```markdown
- Snooze use is common, but this source should be used cautiously for broad population claims. Source: [Harvard / Scientific Reports snooze paper](raw/snooze-paper-list.md)
```

Avoid:

```markdown
- Snooze use is common: https://very-long-url-example.com/...
```

For raw source lists, full links are acceptable because raw files are allowed to be messy and source-preserving.
