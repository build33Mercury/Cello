# Troubleshooting

## The application does not start

- Confirm that the ZIP was fully extracted.
- Confirm that `Run_Simulator.cello.exe` remains beside `_cello_runtime`.
- Do not run the executable from inside the ZIP preview.
- Move the extracted folder to a normal writable location such as Documents or Desktop.
- Restart Windows and try again.

## Windows says a file is missing

The portable package is incomplete or the executable was moved. Re-extract the original release ZIP and preserve the folder structure.

## The first launch is slow

The first launch initializes the model, viewport, simulation worker, state, and warm-start cache. Later launches should normally be faster.

## A second copy will not open

This is expected. Cello uses single-instance behavior and should activate the existing window rather than start a second simulator and worker process.

## The interface does not fit

Cello is designed to adapt from 1024×680 upward. Confirm that Windows display scaling and resolution provide at least that usable area.

## Antivirus or SmartScreen warning

Verify that the file came from the official GitHub Release and compare its SHA-256 checksum with `versions/v1.0.1/SHA256SUMS.txt`. Do not run a differently named or mismatched file.

## Reporting a problem

Use the GitHub bug-report template and include the Cello version, Windows version, exact reproduction steps, and sanitized screenshots or logs.
