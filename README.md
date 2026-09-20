# Cello v3.0.0

![Version](https://img.shields.io/badge/version-3.0.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 3.0 is the **Biochemical Atlas, Cell Dynamics & Division** release.

## Windows release

The public release asset remains one file:

`Cello.exe`

SHA-256:

`e52ab615a7614b3b2b11456eb9e99367ed249cd2d1f873ff5d5ca8511bfd6b69`

## v3 highlights

- repaired Dynamic Pathway Explorer initialization
- cell-aware **View Pathways** buttons that change immediately with the selected cell model
- a 119-entry biochemical pathway atlas spanning major metabolic, signaling, gene-expression, redox, nucleotide, DNA-maintenance, cell-cycle and plant pathway families
- explicit separation of **SIMULATED**, **STATE-DERIVED**, and **REFERENCE SCHEMATIC** pathway coverage
- cell-specific pathways including hepatocyte ketogenesis/glucose-output/urea-cycle views and beta-cell insulin-secretion/biosynthesis/granule views
- DNA replication / S-phase pathway view for nucleated models
- four pathway graph modes: flux history, process snapshot, state snapshot and phase portrait
- brighter cell rendering
- low-amplitude real-time visual mobility for mobile organelles and structures
- triggerable S-phase → prophase → metaphase → anaphase → telophase → cytokinesis visualization ending in two daughter cells

## Scientific boundary

The atlas is broad coverage of major biochemical pathway families; it is not a claim to encode every known reaction, isoenzyme or tissue-specific branch. Reference schematics do not create hidden kinetics.

The mitosis sequence is a visual model-communication demonstration. It does not duplicate the underlying biochemical simulation state or constitute a calibrated kinetic cell-cycle model.

`simulation.py`, `regulation.py`, `perturbations.py`, and `cell_models.py` remain byte-for-byte unchanged from v2.1.0.

## Validation

- 63/63 Python source files parse successfully
- 8/8 built-in cell-model simulation smoke tests pass
- 119/119 pathway definitions are unique
- every pathway labelled SIMULATED references an emitted flux in every cell model where it is exposed
- 4,544/4,544 internal SHA-256 entries verify
- payload ZIP CRC: PASS
- embedded payload footer hash: PASS
- Windows x64 GUI PE structure and resource section: PASS
- native Windows GUI/interactive v3 feature smoke testing: pending host verification

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).
