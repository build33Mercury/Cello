# Cello v1.8.0

![Version](https://img.shields.io/badge/version-1.8.0-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![Status](https://img.shields.io/badge/status-research%20beta-orange)
![Distribution](https://img.shields.io/badge/distribution-single--file-success)

**Cello is an interactive biochemical cell simulator and research-oriented visualization platform for Windows x64.**

Version 1.8.0 adds **Experiment Automation** and refines the interface toward a more conventional desktop scientific application: denser controls, neutral header tools, restrained corner radii, standard queue/results tables, and less decorative dashboard chrome.

## Windows release

The Windows release asset is one file:

`Cello.exe`

No ZIP extraction and no separate Python installation are required. The optimized single-file startup architecture from v1.7 is retained.

Official v1.8.0 SHA-256:

`3cec037031e2abe24995bf171cd8c8039327ad42fe639fc702861014cdf50921`

## Experiment Automation · v1.8

Experiment Automation supports:

- up to three sweep factors per condition matrix
- model-parameter sweeps
- extracellular pH, temperature, osmolarity, volume, and represented-medium species sweeps
- deterministic seed assignment and repeated computational runs
- queue preview before execution
- run status tracking
- final, mean, minimum, maximum, and trapezoidal-AUC response summaries
- one- and two-factor response plotting
- CSV results export
- JSON run-bundle export
- preservation of the current experiment state and v1.7 environment schedule during automated runs
- a 2,000-run design safety limit

Repeated seeds are computational repeats, not biological replicates. Parameter sweeps are model exploration, not empirical dose-response data.

## Interface refinement

v1.8 keeps the Cello identity but uses a more conventional scientific-desktop presentation:

- neutralized header tool buttons
- reduced rounded-card treatment
- standard group boxes and tabbed queue/results views
- more compact status and table typography
- shorter functional descriptions
- plotting libraries remain lazy-loaded until a plot is requested

## Scientific scope

Cello is research-beta software. Outputs are generated from implemented equations, parameters, assumptions, and abstractions. They are not clinical outputs, patient-specific predictions, experimental measurements, or a validated digital twin.

Study-specific use requires appropriate calibration, numerical verification, sensitivity and uncertainty analysis, external or held-out validation where applicable, and independent scientific interpretation.

## Validation status

For the v1.8.0 build:

- PE32+ Windows x64 GUI structure: PASS
- embedded payload SHA-256/footer identity: PASS
- embedded payload ZIP CRC: PASS
- 4,600-entry internal SHA-256 manifest verification: PASS
- 62 Python source files parse successfully: PASS
- Experiment Automation core checks: 9/9 PASS
- v1.7 scientific-core files preserved byte-for-byte: PASS
- Cello PE resource section preserved byte-for-byte from v1.7: PASS

Native Windows launch and interactive Experiment Automation smoke testing remain host-level verification steps.

## Version history

See [CHANGELOG.md](CHANGELOG.md) and [versions/](versions/README.md).

## License and limitations

Cello's original project materials are distributed under the terms in [LICENSE](LICENSE). Bundled third-party components remain governed by their own licenses.
