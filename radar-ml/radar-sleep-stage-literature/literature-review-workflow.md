# Radar Sleep-Stage Literature Review Workflow

Status: Working strategy  
Authority level: Radar/ML research workflow  
Last reviewed: 2026-06-12  
Governing docs:
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/claim-control/claim-control-system.md`
- `radar-ml/radar-ml-read-rules.md`
Downstream docs:
- `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/extraction-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/primary-source-chase-pass-1-2026-06-12.md`
- Future v2 raw artifacts under `radar-ml/radar-sleep-stage-literature/raw/`

## Purpose

This file preserves the workflow, intent, scope, current state, completed passes, next steps, and handoff instructions for the radar sleep-stage literature review.

It is meant to let a new ChatGPT chat continue the review without relying on old planning-chat memory.

Keep raw research artifacts separate from this workflow/status document. Raw files preserve source material, searches, screening decisions, and extraction passes. This file explains how to continue the work.

This file must not turn the literature review into Orisen product claims.

## Scope

The current research scope is radar-based sleep-stage, sleep-phase, sleep-state, and sleep/wake classification.

Radar vital-sign-only papers are out of scope unless the vital-sign signals directly feed sleep-stage or sleep-state classification.

Exclude WiFi CSI, camera, microphone, wearable-only, ECG-only, PPG-only, bed pressure-only, and mattress sensor-only sources unless they are explicitly needed as background for feature design, validation design, or comparison.

Prioritize sources that connect radar signals to PSG labels, expert sleep labels, sleep-stage labels, sleep-state labels, or sleep/wake labels.

## What this workflow is trying to answer

This workflow is trying to determine:

- Which radar devices, radar types, and signal outputs have been used for sleep-stage or sleep-state classification.
- Which radar-derived inputs and features repeatedly appear in credible papers.
- Whether respiration and movement are enough, or whether papers rely on HR, HRV, RRV, waveform, phase, IQ, raw radar, or semi-raw radar data.
- Which methods, datasets, and feature pipelines look reproducible.
- Which papers are least applicable to Orisen because of population, hardware, label, validation, or modality mismatch.
- What radar data access Orisen should require before trusting a module for sleep-stage-aware wake intervention experiments.
- What Orisen should test before relying on sleep-stage-aware or sleep-state-aware intervention.

## Claim boundary

Do not treat papers as proof that Orisen can currently detect sleep stages, reduce grogginess, reduce sleep inertia, move users between sleep stages, or perform sleep-stage-aware wake intervention.

This literature review is technical evidence, design guidance, radar-selection input, feature-design input, and validation-planning input only.

Any future Orisen claim about sleep-stage sensing, vital-sign sensing, grogginess reduction, sleep-inertia reduction, sleep-phase-aware intervention, artificial sleep phase transitioning, real-time sleep-state control, or public product capability must go through Orisen-specific validation and claim-control review.

## Current state

The v1 literature review completed:

1. Deep Research discovery pass.
2. Screening Pass 1.
3. Extraction Pass 1 for the 12 screened P0 sources.
4. Primary-Source Chase Pass 1 for several weak P0 rows.

The v1 work is useful but should now be treated as a historical baseline, not the final source universe.

The current recommended next step is a v2 workflow restart that uses external literature tools, citation-graph expansion, source-access chasing, and better extraction discipline before synthesis.

Do not run broad synthesis yet.

## v1 artifact status

The existing raw artifacts remain preserved under:

`radar-ml/radar-sleep-stage-literature/raw/`

Current v1 artifacts:

- `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/extraction-pass-1-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/primary-source-chase-pass-1-2026-06-12.md`

Do not delete, overwrite, or reorganize these raw files during the v2 research workflow.

If v2 later makes v1 obsolete, mark v1 artifacts as superseded or move/archive them only after a separate repo-governance pass that checks current file reality, references, and repo-file-map impact.

Use `ai-context/repo-governance/repo-file-map.md` for durable file inventory. Do not duplicate the full raw file tree in this workflow doc.

## v2 operating model

The v2 workflow uses external tools for search and first-pass assistance, but GPT worker chats remain responsible for verification, classification, extraction discipline, and Orisen claim safety.

Tool outputs are inputs, not authorities.

Do not accept an AI literature tool's extracted detail as final unless it can be traced to the paper, PDF, abstract, DOI page, publisher page, PubMed page, arXiv page, author copy, dataset page, or another legal primary or near-primary source.

Use the mother/planning chat for:

- workflow design
- deciding which pass to run next
- reviewing worker-chat outputs
- deciding whether repo updates are needed
- keeping claims boundaries visible
- preserving the overall research state

Use worker chats for:

- discovery expansion
- candidate-register cleanup
- source-access chase
- extraction passes
- verification passes
- repository/code search
- dataset search
- synthesis drafts after extraction is complete

## Tool role map

### External literature and AI tools

Use these tools as search and extraction helpers, not final truth sources.

- **Elicit**:
  - Broad paper discovery.
  - Initial literature tables.
  - First-pass extraction suggestions.
  - Similar-paper discovery from seed titles.

- **Semantic Scholar**:
  - Citation graph expansion.
  - DOI, author, venue, citation, and reference metadata.
  - Finding newer papers that cite seed papers.

- **OpenAlex**:
  - Programmatic bibliographic search.
  - Metadata cleanup.
  - Cross-checking titles, authors, venues, DOIs, and publication years.

- **ResearchRabbit / Litmaps**:
  - Visual citation trails.
  - Related-work discovery.
  - Backward and forward citation expansion.
  - Cluster discovery from seed papers.

- **SciSpace / PDF-chat tools**:
  - First-pass PDF reading.
  - Locating methods, features, datasets, limitations, and performance tables.
  - Must be verified against actual paper text before formal extraction.

- **Google Scholar / publisher search / PubMed / arXiv / IEEE / ACM / MDPI / Frontiers / institutional pages**:
  - Legal source access.
  - DOI/PDF/source chase.
  - Verification of exact bibliographic and methods details.

- **GitHub search**:
  - Code availability.
  - Paper-title, author-name, dataset-name, and model-name repository search.
  - Separate true radar sleep-stage repos from generic sleep-stage or vital-sign repos.

### GPT roles

- **Mother chat**:
  - Planner and coordinator.
  - Maintains the workflow state.
  - Decides when to move to the next pass.
  - Reviews worker-chat outputs before repo promotion.

- **Worker GPT chats inside Orisen Radar + ML**:
  - Run one bounded pass at a time.
  - Verify external-tool outputs.
  - Keep extracted facts traceable.
  - Classify uncertainty.
  - Stop at the requested boundary.

- **Orisen General**:
  - Use only if the work changes product claims, roadmap priority, public positioning, fundraising story, customer promise, or validated evidence status.

## v2 workflow phases

### Phase 0: Context and artifact setup

Before continuing the v2 review, read:

- `ai-context/start-here.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
- `ai-context/claim-control/claim-control-system.md`
- `radar-ml/radar-ml-read-rules.md`
- `radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`

Use v1 artifacts as starting context, not final truth.

Do not write to the repo unless explicitly asked.

### Phase 1: v2 discovery expansion

Goal: find a more complete and higher-quality source universe than v1.

Search using:

- seed papers from the v1 P0/P1/P2/Hold list
- Elicit
- Semantic Scholar
- OpenAlex
- ResearchRabbit / Litmaps
- Google Scholar and publisher search
- PubMed, arXiv, IEEE, ACM, MDPI, Frontiers, and institutional pages

Search targets:

- radar sleep-stage classification
- radar sleep-state classification
- radar sleep/wake classification
- radar PSG-labeled sleep monitoring
- UWB radar sleep staging
- IR-UWB radar sleep staging
- FMCW radar sleep staging
- Doppler radar sleep staging
- radar respiratory/movement features used for sleep labels
- radar HR/HRV/RRV features used for sleep labels
- consumer or clinical radar sleep-monitoring systems with papers

Output should be a raw v2 discovery artifact, not a synthesis.

Recommended new raw artifact name:

`radar-ml/radar-sleep-stage-literature/raw/v2-discovery-expansion-YYYY-MM-DD.md`

### Phase 2: Candidate register

Create one master candidate register before deep extraction.

The register should include every candidate source and these fields:

- canonical title
- year
- authors
- venue/source type
- DOI or stable identifier
- legal source link
- PDF/full-text availability
- radar type
- radar frequency
- specific radar/device/chip/module if known
- population
- subject count / nights
- ground truth or reference label source
- sleep labels predicted
- radar-only vs multimodal
- duplicate/version group
- source-access status
- classification category
- priority
- extraction readiness
- notes / caveats

Recommended new raw artifact name:

`radar-ml/radar-sleep-stage-literature/raw/v2-candidate-register-YYYY-MM-DD.md`

### Phase 3: Deduplication and version grouping

Before extraction, group:

- preprint and journal versions
- conference and journal extensions
- same dataset reused across multiple papers
- same research group/system line
- companion papers that share hardware, dataset, or model

Do not silently merge versions.

If a preprint has richer methods than a journal page, use it as a supplementary source while noting the version relationship.

### Phase 4: Screening and priority assignment

Screen each source into one category:

- **A: Direct radar sleep-stage classification**
- **B: Radar sleep/wake classification**
- **C: Radar sleep-state estimation with PSG or sleep labels**
- **D: Radar sleep monitoring but no clear stage/state classification**
- **E: Radar vital signs only**
- **F: Non-radar sleep-stage source**
- **G: Exclude**

Radar vital-sign-only sources belong in E unless the vital signs directly feed sleep-stage or sleep-state classification.

Non-radar sleep-stage sources belong in F only when they are useful for feature design, model design, validation design, or comparison. Otherwise exclude them.

Assign priority:

- **P0**: Extract first. Directly relevant, high-value, and likely important for radar sleep-stage or sleep-state classification.
- **P1**: Extract after P0. Relevant but narrower, older, weaker, pediatric/neonatal, sleep/wake only, or less directly applicable.
- **P2**: Useful background, citation-trail source, or feature/validation context.
- **Hold**: Do not extract yet. Needs full text, source verification, radar/label clarification, or better bibliographic identity.
- **Exclude**: Out of scope for this review.

### Phase 5: Source-access chase

Before deep extraction, chase legal primary or near-primary sources.

Acceptable sources include:

- publisher full text
- PDF from publisher, arXiv, institutional repository, or author page
- PubMed abstract
- DOI landing page
- conference proceedings page
- official dataset page
- official code repository
- official product or company technical paper, with caveats

Do not use pirated PDFs or inaccessible sources.

For each source, assign source-access status:

- Full PDF available
- Full HTML available
- Abstract only
- Metadata only
- Blocked / paywalled
- Source identity unresolved
- Duplicate/version only

### Phase 6: Extraction readiness gate

Before any deep extraction, assign one readiness category:

- Ready for extraction
- Needs primary-source access first
- Needs bibliographic cleanup
- Duplicate / merge with another source
- Exclude
- Background only

Do not run deeper extraction on a paper whose identity, primary source, radar involvement, or label set is still too uncertain.

Ready for extraction does not mean the source is more relevant than pending sources. It only means the source has enough legal source access to extract without guessing.

### Phase 7: Extraction Pass 1, objective top-level facts

For each ready source, extract:

- hyperlinked title
- year
- source type
- specific radar/device/chip/module used
- radar type
- frequency
- placement and distance
- subject count / nights
- population
- radar-only or multimodal
- ground truth / reference label source
- sleep labels predicted
- confidence / notes

If the paper does not state the exact radar, write `not stated`.

Do not guess radar model, frequency, placement, or labels.

### Phase 8: Extraction Pass 2, deeper technical details

For each ready source, extract:

- radar inputs/features used
- respiration waveform
- breathing rate
- breath-to-breath intervals / RRV / BRV
- heart rate
- heartbeat waveform
- inter-beat intervals / HRV
- movement/body motion
- posture
- radar phase / range-bin phase
- IQ / complex samples
- radar cube / raw or semi-raw radar data
- model/method
- epoch length
- reported performance: accuracy / F1 / Cohen's kappa / sensitivity / specificity
- real-time vs offline
- code/data availability
- key limitations
- reproducibility
- relevance to radar-based sleep-stage classification
- confidence level for extracted facts

Extraction Pass 2 should be objective extraction, not synthesis.

It should record what each paper states, what is inferred, and what remains not stated.

### Phase 9: Verification pass

Re-check the most important P0 and strong P1 papers.

Verify:

- exact radar used
- exact input features
- exact ground truth
- exact label mapping
- exact performance numbers
- whether code/data are actually available
- whether the method is real-time or offline
- whether the source is radar-only or multimodal

Use confidence labels:

- **High**: directly stated and verified.
- **Medium**: strongly implied or stated in a near-primary source.
- **Low**: uncertain, indirect, or source-limited.
- **Not stated**: paper/source does not say.

### Phase 10: Code, repo, and dataset search

After the main paper list is stable, search for:

- paper title repositories
- author repositories
- model names
- dataset names
- radar sleep-stage code
- radar sleep/wake code
- UWB/FMCW/Doppler sleep-stage code
- PSG plus radar datasets
- radar plus sleep-label datasets

Separate:

- true radar sleep-stage repos
- generic sleep-stage repos
- radar vital-sign repos
- non-radar repos
- toy or unrelated repos

Do not treat a repo as usable until inputs, labels, license, and reproducibility are checked.

### Phase 11: Synthesis

Run synthesis only after the candidate register, extraction passes, and verification pass are complete enough.

Synthesis should answer:

- Which radars were most commonly used?
- Which radar types seem most promising?
- What features are repeatedly used for radar sleep staging?
- Is respiration plus movement enough, or do papers rely on HR/HRV too?
- Do papers use waveform, phase, IQ, range-bin phase, or raw/semi-raw radar data?
- What accuracy/kappa ranges are realistic in the literature?
- Which methods seem reproducible?
- Which papers are least applicable to Orisen?
- What radar data access should Orisen require?
- What should Orisen test before trusting sleep-stage-aware wake intervention?

Do not convert synthesis into product claims.

### Phase 12: Orisen technical decision output

Only after synthesis, convert the research into practical technical recommendations:

- best radar candidates to investigate
- minimum required radar outputs
- red flags for black-box sensors
- source-access or data-access requirements
- first validation experiments
- sleep-stage model feature requirements
- claims Orisen still cannot make

If this step changes product roadmap, public claims, fundraising narrative, customer promise, or validated evidence status, escalate to Orisen General before updating product or claims docs.

## Quality-control rules

- Do not guess missing details.
- If the paper does not state something, write `not stated`.
- Separate direct paper statements from inference.
- Prefer primary-source verification over AI summaries.
- Keep citations and links traceable.
- Preserve confidence labels for extracted facts.
- Keep radar-only, radar-plus-other-sensor, and non-radar sources separate.
- Do not silently merge preprint and journal versions without noting the version relationship.
- Do not treat patents as validation.
- Do not treat company whitepapers or product-led preprints as independent validation without caveats.
- Do not rewrite or overwrite raw artifacts unless the user explicitly asks.
- Do not write to the repo unless the user explicitly asks.

## Current recommended next step

The immediate next step is **v2 Discovery Expansion**, not Extraction Pass 2.

The next worker chat should:

1. Read this workflow file.
2. Read v1 screening and discovery artifacts only as seed context.
3. Use external literature tools and citation-graph expansion to find missed radar sleep-stage, sleep-state, and sleep/wake sources.
4. Produce a new v2 discovery expansion artifact or draft output.
5. Stop before extraction.

Do not delete or replace v1 raw files during this step.

## Handoff prompt: v2 discovery expansion worker chat

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

This is a continuation of the Orisen Radar + ML radar sleep-stage literature workflow.

Read and follow:

`radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`

Do not rely on memory from prior chats.
Do not write to the repo unless I explicitly ask.
Do not make Orisen product claims.

Task:
Run v2 Discovery Expansion for radar-based sleep-stage, sleep-state, and sleep/wake classification papers.

Use the existing v1 raw artifacts only as seed context, not final truth:
- `radar-ml/radar-sleep-stage-literature/raw/discovery-pass-2026-06-12.md`
- `radar-ml/radar-sleep-stage-literature/raw/screening-pass-1-2026-06-12.md`

Use external tools where helpful:
- Elicit for broad paper discovery and first-pass paper tables
- Semantic Scholar for citations, references, DOI metadata, and related papers
- OpenAlex for bibliographic cleanup and metadata cross-checking
- ResearchRabbit / Litmaps for citation graph expansion
- Google Scholar, PubMed, arXiv, IEEE, ACM, MDPI, Frontiers, publisher pages, and institutional pages for source verification

Search for:
- radar sleep-stage classification
- radar sleep-state classification
- radar sleep/wake classification
- UWB / IR-UWB radar sleep staging
- FMCW radar sleep staging
- Doppler radar sleep staging
- radar PSG-labeled sleep monitoring
- radar respiratory or movement features used for sleep labels
- radar HR/HRV/RRV features used for sleep labels

Output:
- A candidate list of newly found or confirmed sources.
- Mark whether each source is new, already in v1, duplicate/version-linked, or uncertain.
- Include title, year, DOI/source link if available, radar type, label type, ground truth/reference source if known, and why it may matter.
- Do not deeply extract methods yet.
- Do not synthesize Orisen implications yet.
- Stop after discovery expansion.
```

## Handoff prompt: candidate register cleanup worker chat

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

This is a continuation of the Orisen Radar + ML radar sleep-stage literature workflow.

Read and follow:

`radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`

Do not rely on memory from prior chats.
Do not write to the repo unless I explicitly ask.
Do not make Orisen product claims.

Task:
Create or clean the v2 master candidate register from the v1 artifacts and the v2 discovery expansion output provided in this chat.

For each source, classify:
- category: A/B/C/D/E/F/G
- priority: P0/P1/P2/Hold/Exclude
- duplicate/version group
- source-access status
- extraction readiness

Do not run extraction yet.
Stop after the candidate register and readiness classification.
```

## Handoff prompt: extraction worker chat

```text
Read `ai-context/start-here.md` from `HaseebTron/orisen-master-docs` using GitHub.

This is a continuation of the Orisen Radar + ML radar sleep-stage literature workflow.

Read and follow:

`radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`

Do not rely on memory from prior chats.
Do not write to the repo unless I explicitly ask.
Do not make Orisen product claims.

Task:
Run the requested extraction pass only on sources marked ready for extraction in the provided candidate register.

Rules:
- Objective extraction only, not synthesis.
- Do not guess missing details.
- If the paper does not state something, write `not stated`.
- Separate direct paper statements from inference.
- Prefer primary-source verification.
- Keep citations and links traceable.
- Preserve confidence labels for extracted facts.
- Do not turn any result into Orisen product evidence or product claims.
- At the end, list which sources still need PDF/full-text follow-up.
```
