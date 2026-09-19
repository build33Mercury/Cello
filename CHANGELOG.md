# Changelog

All notable changes to Cello are documented here.

The project follows semantic versioning and uses GitHub Releases for downloadable Windows builds.

## [1.8.0] — 2026-09-19

### Added

- Experiment Automation
- Up to three-factor computational condition matrices
- Model-parameter sweeps
- Microenvironment sweeps
- Deterministic seed assignment and repeated model runs
- Queue preview and per-run status
- Final, mean, minimum, maximum, and AUC response summaries
- One- and two-factor response plots
- CSV results export
- JSON run-bundle export
- 2,000-run design guard

### Interface

- Refined Cello toward a conventional desktop-scientific interface
- Neutralized feature-button color coding in the main header
- Reduced oversized radii and decorative card treatment
- Added standard group boxes, tabs, dense tables, and compact status text in Experiment Automation
- Shortened high-visibility interface descriptions
- Kept heavy plotting imports out of the normal startup path

### Scientific behavior

- Automated runs start from the active experiment state
- Active v1.7 environment schedules are honored during automated runs
- Repeated seeds are labeled computational repeats, not biological replicates
- Parameter sweeps are model exploration, not empirical dose-response measurements
- `simulation.py`, `regulation.py`, and `perturbations.py` are byte-for-byte unchanged from v1.7.0

### Validation

- Windows PE32+ x86-64 GUI structure: PASS
- Payload footer SHA-256 identity: PASS
- Payload ZIP CRC: PASS
- 4,600-entry internal checksum manifest: PASS
- Python source parsing: 62/62 PASS
- Experiment Automation core checks: 9/9 PASS
- Cello resource section preserved from v1.7: PASS
- Native Windows launch and interactive automation smoke test: pending host verification

## [1.7.0] — 2026-09-19

### Added

- Microenvironment Engine
- Extracellular temperature, pH, osmolarity, volume, and perfusion controls
- Editable represented-species concentration, reservoir, and exchange-rate controls
- Reproducible model-condition presets
- Scheduled environment events at explicit simulation times
- Medium-replacement schedule events
- Live environment summary and next-event status
- Track Stats environment-event markers
- JSON and CSV environment-schedule export
- Experiment, recovery, and recording metadata preservation for environment schedules

### Numerical behavior

- The worker splits simulation advancement at each scheduled environment-event boundary
- Environment events are therefore applied at model time rather than GUI refresh time

### Scientific guardrails

- Environment presets are model inputs, not validated culture protocols
- Core `simulation.py`, `regulation.py`, and `perturbations.py` are byte-for-byte unchanged from v1.6.0

## [1.6.0] — 2026-09-18

### Added

- Population Mode for independent model-generated virtual-cell ensembles
- Reproducible population seeds
- Configurable parameter heterogeneity
- Population sizes from 2 to 500 virtual cells
- Median and interquartile-range population trajectories
- Endpoint summary statistics and model-state fractions
- Per-cell endpoint inspection
- CSV and JSON population export

### Startup and runtime hardening

- Immediate native Windows startup feedback
- Cached private-runtime reuse
- Deferred heavy analysis imports
- Windows atomic-save retry/fallback handling
- Restored the CPython `struct` wrapper required by direct private-Python startup

## [1.5.0] — 2026-09-17

- Quantitative Analysis workspace
- Descriptive trajectory statistics and publication-oriented export

## [1.4.0] — 2026-09-17

- Perturbation Lab
- Control-state capture and multi-intervention protocols

## [1.3.0] — 2026-09-17

- Dynamic Pathway Explorer

## [1.2.0] — 2026-09-17

- Experiment Workspace

## [1.1.0] — 2026-09-17

- Live research telemetry
- Simulation recording
- Refreshed Cello interface

## [1.0.1] — 2026-08-06

- First formally published portable Windows x64 release
