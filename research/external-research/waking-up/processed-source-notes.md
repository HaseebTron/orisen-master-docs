# Waking Up Processed Source Notes

Status: Working analysis / source-by-source processing
Authority level: External research interpretation
Last reviewed: 2026-05-20
Governing docs:
- `research/external-research/README.md`
- `research/external-research/waking-up/raw/founder-sources.md`
- `research/external-research/waking-up/waking-up-synthesis.md`
- `ai-context/claim-control/claim-control-system.md`

## Purpose

This file holds source-by-source analysis for waking-up-related external research.

It exists to keep raw founder source intake separate from ChatGPT/human interpretation.

Use this file after a source has actually been opened, read, and checked.

Do not use this file as final public-claim authority. Final claim boundaries belong in:

- `product/claims-and-evidence.md`

## Evidence flow

```text
raw/founder-sources.md
↓
processed-source-notes.md
↓
waking-up-synthesis.md
↓
product/claims-and-evidence.md
↓
downstream product, website, pitch deck, marketing, and X docs
```

## File responsibilities

### `raw/founder-sources.md`

Preserves founder-collected source links, labels, rough stats, and raw routing notes.

It should stay close to the original source material.

### `processed-source-notes.md`

Analyzes individual sources after they are checked.

This file should capture what the source actually says, how reliable it is, what it supports, and what it does not support.

### `waking-up-synthesis.md`

Synthesizes across processed source notes into theme-level conclusions about the waking-up problem.

It should not become a source-by-source archive.

### `product/claims-and-evidence.md`

Promotes only claim-relevant, claim-safe conclusions into Orisen's central claim boundary file.

## Processing rules

- Do not add a processed note unless the source has actually been checked.
- Preserve uncertainty.
- Separate source findings from Orisen interpretation.
- Do not treat survey/media/reddit/review sources as proof of prevalence unless methodology supports it.
- Do not treat external research as proof that Orisen works.
- Do not make medical, clinical, or sleep-disorder claims from external sources without appropriate evidence and claim-control review.
- If a source link is broken, truncated, paywalled, or unclear, mark it honestly.

## Processed source note template

```markdown
## Source: [Source title]

- URL:
- Founder label:
- Original raw source:
  - `research/external-research/waking-up/raw/founder-sources.md`
- Problem area: waking-up
- Source type:
- Topic tags:
- Processing status: verified / partially verified / broken link / needs deeper review
- Processed date: YYYY-MM-DD

### What the source actually says

[Neutral summary of the source's relevant content.]

### Relevant findings for Orisen

- [Finding 1]
- [Finding 2]
- [Finding 3]

### Methodology / basis

- Sample:
- Data type:
- Population:
- Timeframe:
- Methodology notes:

### Source quality

- Evidence strength: weak / medium / strong
- Confidence:
- Main limitations:

### What this source can support

- [Careful conclusion the source can support]

### What this source cannot support

- [Claim the source does not prove]

### Orisen interpretation

[How this source affects Orisen's understanding of the waking-up problem.]

### Claim-control notes

- Safe use:
- Unsafe use:
- Needs verification before public use:

### Downstream routing

- Add to `waking-up-synthesis.md`: yes / no / maybe
- Promote to `product/claims-and-evidence.md`: yes / no / only after more evidence
- Useful for product docs: yes / no / maybe
- Useful for marketing/website: yes / no / maybe
- Useful for pitch deck/fundraising: yes / no / maybe
- Useful for X/content: yes / no / maybe
```

## Processing queue

Start with the highest-priority waking-up sources from `raw/founder-sources.md`:

1. Nature Scientific Reports heavy snooze study. Processed in Batch 1.
2. Snooze/sleep inertia source. Processed in Batch 1 using corrected DOI `https://doi.org/10.1186/s40101-022-00317-w`. The original raw PMC URL `https://pmc.ncbi.nlm.nih.gov/articles/PMC8729838/` appears to be incorrect or misrouted.
3. PMC sleep inertia / clinical population source: `https://pmc.ncbi.nlm.nih.gov/articles/PMC5337178/`. Incomplete Batch 1 processing; needs deeper review because full text was not retrieved.
4. SleepJunkie waking-up survey.
5. MattressNerd / MattressInquirer oversleeping and get-out-of-bed stats.
6. New York Post / Talker Research morning struggles article.
7. Apartment Therapy alarm/snooze stats.
8. TechCrunch / Withings Aura wake-up survey claims.

## Processed source notes

## Source: Snooze alarm use in a global population of smartphone users

- URL: `https://www.nature.com/articles/s41598-025-99563-y`
- Founder label: Nature Scientific Reports heavy snooze study
- Original raw source:
  - `research/external-research/waking-up/raw/founder-sources.md`
- Problem area: waking-up
- Source type: peer-reviewed observational app-data study
- Topic tags:
  - snooze alarms
  - morning waking
  - smartphone sleep tracking
  - wake timing
  - sleep behavior
- Processing status: verified
- Processed date: 2026-05-20

### What the source actually says

This paper analyzes objective snooze-alarm behavior in SleepCycle app users.

The dataset includes 21,222 unique iPhone users who used the traditional snooze feature, logged sleep on at least 50% of nights in each month, consented to research use, and contributed 3,017,276 sleep sessions of at least 4 hours between July 1 and December 31, 2022.

On logged nights, 55.6% of sleep sessions ended with snooze use. Among sessions that ended with snoozing, users pressed snooze an average of 2.4 times and spent an average of 10.8 minutes snoozing.

Snooze use was somewhat lower on weekends, somewhat higher in women than men, higher after longer sleep sessions, and higher when bedtime was later than usual.

The authors explicitly say future research is needed to understand how snooze use affects daytime performance.

### Relevant findings for Orisen

- Repeated snooze behavior is common in this dataset, which means waking often involves multiple alarm interactions rather than a single alarm event.
- Snooze behavior appears to cluster more on weekdays and after later-than-usual bedtimes, suggesting that wake-up difficulty is partly behavioral and schedule-linked, not just a one-time alarm-trigger issue.
- The study does not measure wake completion, out-of-bed behavior, grogginess, or restored alertness after waking, so it helps define the problem space but not the effectiveness of any solution.

### Methodology / basis

- Sample: 21,222 unique users and 3,017,276 sleep sessions.
- Data type: Objective app-derived behavioral log data plus limited demographic fields.
- Population: Self-selected SleepCycle iPhone users who used the traditional snooze feature, consented to research use, and logged sleep on at least 50% of nights each month. The largest country groups were the United States, United Kingdom, Japan, Australia, and Germany.
- Timeframe: July 1, 2022 to December 31, 2022.
- Methodology notes: Sessions had to last at least 4 hours. “Sleep time” was when the user pressed Start in the app, “wake time” was the original alarm, and “sleep duration” excluded snoozing. The analysis used raster plots, bootstrapped user-level averages, ANOVA, t-tests, and sleep-time variability z-scores.

### Source quality

- Evidence strength: medium
- Confidence: medium-high
- Main limitations:
  - The paper's “sleep duration” measure is closer to app-defined time from Start to first alarm than true physiologic sleep duration, because it does not capture sleep latency or awakenings.
  - The authors cannot tell whether users were actually asleep between snooze alarms.
  - The study has no age data.
  - The study does not measure restoration, grogginess, or daytime functioning.
  - The sample is not a general-population sample.
  - The data are proprietary and not public.
  - At least one author is employed by SleepCycle.

### What this source can support

- Snoozing is common among engaged users of a smartphone sleep app.
- Snoozing often consists of repeated alarm cycles rather than a single short delay.
- Wake-up difficulty can plausibly be framed as a wake-completion problem in the sense that stopping an alarm is not always the end of the wake-up process, but this source only supports that indirectly by documenting repeated snooze behavior.
- Snooze behavior in this dataset varies with schedule context such as weekdays and later-than-usual bedtimes.

### What this source cannot support

- It does not prove that snoozing causes poorer daytime performance, more grogginess, or worse health outcomes in these users.
- It does not prove that verifying out-of-bed presence improves waking outcomes.
- It does not validate Orisen, presence-based wake completion, or any product intervention.
- It does not support clinical claims about sleep inertia, sleep-stage effects, or treatment efficacy.

### Orisen interpretation

This source is useful as problem-definition evidence, not solution evidence.

It shows that many wake-ups involve repeated alarm interactions over several minutes, which fits Orisen's focus on wake completion rather than simple alarm dismissal.

But the study stops at describing app behavior. It does not show whether users were awake between snoozes, whether they left bed, whether they felt better or worse afterward, or whether an alternative wake system improves anything.

### Claim-control notes

- Safe use:
  - Internal support for claims like “many people snooze repeatedly” or “stopping an alarm is not always the end of the wake-up process,” as long as the wording stays tied to this app-user dataset.
- Unsafe use:
  - “Snoozing is harmful.”
  - “Snoozing increases sleep inertia.”
  - “People who snooze are not truly awake.”
  - “Orisen solves a scientifically proven wake-completion problem.”
  - Any implication that this paper validates Orisen.
- Needs verification before public use:
  - Any prevalence number presented as population-wide.
  - Any statement connecting snooze behavior to grogginess, sleep inertia, cognitive performance, or health outcomes.

### Downstream routing

- Add to `waking-up-synthesis.md`: yes
- Promote to `product/claims-and-evidence.md`: only after more evidence
- Useful for product docs: yes
- Useful for marketing/website: maybe
- Useful for pitch deck/fundraising: maybe
- Useful for X/content: maybe

## Source: Effects of using a snooze alarm on sleep inertia after morning awakening

- URL: `https://doi.org/10.1186/s40101-022-00317-w`
- Original raw URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC8729838/`
- Processing note: The original raw PMC URL appears to be incorrect or misrouted. The intended source was recovered through DOI `10.1186/s40101-022-00317-w`.
- Founder label: PMC snooze / alarm / sleep inertia source
- Original raw source:
  - `research/external-research/waking-up/raw/founder-sources.md`
- Problem area: waking-up
- Source type: peer-reviewed two-part study combining a student survey and a within-subject sleep-lab experiment
- Topic tags:
  - snooze alarms
  - sleep inertia
  - morning awakening
  - polysomnography
  - reaction time
  - students
- Processing status: partially verified
- Processed date: 2026-05-20

### What the source actually says

The accessible corrected source is an open-access article titled *Effects of using a snooze alarm on sleep inertia after morning awakening*.

It reports two studies.

Study 1 surveyed 293 valid responses from healthy Japanese university students and found that 85.7% often used some tool to wake up, while 70.5% often used their phone's snooze function. The main stated reasons were concern about failing to wake on time and wanting reassurance before sleep.

Study 2 was a small, counterbalanced sleep-lab comparison in 10 habitual snooze users. Compared with a no-snooze condition, the snooze condition shortened total sleep, worsened sleep quality in the final 20 minutes before wake time, increased wakefulness and stage N1 sleep, increased arousals and sleep-stage transitions, and was associated with slower reaction time in the last post-wake test block plus worse subjective vigor after waking.

The authors conclude that snooze use may prolong sleep inertia because it produces repeated forced awakenings.

### Relevant findings for Orisen

- Many student snooze users reported using snooze primarily because they were worried about oversleeping, which points to an emotional/reliability dimension of the wake-up problem, not only a sound-design problem.
- In the lab study, repeated snooze alarms fragmented the last 20 minutes of sleep, with more wake time, more stage N1 sleep, more arousals, and more sleep-stage transitions than the no-snooze condition.
- In that same small lab sample, the snooze condition was associated with slower reaction times later in the post-wake window and worse subjective vigor, which is directionally relevant to the hypothesis that repeated forced awakening may be undesirable.

### Methodology / basis

- Sample:
  - Study 1: 293 valid survey respondents.
  - Study 2: 10 healthy Japanese university students, ages 21–26, who already used a mobile phone snooze function 5 to 7 times per week.
- Data type:
  - Study 1: self-report survey data.
  - Study 2: polysomnography, auditory reaction-time testing, and subjective questionnaires in a sleep laboratory.
- Population: Healthy Japanese university students; the sleep-lab sample consisted of habitual snooze users rather than the general population.
- Timeframe: The accessible text does not provide calendar dates for data collection. For each participant in Study 2, the protocol included one week of monitored home sleep, followed by three consecutive lab nights including one adaptation night and two data-collection nights.
- Methodology notes: In Study 2, the snooze condition used four activations at 5-minute intervals during the last 20 minutes before a predetermined wake time. The no-snooze condition used a single final wake stimulus at the predetermined wake time. The two experimental conditions were counterbalanced across participants. A post hoc power analysis for the Study 2 repeated-measures ANOVA yielded 1–β = .47, indicating low power.

### Source quality

- Evidence strength: medium
- Confidence: medium
- Main limitations:
  - The experimental part is very small (n = 10).
  - The experiment is underpowered.
  - The sample is restricted to healthy Japanese university students.
  - The experiment is limited to habitual snooze users.
  - The study took place in a laboratory with predetermined wake times, so it may not capture real-world behavior or authentic fear of oversleeping.
  - The authors note that other age groups and professions need study.
  - The design did not examine waking-method differences as a function of sleep duration.

### What this source can support

- Repeated snooze alarms can fragment the last part of sleep and, in a small within-subject lab study, were associated with slower later reaction time and worse subjective vigor after waking than a single-alarm condition.
- Some habitual snooze users appear to use snooze partly because they want protection or reassurance against oversleeping.
- The wake-up problem is not only “alarm goes off / user hears it”; it can include repeated awakenings, attempts to return to sleep, and degraded end-of-sleep continuity.

### What this source cannot support

- It does not prove that all snooze use in the general population increases sleep inertia or decreases functioning.
- It does not prove that out-of-bed verification or presence sensing reduces sleep inertia.
- It does not validate Orisen or any other wake device.
- It does not support clinical efficacy claims, sleep-stage detection claims, or claims about reducing grogginess in broad consumer populations.

### Orisen interpretation

This source is useful for the narrow proposition that repeated morning alarm interruptions may be counterproductive.

It supports a design instinct to avoid wake flows that depend on repeated forced awakenings and repeated alarm dismissal.

It also suggests that part of the waking problem is confidence: users want assurance they will not oversleep.

But it still does not show that a presence-based system works better, that leaving bed resolves sleep inertia, or that Orisen should make any public sleep-inertia claim.

### Claim-control notes

- Safe use:
  - Internal support for statements like “repeated snooze cycles may fragment the final part of sleep” or “some users snooze because they worry about oversleeping,” with clear mention that the experimental evidence comes from a very small student lab study.
- Unsafe use:
  - “Snoozing definitely causes sleep inertia in everyone.”
  - “Getting out of bed fixes sleep inertia.”
  - “Orisen reduces grogginess.”
  - “Orisen prevents sleep inertia.”
  - Any clinical-sounding claim derived from this paper.
- Needs verification before public use:
  - Any broad statement about all populations.
  - Any public-facing sleep inertia claim.
  - Any reuse of this paper as if it were direct validation of presence-based wake completion.

### Downstream routing

- Add to `waking-up-synthesis.md`: yes
- Promote to `product/claims-and-evidence.md`: only after more evidence
- Useful for product docs: yes
- Useful for marketing/website: no
- Useful for pitch deck/fundraising: maybe
- Useful for X/content: no

## Source: Waking up is the hardest thing I do all day: Sleep inertia and sleep drunkenness

- URL: `https://pmc.ncbi.nlm.nih.gov/articles/PMC5337178/`
- Founder label: PMC sleep inertia / clinical population source
- Original raw source:
  - `research/external-research/waking-up/raw/founder-sources.md`
- Problem area: waking-up
- Source type: peer-reviewed review article
- Topic tags:
  - sleep inertia
  - sleep drunkenness
  - hypersomnia
  - wake transition
  - clinical sleep medicine
- Processing status: needs deeper review
- Processed date: 2026-05-20

### What the source actually says

Direct full-text access to the provided PMCID was blocked in the Batch 1 Deep Research pass.

Accessible bibliographic metadata identify the source as Lynn M. Trotti's 2017 *Sleep Medicine Reviews* article, *Waking up is the hardest thing I do all day: Sleep inertia and sleep drunkenness* (volume 35, pages 76–84; PMCID PMC5337178; PMID 27692973).

Indirect summaries that cite this review frame it as a paper about impaired wakefulness during the sleep-to-wake transition and its connection to “sleep drunkenness,” including relevance to hypersomnia and other clinically meaningful wake-up difficulty.

Because the full text was not directly reviewed in the Batch 1 pass, the substantive content below should be treated as provisional and verified against the article before any public use.

### Relevant findings for Orisen

- The source is relevant for defining the boundary between ordinary waking friction and clinically significant sleep inertia / sleep drunkenness.
- Indirect summaries tied to the review associate sleep drunkenness with difficulty transitioning from sleep to wake, including confusion, disorientation, and repeated return to sleep; these details still need direct verification from the article itself.
- As a review focused on sleep inertia and sleep drunkenness, the source is more useful for internal problem-framing and medical-boundary setting than for validating any wake-device outcome.

### Methodology / basis

- Sample: Not a primary participant sample; this appears to be a review article rather than a new experiment.
- Data type: Literature review / clinical review. The exact review method could not be extracted because the full text was inaccessible in this pass.
- Population: Likely mixed prior literature with attention to sleep inertia and clinical “sleep drunkenness,” potentially including hypersomnia-related populations, but exact scope was not directly verified.
- Timeframe: Published in 2017. The literature-search window was not directly verifiable in this pass.
- Methodology notes: Because the provided PMC link did not yield article text in the Batch 1 pass, search strategy, inclusion criteria, and evidence hierarchy could not be extracted and should be treated as unknown pending direct review.

### Source quality

- Evidence strength: weak
- Confidence: low
- Main limitations:
  - Full text was not directly retrieved from the provided PMCID during the Batch 1 pass.
  - The article appears to be a review rather than a new primary study.
  - Its clinical focus may not map cleanly onto a general-population consumer waking product.
  - Because the detailed content was not directly verified, this note should not be used as a public evidence source without a fresh pass that retrieves the article itself.

### What this source can support

- Sleep inertia / sleep drunkenness is a recognized topic in sleep-medicine literature rather than just a colloquial complaint about mornings.
- Internal distinction between general wake-up behavior and clinically meaningful wake-transition impairment is important.

### What this source cannot support

- It cannot support any claim that Orisen treats sleep inertia, sleep drunkenness, hypersomnia, narcolepsy, or any other clinical condition.
- It cannot support consumer-prevalence claims or duration claims from this note, because the full text was not directly reviewed.
- It cannot serve as product validation.

### Orisen interpretation

This source is best treated as an internal guardrail.

It suggests that wake completion in a consumer product context should stay clearly separated from clinical sleep-inertia or sleep-drunkenness language unless Orisen later develops much stronger, directly relevant evidence.

In other words, this source is more valuable for narrowing what Orisen should not claim than for supporting what Orisen can claim.

### Claim-control notes

- Safe use:
  - Internal reminder that clinical sleep inertia / sleep drunkenness and ordinary “hard to wake up” behavior are not the same thing.
- Unsafe use:
  - Any public statement that Orisen reduces sleep inertia, treats sleep drunkenness, helps hypersomnia, or has clinically meaningful wakefulness effects.
- Needs verification before public use:
  - All substantive content from this source beyond title-level framing and bibliographic metadata.

### Downstream routing

- Add to `waking-up-synthesis.md`: yes, but only as a caveat/guardrail until full text is reviewed
- Promote to `product/claims-and-evidence.md`: no
- Useful for product docs: yes
- Useful for marketing/website: no
- Useful for pitch deck/fundraising: maybe, but only as internal caution
- Useful for X/content: no
