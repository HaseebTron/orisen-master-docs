# Founder Source Categorization Map

Status: Raw/source organization map
Authority level: Raw organization / unverified
Last updated: 2026-05-20
Canonical raw source file:
- `research/external-research/raw/founder-full-source-list.md`
Related raw shortlist:
- `research/external-research/raw/founder-pitch-deck-source-shortlist.md`
Governing docs:
- `research/external-research/README.md`
- `ai-context/claim-control/claim-control-system.md`

## Purpose

This file explains how the founder's full external source list should be routed into problem-first research folders.

It does not replace the canonical raw file. The canonical raw file preserves the original source list as provided. This map explains where each section belongs and how future AI/human review should process it.

## Categorization method used in first pass

First-pass categorization was based on:

- the founder's visible headings
- surrounding notes
- obvious topic labels
- source/domain hints
- whether the item appears to be a paper, article, Reddit/forum link, market report, competitor/review note, or target-segment clue

First-pass categorization was not based on:

- opening every link
- reading every paper in full
- verifying every statistic
- checking whether every URL resolves
- deciding whether a claim is safe for public use

Reason:

- The goal of the first pass is raw organization, not evidence validation.
- Opening and evaluating every link belongs in later research passes.
- The original list contains truncated links, article snippets, survey claims, market-report pages, Reddit links, and possibly AI-generated notes.
- Treating all of that as verified evidence would be unsafe.

## Link preservation rule

- Preserve links exactly as provided in the canonical raw file.
- Do not silently fix, shorten, expand, or replace links.
- If a link looks truncated or unclear, mark it as `needs source verification` later.
- Do not copy the full raw list into problem folders unless a deliberate processing pass is being performed.
- For now, problem-area raw files may point back to the canonical raw archive.

## Problem-first destination folders

External research is organized by Orisen problem area first. Source type belongs inside each entry as metadata.

Current destination folders:

- `research/external-research/waking-up/`
- `research/external-research/going-to-sleep/`
- `research/external-research/during-sleep/`
- `research/external-research/sleep-tracking-and-validation/`
- `research/external-research/competitors-and-substitutes/`
- `research/external-research/market-and-category/`

Each folder uses:

```text
raw/founder-sources.md
synthesis.md
```

## Source type metadata

Use source type inside entries instead of making source type the main folder structure.

Suggested source types:

- research paper
- article/media
- survey/report
- market report
- Reddit/forum
- competitor review
- product page
- expert/organization source
- unknown / needs verification

## Category mapping

### 1. Waking up

Destination folder:

- `research/external-research/waking-up/`

Relevant raw sections in canonical file:

- `Waking up`
- `Sources with Good stats`
- `Proof of Demand → Proof of demand for a more comfortable wakeup`
- parts of `Target Segments Most Likely to Buy`

Use for:

- alarm usage stats
- snoozing stats
- chronic snoozer claims
- oversleeping stats
- bad-morning stats
- get-out-of-bed delay
- wake-up mood impact
- sleep inertia and grogginess
- demand for easier or better wake-up experiences

Highest-priority sources to verify first:

- Nature Scientific Reports heavy snooze study
- PMC sources on snoozing and sleep inertia
- sources connected to sleep inertia, arousal threshold, or wake-stage effects
- survey/article sources only after methodology is checked

Evidence caution:

- This category is closest to Orisen's current wedge.
- Many survey/article sources may be weak or marketing-driven.
- Do not use percentages publicly until the original methodology is checked.
- External research does not prove Orisen works.

### 2. Going to sleep

Destination folder:

- `research/external-research/going-to-sleep/`

Relevant raw sections in canonical file:

- parts of `During Sleep`
- difficulty falling asleep sources
- insomnia prevalence sources
- bedtime, anxiety, white noise, and sleep-onset sources if present

Use for:

- sleep onset problems
- difficulty falling asleep
- bedtime support
- white noise and sound
- circadian light exposure
- future bedtime routines

Evidence caution:

- This is roadmap-relevant but less central to the first wake-up reliability wedge.
- Do not let broad sleep-health stats dilute Orisen's narrow early customer focus.
- Do not make insomnia or treatment claims from these sources.

### 3. During sleep

Destination folder:

- `research/external-research/during-sleep/`

Relevant raw sections in canonical file:

- `During Sleep`
- sleep quality sources
- staying asleep sources
- unrefreshing sleep sources
- daytime sleepiness sources
- sleep duration sources

Use for:

- general sleep quality context
- staying asleep
- nighttime disruptions
- unrefreshing sleep
- daytime sleepiness
- broader sleep-health background

Evidence caution:

- This category helps roadmap and context.
- It is less directly tied to Orisen's first wedge than waking-up evidence.
- Do not use this category to claim Orisen improves sleep quality without Orisen-specific testing.

### 4. Sleep tracking and validation

Destination folder:

- `research/external-research/sleep-tracking-and-validation/`

Relevant raw sections in canonical file:

- sleep tracking sources
- wearable sleep tracker sources
- sleep-stage accuracy sources
- PSG, actigraphy, or validation-method sources
- consumer sleep device limitations
- radar/ML validation references if present

Use for:

- sleep-stage accuracy limits
- consumer sleep tracker limitations
- validation design
- PSG and actigraphy comparison
- radar/ML claim discipline
- sleep-phase-aware intervention claim boundaries

Evidence caution:

- This category is mainly for technical and claims discipline.
- Do not use these sources to claim Orisen accurately detects sleep stages unless Orisen-specific testing supports that claim.

### 5. Competitors and substitutes

Destination folder:

- `research/external-research/competitors-and-substitutes/`

Relevant raw sections in canonical file:

- `Waking up → Reviews and Reddit`
- notes mentioning Hatch, Withings Aura, soft wake-up devices, smartphone alarms, Apple/Android alarm issues, next-generation alarm clocks, and other substitutes
- product reviews and buyer guides
- Reddit/forum posts about products or failed solutions

Use for:

- substitute products
- what buyers already pay for
- what existing products fail at
- whether solutions are pleasant but ineffective or effective but brutal
- partner disturbance
- phone dependence
- alarm reliability problems
- customer language around failed solutions

Evidence caution:

- Competitor evidence is useful for positioning and product learning.
- It does not prove Orisen will win or that users will pay for Orisen.
- Do not cherry-pick negative reviews as if they represent all users.

### 6. Market and category

Destination folder:

- `research/external-research/market-and-category/`

Relevant raw sections in canonical file:

- `Proof of Demand → Proof of Demand for better sleep in general`
- `Market Size & Growth (Sleep Industry in general)`
- broad sleep economy/category sources
- target segment sizing sources when not better routed elsewhere

Use for:

- sleep economy
- sleep aids market
- sleep tech devices market
- alarm clock market
- wearable sleep tracker market
- investor/category framing
- market-growth context

Evidence caution:

- Market reports do not prove demand for Orisen.
- Paid market-report snippets often conflict or use unclear methodology.
- Treat them as category framing, not wedge validation.

## Recommended next processing order

1. Verify and synthesize waking-up, snoozing, oversleeping, and sleep-inertia sources.
2. Process competitor/substitute reviews and extract repeated failure patterns.
3. Extract Reddit/forum customer language into structured raw excerpts only when needed.
4. Process sleep-tracking and validation sources before making sleep-stage or sensor-informed claims.
5. Process going-to-sleep and during-sleep sources for roadmap context.
6. Process market-and-category sources for fundraising context after higher-priority evidence is organized.
7. Use synthesis outputs to update `product/claims-and-evidence.md` only when evidence is verified and claim-safe.

## Next AI research pass

For the next pass, process sources in small batches.

Each processed source should use this format:

```markdown
## Source title

- URL:
- Founder label:
- Original raw source: `research/external-research/raw/founder-full-source-list.md`
- Problem area:
- Source type:
- Topic tags:
- Likely use:
- Current status: saved, not fully analyzed
- Notes:
```

Later, after verification, add more fields if needed:

- author/organization
- publication date
- methodology
- key finding
- limitations
- direct relevance to Orisen
- claims supported
- claims not supported
- confidence level
- whether safe to cite publicly

Do not ask AI to read and conclude from the entire full source list at once.
