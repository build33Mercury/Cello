# Cello v2.0.0

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 2.0 is a major visual-biology and model-workflow release. It redesigns all eight built-in cell-model visual profiles, upgrades the Pathway Explorer into a professional model-graph workspace, and adds a Cell Model Library for specifications and reproducible presets.

## Windows release

The public release asset remains one file:

`Cello.exe`

SHA-256:

`3f2750f387a255f22dcc5b07cc510851da3a9bf53ee3735a0054f47db9f24be5`

## Cello 2.0

### Visual biology overhaul

- redesigned mammalian cell scaffold with restrained membrane/cytosol materials
- upgraded nucleus/chromatin, ER, Golgi, mitochondria, vesicle and ribosome rendering
- hepatocyte-specific polarity, glycogen and lipid landmarks
- rebuilt neuronal arbor, axon, myelin and terminals
- improved adipocyte lipid-droplet profile
- procedural biconcave erythrocyte
- expanded pancreatic beta-like granule rendering
- skeletal-myocyte sarcomere cues
- angular plant wall/membrane/vacuole profile with peripheral chloroplasts

### Pathway workspace

- professional node-and-arrow pathway schematics
- represented-process labels and live model-flux values
- inhibition/inactivity status styling
- PNG pathway-diagram export
- retained process/state tables and live flux history

### Cell Model Library

- inspect all eight built-in model specifications
- export model specifications
- save/import reproducible presets
- presets reference built-in models and explicit parameter/environment overrides
- imported presets do not silently inject new kinetic code

## Scientific preservation

The v2 visual overhaul changes presentation and workflow, not the kinetic core. `simulation.py`, `regulation.py`, and `perturbations.py` are byte-for-byte unchanged from v1.8.0. Non-visual scientific fields in all built-in CellModelSpec entries are also unchanged.

Cell geometry and pathway schematics remain explanatory model visualizations, not microscopy-derived reconstructions, experimental measurements, clinical outputs or validated digital twins.

## Validation

Build-time checks passed for all eight cell models, source parsing, payload integrity, internal checksums and scientific-core preservation. Native Windows GUI verification remains a host-level check.

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).
