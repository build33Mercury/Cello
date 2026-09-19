# Cello v2.1.0

![Version](https://img.shields.io/badge/version-2.1.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 2.1.0 adds **Spatial Biology** and **cell-specific pathway workspaces** while retaining the full v2 visual overhaul, Cell Model Library, Experiment Automation, Microenvironment Engine, Population Mode, Quantitative Analysis, Perturbation Lab, Experiment Workspace, recording, and telemetry.

## Windows release

The Windows release asset remains one file:

`Cello.exe`

SHA-256:

`edfadd5362a8ebf042891928c26e7ccd3964948ca676fb906885145785fb718b`

## Cell-specific pathways

Specialized pathways now appear only when the matching cell model is active.

- **Hepatocyte:** hepatic glucose production, ketogenesis, nitrogen disposal / urea cycle
- **Neuron:** membrane excitation, synaptic vesicle cycle
- **Adipocyte:** substrate storage / lipolysis
- **Erythrocyte:** 2,3-BPG / oxygen-affinity coupling, NADPH / glutathione redox
- **Pancreatic beta cell:** glucose-stimulated insulin secretion
- **Skeletal myocyte:** excitation-contraction coupling, fuel mobilization
- **Plant mesophyll:** photosynthesis / carbon fixation, starch / respiratory partitioning, vacuolar osmotic regulation
- **Generic mammalian:** core pathways only

These maps are constrained to processes already represented by Cello. They do not silently add new kinetic equations.

## Spatial Biology

The new Spatial Biology workspace exposes:

- deterministic organelle render-space positions
- pathway-anchor overlays
- organelle-kind filtering
- local model activity and damage readouts
- represented-count metadata
- CSV and JSON spatial snapshot export
- PNG projection export

Spatial coordinates are Cello visualization coordinates, not microscopy or spatial-omics measurements.

## Scientific preservation

`simulation.py`, `regulation.py`, `perturbations.py`, `cell_models.py`, and `scene.py` are byte-for-byte unchanged from v2.0.0.

## Validation

- 63/63 Python source files parse successfully
- 8/8 cell-model simulation smoke tests pass
- all 14 specialized pathway definitions reference fluxes emitted by the matching cell model
- SpatialLayoutEngine smoke test passes across all 8 models with zero unresolved placements at seed 1010
- 4,546 internal payload checksums verify
- payload ZIP CRC: PASS
- embedded payload footer SHA-256: PASS

Native Windows GUI and interactive Spatial Biology/pathway testing remain host-level verification steps.

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).
