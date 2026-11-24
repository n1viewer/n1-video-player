# Corresponding source downloads

This repository hosts release-specific source materials for the third-party runtime of N1 Video Player. The application itself is distributed separately from these source materials.

**Current status:** the [2.14.79 third-party source bundle](https://github.com/n1viewer/n1-video-player/releases/tag/runtime-1a33f61934fb074e6903ad36) is published. The runtime inventory matches the tested Store package and the corrected standalone installation.

## Find the correct archive

1. Locate `licenses/N1_SOURCE_REFERENCE.txt` in the installed application package. It identifies the VLC revision, Runtime ID, archive name, SHA-256 and official download page.
2. Find the matching Runtime ID in [GitHub Releases](https://github.com/n1viewer/n1-video-player/releases). The application version alone may not uniquely identify a runtime.
3. Download the named asset `N1VP-third-party-source-<Runtime ID>.zip` and its companion `.zip.sha256` file. GitHub's automatically generated **Source code (zip)** and **Source code (tar.gz)** archives of this repository are not the corresponding library source bundle.
4. Verify the SHA-256 before extracting the archive. In PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\N1VP-third-party-source-<Runtime ID>.zip'
```

Compare the result with the digest in the companion checksum file and the installed source reference. Replace the placeholder with the actual runtime ID.

## What to look for in the archive

The source bundle is intended to include the exact modified VLC source, corresponding dependency sources, applicable license and copyright notices, build recipes and configuration, a runtime inventory, and release-specific build and library-replacement instructions. Read `SOURCE_EXPORT_REPORT.json` and the included build and replacement instructions inside the archive. The proprietary N1 application source is not part of these materials.

If an archive needs to be split to fit hosting limits, the release must provide every part, a reconstruction procedure, and the checksum of the reconstructed original archive.

## Release index

| Application version | Runtime ID | Source archive | Status |
| --- | --- | --- | --- |
| 2.14.79 | `1a33f61934fb074e6903ad36` | [ZIP](https://github.com/n1viewer/n1-video-player/releases/download/runtime-1a33f61934fb074e6903ad36/N1VP-third-party-source-1a33f61934fb074e6903ad36.zip) · [SHA-256](https://github.com/n1viewer/n1-video-player/releases/download/runtime-1a33f61934fb074e6903ad36/N1VP-third-party-source-1a33f61934fb074e6903ad36.zip.sha256) | Published |

Archive size: 990,915,558 bytes.

SHA-256: `7d7bd15d73afc085f50b2e6410837c3773b02061391bc0987bb377b48c49633d`.

The source export report describes its scope and limitations. Publication and binary hash matching do not by themselves establish complete license compliance.

Official license page: https://n1viewer.com/video-player/licenses/

[Third-party software and licensing terms](THIRD_PARTY.md)
