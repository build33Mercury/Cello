# Troubleshooting

## The application does not start

Current Windows releases are distributed as a single file named `Cello.exe`.

1. Confirm that the file is named `Cello.exe`.
2. Run it from a normal writable location such as Downloads, Documents, or Desktop.
3. Do not place it inside a ZIP archive or run it from an archive preview.
4. If startup fails, open:

   `%LOCALAPPDATA%\Cello\logs`

5. Include `CELLO_BOOTSTRAP_ERROR.txt` and `CELLO_RUNTIME.log` when reporting the problem.

Cello prepares a private versioned runtime under `%LOCALAPPDATA%\Cello\runtime`. A corrected release uses a different payload hash and therefore prepares a fresh runtime automatically.

## Python runtime or PySide6 startup error

If the diagnostic reports a Python exception, use `CELLO_RUNTIME.log` as the authoritative traceback. The single-file v1.1.0–v1.6.0 repair dated 2026-09-18 restores the CPython `struct` wrapper required by Shiboken/PySide6 startup.

## The first launch is slow

The first launch verifies and prepares the private runtime, then initializes the model, viewport, simulation worker, and initial state. Later launches can reuse the versioned runtime cache.

## A second copy will not open

Cello uses single-instance behavior. When an existing instance is active, a second launch may activate the existing application instead of starting another simulator.

## The interface does not fit

Cello is designed to adapt from 1024×680 upward. Confirm that Windows display scaling and resolution provide at least that usable area.

## Antivirus or SmartScreen warning

Only use `Cello.exe` obtained from the official Cello release. Verify its SHA-256 against the metadata for that version before running it. Independently distributed executables may not yet have Windows reputation-based signing recognition.

## Reporting a problem

Use the GitHub bug-report template and include the Cello version, Windows version, exact reproduction steps, and sanitized copies of:

- `%LOCALAPPDATA%\Cello\logs\CELLO_BOOTSTRAP_ERROR.txt`
- `%LOCALAPPDATA%\Cello\logs\CELLO_RUNTIME.log`
- any Cello error report generated alongside those logs
