# External Research

Status: Working research structure
Authority level: Research organization / raw-source routing
Last reviewed: 2026-05-20
Governing docs:
- `ai-context/source-of-truth-rules.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/claim-control/claim-control-system.md`

## Purpose

This folder organizes external research for Orisen.

The structure is problem-first, not source-type-first.

That means sources are grouped by the Orisen problem area they help investigate, not primarily by whether they are papers, articles, Reddit posts, reviews, or market reports.

## Evidence flow

External research should flow through this sequence:

```text
Canonical raw archive
->
Problem-area raw intake files
->
Problem-area raw-sources-reviewed.md files, when created
->
Problem-area synthesis.md files
->
claim-control / product docs
```

The practical file-layer model is:

```text
raw/
= preserved raw/source intake

raw-sources-reviewed.md
= optional but preferred source-by-source review layer

synthesis.md
= pattern-level interpretation for that folder/problem area

claim-control / product docs
= durable claim boundaries and safe public language
```

Do not skip directly from an external source to a public claim.

`raw-sources-reviewed.md` is preferred when a folder has multiple sources or when source quality needs structured review. It is not required for every folder immediately.

A `synthesis.md` file should normally build from `raw-sources-reviewed.md` when that file exists. If no reviewed layer exists yet, the synthesis may build directly from raw files, but it must say that clearly and preserve traceability back to raw/source material.

## Raw archive

The `raw/` folder preserves founder-provided source lists and organization notes.

The canonical raw archive for the first external source batch is:

- `research/external-research/raw/founder-full-source-list.md`

This file should remain the fallback archive. Do not delete it or heavily rewrite it.

The pitch-deck shortlist is preserved separately:

- `research/external-research/raw/founder-pitch-deck-source-shortlist.md`

The first-pass organization map is:

- `research/external-research/raw/founder-source-categorization-map.md`

## Problem-first folders

Current problem areas:

- `waking-up/`
- `going-to-sleep/`
- `during-sleep/`
- `sleep-tracking-and-validation/`
- `competitors-and-substitutes/`
- `market-and-category/`

Each problem folder should use this research-layer model:

```text
raw/
raw-sources-reviewed.md, optional / when created
synthesis.md
```

The `raw/` layer preserves raw/source intake.

The `raw-sources-reviewed.md` layer reviews raw sources source-by-source. It is optional when a folder is still early, but preferred before a mature synthesis or claim-control update.

The `synthesis.md` layer interprets patterns for that folder/problem area. It should state whether it is based on reviewed source notes or directly on raw files.

## Source type as metadata

Source type belongs inside entries as metadata.

Examples:

- research paper
- article/media
- survey/report
- market report
- Reddit/forum
- competitor review
- product page
- expert/organization source
- unknown / needs verification

Source type should not be the main folder structure unless a future folder becomes large enough to justify subfolders.

## Claim-safety rule

External research does not prove Orisen works.

Use external research to:

- understand the problem space
- identify customer language
- find competitor and substitute gaps
- understand scientific plausibility and limitations
- support market/category framing carefully
- discover what needs to be tested with Orisen-specific users

Do not use external research alone to claim:

- Orisen reduces grogginess
- Orisen reduces sleep inertia
- Orisen detects sleep stages accurately
- Orisen clinically improves sleep
- Orisen has broad-market demand
- Orisen has proven willingness to pay

Those claims require Orisen-specific evidence and synthesis before promotion into `product/claims-and-evidence.md`.

## Processing rule

Do not copy the entire canonical raw list into every problem folder by default.

For now, problem-area raw files may point back to the canonical raw archive and describe which sections should be processed later.

Move or copy source entries into problem folders only during a deliberate research pass where the source is being verified, tagged, and prepared for source-by-source review or synthesis.

If `raw-sources-reviewed.md` does not exist yet, do not pretend the sources have been reviewed. Treat the folder's raw material as unreviewed source intake until a reviewed layer or clearly scoped synthesis exists.
