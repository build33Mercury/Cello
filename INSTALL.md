# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 3.1.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

Download the v3.1.0 asset named `Cello.exe` and double-click it.

The first launch prepares a private versioned runtime under:

`%LOCALAPPDATA%\Cello\runtime`

Later launches reuse the prepared runtime.

Verify the file:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Expected SHA-256:

`d0751627a2ae980026e10d2bfed4f41961eb249f88353e1f82b8295049becbd9`

Startup diagnostics are written under `%LOCALAPPDATA%\Cello\logs`.
