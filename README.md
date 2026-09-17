# Cello v1.6.0

![Version](https://img.shields.io/badge/version-1.6.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 1.6.0 adds Population Mode for reproducible virtual-cell ensembles while retaining the Experiment Workspace, Dynamic Pathway Explorer, Perturbation Lab, Quantitative Analysis, simulation recording, and live telemetry introduced across v1.1–v1.5.

## Windows release

The Windows release asset is a single file:

`Cello.exe`

No ZIP extraction and no separate Python installation are required. Double-click `Cello.exe` to launch.

The executable contains Cello's private application payload and verifies it before preparing a versioned runtime under `%LOCALAPPDATA%\Cello\runtime`. Startup diagnostics are written under `%LOCALAPPDATA%\Cello\logs`.

## Current capabilities

- interactive 3D biochemical cell visualization
- deterministic biochemical simulation and model-state inspection
- simulation recording and Track Stats live telemetry
- Experiment Workspace with projects, branches, runs, notes, conditions, and comparisons
- Dynamic Pathway Explorer
- Perturbation Lab
- Quantitative Analysis with descriptive statistics and publication-oriented export
- Population Mode with reproducible model-generated virtual-cell ensembles

## Population Mode · v1.6

Population Mode supports:

- 2–500 independent virtual-cell model replicates
- reproducible population seeds
- configurable model-parameter heterogeneity
- ATP, glucose, ROS, pH, damage, oxygen, membrane-potential, and pathway-flux metrics
- median and interquartile-range trajectories
- endpoint mean, SD, median, quartiles, minimum, and maximum
- model-state fractions for healthy, stressed, injured, irreversibly injured, and necrotic virtual cells
- per-cell endpoint export to CSV
- structured JSON population export
- cancellable background population computation

Population outputs are simulated virtual-cell replicates. They are not biological replicates, patient observations, or experimental measurements.

## Scientific scope

Cello is research-beta software. Its outputs are generated from the equations, parameters, assumptions, and abstractions implemented in the model. They are not clinical outputs, patient-specific predictions, a validated digital twin, or evidence that a biological mechanism is correct by themselves.

Study-specific use requires appropriate calibration, numerical verification, sensitivity and uncertainty analysis, external or held-out validation where applicable, and independent scientific interpretation.

## Release validation

The rebuilt single-file Windows executables are structurally validated as PE32+ x86-64 GUI applications, contain the Cello icon resources, contain checksum-verified embedded payloads, and passed payload ZIP integrity checks. The v1.6 source compiles successfully and its population-core simulation smoke test passes. Core `simulation.py`, `regulation.py`, and `perturbations.py` are byte-for-byte unchanged from v1.5.0.

A native Windows GUI smoke launch remains a host-level validation step and should be performed on Windows before a build is declared release-verified.

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).

## License and limitations

Cello's original project materials are distributed under the terms in [LICENSE](LICENSE). Bundled third-party components remain governed by their own licenses.
