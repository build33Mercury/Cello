# Changelog

All notable changes to Cello are documented here.

The project follows semantic versioning and uses GitHub Releases for downloadable builds.

## [1.1.0] — 2026-08-29

### Added

#### Record Simulation

* Added a dedicated **Record Simulation** control
* Added persistent simulation trajectory capture
* Added approximately 0.10-second target sampling
* Added structured CSV trajectory export
* Added recording metadata and provenance preservation
* Added simulation parameter preservation
* Added biological profile preservation
* Added environment and biosettings preservation
* Added entity configuration preservation
* Added entity addition, update, and removal history
* Added software and model version metadata
* Added recording duration and sample-count metadata
* Added automatic 300 DPI PNG summary figures
* Added automatic PDF summary figures
* Added recording-package manifest generation
* Added member-level integrity hashes
* Added recovery recording behavior for interrupted sessions

#### Track Stats

* Added the **Track Stats** live research telemetry overlay
* Added live simulation-time reporting
* Added live viability reporting
* Added live intracellular pH reporting
* Added live membrane-potential reporting
* Added ATP concentration plotting
* Added intracellular glucose plotting
* Added glycolysis-flux plotting
* Added TCA-cycle-flux plotting
* Added ATP-synthase-flux plotting
* Added bounded telemetry history for long-running sessions
* Added telemetry redraw throttling for interface responsiveness
* Added light-theme support
* Added dark-theme support
* Added direct integration with live simulation snapshots

### Improved

* Updated application version to 1.1.0
* Updated Windows application metadata
* Updated the Cello single-instance application identifier
* Expanded simulation-state observability
* Expanded research-oriented output and export capabilities
* Improved provenance preservation for recorded simulation runs
* Preserved the established portable Windows application structure
* Rebuilt the Windows x64 executable from the updated application source

### Validation

The v1.1.0 Windows release passed:

* Python source compilation checks
* GUI import checks
* biochemical simulation advancement tests
* recording generation tests
* recording ZIP integrity checks
* recording manifest checksum verification
* Windows x64 PyInstaller build
* bundled runtime validation
* Qt runtime consistency checks
* native Windows GUI smoke launch
* final portable-package integrity verification

### Distribution

* Release asset: `cello_1.1_windows_x64.zip`
* Extracted application directory: `Cello_1.1_Portable`
* Launcher: `Run_Simulator.cello.exe`
* Platform: Windows x64
* Package type: portable ZIP
* No separate Python installation required

### Scientific status

* Research beta
* Model-generated simulation outputs
* Not clinically validated
* Not a patient-specific predictor
* Not a validated digital twin
* Not a diagnostic system
* Not a treatment-selection system
* Experimental and biological validation remain necessary for scientific interpretation

## [1.0.1] — 2026-08-06

### Added

* Official portable Windows x64 distribution
* Single user-facing launcher: `Run_Simulator.cello.exe`
* Bundled private Python and scientific runtime
* Desktop shortcut creation after first successful launch
* Cello application and taskbar icon integration
* Versioned warm-start cache

### Improved

* Startup flow now uses one persistent loading window
* Main simulator window appears once after viewport, worker, and cell state readiness
* Warm-start readiness gate reduced from three snapshots to two
* Responsive interface behavior from 1024×680 upward
* Dark mode, contrast icons, panel visibility controls, explicit pH readouts, research tools, and scientific audits retained in the portable build

### Distribution

* Release asset: `Cello_1.0.1_Portable_Windows_x64.zip`
* Platform: Windows x64
* Package type: portable ZIP

### Scientific status

* Research beta
* Not clinically validated
* Not a patient-specific predictor or digital twin

## Earlier development builds

Earlier internal development builds were not formally archived as public GitHub releases. The public version history begins with v1.0.1. This avoids inventing a fake release history for appearances.
