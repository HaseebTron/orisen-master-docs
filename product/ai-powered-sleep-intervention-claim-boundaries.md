# AI-Powered Sleep Intervention Claim Boundaries

## Purpose

This file adds claim boundaries for newer Orisen future directions:

- AI sleep agents
- voice intervention
- vital-sign sensing
- sleep-stage sensing
- autonomous intervention

Use this file with `product/claims-and-evidence.md`. It does not override the existing claims file. It extends it with specific guardrails for the new AI-powered sleep intervention direction.

## Core rule

Do not make the AI-agent story move faster than the product evidence.

Orisen can discuss a larger future direction, but it must separate:

- what is currently validated
- what has been physically prototyped
- what is being built now
- what is planned
- what is a hypothesis
- what is long-term vision
- what is unsupported or unsafe

Wake completion remains the strongest current wedge.

## Current strongest evidence

Current strongest evidence still supports:

- presence-based wake completion
- local alarm behavior
- re-trigger behavior if the user returns to bed
- non-contact sensing as a core product direction
- early user pain around waking up and getting out of bed

The newer AI-powered sleep intervention direction is primarily roadmap, architecture, and long-term vision unless specific capabilities are separately built and tested.

## AI sleep agents

### Status

Long-term vision / future architecture direction.

### Safe wording

- "Orisen is being built as a hardware layer for AI-powered sleep intervention."
- "Future versions may let sleep software or AI agents use Orisen to sense context and act in the bedroom."
- "Orisen could become the physical interface for AI sleep agents, starting with wake-up reliability."
- "The AI-agent direction is future-facing; wake completion is the first concrete intervention layer."

### Internal wording

- "AI sleep agent" means software that can use context, decide what intervention to run, act through Orisen's outputs, and adapt based on feedback.
- Orisen may provide the hardware layer: sensing inputs, local execution, voice/audio/light outputs, wake behavior, and feedback signals.

### Avoid wording

- "Orisen has autonomous AI sleep agents."
- "Orisen's AI agent fixes your sleep."
- "Our AI knows exactly what your sleep needs."
- "Orisen is a proven sleep agent platform."
- "AI agents optimize your sleep automatically."

### What evidence does not prove yet

Current evidence does not prove:

- AI-agent capability
- autonomous decision quality
- better sleep outcomes from AI intervention
- safety or user trust for AI-controlled bedroom behavior
- retention, willingness to pay, or product-market fit for AI-agent features

### Validation needed to upgrade

- A working software-agent prototype connected to device/app context
- Clear user-permission and override rules
- Logs showing what the agent decided and what happened next
- User testing around trust, annoyance, safety, and perceived value
- Evidence that agent-driven interventions outperform static routines or manual settings

## Voice intervention

### Status

Planned / future intervention channel.

### Safe wording

- "Future versions may use intelligent voice interaction as one intervention channel."
- "Voice may support wake-up dialogue, bedtime guidance, and contextual prompts."
- "Voice is one possible output alongside audio, light, timing, and wake behavior."

### Internal wording

- Voice should make the system feel more agentic only where it improves the sleep/wake outcome.
- Voice should not be the whole product identity.
- Voice must be tested for usefulness, trust, privacy perception, and annoyance.

### Avoid wording

- "Orisen has a proven AI sleep coach."
- "Orisen talks you into perfect sleep."
- "Orisen's voice assistant fixes your sleep."
- "Orisen knows exactly what to say to wake you up."
- "Orisen replaces a sleep coach or clinician."

### What evidence does not prove yet

Current evidence does not prove:

- voice improves wake completion
- voice improves bedtime behavior
- users want a talking device in the bedroom
- voice is acceptable during sleep/wake states
- conversational interaction improves sleep outcomes

### Validation needed to upgrade

- Prototype voice flows
- User testing on wake-up and bedtime voice scripts
- Opt-in/opt-out testing
- Measures of annoyance, trust, comprehension, and behavior change
- Comparisons against non-voice audio/light flows

## Vital-sign sensing

### Status

Future technical direction / not validated for public accuracy claims.

### Safe wording

- "Orisen is exploring non-contact sensing for future vital-sign-related signals."
- "Vital-sign-related sensing is a future technical direction that requires validation."
- "The core wake-up benefit should not depend on validated vital-sign tracking."

### Internal wording

- Vital-sign sensing may become useful for sleep context, personalization, and future intervention layers.
- Vital-sign sensing claims must distinguish raw technical capability from validated consumer or clinical accuracy.

### Avoid wording

- "Orisen accurately tracks your vital signs."
- "Orisen provides medical-grade heart-rate or breathing data."
- "Orisen is better than wearables for vital signs."
- "Orisen replaces clinical monitoring."
- "Orisen can diagnose or monitor sleep disorders."

### What evidence does not prove yet

Current evidence does not prove:

- accurate vital-sign detection
- reliable performance across bedrooms, users, positions, bedding, pets, or motion
- clinical-grade accuracy
- better accuracy than wearables
- improved outcomes from vital-sign-based intervention

### Validation needed to upgrade

- Bench testing against reference sensors
- Real-bedroom validation across users and nights
- Error bounds and confidence reporting
- Testing under varied placement, bedding, motion, and distance conditions
- Clear separation between consumer context signals and medical-grade measurements

## Sleep-stage sensing

### Status

Future technical direction / not validated.

### Safe wording

- "Orisen is researching non-contact sensing for future sleep-state estimation."
- "Future versions may become sleep-phase-aware if the sensing pipeline is validated."
- "Sleep-stage sensing is a roadmap item, not a current proven capability."

### Internal wording

- Sleep-stage sensing may support personalized wake intervention, but it must not be assumed.
- Sleep-phase-aware intervention should be validated separately from sleep-stage classification accuracy.

### Avoid wording

- "Orisen accurately detects sleep stages."
- "Orisen wakes you in the perfect sleep stage."
- "Orisen always wakes you from light sleep."
- "Orisen controls sleep stages."
- "Orisen replaces PSG."
- "Orisen provides clinical-grade sleep staging."

### What evidence does not prove yet

Current evidence does not prove:

- accurate sleep-stage classification
- reliable sleep-stage inference from radar in real bedrooms
- correct wake timing based on sleep stage
- improved wake outcomes from sleep-phase-aware intervention
- clinical sleep staging capability

### Validation needed to upgrade

- Labeled sleep-stage dataset
- Validation against PSG or appropriate reference methods
- Real-bedroom testing across users and nights
- Accuracy/error metrics with limitations
- Outcome testing showing sleep-stage-aware intervention improves user experience versus fixed timing

## Autonomous intervention

### Status

Future direction / hypothesis.

### Safe wording

- "Future versions may autonomously adjust interventions within user-approved boundaries."
- "Orisen is exploring adaptive intervention logic that can change audio, light, timing, or wake behavior based on context."
- "Autonomous behavior must remain permissioned, transparent, and overrideable."

### Internal wording

- Autonomy should mean controlled adaptation inside safe user-defined boundaries.
- Autonomous intervention must be subordinate to local reliability, user trust, and deliberate control.

### Avoid wording

- "Orisen autonomously optimizes your sleep."
- "Orisen fixes sleep automatically."
- "Orisen controls your sleep environment for you."
- "Set it and forget it, Orisen handles your sleep."
- "Orisen knows better than the user."

### What evidence does not prove yet

Current evidence does not prove:

- autonomous intervention works
- autonomous decisions improve sleep/wake outcomes
- users trust autonomous sleep behavior
- autonomous behavior is safe or non-annoying
- autonomous behavior improves retention or willingness to pay

### Validation needed to upgrade

- Clearly defined autonomy boundaries
- User permission model
- Override and failure-mode testing
- Logs of autonomous decisions and outcomes
- User trust and annoyance testing
- Outcome comparison against static/manual routines

## Approved future-facing combined wording

Use carefully in fundraising or internal strategy:

> Orisen is building toward a non-wearable bedroom hardware layer for AI-powered sleep intervention. Wake completion is the first concrete intervention layer; future layers may include voice-guided routines, sensor-informed wake behavior, and software/AI agents that can sense context and act through the device.

Use shorter:

> Orisen is being built as a hardware layer for software-defined sleep interventions, starting with wake completion.

Use only when the audience understands AI agents:

> Future AI sleep agents could use Orisen as the physical interface for sensing and intervention in the bedroom.

## Unsafe combined wording

Avoid:

- "Orisen is an autonomous AI agent that fixes sleep."
- "Orisen tracks vital signs and sleep stages accurately without wearables."
- "Orisen controls your sleep stages using AI."
- "Orisen replaces wearables and sleep labs."
- "Orisen is clinically validated AI sleep intervention."
- "Orisen guarantees better sleep through autonomous intervention."

## Relationship to current public claims

These boundaries do not weaken the long-term vision.

They keep the current public story disciplined:

- current validated wedge: presence-based wake completion
- careful current identity: non-contact sleep intervention device for people who struggle to wake up
- near-term roadmap: gradual audio/light and sensor-informed wake intervention
- long-term direction: hardware layer for AI-powered sleep intervention
- not yet validated: AI agents, voice intervention outcomes, vital-sign accuracy, sleep-stage accuracy, autonomous optimization, clinical outcomes