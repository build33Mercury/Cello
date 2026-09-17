# Cello v1.1.0

![Cello](cello.png)

![Version](https://img.shields.io/badge/version-1.1.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-portable-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 1.1.0 adds a redesigned Cello interface, the new blue Cello identity, live research telemetry, configurable live plots, event markers, and structured simulation recording while preserving the existing biochemical model and 3D simulator.

## Windows release

The official v1.1.0 portable package is:

`Cello_1.1.0_Windows_x64_Portable.zip`

After downloading and extracting the complete ZIP, launch:

`Run_Simulator.cello.exe`

No separate Python installation is required. Keep `_cello_runtime`, `src`, `assets`, `docs`, and `models` beside the launcher.

> GitHub's automatically generated source-code archives are not the portable Windows application. Use the ZIP attached to the v1.1.0 GitHub Release.

## What is new in v1.1.0

### Interface and branding

- New blue Cello application icon and in-app brand mark
- Refreshed light and dark themes
- Cleaner header, cards, menus, controls, status indicators, hover states, and spacing
- Unified startup-window and simulator branding
- Clear recording and telemetry active states

### Live Research Telemetry

`Track Stats` opens a live overlay over the simulator. Users can select real state variables and pathway outputs emitted by the active Cello model.

Available model-state readouts include, where represented by the active model:

- ATP
- intracellular glucose
- mitochondrial oxygen
- NADH
- ROS proxy
- intracellular pH
- membrane potential
- calcium

Available pathway readouts include:

- glycolysis
- TCA cycle
- ATP synthase
- beta-oxidation
- pentose phosphate pathway
- glutaminase
- serine synthesis

Additional v1.1 telemetry features include ATP, glucose, viability, and event-count chips; pausing plot rendering without pausing the simulation; clearing the displayed history without resetting the model; and intervention/recording event markers.

### Simulation Recording

`Record Simulation` creates a structured experiment bundle containing:

```text
trajectory.csv
events.csv
recording.json
figures/
manifest.json
README.txt
```

Recording packages preserve model-generated trajectories, intervention history, environment and profile context, software/model versions, sampling metadata, summary figures, and SHA-256 integrity information.

## Scientific scope

Cello is research-beta software. Its outputs are simulations generated from the equations, parameters, assumptions, and abstractions implemented in the model. They are not experimental measurements, clinical outputs, patient-specific predictions, or evidence that a biological mechanism is accurate by themselves.

Study-specific scientific use requires appropriate calibration, numerical verification, sensitivity and uncertainty analysis, held-out or external validation, and independent interpretation.

## Integrity

Official v1.1.0 Windows ZIP SHA-256:

```text
b636317b71a53dcec70cb7a127146a5f16c35ec6b4d8aad58b961afe236ba175
```

`Run_Simulator.cello.exe` SHA-256:

```text
f4093b1be2d2c85e935b5447dab8a49b0b8d7c33211715a7f388b21236a85339
```

See [INSTALL.md](INSTALL.md) for installation and checksum verification.

## Validation status

The v1.1.0 package has passed source-level compilation and automated regression/scientific checks used for this build, with 68 tests passing and 0 failing. The packaged launcher is structurally verified as a Windows x64 PE GUI executable with the Cello icon embedded and the expected bundled Python runtime present.

Native Windows GUI smoke testing is a separate host-level check and should be performed on Windows after downloading the final release asset.

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).

## License and limitations

Cello's original project materials are distributed under the terms in [LICENSE](LICENSE). Bundled third-party components remain governed by their own licenses.
