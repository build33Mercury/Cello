# Cello v1.6.0

Release theme: Population Mode.

## Windows asset

`Cello.exe`

SHA-256:

```text
01286b1a4ce8a0c6bfd8677d610d4db08da66269fd1a221b5e4a53a7b0807023
```

Population Mode adds 2–500 independent model-generated virtual-cell replicates, reproducible population seeds, configurable parameter heterogeneity, population trajectory summaries, endpoint distributions, model-state fractions, and CSV/JSON export.

Population outputs are simulations, not biological replicates or experimental observations.

Build-time checks passed for Python source compilation, population-core simulation smoke testing, PE32+ x86-64 structure, icon resources, embedded payload checksum validation, and embedded ZIP CRC. Core `simulation.py`, `regulation.py`, and `perturbations.py` are byte-for-byte unchanged from v1.5.0.

Native Windows GUI smoke testing remains required before host-level release verification.
