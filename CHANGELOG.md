# Changelog

All notable changes to Cello are documented here.

The project follows semantic versioning and uses GitHub Releases for downloadable builds.

## [1.0.1] — 2026-08-06

### Added

- Official portable Windows x64 distribution
- Single user-facing launcher: `Run_Simulator.cello.exe`
- Bundled private Python and scientific runtime
- Desktop shortcut creation after first successful launch
- Cello application and taskbar icon integration
- Versioned warm-start cache

### Improved

- Startup flow now uses one persistent loading window
- Main simulator window appears once after viewport, worker, and cell state readiness
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

Earlier internal development builds were not formally archived as public GitHub releases. The public version history begins with v1.0.1. This avoids inventing a fake release history for appearances.
