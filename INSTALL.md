# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 3.2.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

Download the v3.2.0 asset named `Cello.exe` and double-click it.

The first launch prepares a versioned private runtime under:

`%LOCALAPPDATA%\Cello\runtime`

Later launches reuse the prepared runtime.

Verify the release:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Expected SHA-256:

`f0e8ca33e1806d4b6c863e8ffdd25fbe0b191c34a3144a488c220b2af71e3a30`

Startup diagnostics are written under `%LOCALAPPDATA%\Cello\logs`.
