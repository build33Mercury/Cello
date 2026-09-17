# Changelog

All notable changes to Cello are documented here.

The project follows semantic versioning and uses GitHub Releases for downloadable compiled builds.

## [1.1.0] — 2026-09-17

### Added

#### Live Research Telemetry

- Added selectable live state-variable telemetry
- Added selectable live pathway-flux telemetry
- Added `Pause Plot` to freeze plot rendering without pausing the simulation
- Added ATP, glucose, viability, and event-count telemetry chips
- Added intervention add/update/remove event markers
- Added recording start/stop event markers
- Added bounded telemetry history and redraw throttling for responsiveness

#### Simulation Recording

- Added dedicated simulation recording independent of ordinary rolling UI history
- Added `trajectory.csv` export
- Added `events.csv` export
- Added provenance-rich `recording.json`
- Added PNG and PDF summary figures
- Added SHA-256 member manifests
- Added recording event count and observed median sample interval metadata
- Added recovery export behavior for interrupted active recordings

#### Branding and interface

- Added the new blue Cello application icon and in-app brand mark
- Refreshed light and dark themes around the Cello visual identity
- Improved application header, startup window, cards, menus, controls, status indicators, active states, hover states, and spacing
- Added clearer software/model version presentation

### Changed

- Updated the application and release metadata to 1.1.0
- Improved recording-control state feedback
- Improved Windows launcher behavior for the main application and simulation-worker command-line forwarding
- Preserved the existing biochemical equations and core cell-model behavior during the interface/telemetry update

### Validation

The current v1.1.0 portable package completed:

- Python source compilation checks
- 68 automated source-level regression/scientific tests with 0 failures
- recording and export checks
- package ZIP integrity checks
- release manifest/checksum generation
- Windows x64 PE launcher structure verification
- embedded application-icon verification
- bundled Python runtime presence verification
- simulation-worker command-line forwarding verification

Native Windows GUI smoke testing remains a host-level check to perform on Windows after downloading the final GitHub release asset.

### Distribution

- Release asset: `Cello_1.1.0_Windows_x64_Portable.zip`
- Extracted application directory: `Cello_1.1.0_Windows_x64_Portable`
- Launcher: `Run_Simulator.cello.exe`
- Platform: Windows x64
- Package type: portable ZIP
- Separate Python installation: not required
- ZIP SHA-256: `b636317b71a53dcec70cb7a127146a5f16c35ec6b4d8aad58b961afe236ba175`

### Scientific status

- Research beta
- Model-generated outputs only
- Not clinically validated
- Not a patient-specific predictor
- Not a validated digital twin
- Not a diagnostic or treatment-selection system
- Biological claims require study-specific validation

## [1.0.1] — 2026-08-06

### Added

- Official portable Windows x64 distribution
- Single user-facing launcher: `Run_Simulator.cello.exe`
- Bundled private Python and scientific runtime
- Desktop shortcut creation after first successful launch
- Cello application and taskbar icon integration
- Versioned warm-start cache

### Improved

- Startup flow uses one persistent loading window
- Main simulator window appears after viewport, worker, and cell-state readiness
- Warm-start readiness gate reduced from three snapshots to two
- Responsive interface behavior from 1024×680 upward
- Dark mode, contrast icons, panel visibility controls, explicit pH readouts, research tools, and scientific audits retained in the portable build

### Distribution

- Release asset: `Cello_1.0.1_Portable_Windows_x64.zip`
- Platform: Windows x64
- Package type: portable ZIP

### Scientific status

- Research beta
- Not clinically validated
- Not a patient-specific predictor or digital twin

## Earlier development builds

Earlier internal development builds were not formally archived as public GitHub releases. The public version history begins with v1.0.1.
