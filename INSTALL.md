# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 1.8.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

## Run

1. Open the repository's **Releases** page.
2. Select Cello v1.8.0.
3. Download `Cello.exe`.
4. Double-click `Cello.exe`.

There is no ZIP to extract and no companion runtime folder to keep beside the executable.

## Private runtime and startup

On first launch, `Cello.exe` prepares a versioned private runtime under:

`%LOCALAPPDATA%\Cello\runtime`

Later launches reuse the prepared runtime. Startup diagnostics are written under:

`%LOCALAPPDATA%\Cello\logs`

## Verify v1.8.0

Use PowerShell:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Expected SHA-256:

`3cec037031e2abe24995bf171cd8c8039327ad42fe639fc702861014cdf50921`

## Validation status

The v1.8.0 executable is structurally checked as a Windows x64 GUI executable. Its embedded payload passed footer-hash, ZIP CRC, internal-manifest, source-parse, and Experiment Automation core checks.

A native Windows launch and interactive Experiment Automation smoke test remain required before the exact published binary is called host-verified.

## Uninstall

Close Cello and delete `Cello.exe`. To remove the private runtime cache and logs as well, delete `%LOCALAPPDATA%\Cello`.

## Troubleshooting

If startup fails, inspect `%LOCALAPPDATA%\Cello\logs\CELLO_BOOTSTRAP_ERROR.txt` and `%LOCALAPPDATA%\Cello\logs\CELLO_RUNTIME.log`.
