# V-LD3 Vital Signs Demo Compatibility

Status: Working technical synthesis
Authority level: Domain strategy / Radar-ML evidence
Last reviewed: 2026-06-10
Governing docs:
- `radar-ml/radar-ml-read-rules.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/source-of-truth-rules.md`

## Current Verdict

- RFbeam says TI's IWRL6432 Vital Signs demo is running on V-LD3.
- It should use a V-LD3-specific config, not stock TI BOOST/AOP config.
- This supports technical feasibility for testing HR/BR.
- It does not validate sleep use, HRV/RRV, or sleep-stage-aware intervention.

## Evidence

- RFbeam email response: TI Vital Signs demo is running on V-LD3.
- RFbeam provided `Vital_Signs_With_Tracking_V-LD3.cfg`.
- Local inspection found the config plausibly compatible with stock TI Vital Signs appimage.
- V-LD3 uses TI IWRL6432 and exposes flashing/eval-kit access.
- RFbeam says normal blankets are transparent to radar.
- RFbeam has not tested bed/sleep-like HR/BR performance.

## Config Findings

- V-LD3 config uses V-LD3-specific `antGeometryCfg`.
- Inspected config uses `compRangeBiasAndRxChanPhase`.
- RFbeam said newer eval-kit configs may use `loadAntennaCal`.
- Open question: exact calibration path for the purchased eval-kit version.

## RFbeam Testing So Far

- TI Vital Signs demo: running on V-LD3 per RFbeam.
- MicroDoppler demo: RFbeam says breathing is clearly visible.
- RFbeam says heartbeat-related detections can be seen if the person is not breathing.
- RFbeam has not done sleep-like testing.

## Still Unvalidated

- 0.5 to 1.5 m sleep placement.
- Side sleeping.
- Chest not facing sensor.
- Through-blanket performance in Orisen geometry.
- HR/BR accuracy in bed.
- HRV/RRV.
- Sleep staging.
- Intervention control.

## Practical Next Tests

- Flash TI Vital Signs appimage.
- Use RFbeam V-LD3 config.
- Confirm CLI accepts all commands.
- Confirm Vital Signs TLV output.
- Compare HR/BR against a reference sensor.
- Test supine, side-facing, side-away, and blanket conditions.

## Claim Boundary

Safe internal wording:
- "RFbeam says TI Vital Signs runs on V-LD3 with a V-LD3-specific config."
- "V-LD3 is worth testing for HR/BR experiments."

Do not claim:
- validated sleep HR/BR performance
- validated HRV/RRV
- sleep-stage detection
- grogginess reduction
- sleep-state control
