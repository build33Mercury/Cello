# Changelog

## [2.1.0] — 2026-09-19

### Cell-specific pathways

- Specialized pathway choices are filtered by the selected cell model
- Hepatocyte: hepatic glucose production, ketogenesis, urea-cycle/nitrogen disposal
- Neuron: membrane excitation and synaptic vesicle cycle
- Adipocyte: storage/lipolysis
- Erythrocyte: 2,3-BPG/oxygen-affinity and NADPH/glutathione redox
- Pancreatic beta cell: glucose-stimulated insulin secretion
- Skeletal myocyte: excitation-contraction coupling and fuel mobilization
- Plant mesophyll: photosynthesis, carbon partition, vacuolar/osmotic regulation

### Spatial Biology

- Added render-space organelle XY projection
- Added pathway-anchor overlay and organelle filtering
- Added local model activity/damage table
- Added represented-count metadata
- Added CSV, JSON and PNG spatial export

### Scientific preservation

- No new kinetic equations were added for specialized pathway display
- `simulation.py`, `regulation.py`, `perturbations.py`, `cell_models.py` and `scene.py` are unchanged from v2.0.0

## [2.0.0] — 2026-09-19

- Visual Biology & Model Library major release

## [1.8.0] — 2026-09-19

- Experiment Automation
