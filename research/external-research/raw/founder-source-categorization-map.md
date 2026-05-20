# Founder Source Categorization Map

Status: Raw/source organization map
Authority level: Raw organization / unverified
Last updated: 2026-05-20
Canonical raw source file:
- `research/external-research/raw/founder-full-source-list.md`
Related raw shortlist:
- `research/external-research/raw/founder-pitch-deck-source-shortlist.md`

## Purpose

This file explains how the founder's full external source list should be split into evidence categories.

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
- Opening and evaluating every link belongs in the next research pass.
- The original list contains truncated links, article snippets, survey claims, market-report pages, Reddit links, and possibly AI-generated notes. Treating all of that as verified evidence would be unsafe.

## Link preservation rule

- Preserve links exactly as provided in the canonical raw file.
- Do not silently fix, shorten, expand, or replace links.
- If a link looks truncated or unclear, mark it as `needs source verification` later.
- If the same source appears in multiple categories, do not duplicate the raw source unless needed. Point back to the canonical raw list.

## Category mapping

### 1. Waking up / snoozing / oversleeping

Destination synthesis folder:

- `research/external-research/sleep-inertia/`

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
- demand for easier or better wake-up experiences

Highest-priority sources to verify first:

- Nature Scientific Reports heavy snooze study
- PMC sources on snoozing and sleep inertia
- Washington Post / Time summaries only if they point to primary research
- SleepJunkie / Withings / survey sources only after checking methodology

Evidence caution:

- This category is closest to Orisen's wedge.
- Still, many survey/article sources may be weak or marketing-driven.
- Do not use percentages publicly until the original methodology is checked.

### 2. Sleep inertia / sleep science / wake-stage claims

Destination synthesis folder:

- `research/external-research/sleep-inertia/`

Relevant raw sections in canonical file:

- `Impact of Poor Wake-Up Experience`
- sleep inertia notes under `Proof of Demand → Proof of demand for a more comfortable wakeup`
- nurse / shift-worker / severe sleep-inertia target-segment notes
- PMC links related to sleep inertia

Use for:

- grogginess
- sleep inertia duration
- waking from sleep stages
- arousal threshold
- clinical populations with severe sleep inertia
- claim boundaries around “easier wake-up”

Highest-priority sources to verify first:

- PMC sleep inertia review links
- nurse severe sleep-inertia source
- any source that discusses sleep-stage effects, arousal threshold, or clinical populations

Evidence caution:

- Scientific plausibility is not Orisen-specific validation.
- Do not use this category to claim Orisen reduces grogginess or sleep inertia before Orisen-specific testing.

### 3. General sleep health / falling asleep / poor sleep stats

Destination synthesis folder:

- `research/external-research/articles-and-media/`
- some high-quality sources may also belong in future `research/external-research/sleep-inertia/` if they discuss wake outcomes directly

Relevant raw sections in canonical file:

- `During Sleep`
- `Sources with Good stats`

Use for:

- general sleep trouble prevalence
- falling asleep stats
- staying asleep stats
- unrefreshing sleep
- daytime sleepiness
- broad sleep-health context

Higher-quality sources to verify first:

- CDC
- National Sleep Foundation
- Statistics Canada
- Sleep Foundation
- peer-reviewed PMC sources

Lower-priority / caution sources:

- StudyFinds
- mattress/affiliate blogs
- article aggregators

Evidence caution:

- This category helps context and fundraising narrative.
- It is less directly tied to Orisen's first wedge than waking/snoozing/oversleeping evidence.

### 4. Reddit / forum customer language

Destination synthesis folder:

- `research/external-research/reddit-forums/`

Relevant raw sections in canonical file:

- `Waking up → Reviews and Reddit`
- `Proof of Demand → Proof of demand for a more comfortable wakeup → Reddit threads`

Use for:

- exact customer language
- severe pain examples
- what people tried
- what failed
- emotional language around waking up, grogginess, ADHD, and getting out of bed

Evidence caution:

- Reddit is useful for language and qualitative pain discovery.
- Reddit should not be treated as statistical evidence.
- Copy short excerpts and links only. Do not turn Reddit anecdotes into prevalence claims.

### 5. Competitor reviews / substitutes

Destination synthesis folder:

- `research/external-research/competitor-reviews/`

Relevant raw sections in canonical file:

- `Waking up → Reviews and Reddit`
- notes mentioning Hatch, Withings Aura, soft wake-up devices, smartphone alarms, Apple/Android alarm issues, next-generation alarm clocks, and soft wake devices

Use for:

- substitute products
- what buyers already pay for
- what existing products fail at
- whether solutions are “pleasant but ineffective” or “effective but brutal”
- partner disturbance
- phone dependence
- alarm reliability problems

Evidence caution:

- The current list has pointers, not enough structured review data.
- A proper competitor-review pass should collect reviews from Amazon, App Store, Google Play, Reddit, and product review sites separately.

### 6. Market reports / category size / investor context

Destination synthesis folder:

- `research/external-research/market-reports/`

Relevant raw sections in canonical file:

- `Proof of Demand → Proof of Demand for better sleep in general`
- `Market Size & Growth (Sleep Industry in general)`

Use for:

- sleep economy
- sleep aids market
- sleep tech devices market
- sleep disorder market
- sleep apnea device market
- investor/category framing
- funding and market-growth context

Evidence caution:

- Market reports do not prove demand for Orisen.
- Paid market-report snippets often conflict or use unclear methodology.
- Treat them as category framing, not wedge validation.

### 7. Target segments

Destination synthesis folder:

- `product/target-customer.md`
- `research/external-research/sleep-inertia/`
- `research/external-research/articles-and-media/`

Relevant raw sections in canonical file:

- `Target Segments Most Likely to Buy`

Use for:

- nurses
- heavy sleepers
- chronic snoozers
- health-conscious consumers
- shift workers
- students
- professionals with strict schedules

Evidence caution:

- These are segment hypotheses, not validated ICP conclusions.
- Keep the primary ICP behavioral: people who repeatedly fail between alarm time and actually being out of bed.

## Recommended next processing order

1. Verify and synthesize waking/snoozing/oversleeping sources.
2. Verify and synthesize sleep inertia / wake-stage science sources.
3. Extract Reddit/forum language into a dedicated raw excerpt file.
4. Collect structured competitor-review data from original review sources.
5. Process market reports only after the above are done.
6. Use the resulting synthesis to update `product/target-customer.md` and `product/claims-and-evidence.md`.

## Next AI research pass

For the next pass, each source should be moved from raw intake to structured source notes with:

- source title
- link
- source type
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

Do this in small batches. Do not ask AI to read and conclude from the entire full source list at once.
