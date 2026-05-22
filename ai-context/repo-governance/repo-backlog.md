# Repo Backlog

Status: Working backlog
Authority level: AI context / Repo governance / Planning
Last reviewed: 2026-05-22
Governing docs:
- `ai-context/repo-governance/repo-purpose.md`
- `ai-context/repo-governance/repo-operating-model.md`
- `ai-context/repo-governance/repo-structure.md`
- `ai-context/repo-governance/repo-file-map.md`
- `ai-context/repo-governance/repo-change-checklist.md`
Downstream docs:
- Future repo cleanup sessions
- Future source-of-truth doc creation tasks
- Future folder context-map updates

## Purpose

This file tracks Orisen source-of-truth docs, sections, evidence, decisions, and cleanup items that should be created, filled in, or revisited later.

Use this file when a needed doc or section is identified but should not be fully written yet.

This file should stay lightweight. It is a checklist, not a strategy document.

Before acting on a backlog item, check `ai-context/repo-governance/repo-file-map.md` to confirm whether the file already exists, was renamed, or should still be created.

## Recurring checks

- [ ] Run repo integrity check monthly or after major source-of-truth updates.
  - Load the Orisen General full reference pack from `ai-context/context-map.md`.
  - Check for contradictions, stale docs, authority ambiguity, missing propagation updates, missing evidence entries, and missing decision-log entries.
  - Do not rewrite the repo automatically. Produce a prioritized cleanup list first.

## Created starter docs that need future fill-in

- [ ] `product/target-customer.md`
  - Status: Starter doc created.
  - Needs: Narrower first customer segment, excluded users, pain-level criteria, willingness-to-pay evidence, and early pilot target.

- [ ] `product/roadmap.md`
  - Status: Starter doc created.
  - Needs: More specific sequencing after software, hardware, radar, pilot, and validation progress become clearer.

- [ ] `software/software-context-map.md`
  - Status: Starter doc created.
  - Needs: Links or summaries from the current Orisen Software repo docs, active slice docs, and implementation status.

- [ ] `radar-ml/radar-ml-context-map.md`
  - Status: Starter doc created.
  - Needs: More detail when radar/ML work becomes active, including radar module decisions, signal-processing docs, model docs, and validation docs.

- [ ] `marketing/positioning-and-messaging.md`
  - Status: Starter doc created.
  - Needs: Customer language, tested messaging, website results, and positioning refinements.

- [ ] `marketing/post-performance-log.md`
  - Status: Existing durable doc.
  - Needs: Ongoing post/campaign metrics, waitlist impact, comments/replies, lessons, and reusable content ideas.

- [ ] `fundraising/investor-narrative.md`
  - Status: Starter doc created.
  - Needs: Stronger traction, evidence, deck narrative, investor feedback, and fundraising-specific proof points.

## Evidence and validation backlog note

Do not create `validation/evidence-log.md` by default.

Current evidence and validation routing should use:

- `product/claims-and-evidence.md` for product claim boundaries and evidence summaries
- `ai-context/claim-control/claim-control-log.md` for durable claim-control decisions
- `marketing/post-performance-log.md` for marketing performance and waitlist evidence
- source-specific research folders for raw/source material and synthesis

Create a separate `validation/evidence-log.md` only if evidence volume becomes large enough that the existing product, claim-control, marketing, and research docs are no longer enough.

## Marketing + GTM doc build order

Use this order to build the minimum source-of-truth docs needed for founder-led X content.

This table is a doc-building workflow, not source-of-truth product strategy. The actual source of truth remains in the docs listed below.

| Step | File | Depth | What the file will contain |
|---:|---|---|---|
| 1 | `ai-context/current-state.md` | Light draft, not fully filled in | Current working truth for Orisen: what it is, current product direction, assumed audience, validated wedge, planned direction, uncertainty, and claims boundaries. |
| 2 | `product/product-overview.md` | Light draft | Plain-English product plan: what Orisen does, what is built, MVP scope, first customer-ready product, and long-term vision. |
| 3 | `product/target-customer.md` | Deeper work | First target customer assumptions, excluded users, pain points, urgency, willingness-to-pay assumptions, alternatives, objections, and open validation questions. |
| 4 | `ai-context/current-state.md` | Update after target customer work | Revise audience, first problem, current priority, and open questions based on target customer work. |
| 5 | `product/claims-and-evidence.md` | Careful work | Safe claims, careful claims, claims to avoid, what is validated, what is assumed, and what evidence is needed for stronger claims. |
| 6 | `ai-context/claim-control/claim-control-log.md` | Evidence cleanup | Durable claim-control decisions and evidence entries that materially affect product, marketing, fundraising, or technical claims. |
| 7 | `product/product-overview.md` | Update after claims/evidence | Separate built features, MVP scope, first customer-ready product, roadmap, and long-term vision. |
| 8 | `ai-context/current-state.md` | Mostly filled in | Finalize top-level current truth after product, customer, claims, and evidence docs are clearer. |
| 9 | `marketing/positioning-and-messaging.md` | Messaging draft | Simple explanation, main wedge, what to emphasize, what to avoid, safe phrases, careful phrases, and default positioning. |
| 10 | `marketing/customer-language.md` | Deeper research | Exact customer language about oversleeping, alarms, grogginess, going back to bed, failed routines, frustration, and desired outcomes. |
| 11 | `marketing/positioning-and-messaging.md` | Update after customer language | Improve messaging using real customer language. |
| 12 | `marketing/content-pillars.md` | Content system | Recurring topics for founder-led content: broken mornings, building Orisen, sleep tech opinions, customer pain, founder lessons, product progress, traction, and vision. |
| 13 | `marketing/founder-led-content.md` | Founder voice | Tone, beliefs, founder story, recurring opinions, technical depth, vulnerability level, and what to avoid. |
| 14 | `marketing/x-playbook.md` | X strategy | Target audience on X, cadence, formats, hooks, reply strategy, CTA rules, build-in-public rules, and examples. |
| 15 | `marketing/tweet-bank.md` | Execution doc | Drafted tweets, hooks, threads, replies, build updates, customer-pain posts, founder takes, and CTAs. |
| 16 | `marketing/weekly-content-calendar.md` | Execution doc | Weekly posting plan and content mix. |
| 17 | `marketing/post-performance-log.md` | Existing execution doc | Track post performance, lessons, signups, replies, and reusable ideas. |

## Future docs to consider later

Do not create these unless the workstream becomes active enough to justify them.

- [ ] `business/business-model.md`
- [ ] `business/pricing.md`
- [ ] `business/competitors.md`
- [ ] `hardware/hardware-context-map.md`
- [ ] `hardware/hardware-overview.md`
- [ ] `marketing/customer-language.md`
- [ ] `marketing/content-pillars.md`
- [ ] `marketing/founder-led-content.md`
- [ ] `marketing/gtm.md`
- [ ] `marketing/linkedin-playbook.md`
- [ ] `marketing/x-playbook.md`
- [ ] `marketing/tweet-bank.md`
- [ ] `marketing/weekly-content-calendar.md`
- [ ] `fundraising/traction.md`
- [ ] `fundraising/outreach-strategy.md`

## Notes

- Add items here when a future doc, missing section, or cleanup task is identified.
- Check off items once the relevant doc is created and filled in enough to be useful.
- Keep this file simple. Do not turn it into a second source-of-truth system.
