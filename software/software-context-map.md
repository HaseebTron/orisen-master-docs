# Software Context Map

## Purpose

This file is the routing map for Orisen software work.

Use it to decide which software docs to read for firmware, app, backend, cloud, device setup, alarm sync, OTA, BLE onboarding, and slice-based implementation questions.

This file does not replace software source-of-truth docs. It points ChatGPT projects and human readers to the right software context.

## Always read first for important software work

For software work that may affect product behavior, reliability, claims, or roadmap, start with:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/roadmap.md`

For implementation-only work, use the relevant Orisen Software repo docs and active slice docs.

## Software folder role

The software docs should define:

- Firmware architecture
- App architecture
- Backend and cloud architecture
- Device setup and onboarding
- Alarm sync
- Local alarm execution
- Wake completion logic
- OTA update behavior
- BLE provisioning
- Slice-by-slice implementation status
- Software constraints and decisions

Software docs define implementation reality. They should not redefine company truth, product positioning, customer promise, or public claims.

## Software workstreams

### Firmware

Use for:

- ESP32 firmware
- Local alarm execution
- Presence-based wake completion
- Re-trigger behavior
- Gradual audio/light control
- OTA eligibility and update checks
- Local storage
- Device state machine

### App

Use for:

- iPhone app
- User account creation
- Alarm setting UI
- Device setup flow
- Pairing/onboarding
- TestFlight MVP

### Backend and cloud

Use for:

- Supabase
- Alarm settings storage
- Device sync
- User-device relationship
- Edge Functions
- Basic logs
- Future device messaging

### BLE onboarding

Use for:

- Wi-Fi provisioning
- Device claiming
- Setup payloads
- BLE service and characteristic design
- Setup retry behavior

### OTA

Use for:

- Firmware update metadata
- GitHub Releases OTA path
- Version comparison
- Update eligibility
- Production hardening later

## Slice-based workflow

Software implementation should generally continue slice by slice.

A new software slice should usually get a new ChatGPT chat in Orisen Software.

Keep each slice focused on one vertical product capability.

## Escalation to Orisen General

Escalate to Orisen General when a software decision affects:

- Product scope
- Customer promise
- Public claims
- Roadmap priority
- First customer-ready product definition
- Reliability promise
- Pricing or launch readiness

## Notes

- This is a starter context map.
- Fill this file with links to the current Orisen Software repo docs after the software docs are copied or summarized into this master-docs repo.
