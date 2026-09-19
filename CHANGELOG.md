# Changelog

All notable changes to Cello are documented here.

The project follows semantic versioning and uses GitHub Releases for downloadable Windows builds.

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

### Validation

- Windows PE32+ x86-64 GUI structure: PASS
- Embedded payload SHA-256/footer identity: PASS
- Payload ZIP CRC: PASS
- Internal payload manifest verification: PASS
- Python source compilation: PASS
- Microenvironment schedule normalization/application: PASS
- Exact schedule-boundary integration smoke test: PASS
- Native Windows launch and Microenvironment Engine smoke test: pending host verification

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

### Startup and runtime hardening

The single-file v1.1.0–v1.6.0 builds were rebuilt again after real Windows startup testing exposed both runtime-compatibility and startup-latency problems.

- Added an immediate native Windows Cello startup window before Python/Qt import
- Warm launches now reuse the prepared private runtime without re-extracting the embedded payload
- Removed the redundant full embedded-payload read before first-run extraction
- Deferred `MainWindow` import until after the lightweight startup cover is visible
- Deferred Pathway Explorer, Perturbation Lab, Quantitative Analysis, Population Mode, plugin, recording-export, and reproducibility modules until their features are opened
- Made Track Stats load Matplotlib only when plotting is actually opened
- Moved desktop-shortcut creation off the GUI startup path
- Added retry/fallback handling around Windows atomic file replacement for autosave, startup cache, and project archives
- Restored the CPython `struct` wrapper required by Shiboken/PySide6 when using the private Python runtime directly
- Kept versioned payload-hash runtime isolation so repaired builds do not reuse stale caches

### Scientific guardrails

- Population outputs are model-generated virtual-cell replicates, not biological replicates
- Heterogeneity is an imposed model assumption with a reproducible seed
- `simulation.py`, `regulation.py`, and `perturbations.py` are byte-for-byte unchanged by the startup/performance repairs

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

## [1.0.1] — 2026-08-06

### Added

- First formally published portable Windows x64 release
- Bundled private Python and scientific runtime
- Desktop shortcut and Cello application integration
