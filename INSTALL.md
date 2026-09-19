# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 2.1.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

Download `Cello.exe` and double-click it.

The first launch prepares a versioned private runtime under `%LOCALAPPDATA%\Cello\runtime`. Later launches reuse that runtime.

Verify the download with:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Expected SHA-256:

`edfadd5362a8ebf042891928c26e7ccd3964948ca676fb906885145785fb718b`

Startup diagnostics are written under `%LOCALAPPDATA%\Cello\logs`.
