# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 1.0.1 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Package type | Portable ZIP |
| Separate Python required | No |
| Installer required | No |

## Standard installation

1. Open the repository's **Releases** page.
2. Select **Cello v1.0.1**.
3. Download `Cello_1.0.1_Portable_Windows_x64.zip` from the release assets.
4. Right-click the ZIP and select **Extract All**.
5. Open the extracted `Cello_1.0.1_Portable` folder.
6. Double-click `Run_Simulator.cello.exe`.

Windows may hide the final `.exe` extension, so the launcher can appear as `Run_Simulator.cello`.

## Important folder rule

Do not move the executable away from `_cello_runtime`.

The folder must remain structured like this:

```text
Cello_1.0.1_Portable/
├── Run_Simulator.cello.exe
├── _cello_runtime/
├── README_FIRST.txt
├── RELEASE_NOTES_1.0.0.txt
└── SCIENTIFIC_LIMITATIONS.txt
```

The private runtime contains Cello's Python and scientific dependencies. No system-wide Python installation is needed.

## First launch

The first launch performs complete initialization of:

- The biochemical model
- The 3D viewport
- The simulation worker
- The initial cell state
- The versioned warm-start cache

A loading window remains visible until the simulator is ready. After a successful first launch, Cello creates a desktop shortcut using the cell icon.

## Later launches

Later launches can use the warm-start cache. Starting Cello while it is already running activates the existing window rather than opening a second simulator and worker process.

## Verify the download

The official SHA-256 checksum is:

```text
9f5bef711a02418ea6b2e15016d4dd065ada45e59848cfbeb2e127ab95ea71d3
```

### PowerShell

Open PowerShell in the folder containing the ZIP and run:

```powershell
Get-FileHash .\Cello_1.0.1_Portable_Windows_x64.zip -Algorithm SHA256
```

The displayed hash must exactly match the official value above.

## Windows security warning

Because an independently distributed build may not have a widely recognized code-signing reputation, Windows can display a SmartScreen warning. Only run a file downloaded from the official repository release, verify its checksum, and do not bypass a warning for a file obtained elsewhere.

## Uninstall

Cello is portable. To remove it:

1. Close Cello.
2. Delete the extracted `Cello_1.0.1_Portable` folder.
3. Delete the desktop shortcut if one was created.
4. Delete the original downloaded ZIP if no longer needed.

No separate Python installation or traditional Windows uninstaller is involved.

## Troubleshooting

See **[docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md)**.
