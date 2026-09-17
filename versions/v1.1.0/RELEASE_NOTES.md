# Cello v1.1.0 Release Notes

## Live Research Telemetry

Cello v1.1 introduces a substantially expanded `Track Stats` system. Users can select model state variables and pathway outputs for live plotting, pause plot rendering without pausing the simulation, clear visible history without resetting the model, and inspect intervention/recording event markers.

Model-state options include ATP, intracellular glucose, mitochondrial oxygen, NADH, ROS proxy, intracellular pH, membrane potential, and calcium where represented by the active model. Pathway outputs include glycolysis, TCA cycle, ATP synthase, beta-oxidation, pentose phosphate pathway, glutaminase, and serine synthesis.

## Simulation Recording

`Record Simulation` now produces structured experiment bundles containing trajectory data, timestamped events, provenance metadata, summary figures, and SHA-256 integrity information.

Typical recording contents include:

```text
trajectory.csv
events.csv
recording.json
figures/
manifest.json
README.txt
```

## Interface Refresh

- New blue Cello application icon and in-app brand mark
- Reworked light and dark themes
- Cleaner header, cards, menus, controls, active states, hover states, status indicators, and spacing
- Unified startup and simulator visual identity
- Clearer recording and telemetry state feedback

## Windows Packaging

- Portable Windows x64 package
- Required launcher: `Run_Simulator.cello.exe`
- Bundled private Python 3.12 scientific runtime
- No separate Python installation required
- Worker command-line forwarding preserved in the launcher

## Validation

The prepared v1.1.0 package completed 68 automated source-level checks with 0 failures, ZIP integrity checks, release-manifest/checksum generation, Windows x64 PE launcher structure verification, embedded icon verification, runtime presence verification, and worker command-line forwarding verification.

A final native Windows GUI smoke launch remains a host-level release check.

## Scientific boundary

Cello v1.1.0 remains research-beta software. Telemetry and recordings are outputs of the implemented model, not experimental measurements, clinical outputs, patient-specific predictions, or independent evidence of biological accuracy. Appropriate calibration, numerical verification, sensitivity/uncertainty analysis, and external validation are required for scientific claims.
