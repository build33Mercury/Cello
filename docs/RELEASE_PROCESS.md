# Release process

## 1. Update metadata

Update these files to the new version:

- `VERSION`
- `CHANGELOG.md`
- `README.md`
- `CITATION.cff`
- `versions/v<version>/`
- `SECURITY.md`

## 2. Build and test

Produce the portable Windows ZIP and test it on a clean Windows x64 environment.

Required filename pattern:

```text
Cello_<version>_Portable_Windows_x64.zip
```

## 3. Generate checksums

```powershell
Get-FileHash .\Cello_<version>_Portable_Windows_x64.zip -Algorithm SHA256
```

Record the result in:

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

## 5. Create GitHub Release

1. Open **Releases**.
2. Choose **Draft a new release**.
3. Select or create tag `v<version>`.
4. Use title `Cello v<version>`.
5. Paste the prepared release notes.
6. Attach the portable ZIP and checksum file.
7. Mark as a pre-release only when the build is not the current stable demo.
8. Publish.

## 6. Verify

- Download the release asset from GitHub.
- Recompute its SHA-256.
- Confirm the executable launches after extraction.
- Confirm the README latest-release link resolves.
- Confirm the release is listed as latest when intended.

## v1.0.1 official checksum

```text
9f5bef711a02418ea6b2e15016d4dd065ada45e59848cfbeb2e127ab95ea71d3
```
