# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 1.1.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Package type | Portable ZIP |
| Separate Python required | No |
| Installer required | No |

## Standard installation

1. Open the repository's **Releases** page.
2. Select **Cello v1.1.0**.
3. Download `Cello_1.1.0_Windows_x64_Portable.zip` from the release assets.
4. Extract the complete ZIP to a normal folder.
5. Open the extracted `Cello_1.1.0_Windows_x64_Portable` directory.
6. Double-click `Run_Simulator.cello.exe`.

Windows may hide the final `.exe` extension, so the launcher can appear as `Run_Simulator.cello`.

## Important folder rule

Do not move the launcher away from the rest of the portable package. Keep the application directory intact:

```text
Cello_1.1.0_Windows_x64_Portable/
├── Run_Simulator.cello.exe
├── _cello_runtime/
├── src/
├── assets/
├── docs/
├── models/
├── README.md
├── CHANGELOG.md
├── RELEASE_NOTES_1.1.txt
└── SCIENTIFIC_LIMITATIONS.txt
```

The private runtime contains Cello's bundled Python and scientific dependencies. No system-wide Python installation is needed.

## First launch

The first launch initializes the biochemical model, 3D viewport, simulation worker, initial cell state, interface, and local runtime resources.

## Verify the download

Official v1.1.0 Windows ZIP SHA-256:

```text
b636317b71a53dcec70cb7a127146a5f16c35ec6b4d8aad58b961afe236ba175
```

### PowerShell

Open PowerShell in the directory containing the ZIP and run:

```powershell
Get-FileHash .\Cello_1.1.0_Windows_x64_Portable.zip -Algorithm SHA256
```

The displayed hash must exactly match the official value above.

The bundled launcher SHA-256 is:

```text
f4093b1be2d2c85e935b5447dab8a49b0b8d7c33211715a7f388b21236a85339
```

## Windows security warning

Because an independently distributed executable may not yet have a widely recognized code-signing reputation, Windows can display a SmartScreen warning. Only run a copy obtained from the official Cello repository release and verify the SHA-256 checksum first.

## Native Windows validation

The v1.1.0 package is structurally verified as a Windows x64 portable build and passed its source-level automated checks. A final GUI smoke launch should still be performed on a Windows x64 host after downloading the published release asset.

## Uninstall

Cello is portable. Close Cello, remove the extracted application folder, remove any shortcut you created, and delete the downloaded ZIP if no longer needed.

## Troubleshooting

See [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md).
