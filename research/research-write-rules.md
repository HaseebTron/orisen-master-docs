# Research Write Rules

Status: Source of truth
Authority level: Research / Writing rules
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/source-of-truth-rules.md`
- `ai-context/claim-control/claim-control-system.md`
- `research/research-read-rules.md`
Downstream docs:
- Research synthesis files
- Research summary docs
- Claim/evidence update tasks

## Purpose

This file defines how to write or update research docs, especially synthesis files.

Use it after `research/research-read-rules.md` has identified which research inputs matter for the task.

This file does not make research into product truth. It defines how research should be preserved, interpreted, summarized, and routed into claim-control or product docs when appropriate.

## Raw vs processed vs synthesis docs

Keep research layers separate:

- Raw/source docs preserve source material with minimal interpretation.
- Processed docs organize, clean up, or summarize source material without turning it into final conclusions.
- Synthesis docs interpret patterns across multiple sources and state what those patterns may mean for Orisen.

Do not overwrite raw/source material with conclusions. Do not erase raw notes, source lists, transcripts, exports, or founder-provided source material unless the user explicitly asks and repo-governance rules support it.

## Required structure for synthesis files

Synthesis files should usually include:

- Purpose
- Source basis
- Key findings
- Orisen implications
- What this supports
- What this does not support
- Limitations
- Claim-control notes
- Open questions or follow-up research
- Source traceability links

Use this structure flexibly, but every synthesis file should make evidence strength, limitations, and traceability clear.

## How to summarize raw/source files

When summarizing raw or source files:

- Preserve the distinction between what the source says and what Orisen infers from it.
- Link back to the raw/source file for meaningful facts, quotes, data points, or interpretations.
- Summarize only what is relevant to the research question.
- Keep uncertainty visible when source quality, sample size, context, or applicability is weak.
- Avoid turning a single source into a broad market, product, or clinical conclusion.

Raw notes can be messy. Synthesis should be clearer, but it should not pretend the source is stronger than it is.

## How to write Orisen implications safely

Orisen implications should be written as interpretations, not automatic decisions.

Use careful language such as:

- "This suggests..."
- "This may support..."
- "This is consistent with..."
- "This raises a risk that..."
- "This should be tested before..."

Avoid language that implies proof unless the evidence is direct and strong.

When an implication affects product truth, public claims, roadmap, marketing, fundraising, or technical feasibility framing, route it through the relevant higher-authority docs instead of treating the synthesis as final authority.

## Separate facts, interpretation, assumptions, and claims

Research writing must separate:

- Source facts: what the source, interview, expert, study, or raw note actually says.
- Interpretation: what the evidence appears to suggest for Orisen.
- Assumptions: what Orisen believes or hypothesizes but has not proven.
- Claims: statements that could appear in product, marketing, fundraising, investor, technical, or public-facing material.

Do not hide these categories inside polished prose. If a synthesis contains claims, classify whether they are validated, early signal, built but not validated, planned, hypothesis, long-term vision, or unsupported.

## State limitations

Every synthesis file should state limitations when relevant, including:

- small or biased sample
- founder-written notes
- secondary or indirect sources
- sources about adjacent products or contexts
- lab results that may not transfer to real bedrooms
- expert commentary that is directional but not proof
- missing direct Orisen testing
- missing willingness-to-pay, retention, reliability, or efficacy evidence

Limitations are part of the research output, not a footnote to remove later.

## Preserve traceability

Every meaningful synthesis conclusion should be traceable back to raw or processed sources.

Use readable Markdown links to source files. Do not duplicate large raw excerpts unless necessary and allowed. If exact wording matters, link to the raw/source file and quote only the minimum needed.

If a conclusion cannot be traced to a source, label it as an assumption or open question.

## Product claims and evidence

Consult `product/claims-and-evidence.md` when research may affect:

- public product claims
- marketing claims
- fundraising claims
- validation status
- evidence strength
- what Orisen can safely say today

Update `product/claims-and-evidence.md` only when the synthesis produces a durable claim-relevant conclusion that should guide downstream product, marketing, or fundraising work. Do not copy every research detail into it.

## Claim-control docs

Consult `ai-context/claim-control/claim-control-system.md` when classifying evidence, judging claim strength, or deciding whether wording is safe.

Consult `ai-context/claim-control/claim-control-log.md` when the research creates or changes a conservative, claim-relevant evidence entry.

Update claim-control docs only when research materially affects claim safety, evidence classification, validation status, or public-facing language boundaries.

## What not to do

Do not:

- turn research into product truth automatically
- overclaim beyond the evidence
- rewrite raw notes as conclusions
- erase raw/source material
- treat expert commentary as proof by itself
- treat scientific plausibility as evidence that Orisen works
- treat market reports, Reddit posts, reviews, or anecdotes as statistical proof
- imply roadmap or future capabilities are already built or validated
- promote a synthesis conclusion into marketing, fundraising, or product truth without checking the governing docs

Research should improve Orisen's judgment. It should not make unsupported claims sound more official.
