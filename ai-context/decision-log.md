# Decision Log

## Purpose

This file records major Orisen source-of-truth, workflow, product, strategy, and documentation decisions.

It is not a replacement for detailed docs.

Use it to preserve the reasoning behind important decisions so future chats do not lose context or accidentally reverse decisions without noticing.

## How to use this file

Add an entry when a decision affects:

- company truth
- product direction
- target customer
- claims
- evidence standards
- roadmap
- ChatGPT workflow
- project routing
- source-of-truth hierarchy
- major documentation structure
- marketing or fundraising narrative
- cross-domain tradeoffs

Do not log tiny wording edits or temporary drafts.

## Entry format

```markdown
## YYYY-MM-DD — Decision title

Decision:
- [What was decided]

Reason:
- [Why this decision was made]

Impacted docs:
- `[file/path.md]`

Implications:
- [What downstream work should do differently]

Open questions:
- [Any unresolved questions]
```

## 2026-05-16 — AI operating mode added

Decision:
- ChatGPT should act as a non-agreeable, high-context company reasoning partner when working on Orisen.
- The AI should reason from high-level source-of-truth docs downward and treat the user's latest message as a proposal, not as source-of-truth.

Reason:
- Orisen's documentation workflow depends on high-level docs grounding lower-level docs.
- If ChatGPT passively agrees with the user or writes lower-level docs from the latest prompt alone, the documentation hierarchy can become contaminated.
- The company needs AI assistance that protects source-of-truth consistency, evidence discipline, product focus, and claims safety.

Impacted docs:
- `ai-context/ai-operating-mode.md`
- `ai-context/doc-creation-rules.md`
- `ai-context/start-here.md`
- `ai-context/context-map.md`
- `ai-context/source-of-truth-rules.md`

Implications:
- Future Orisen chats should not merely load docs and answer agreeably.
- They should challenge weak, overclaimed, stale, or contradictory requests.
- Lower-level docs should be drafted from higher-level docs, validation evidence, and relevant domain context.

Open questions:
- Whether older docs need metadata blocks added manually over time.
- Whether each folder should later receive a stricter context map and doc template.

## 2026-05-16 — Evidence standard added

Decision:
- Orisen should classify evidence and claims using a shared evidence standard.

Reason:
- Orisen's product direction includes validated features, early signals, planned features, technical hypotheses, and long-term vision.
- Without a common evidence standard, marketing, fundraising, and product docs could overstate grogginess reduction, sleep-stage accuracy, or artificial sleep phase transitioning.

Impacted docs:
- `validation/evidence-standard.md`
- `validation/evidence-log.md`
- `product/claims-and-evidence.md`
- marketing docs
- fundraising docs
- radar/ML docs

Implications:
- Claims should be classified as validated, early signal, built but not validated, planned, hypothesis, long-term vision, or unsupported.
- Public-facing claims should become stronger only when evidence becomes stronger.

Open questions:
- Whether current evidence-log entries should be reformatted to match the new evidence standard.
