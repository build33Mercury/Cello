# Release process

## 1. Update release metadata

Before publishing a Cello version, update:

- `VERSION`
- `README.md`
- `CHANGELOG.md`
- `INSTALL.md`
- `CITATION.cff`
- `versions/README.md`
- `versions/v<version>/`

## 2. Build and validate

Produce a professional portable Windows x64 package containing the exact launcher:

```text
Run_Simulator.cello.exe
```

The standard release filename is:

```text
Cello_<version>_Windows_x64_Portable.zip
```

At minimum, validate source compilation, automated tests, package integrity, launcher architecture, bundled runtime presence, release metadata, and checksums. A final native Windows GUI smoke launch should be completed on a Windows x64 host.

## 3. Generate checksums

```powershell
Get-FileHash .\Cello_<version>_Windows_x64_Portable.zip -Algorithm SHA256
```

Record release hashes in:

```text
versions/v<version>/SHA256SUMS.txt
```

## 4. Commit and tag

```bash
git add .
git commit -m "Release Cello v<version>"
git tag -a v<version> -m "Cello v<version>"
git push origin main
git push origin v<version>
```

## 5. Create the GitHub Release

1. Open **Releases**.
2. Draft a new release.
3. Select or create tag `v<version>`.
4. Use title `Cello v<version> - Windows x64 Portable`.
5. Add the prepared release notes.
6. Attach the portable ZIP and checksum file.
7. Publish as the current release when validation is complete.

## 6. Post-publication verification

- Download the release asset from GitHub.
- Recompute SHA-256 and compare with the repository metadata.
- Extract the full package.
- Confirm `Run_Simulator.cello.exe` launches successfully on Windows x64.
- Confirm the new application icon and UI branding are present.
- Confirm the README and install instructions point to the current version.
- Confirm the release is marked latest when intended.

## v1.1.0 prepared checksums

```text
ZIP:      b636317b71a53dcec70cb7a127146a5f16c35ec6b4d8aad58b961afe236ba175
Launcher: f4093b1be2d2c85e935b5447dab8a49b0b8d7c33211715a7f388b21236a85339
```
