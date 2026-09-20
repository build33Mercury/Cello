# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 3.0.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

Download the v3.0.0 asset named `Cello.exe` and double-click it.

The first launch prepares a private runtime under `%LOCALAPPDATA%\Cello\runtime`. Later launches reuse the versioned prepared runtime.

Verify the file:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Expected SHA-256:

`e52ab615a7614b3b2b11456eb9e99367ed249cd2d1f873ff5d5ca8511bfd6b69`

Startup diagnostics are written under `%LOCALAPPDATA%\Cello\logs`.

Native Windows launch of the exact release bytes remains the final host-level verification step.
