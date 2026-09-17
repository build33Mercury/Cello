# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 1.6.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

## Run

1. Open the repository's **Releases** page.
2. Select the desired Cello version.
3. Download the release asset named `Cello.exe`.
4. Double-click `Cello.exe`.

There is no ZIP to extract and no companion runtime folder to keep beside the executable.

## Private runtime

`Cello.exe` contains a checksum-protected application payload. On launch it prepares a private cache under:

```text
%LOCALAPPDATA%\Cello\runtime
```

The cache is versioned by the embedded payload hash. Cello verifies the embedded payload before using it.

Startup diagnostics are written under:

```text
%LOCALAPPDATA%\Cello\logs
```

## Verify a release

Use PowerShell:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Compare the result with the SHA-256 published for the specific release version.

## Windows security warning

Because an independently distributed executable may not yet have a widely recognized code-signing reputation, Windows can display a SmartScreen warning. Only run a copy obtained from the official Cello repository release and verify its SHA-256 first.

## Validation status

The rebuilt single-file executables are structurally checked as Windows x64 GUI executables and their embedded payloads are checksum- and CRC-verified during the build process. A native Windows GUI smoke launch is still required before calling any individual build host-verified.

## Uninstall

Close Cello and delete `Cello.exe`. To remove the private runtime cache and logs as well, delete `%LOCALAPPDATA%\Cello`.

## Troubleshooting

If startup fails, inspect `%LOCALAPPDATA%\Cello\logs\CELLO_BOOTSTRAP_ERROR.txt` and `%LOCALAPPDATA%\Cello\logs\CELLO_RUNTIME.log`.
