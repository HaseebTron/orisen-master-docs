# Source-of-Truth Rules

## Purpose of this file

This file defines how Orisen documentation should be interpreted, updated, and used as context.

Its job is to prevent old notes, brainstorms, MVP-only plans, or unvalidated ideas from being mistaken for current company truth.

Use this file when creating, editing, or interpreting any Orisen strategy, product, marketing, fundraising, software, hardware, or business document.

## Core rule

When documents conflict, do not average them together.

Instead, identify which document is most authoritative for the specific question, then flag the conflict clearly before making recommendations.

## Authority hierarchy

When there is a conflict, use this hierarchy by default:

1. `ai-context/current-state.md`

   - Highest-level current truth for company, product, customer, positioning, validation, and priorities.
   - Use this as the primary reference for what Orisen is currently building and how it should be described.

2. Other files inside `ai-context/`

   - Use these as high-level operating rules and strategic context.
   - These files should define how the company thinks, makes decisions, and interprets other docs.

3. Product strategy docs

   - Use these for product direction, customer promise, roadmap boundaries, and prioritization.
   - These must stay consistent with `ai-context/current-state.md`.

4. Validation and evidence docs

   - Use these for what has actually been tested, proven, observed, or supported by data.
   - These should override unsupported marketing or fundraising claims.

5. MVP and software scope docs

   - Use these for implementation scope, engineering sequencing, and current build priorities.
   - These do not define the full company vision or final customer-ready product by themselves.

6. Marketing, fundraising, and pitch docs

   - Use these for communication, narrative, and external framing.
   - These must not claim more than the current-state and validation docs support.

7. Old notes, brainstorms, chat exports, and rough drafts

   - Treat these as inputs, not decisions.
   - Do not treat them as current truth unless they have been promoted into a source-of-truth file.

## How to treat different types of docs

### Current truth

Current truth means a decision that should guide company, product, and messaging work today.

Current truth should be written in clear source-of-truth files, especially inside `ai-context/`.

A claim should only be treated as current truth if it is clearly stated in an authoritative doc and does not conflict with a newer or higher-level source.

### Assumptions

Assumptions are beliefs that guide current work but are not fully proven.

They should be labeled as assumptions, not facts.

Examples:

- Which early customer segment will pay first
- How much users will value grogginess reduction
- What level of sleep-stage accuracy is good enough
- Which intervention approach will work best
- What price point the first customers will accept

Assumptions can guide decisions, but they should not be presented as validated evidence.

### Validated claims

Validated claims are supported by real testing, customer behavior, user feedback, or other evidence.

Validated claims should be separated from planned claims.

For Orisen, the strongest validated wedge is presence-based guaranteed wake completion.

Claims about sleep-phase-aware intervention, artificial sleep phase transitioning, sleep-stage accuracy, and grogginess reduction should remain careful until supported by testing.

### Planned features

Planned features are features the company intends to build but has not fully validated yet.

They should be described as roadmap, planned direction, or active exploration.

They should not be described as already working, proven, or customer-validated unless evidence exists.

### Long-term vision

Long-term vision describes where Orisen is going.

It can be ambitious, but it should not be confused with the current MVP or first customer-ready product.

Long-term vision may include advanced sleep-state sensing, personalized intervention, sleep onset support, long-term adaptation, and broader sleep intervention features.

These should be framed as future direction unless already built and validated.

## MVP docs vs company truth

MVP docs are about what to build first.

They are not the same as company positioning.

The engineering MVP is focused on proving the connected product loop and guaranteed wake completion.

The first customer-ready product should go beyond the engineering MVP and include a basic version of gradual, sensor-informed, or sleep-phase-aware wake intervention if technically feasible.

The long-term company vision is broader than the MVP.

Do not reduce Orisen to only the MVP scope.

## How marketing and fundraising docs should work

Marketing and fundraising docs should translate current truth into a compelling external story.

They should not invent capabilities that product and validation docs do not support.

Marketing and fundraising can emphasize ambition, but must clearly separate:

- What works today
- What has been validated
- What is being built next
- What is the long-term vision
- What still needs proof

Strong but careful messaging is preferred over exaggerated claims.

Avoid claims like:

- "Eliminates grogginess"
- "Perfectly wakes you in light sleep"
- "Controls sleep stages"
- "Clinically proven"
- "Guarantees better sleep"
- "Accurately detects sleep stages"

Use safer phrasing unless validation supports stronger claims:

- "Designed to make waking up more reliable"
- "Built for people who struggle to get out of bed"
- "Uses presence detection to help ensure wake completion"
- "Aims to reduce grogginess through gradual, sensor-informed intervention"
- "Working toward sleep-phase-aware wake-up behavior"

## How product docs should work

Product docs should define the customer problem, product promise, user experience, feature priorities, and roadmap logic.

They should stay consistent with:

- `ai-context/current-state.md`
- validation evidence
- engineering feasibility
- current company priorities

Product docs should clearly separate:

- Required first-product features
- MVP-only implementation scope
- Later roadmap features
- Long-term vision
- Open questions

## How software and engineering docs should work

Software and engineering docs should define implementation details, build sequence, architecture, constraints, and technical decisions.

They should not redefine the company promise by accident.

When software docs describe MVP scope, they should be understood as engineering scope, not final company positioning.

If engineering constraints force a product or strategy change, that conflict should be raised and reflected in the relevant source-of-truth docs.

## How business docs should work

Business docs should connect the product direction to customer segments, pricing, market strategy, fundraising, GTM, partnerships, and operations.

They should not override product truth or validation evidence.

Business strategy should be grounded in:

- The current customer focus
- The validated wedge
- The first customer-ready product direction
- Evidence from users and market testing
- Realistic technical timelines

## How to handle conflicts between docs

When two docs conflict:

1. Identify the exact conflict.
2. Identify which document is more authoritative for that topic.
3. Check whether one doc is older, narrower, MVP-only, speculative, or brainstorm-based.
4. Treat unsupported or lower-authority claims as stale, uncertain, or provisional.
5. Do not silently merge conflicting claims.
6. Recommend which file should be updated so the source of truth becomes clearer.

Use this format when helpful:

```markdown
Conflict found:
- Doc A says:
- Doc B says:

Interpretation:
- Current source of truth appears to be:
- The conflicting statement should be treated as:

Recommended update:
- Update:
- Change:
