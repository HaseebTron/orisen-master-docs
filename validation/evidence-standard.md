# Evidence Standard

## Purpose

This file defines how Orisen should classify evidence, validation, assumptions, and claims.

It exists to prevent product, marketing, fundraising, radar, software, or hardware docs from overstating what is actually proven.

Use this file when deciding whether Orisen can make a claim, promote an assumption, or describe a feature as validated.

## Core rule

Do not treat interest, belief, strategy, technical possibility, or founder conviction as validation.

Evidence must be tied to a specific claim.

A claim is only validated for the context that the evidence actually supports.

## Evidence categories

### Validated

A claim is validated when it is supported by real evidence from users, prototypes, tests, experiments, sales, usage, or reliable external sources.

Validated does not mean universally proven.

It means the evidence is strong enough for the specific claim being made.

Examples:

- Users tested a prototype and changed behavior in the intended way.
- Users paid, preordered, or committed under realistic conditions.
- A technical feature worked repeatedly in conditions similar to intended use.
- A claim is supported by credible scientific literature and the product implementation reasonably matches the studied conditions.

### Early signal

Early signal means evidence suggests a direction is promising but is not yet strong enough for broad claims.

Examples:

- waitlist signups from a landing page
- positive customer interviews
- prototype feedback from a small number of users
- strong engagement with a post
- people understanding the pain quickly
- expert interest without direct product validation

Early signal can guide strategy, but should not be presented as proof.

### Built but not validated

Built but not validated means the feature exists technically, but there is not enough evidence that it solves the user problem in real conditions.

Examples:

- firmware feature implemented and tested by the team
- app flow working locally
- device sync working in development
- basic sensor behavior working in controlled tests

Built is not the same as customer-validated.

### Planned

Planned means Orisen intends to build the feature or capability, but it is not yet implemented or validated.

Planned features should be described as roadmap, direction, or upcoming work.

### Hypothesis

A hypothesis is a belief being tested.

Examples:

- users will pay for guaranteed wake completion
- sensor-informed wake intervention will reduce perceived grogginess
- radar-derived HRV/RRV will be good enough for useful sleep-stage estimation
- a narrow oversleeping audience will convert better than generic sleep-optimization users

Hypotheses should be tested, not written as facts.

### Unsupported or unsafe claim

A claim is unsupported or unsafe when it implies more certainty, evidence, or capability than Orisen currently has.

Examples:

- clinically proven
- eliminates grogginess
- guarantees better sleep
- accurately detects sleep stages
- wakes users in the perfect sleep stage
- controls sleep stages
- manipulates biology in real time

Avoid these unless evidence later supports them and source-of-truth docs are updated.

## Claim classification rule

For every important product, marketing, fundraising, or technical claim, classify it as one of:

- validated
- early signal
- built but not validated
- planned
- hypothesis
- long-term vision
- unsupported or unsafe

If the classification is unclear, default to the more conservative category.

## Evidence strength levels

### Level 0: No evidence

The idea is based on intuition, strategy, or possibility only.

Use as a hypothesis, not a claim.

### Level 1: Anecdotal signal

There is informal feedback, founder experience, or a small number of conversations.

Useful for exploration.

Not enough for strong public claims.

### Level 2: Qualitative pattern

Multiple target users independently describe the same pain, desire, or behavior.

Useful for positioning and product direction.

Still not proof of willingness to pay or product efficacy.

### Level 3: Prototype signal

Users interact with a prototype or realistic demo and show meaningful interest, behavior change, or feedback.

Can support careful claims about user understanding and problem relevance.

### Level 4: Real-world usage signal

Users use the product or prototype in realistic conditions and receive the intended benefit.

Can support stronger product claims, depending on sample size and consistency.

### Level 5: Commercial validation

Users pay, preorder, renew, or repeatedly use the product under realistic conditions.

Can support claims around demand, willingness to pay, and product value.

### Level 6: Rigorous technical or clinical validation

A claim is supported by controlled testing, statistically meaningful data, credible studies, or clinical-grade evaluation where relevant.

Required before making strong claims about sleep-stage accuracy, clinical outcomes, or physiological effects.

## Orisen-specific evidence guidance

### Presence-based guaranteed wake completion

This is currently the strongest validated wedge.

Evidence can support careful claims that:

- the feature is meaningfully different from normal alarms
- users with wake-up problems understand its value
- leaving bed is central to solving the behavior problem
- re-triggering if the user returns to bed addresses a real failure mode

Do not overextend this evidence into claims about reducing grogginess or improving sleep quality.

### Grogginess and sleep inertia reduction

This is strategically important but should be claimed carefully until tested.

Allowed careful phrasing:

- aims to reduce grogginess
- designed to make waking feel less brutal
- building toward sensor-informed wake intervention
- testing gradual audio/light intervention to improve mornings

Avoid:

- eliminates grogginess
- fixes sleep inertia
- clinically improves sleep inertia
- guarantees easier mornings

### Sleep-stage estimation

Do not claim accurate sleep-stage detection unless Orisen has evidence from relevant real-world testing.

Radar papers, public datasets, and technical feasibility can support exploration, but they do not automatically validate Orisen's implementation.

Separate:

- literature support
- lab performance
- prototype performance
- real-bedroom performance
- customer-facing product reliability

### Artificial sleep phase transitioning

Treat artificial sleep phase transitioning as planned or experimental unless directly validated.

Use careful language:

- working toward
- exploring
- testing
- early version of sensor-informed intervention
- designed to guide the user toward a lighter wake-up state

Avoid implying proven control of sleep stages.

### Waitlist and landing page signal

Waitlist signups are evidence of interest, not proof of paid demand.

They may support:

- problem resonance
- messaging interest
- early demand signal
- channel signal

They do not prove:

- willingness to pay
- retention
- clinical efficacy
- broad-market demand
- product-market fit

## Marketing claim standard

Marketing can be emotionally sharp, but claims must remain supportable.

Good marketing should translate truth, not inflate it.

Before using a claim publicly, ask:

- Is this built?
- Is it validated?
- Is it an assumption?
- Could a user reasonably interpret this as stronger than what we know?
- Would this still feel honest if an expert challenged it?

## Fundraising claim standard

Fundraising can communicate ambition, but must clearly separate:

- current traction
- current build status
- validated wedge
- roadmap
- long-term vision
- open technical risk

Investors can hear ambitious vision, but they should not be misled about what is already proven.

## Technical evidence standard

Technical docs should distinguish:

- manufacturer capabilities
- open-source project capabilities
- paper results
- lab experiment results
- Orisen prototype results
- real-bedroom results
- production readiness

Do not treat another team's paper, dataset, or demo as evidence that Orisen's exact product works.

Use external research to guide the path, not to overclaim current capability.

## Evidence logging rule

When adding evidence to `validation/evidence-log.md`, include:

- date
- evidence type
- source
- what happened
- what claim it supports
- what claim it does not support
- confidence level
- limitations
- related docs that may need updating

## Default stance

Be ambitious in vision.

Be conservative in evidence.

A claim should become stronger only when the evidence becomes stronger.
