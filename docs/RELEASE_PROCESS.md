# Release process

## 1. Update metadata

Update:

- `VERSION`
- `CHANGELOG.md`
- `README.md`
- `INSTALL.md`
- `CITATION.cff`
- `versions/v<version>/`

## 2. Build

Produce one Windows x64 executable named:

```text
Cello.exe
```

The release executable must contain the Cello icon resources and a checksum-protected embedded application payload. The payload must contain the intended version's current source/runtime/assets and must not depend on a companion folder beside the executable.

## 3. Validate

Required build-time checks:

- PE32+ x86-64 GUI structure
- Cello icon resource directory present
- embedded payload marker present
- embedded payload SHA-256 matches the footer
- embedded payload ZIP CRC passes
- bundled `python312.dll` present
- `src/cello_p10/entry.py` present
- intended `VERSION` and release metadata present
- Python source compilation passes
- version-specific regression/smoke checks pass

Required host-level check before declaring a release verified:

- launch `Cello.exe` on a clean supported Windows x64 host
- confirm main UI reaches ready state
- confirm simulation worker starts
- exercise the release's headline feature
- close and relaunch from the cached runtime
- inspect `%LOCALAPPDATA%\Cello\logs` for unexpected errors

## 4. Generate checksum

```powershell
Get-FileHash .\Cello.exe -Algorithm SHA256
```

Record the exact hash in the version metadata and GitHub Release notes.

## 5. Commit and tag

Commit metadata changes, tag `v<version>`, and push the tag only after the intended release state is frozen.

## 6. Publish GitHub Release

Create the release for tag `v<version>` and attach exactly the intended Windows asset:

```text
Cello.exe
```

Publish the SHA-256 in the release notes.

## 7. Post-publication verification

Download `Cello.exe` from the published GitHub Release, recompute SHA-256, and perform the native Windows smoke launch on the downloaded bytes rather than only on a local pre-upload copy.
