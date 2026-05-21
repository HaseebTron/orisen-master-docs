# Product Questions And Objections

Status: Working product question log
Authority level: Product reasoning / unresolved objection handling
Last reviewed: 2026-05-20

## Purpose

This file captures important consumer, investor, and product-design questions that need to be answered carefully before being turned into website copy, FAQ content, pitch wording, or public claims.

This file is not a final marketing FAQ.

Use it to preserve objections, founder thinking, open tradeoffs, and possible response directions.

Downstream public wording should still be routed through:

- `product/product-overview.md`
- `product/claims-and-evidence.md`
- `marketing/positioning-and-messaging.md`
- `ai-context/claim-control/claim-control-system.md`

## Question: What if the user wants to sleep in after the alarm starts?

### Why this matters

Orisen is designed to prevent half-asleep alarm bypass.

At the same time, users still need a legitimate way to override the system when plans change, they are sick, it is a holiday, they forgot to update the schedule, or they genuinely decide to sleep in.

This question matters because the wake-completion wedge depends on making easy in-bed bypass difficult, while user trust depends on preserving a deliberate override path.

### Current product thinking

- Before the wake window, schedule changes should be easy.
- Users should be able to skip, change, or disable an upcoming alarm normally through the app before the wake window.
- During the alarm-critical window, normal in-bed controls should not fully disable wake completion.
- A full override should exist, but it should require deliberate action away from bed.
- Possible implementations include:
  - Physical recovery code
  - QR card
  - NFC card
  - Recovery token stored away from the bed
- The recovery method could be stored in a remote place, such as the original product box or another non-bedside location.

### Founder hypothesis

The product should protect the user's prior awake decision from their half-asleep morning self.

The decision to sleep in should still be possible, but it should be made consciously, not through an easy in-bed bypass.

Unexpected same-morning sleep-in decisions may be less common than the core failure mode of half-asleep alarm dismissal, but this should be treated as a hypothesis rather than a proven fact.

### Potential user objection

“If I have to get up and find a code, then I am already awake and it is harder to go back to sleep.”

### Current response direction

That objection is real. Orisen should not pretend this flow is frictionless.

The intended tradeoff is that the product prioritizes reliable wake completion for users whose main problem is impulsive, half-asleep alarm bypass.

For legitimate planned sleep-ins, the preferred path is to change or skip the alarm before the wake window.

For unexpected morning changes, the override exists, but it is intentionally higher-friction so that the choice is deliberate.

The response should avoid making the product sound hostile or punitive.

The public framing should emphasize deliberate control, not punishment.

### Open questions

- Is a paper recovery code too annoying?
- Would QR or NFC be better than a typed code?
- Where should the recovery token be stored?
- How long should a recovery code be?
- Should the app require out-of-bed detection before accepting an override?
- Should there be different override levels for sick day, emergency, travel, guest mode, or vacation mode?
- How do we avoid making the product feel hostile?
- How do we explain this publicly without sounding like the device traps the user?
- How should this behavior be tested with early users?
- What wording belongs in website FAQ versus onboarding versus support docs?

## Future questions to add

- What happens if the device is unplugged?
- What happens if the user removes the device from the wall?
- What happens if the power goes out?
- What happens if Wi-Fi is down?
- What if two people share the bed?
- What if the user is sick?
- What if the user has a roommate or partner?
- How loud does Orisen get?
- Can Orisen be too aggressive?
- What if the user does not want sleep tracking?
- What if the user does not want a wearable?
- What makes Orisen different from a phone alarm, Alarmy, Ruggie, Hatch, Sleep Cycle, or Eight Sleep?
