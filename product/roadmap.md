# Product Roadmap

## Purpose

This file separates Orisen's engineering MVP, first customer-ready product, pilot product, launch scope, later roadmap, and long-term platform direction.

Its job is to prevent MVP scope, software implementation status, and long-term vision from being mixed together.

This file should stay consistent with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- [`product/ai-powered-sleep-intervention-direction.md`](ai-powered-sleep-intervention-direction.md)
- `ai-context/claim-control/claim-control-log.md`

## Roadmap principle

Reliability comes before intelligence.

Orisen must first make waking up reliable. AI, cloud intelligence, sleep-stage estimation, vital-sign sensing, conversational interaction, autonomous intervention, and personalization are valuable only if the core wake-up system works.

Wake completion remains the first software-defined intervention and the strongest current wedge.

## Engineering MVP

The engineering MVP should prove the basic connected product loop:

- User account creation
- Device setup and pairing
- App-based alarm setting
- Cloud storage of alarm settings
- Syncing alarm settings to the device
- Local alarm storage on the device
- Local alarm execution at the correct time
- Presence-based wake completion
- Re-trigger behavior if the user returns to bed
- Basic gradual audio and light wake-up
- Basic logging
- Basic OTA update path, if feasible

The engineering MVP does not need to prove the full long-term product vision.

The engineering MVP does not need:

- AI agents
- Conversational AI
- Validated vital-sign sensing
- Validated sleep-stage sensing
- Autonomous intervention
- Full software-agent integrations
- Validated grogginess or sleep-inertia reduction

## First Customer-Ready Product

The first customer-ready product should go beyond the engineering MVP enough to deliver a credible customer promise.

It should include:

- Reliable local alarm execution
- Presence-based wake completion
- Re-trigger behavior if the user returns to bed
- Anti-bypass behavior during alarm-critical windows
- Simple usable app experience
- Planned schedule-change controls before the wake window
- Higher-friction deliberate override behavior during alarm-critical windows
- Gradual audio wake-up behavior
- Gradual light wake-up behavior
- Basic sleep/session logging where useful
- Basic device reliability and OTA support
- Basic sensor-informed wake intervention if feasible
- Sleep-phase-aware wake intervention if technically feasible
- Careful user-facing claims around less brutal mornings

It does not need:

- A perfect sleep-stage model
- Validated vital-sign sensing
- Validated sleep-stage sensing
- Validated AI-agent capability
- Validated conversational sleep coaching
- Autonomous sleep optimization
- Proven artificial sleep phase transitioning

Future features should not be claimed as current outcomes. Grogginess reduction, sleep-inertia reduction, sleep-stage accuracy, vital-sign accuracy, autonomous intervention, AI-agent capability, and artificial sleep phase transitioning all need evidence before stronger claims are allowed.

## Pilot Product

The pilot product should be designed to collect evidence, not to look like a fully scaled consumer product.

The first pilot should test:

- Whether users trust Orisen as their main alarm
- Whether wake completion reduces oversleeping or returning to bed
- Whether gradual audio/light makes mornings feel less brutal
- Whether users understand the product value quickly
- Whether users would pay for the product
- What reliability issues appear in real bedrooms
- What claims are supported by actual usage

Later pilots may test:

- Whether non-wearable sleep-context signals improve intervention quality
- Whether users trust a bedroom device that senses sleep context without requiring a wearable
- Whether users want conversational or voice-guided sleep/wake support
- Whether voice interaction helps wake completion, bedtime routines, or user trust
- Whether AI-assisted recommendations or interventions improve real behavior versus static routines
- Whether any autonomous intervention should be allowed inside explicit user-approved boundaries

## V1 Launch Product

The v1 launch product should be defined after pilot evidence improves.

Do not finalize v1 launch scope until the following are better understood:

- First customer segment
- Required reliability standard
- Pricing and willingness to pay
- Hardware readiness
- Radar/sensing readiness
- App reliability
- Claims supported by evidence
- User trust around non-contact sensing and bedroom privacy
- User appetite for voice or conversational intervention
- Technical readiness of any AI-assisted or autonomous intervention layer

## Later Roadmap

Later roadmap items may include:

- More robust sensor-informed wake intervention
- More accurate sleep-state estimation
- Non-wearable sleep-context sensing
- Non-contact vital-sign-related sensing where technically feasible and validated
- Sleep-stage-related sensing where technically feasible and validated
- Personalized wake intervention
- Artificial sleep phase transitioning if validated
- Long-term user adaptation
- Advanced sleep history and insights when they improve intervention
- Sleep onset support
- White noise and bedtime routines
- Sleep-supportive lighting
- Voice-guided bedtime support
- Voice-guided wake-up support
- Conversational sleep intervention where useful and user-trusted
- Wearable integrations as optional context sources, while preserving a non-wearable core experience
- Health-platform integrations
- Software-defined intervention layers built on the same hardware foundation
- AI sleep-agent or software-agent integrations
- Android app
- Multi-device households
- Subscription features where value is clear
- Production-grade fleet management

## Long-Term Platform Direction

Orisen's long-term product direction may be understood as a non-wearable bedroom hardware foundation for software-defined sleep interventions, including possible future AI-assisted layers.

This means one hardware foundation may eventually support multiple software-defined sleep interventions over time.

Potential sensing inputs include:

- Presence
- Movement
- Sleep/wake context
- Vital-sign-related signals where technically feasible and validated
- Sleep-stage-related signals where technically feasible and validated
- App, schedule, history, wearable, health-platform, and connected-context inputs where user-permitted

Potential intervention outputs include:

- Audio
- Light
- Voice interaction
- Timing changes
- Wake-completion behavior
- Bedtime and wake routines

Potential software-defined intervention layers include:

- Wake completion
- Easier wake-up support
- Sleep onset support
- Schedule correction
- Personalized routines
- AI-assisted or autonomous sleep interventions inside explicit user-approved boundaries

This is a long-term architecture direction, not proof that all of these layers are currently built, validated, safe, useful, or claimable publicly.

## Not Now

Unless future evidence or strategy changes, do not prioritize these for the engineering MVP:

- Full Android app
- Public App Store or Google Play launch
- Subscription billing
- Advanced sleep dashboard
- Multi-device households
- Advanced family/account sharing
- Continuous raw radar cloud streaming
- Fully polished ML model
- Validated vital-sign sensing
- Validated sleep-stage sensing
- Full conversational AI system
- Autonomous sleep agent behavior
- Complex notification system
- Complex admin dashboard
- Production-scale analytics
- Smart home integrations
- Apple Health or Google Fit integration

## Open Questions

- What is the minimum acceptable first customer-ready product?
- What level of sensor-informed wake intervention is enough for first customers?
- What must be true before paid preorders?
- What must be true before a broader v1 launch?
- Which roadmap items are actually valuable to users versus just interesting technically?
- Which voice interactions feel helpful rather than annoying or intrusive?
- What sensing claims can be supported without overclaiming vital-sign or sleep-stage accuracy?
- What should count as an AI sleep-agent integration versus ordinary app/cloud software?
- Which autonomous behaviors should be allowed only after explicit user permission and real-world testing?

## Notes

- Update this file as evidence, technical progress, and customer feedback improve.
- Voice interaction, AI sleep agents, vital-sign sensing, sleep-stage sensing, and autonomous intervention should remain claim-controlled future directions until validated.
- Use `product/claims-and-evidence.md` before turning roadmap language into marketing, fundraising, app, or customer-facing claims.
