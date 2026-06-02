# Product Roadmap

## Purpose

This file separates Orisen's engineering MVP, first customer-ready product, pilot product, v1 launch, and long-term roadmap.

Its job is to prevent MVP scope, software implementation status, and long-term vision from being mixed together.

This file should stay consistent with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `ai-context/claim-control/claim-control-log.md`

## Roadmap principle

Reliability comes before intelligence.

Orisen must first make waking up reliable. AI, cloud intelligence, sleep-stage estimation, vital-sign sensing, conversational interaction, autonomous intervention, and personalization are valuable only if the core wake-up system works.

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

The engineering MVP does not need to include conversational AI, validated vital-sign sensing, sleep-stage sensing, autonomous AI agents, or full software-agent integrations.

## First customer-ready product

The first customer-ready product should go beyond the engineering MVP enough to deliver a credible customer promise.

It should include:

- Reliable local alarm execution
- Presence-based wake completion
- Re-trigger behavior if the user returns to bed
- Simple usable app experience
- Gradual audio wake-up behavior
- Gradual light wake-up behavior
- Basic sleep/session logging where useful
- Basic device reliability and OTA support
- Basic sensor-informed wake intervention if feasible
- Sleep-phase-aware wake intervention if technically feasible
- Careful user-facing claims around reduced grogginess and sleep inertia

It does not need a perfect sleep-stage model.

It should not overclaim grogginess reduction, sleep-stage accuracy, vital-sign accuracy, autonomous intervention, AI-agent capability, or artificial sleep phase transitioning until supported by evidence.

## Pilot product

The pilot product should be designed to collect evidence, not to look like a fully scaled consumer product.

The pilot should test:

- Whether users trust Orisen as their main alarm
- Whether wake completion reduces oversleeping or returning to bed
- Whether gradual audio/light makes mornings feel less brutal
- Whether users understand the product value quickly
- Whether users would pay for the product
- What reliability issues appear in real bedrooms
- What claims are supported by actual usage

Potential later pilots may also test:

- Whether users want conversational or voice-guided sleep/wake support
- Whether voice interaction helps wake completion, bedtime routines, or user trust
- Whether non-wearable sleep-context signals improve intervention quality
- Whether users trust a bedroom device that senses sleep context without requiring a wearable
- Whether AI-assisted recommendations or interventions improve real behavior versus static routines

## V1 launch product

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
- User appetite for voice/conversational intervention
- Actual technical readiness of any AI-assisted or autonomous intervention layer

## Later roadmap

Later roadmap items may include:

- More accurate sleep-stage model
- Non-wearable sleep-context sensing
- Non-contact vital-sign sensing where technically feasible
- Sleep-stage sensing where technically feasible and validated
- Personalized wake intervention
- Artificial sleep phase transitioning
- Long-term user adaptation
- Advanced sleep history and insights
- Subscription features
- Sleep onset support
- White noise and bedtime routines
- Voice-guided bedtime support
- Voice-guided wake-up support
- Conversational sleep intervention where useful and user-trusted
- Android app
- Multi-device households
- Health platform integrations
- Wearable integrations as optional context sources, while preserving a non-wearable core experience
- AI sleep-agent or software-agent integrations
- Software-defined intervention layers built on the same hardware foundation
- Production-grade fleet management

## Long-term platform direction

Orisen's long-term product direction may be understood as a non-wearable bedroom hardware layer for AI-powered sleep intervention.

This means the device may eventually provide:

- Sensing inputs:
  - presence
  - movement
  - sleep/wake context
  - vital-sign-related signals where technically feasible
  - sleep-stage-related signals where technically feasible and validated
  - app, schedule, history, and connected-context inputs where user-permitted
- Intervention outputs:
  - audio
  - light
  - voice interaction
  - timing changes
  - wake-completion behavior
  - bedtime and wake routines
- Software-defined intervention layers:
  - wake completion
  - easier wake-up support
  - sleep onset support
  - schedule correction
  - personalized routines
  - future AI-assisted or autonomous sleep interventions

This is a long-term architecture direction, not proof that all of these layers are currently built, validated, or safe to claim publicly.

## Not now

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

## Open questions

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

- This file is a starter roadmap.
- Update it as evidence, technical progress, and customer feedback improve.
- Voice interaction, AI sleep agents, vital-sign sensing, sleep-stage sensing, and autonomous intervention should remain claim-controlled future directions until validated.