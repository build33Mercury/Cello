# Cello v1.7.0

![Version](https://img.shields.io/badge/version-1.7.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 1.7.0 adds the **Microenvironment Engine** while retaining Population Mode, Quantitative Analysis, Perturbation Lab, Dynamic Pathway Explorer, Experiment Workspace, simulation recording, and live telemetry.

## Windows release

The Windows release asset is one file:

`Cello.exe`

No ZIP extraction and no separate Python installation are required. The optimized single-file startup architecture introduced in the repaired release line is retained.

Official v1.7.0 SHA-256:

`2cada31c7023183b98b322a4251c55a391db80be04f0ca20ac07bd36741fa09d`

## Microenvironment Engine · v1.7

The Microenvironment Engine exposes extracellular boundary conditions already represented by Cello and adds reproducible time-scheduled environmental changes.

It supports:

- extracellular temperature
- extracellular pH
- osmolarity
- medium volume
- perfusion state
- represented extracellular species concentrations
- reservoir concentrations
- species exchange rates
- model-condition presets
- scheduled environment events at explicit simulation times
- medium-replacement events
- live environment status and next-event reporting
- environment-event markers in Track Stats
- JSON and CSV schedule export
- preservation of environment schedules in experiment/recovery/recording metadata

Scheduled changes are applied by the simulation worker at the requested model time. The integration interval is split at event boundaries so event timing does not depend on GUI refresh timing.

Presets are labeled **model conditions**. They are not experimentally validated culture protocols or claims that a particular tissue, incubator, organism, patient, or disease state has been reproduced.

## Current capabilities

- interactive 3D biochemical cell visualization
- deterministic biochemical simulation and model-state inspection
- simulation recording and Track Stats live telemetry
- Experiment Workspace
- Dynamic Pathway Explorer
- Perturbation Lab
- Quantitative Analysis
- Population Mode
- Microenvironment Engine

## Scientific scope

Cello is research-beta software. Outputs are generated from implemented equations, parameters, assumptions, and abstractions. They are not clinical outputs, patient-specific predictions, experimental measurements, or a validated digital twin.

Study-specific use requires appropriate calibration, numerical verification, sensitivity and uncertainty analysis, external or held-out validation where applicable, and independent scientific interpretation.

## Validation status

For the v1.7.0 build:

- PE32+ Windows x64 GUI structure: PASS
- embedded payload SHA-256/footer identity: PASS
- embedded payload ZIP CRC: PASS
- internal payload manifest verification: PASS
- required private Python/Qt runtime components: PASS
- Python source compilation: PASS
- microenvironment schedule normalization/application tests: PASS
- exact environment-event boundary integration smoke test: PASS
- `simulation.py`, `regulation.py`, and `perturbations.py` unchanged from v1.6.0: PASS

Native Windows launch and headline-feature smoke testing remain host-level release verification steps.

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).

## License and limitations

Cello's original project materials are distributed under the terms in [LICENSE](LICENSE). Bundled third-party components remain governed by their own licenses.
