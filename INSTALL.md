# Installing Cello

## Supported release

| Item | Value |
|---|---|
| Version | 2.0.0 |
| Operating system | Windows 10 or Windows 11, 64-bit |
| Distribution | Single Windows executable |
| File name | `Cello.exe` |
| Separate Python required | No |
| Installer required | No |

Download `Cello.exe` from the v2.0.0 release and double-click it.

The first launch prepares Cello's private versioned runtime under `%LOCALAPPDATA%\Cello\runtime`. Later launches reuse that runtime.

Verify the download with:

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Expected SHA-256:

`3f2750f387a255f22dcc5b07cc510851da3a9bf53ee3735a0054f47db9f24be5`

Startup diagnostics are written under `%LOCALAPPDATA%\Cello\logs`.
