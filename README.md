# Cello v3.1.0

![Version](https://img.shields.io/badge/version-3.1.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 3.1 is a stabilization and workflow-polish release built on v3.0.

## Windows release

The public release asset remains one file:

`Cello.exe`

SHA-256:

`d0751627a2ae980026e10d2bfed4f41961eb249f88353e1f82b8295049becbd9`

## v3.1 improvements

### Pathway Explorer

- coverage filters for **Simulated**, **State-derived**, and **Reference schematic**
- **Cell-specific** filter
- persistent pinned pathways
- Ctrl+F search focus
- pathway graph export to PNG, PDF, and SVG
- pathway tables/maps remain available if the plotting backend cannot initialize
- guarded startup with a dedicated `PATHWAY_EXPLORER_ERROR.txt` diagnostic instead of a silent failure

### Cell dynamics

- mitosis pause/resume
- 0.5×, 1×, 1.5×, and 2× playback speeds
- live stage/progress display
- division demo disabled for cell models outside the explicitly supported visual-demo set
- user-toggleable ambient organelle motion

## Scientific preservation

v3.1 does not add or modify kinetic equations or pathway definitions.

The following files are byte-for-byte unchanged from v3.0:

- `simulation.py`
- `regulation.py`
- `perturbations.py`
- `cell_models.py`
- `pathway_data.py`

Pathway coverage retains the v3 contract: **SIMULATED**, **STATE-DERIVED**, and **REFERENCE SCHEMATIC**.

The cell-division sequence remains a visual communication demonstration, not a calibrated kinetic cell-cycle model.

## Validation

- 63/63 Python source files parse successfully
- 8/8 built-in cell-model simulation smoke tests pass
- 119/119 pathway definitions remain unique
- simulated pathways retain emitted-flux coverage
- 4,544/4,544 internal SHA-256 entries verify
- embedded payload ZIP CRC: PASS
- embedded payload footer hash: PASS
- Windows x64 GUI PE/resource structure: PASS
- native Windows GUI smoke test: pending host verification

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).
