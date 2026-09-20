# Cello v3.2.0

![Version](https://img.shields.io/badge/version-3.2.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 3.2 adds **Model Sensitivity & Uncertainty** diagnostics while preserving the v3.1 kinetic and pathway-definition core.

## Windows release

The public release asset remains one file:

`Cello.exe`

SHA-256:

`f0e8ca33e1806d4b6c863e8ffdd25fbe0b191c34a3144a488c220b2af71e3a30`

## Sensitivity & Uncertainty

The new workspace supports:

- local finite-difference sensitivity analysis
- normalized elasticity where baseline factor and response are non-zero
- reproducible Latin-hypercube uncertainty propagation
- up to 12 simultaneously varied factors
- up to 500 uncertainty samples
- cell-model-specific recommended parameter sets
- final value, time mean, minimum, maximum and AUC response statistics
- standardized regression coefficients and Pearson-correlation screening metrics
- deterministic seeds
- cancellable background execution with progress reporting
- CSV and JSON export
- diagnostic plotting

## Scientific interpretation

Local sensitivity is neighborhood-specific and depends on the selected range, model state, duration and response statistic.

Uncertainty propagation uses independent uniform ranges explicitly chosen by the user. Those ranges are model assumptions unless independently supported by data.

Standardized regression coefficients and correlations are screening diagnostics, not causal-effect estimates. Computational samples are not biological replicates.

## Scientific preservation

The following v3.1 files are byte-for-byte unchanged:

- `simulation.py`
- `regulation.py`
- `perturbations.py`
- `cell_models.py`
- `pathway_data.py`

The 119-entry pathway atlas is unchanged.

## Validation

- Python source parse: 65/65 PASS
- built-in cell-model simulation smoke tests: 8/8 PASS
- local sensitivity core test: PASS
- uncertainty core test: PASS
- embedded payload ZIP CRC: PASS
- internal SHA-256 manifest: 4,547/4,547 PASS
- Windows x64 GUI PE/resource structure: PASS
- native Windows GUI workspace smoke test: pending host verification

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).
