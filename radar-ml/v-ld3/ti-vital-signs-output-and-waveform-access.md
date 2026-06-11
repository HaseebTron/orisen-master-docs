# TI Vital Signs Output and Waveform Access

Status: Working technical synthesis
Authority level: Domain strategy / Radar-ML evidence
Last reviewed: 2026-06-10
Governing docs:
- `radar-ml/radar-ml-read-rules.md`
- `ai-context/claim-control/claim-control-system.md`
- `ai-context/source-of-truth-rules.md`

## Current Verdict

- Stock TI IWRL6432 Vital Signs output gives HR and BR numbers.
- It does not output true heartbeat or breathing waveforms.
- Stock output is not sufficient for real HRV.
- Stock output is not sufficient for proper BRV/RRV.
- Firmware appears to compute more useful phase/waveform-related data internally, but stock TLV does not export it.

## Stock Output

Stock Vital Signs TLV includes:
- `heartRate`
- `breathingRate`
- `breathingDeviation`
- `rangebin`
- short heart-rate history
- short breathing-rate history

## Important Parser Caveat

- TI parser names two arrays `heartWaveform` and `breathWaveform`.
- Firmware inspection found these arrays are filled with recent scalar HR/BR estimates.
- They are not true waveform samples.
- Treat the visualizer naming as misleading for HRV/RRV purposes.

## HRV Feasibility

Verdict:
- No real HRV from stock output.

Reason:
- HRV needs beat-to-beat timing or a cardiac waveform.
- Stock output gives heart-rate estimates, not heartbeat timestamps or waveform data.
- Heart-rate trend variability should not be called HRV.

## BRV/RRV Feasibility

Verdict:
- Not enough for proper BRV/RRV.
- May support rough breathing-rate trend variability only.

Reason:
- Proper BRV/RRV needs breath-to-breath timing or respiration waveform.
- Stock output gives breathing-rate estimates, not breath timestamps or true waveform data.

## Internal Firmware Data

- Firmware appears to compute phase-derived buffers and spectral peaks internally.
- This suggests Orisen may not need to start from raw ADC/radar cube.
- Main gap is exporting the useful internal signal.

## Recommended First Export Path

Add a custom UART TLV that exports:
- `frameNumber`
- selected `rangeBin`
- sample count
- sample period or frame period
- selected-bin phase or unwrapped phase
- respiration waveform if available
- `heartRate`
- `breathingRate`
- quality/confidence if available

## Later Export Paths

After respiration/phase export:
- heartbeat waveform
- cardiac-band filtered phase
- peak timestamps
- breath-to-breath intervals
- beat-to-beat intervals

Avoid raw ADC/SPI/radar cube as the first path unless internal waveform export is insufficient.

## What Stock Output Can Support

- HR monitoring experiments.
- BR monitoring experiments.
- Rough trend analysis.
- Initial placement/posture tests.

## What Stock Output Cannot Support

- Real HRV.
- Proper BRV/RRV.
- Beat-to-beat intervals.
- Breath-to-breath intervals.
- True heartbeat waveform logging.
- True respiration waveform logging.
- Sleep-stage-ready waveform features.

## Claim Boundary

Do not claim:
- stock TI output supports HRV
- stock TI output supports proper BRV/RRV
- waveform access is already available externally
- sleep-stage readiness from stock output

Safe internal wording:
- "Stock TI output supports HR/BR numbers."
- "HRV/RRV require additional waveform, phase, or peak-timing export work."
