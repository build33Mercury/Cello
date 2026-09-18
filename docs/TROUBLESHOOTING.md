# Troubleshooting

## Cello takes time to open

Current single-file releases show a native Cello startup window immediately after launch.

On the first run, Cello prepares its private runtime under:

`%LOCALAPPDATA%\Cello\runtime`

Later launches reuse the prepared runtime and should avoid the extraction phase.

If every launch behaves like a first launch, include the startup logs when reporting the issue because the runtime-ready marker may not be persisting.

## The application does not start

1. Confirm that the file is named `Cello.exe`.
2. Run it from a normal writable location such as Downloads, Documents, or Desktop.
3. If startup fails, open `%LOCALAPPDATA%\Cello\logs`.
4. Include `CELLO_BOOTSTRAP_ERROR.txt` and `CELLO_RUNTIME.log` in the report.

## Python runtime or PySide6 startup error

Use `CELLO_RUNTIME.log` as the authoritative traceback.

The repaired single-file line includes the CPython `struct` wrapper required by Shiboken/PySide6 when Cello starts its private Python runtime directly.

## Autosave or project-save permission error

Windows antivirus/indexing can briefly lock a destination while Cello is replacing a small state file. Current rebuilt releases retry the atomic replacement and use a fallback write path if the lock persists.

If the problem continues, include the exact error report from `%LOCALAPPDATA%\Cello\logs`.

## A second copy will not open

This is expected when Cello is already running. The application uses single-instance behavior and activates the existing instance.

## Antivirus or SmartScreen warning

Only use `Cello.exe` obtained from the official Cello release and compare its SHA-256 with the version metadata under `versions/v<version>/SHA256SUMS.txt`.

## Reporting a problem

Include:

- Cello version
- Windows version
- exact reproduction steps
- `%LOCALAPPDATA%\Cello\logs\CELLO_BOOTSTRAP_ERROR.txt`
- `%LOCALAPPDATA%\Cello\logs\CELLO_RUNTIME.log`
- any additional Cello error report generated in the same folder
