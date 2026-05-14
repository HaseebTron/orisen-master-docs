# Software Context Map

## Purpose

This file is the routing map for Orisen software work.

Use it to decide which software docs to read for firmware, app, backend, cloud, device setup, alarm sync, OTA, BLE onboarding, and slice-based implementation questions.

This file does not replace software source-of-truth docs. It points ChatGPT projects and human readers to the right software context.

## Implementation source repo

Detailed software implementation source of truth lives primarily in:

- `HaseebTron/Orisen`

Use this master-docs repo for company/product/claims/roadmap boundaries.

Use `HaseebTron/Orisen` for implementation details, code, active slice status, firmware/app/backend files, build errors, and software decisions.

## Default software repo entry docs

For most Orisen Software implementation work, read these files from `HaseebTron/Orisen` when available:

- `docs/slices.md`
- `docs/decisions.md`
- `docs/ai-coding-rules.md`
- active slice spec doc
- relevant architecture/spec docs

For code or debugging work, also read the specific code files, logs, or config files involved in the task.

Do not read every software file by default. Use the lightest context that can answer safely.

## Always read first for important software work

For software work that may affect product behavior, reliability, claims, or roadmap, start with these master-docs files:

- `ai-context/current-state.md`
- `ai-context/source-of-truth-rules.md`
- `product/product-overview.md`
- `product/claims-and-evidence.md`
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

## Mid-chat context expansion

If a software chat later asks a more specific software question than the initial baseline docs covered, expand context inside the same chat instead of rerunning the full boot workflow.

Before answering, read this context map and the most relevant task-specific docs below.

State which extra files were read when the context expansion is meaningful.

If a software question changes product truth, public claims, roadmap priority, first customer-ready product scope, pricing, or fundraising story, escalate to Orisen General.

## Software workstreams and routing

### Slice planning and implementation

Use for:

- Starting a new software slice
- Deciding what belongs in the active slice
- Reviewing slice completion
- Planning next slice work
- Creating Codex prompts for slice implementation

Read from `HaseebTron/Orisen` when available:

- `docs/slices.md`
- `docs/decisions.md`
- `docs/ai-coding-rules.md`
- active slice spec doc
- relevant architecture/spec docs

Also read from this repo if product scope or roadmap matters:

- `product/roadmap.md`
- `product/product-overview.md`

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
- Serial logs and firmware debugging

Read from `HaseebTron/Orisen` when available:

- `orisen-firmware/src/main.cpp`
- `orisen-firmware/platformio.ini`
- `docs/slices.md`
- active slice spec doc
- `docs/decisions.md`
- `docs/ai-coding-rules.md`

### App

Use for:

- iPhone app
- Expo app
- User account creation
- Alarm setting UI
- Device setup flow
- Pairing/onboarding
- TestFlight MVP
- App-side Supabase logic

Read from `HaseebTron/Orisen` when available:

- `orisen-app/App.tsx`
- app Supabase client/config files
- app `.env.example`
- active slice spec doc
- `docs/slices.md`
- `docs/decisions.md`

### Backend and cloud

Use for:

- Supabase
- Alarm settings storage
- Device sync
- User-device relationship
- Edge Functions
- Device status table
- Basic logs
- Future device messaging

Read from `HaseebTron/Orisen` when available:

- Supabase schema docs or migrations if they exist
- Edge Function code if it exists
- active slice spec doc
- `docs/decisions.md`
- `docs/slices.md`

### BLE onboarding

Use for:

- Wi-Fi provisioning
- Device claiming
- Setup payloads
- BLE service and characteristic design
- Setup retry behavior
- Reset and re-onboarding behavior

Read from `HaseebTron/Orisen` when available:

- `docs/slice-6-ble-setup-and-onboarding-spec.md`
- active BLE-related firmware/app files
- `docs/slices.md`
- `docs/decisions.md`
- `docs/ai-coding-rules.md`

### OTA

Use for:

- Firmware update metadata
- GitHub Releases OTA path
- Version comparison
- Update eligibility
- Rollback behavior
- Production hardening later

Read from `HaseebTron/Orisen` when available:

- `docs/slice-4-ota-updates-spec.md`
- `docs/post-mvp-production-hardening.md`
- OTA-related firmware code
- `docs/decisions.md`

### Debugging and log review

Use for:

- Serial logs
- Build errors
- Runtime behavior
- Git status interpretation
- Testing steps
- Deciding whether to commit/push

Read only the docs/files needed for the bug or check.

Do not rerun broad product context unless the bug affects product behavior, reliability promise, or architecture.

## Slice-based workflow

Software implementation should generally continue slice by slice.

A new software slice should usually get a new ChatGPT chat in Orisen Software.

Keep each slice focused on one vertical product capability.

When a slice is completed:

- Update the relevant Orisen Software docs
- Commit and push the software repo
- Update this master-docs repo only if source-of-truth, product, roadmap, or cross-project context changed

## Escalation to Orisen General

Escalate to Orisen General when a software decision affects:

- Product scope
- Customer promise
- Public claims
- Roadmap priority
- First customer-ready product definition
- Reliability promise
- Pricing or launch readiness
- Fundraising narrative

## Current stable software docs in this repo

Currently stable software docs in this repo:

- `software/software-context-map.md`

The detailed implementation source of truth currently lives primarily in `HaseebTron/Orisen`.

## Notes

- This context map intentionally references `HaseebTron/Orisen` because implementation details should remain close to the code.
- Fill this file with more exact links if key software docs are copied or summarized into this master-docs repo later.
