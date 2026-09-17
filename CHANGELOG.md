# Changelog

All notable changes to Cello are documented here.

The project follows semantic versioning and uses GitHub Releases for downloadable Windows builds.

## [1.6.0] — 2026-09-18

### Added

- Population Mode for independent model-generated virtual-cell ensembles
- Reproducible population seeds
- Configurable parameter heterogeneity
- Population sizes from 2 to 500 virtual cells
- Median and interquartile-range population trajectories
- Endpoint mean, SD, median, quartiles, minimum, and maximum
- Model-state fractions for healthy, stressed, injured, irreversibly injured, and necrotic virtual cells
- Per-cell endpoint inspection
- CSV and JSON population export
- Cancellable background population computation

### Packaging

- Replaced the multi-file portable launcher layout with one Windows x64 release asset named `Cello.exe`
- Added an embedded-payload bootstrap that verifies the payload SHA-256 before extraction
- Added versioned runtime caching under `%LOCALAPPDATA%\Cello\runtime`
- Added bootstrap/runtime diagnostics under `%LOCALAPPDATA%\Cello\logs`
- Preserved Cello icon resources in the rebuilt executable

### Scientific guardrails

- Population outputs are model-generated virtual-cell replicates, not biological replicates
- Heterogeneity is an imposed model assumption with a reproducible seed
- Core `simulation.py`, `regulation.py`, and `perturbations.py` are byte-for-byte unchanged from v1.5.0

### Validation

- Python source compilation: PASS
- Population-core simulation smoke test: PASS
- Embedded payload SHA-256 verification: PASS
- Embedded payload ZIP CRC: PASS
- Windows PE32+ x86-64 structure: PASS
- Cello icon resource directory: PASS
- Native Windows GUI smoke launch: still required before host-level release verification

## [1.5.0] — 2026-09-17

### Added

- Quantitative Analysis workspace
- Time-series, distribution, scatter, correlation-heatmap, and run-comparison views
- Descriptive statistics, start/end change, fold change, percent change, trapezoidal AUC
- Peak/trough detection and late-window stability diagnostics
- CSV/JSON summary export and PNG/PDF/SVG figure export

## [1.4.0] — 2026-09-17

### Added

- Perturbation Lab
- Target-first perturbation design
- Chemical perturbation and enzyme-activity scaling workflows
- Control-state capture and restoration
- Multi-intervention protocols
- Live effect manifests
- JSON and CSV protocol export

## [1.3.0] — 2026-09-17

### Added

- Dynamic Pathway Explorer
- Live pathway flux history
- Interactive pathway maps and reaction inspection
- Model-state, inhibition, evidence, and compartment cues
- JSON and CSV pathway snapshot export

## [1.2.0] — 2026-09-17

### Added

- Experiment Workspace
- `.cello-project` project archives with SHA-256 member verification
- Project and experiment notes
- Experiment duplication/branching
- Multiple runs per experiment
- Multi-run trajectory comparison and project-summary export

## [1.1.0] — 2026-09-17

### Added

- New blue Cello application identity
- Configurable live research telemetry
- Simulation recording with trajectory, event, provenance, figure, and checksum output
- Event markers and improved recording-state feedback
- Refreshed light and dark interface

### Rebuilt distribution

The v1.1.0–v1.5.0 Windows builds were rebuilt into the same single-file `Cello.exe` bootstrap architecture used by v1.6.0 after the earlier multi-file startup path proved unreliable. These rebuilds are structurally and payload-integrity validated; native Windows GUI smoke testing remains the final host-level check.

## [1.0.1] — 2026-08-06

### Added

- First formally published portable Windows x64 release
- Bundled private Python and scientific runtime
- Desktop shortcut and Cello application integration

## Earlier development builds

Earlier internal development builds were not formally archived as public GitHub releases. The public version history begins with v1.0.1.
