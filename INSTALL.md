# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 1.7.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

## Run

1. Open the repository's **Releases** page.
2. Select Cello v1.7.0.
3. Download `Cello.exe`.
4. Double-click `Cello.exe`.

There is no ZIP to extract and no companion runtime folder to keep beside the executable.

## Private runtime and startup

On first launch, `Cello.exe` prepares a versioned private runtime under:

`%LOCALAPPDATA%\Cello\runtime`

Later launches reuse the prepared runtime. Startup diagnostics are written under:

`%LOCALAPPDATA%\Cello\logs`

## Verify v1.7.0

Use PowerShell:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Expected SHA-256:

`2cada31c7023183b98b322a4251c55a391db80be04f0ca20ac07bd36741fa09d`

## Windows security warning

Because an independently distributed executable may not yet have a widely recognized code-signing reputation, Windows can display a SmartScreen warning. Only run a copy obtained from the official Cello repository release and verify its SHA-256 first.

## Validation status

The v1.7.0 executable is structurally checked as a Windows x64 GUI executable; its embedded payload is checksum- and CRC-verified; startup-critical Python sources compile; and the new Microenvironment scheduling core passes model-time boundary tests.

A native Windows launch remains required before the exact published binary is called host-verified.

## Uninstall

Close Cello and delete `Cello.exe`. To remove the private runtime cache and logs as well, delete `%LOCALAPPDATA%\Cello`.

## Troubleshooting

If startup fails, inspect `%LOCALAPPDATA%\Cello\logs\CELLO_BOOTSTRAP_ERROR.txt` and `%LOCALAPPDATA%\Cello\logs\CELLO_RUNTIME.log`.
