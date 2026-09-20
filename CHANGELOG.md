# Changelog

## [3.0.0] — 2026-09-20

### Biochemical Pathway Atlas
- fixed Dynamic Pathway Explorer initialization and cell-model synchronization
- expanded to 119 pathway definitions
- added simulated/state-derived/reference-schematic coverage labels
- added pathway-family filtering and search
- added active-cell-specific View Pathways buttons
- added DNA-replication and mitosis/cytokinesis pathway views
- added four graph modes: flux history, process snapshot, state snapshot and phase portrait

### Cell-specific pathways
- hepatocyte: glucose production, ketogenesis, urea cycle, bile-acid synthesis, lipoprotein assembly, CYP detoxification
- neuron: excitation, synaptic vesicle cycle, glutamate-glutamine interface, axonal transport
- adipocyte: storage/lipolysis and insulin-dependent GLUT4 trafficking
- erythrocyte: 2,3-BPG/oxygen affinity, glutathione redox, methemoglobin reduction, ATP-dependent membrane homeostasis
- pancreatic beta cell: insulin secretion, insulin biosynthesis/processing schematic and granule trafficking
- skeletal myocyte: excitation-contraction, fuel mobilization and phosphocreatine shuttle
- plant mesophyll: photosynthesis/carbon fixation, carbon partition, osmotic regulation and nitrogen assimilation

### Cell visualization
- brighter material/lighting treatment
- activated the existing nuclear DNA-replication visual layer
- added restrained real-time visual mobility to mobile organelles/structures
- added triggerable visual S phase → mitosis → cytokinesis sequence ending in two daughter cells

### Scientific preservation
- simulation.py unchanged from v2.1.0
- regulation.py unchanged from v2.1.0
- perturbations.py unchanged from v2.1.0
- cell_models.py unchanged from v2.1.0
- reference schematics are not assigned fabricated kinetic fluxes

## [2.1.0] — 2026-09-19
- Spatial Biology & Cell-Specific Pathways

## [2.0.0] — 2026-09-19
- Visual Biology & Model Library

## [1.8.0] — 2026-09-19
- Experiment Automation
