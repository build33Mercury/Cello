# Cello v1.1.0

Release package prepared on 2026-09-17.

## Distribution

- Platform: Windows x64
- Package: portable ZIP
- Asset: `Cello_1.1.0_Windows_x64_Portable.zip`
- Launcher: `Run_Simulator.cello.exe`
- Separate Python installation: not required

## SHA-256

Portable ZIP:

```text
b636317b71a53dcec70cb7a127146a5f16c35ec6b4d8aad58b961afe236ba175
```

Launcher inside the portable package:

```text
f4093b1be2d2c85e935b5447dab8a49b0b8d7c33211715a7f388b21236a85339
```

## Highlights

- New blue Cello application identity
- Refreshed light and dark UI
- Live Research Telemetry
- Selectable state and pathway plots
- Pause Plot
- Live ATP, glucose, viability, and event indicators
- Intervention and recording event markers
- Structured simulation recording
- Trajectory, event, provenance, figure, and checksum exports

## Validation

The prepared package reports 68 source-level automated checks passing with 0 failures. The Windows launcher was structurally verified as a PE32+ x86-64 GUI executable with the Cello icon embedded, expected runtime files present, and worker command-line forwarding preserved.

A native Windows GUI smoke launch remains a release-host verification step.

## Scientific status

Research beta. Cello outputs are model-generated simulations and are not clinical outputs, patient-specific predictions, experimental measurements, or biological validation by themselves.

See [RELEASE_NOTES.md](RELEASE_NOTES.md), [SHA256SUMS.txt](SHA256SUMS.txt), and [release-manifest.json](release-manifest.json).
