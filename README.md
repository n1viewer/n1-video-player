# N1 Video Player — third-party sources

This repository is the release archive for the open-source components distributed with N1 Video Player for Windows, including the modified VLC runtime. The application itself is proprietary. Each third-party component retains its own license.

## Find sources for a build

1. Open `licenses/N1_SOURCE_REFERENCE.txt` in the installed package and copy the **Runtime ID**.
2. Open [Releases](https://github.com/n1viewer/n1-video-player/releases) and find the release that lists that Runtime ID. The application version can be shared by builds with different runtimes.
3. Under **Assets**, download `N1VP-third-party-source-<Runtime ID>.zip` and its matching `.zip.sha256` file. GitHub’s automatic “Source code” links contain the repository README. The named asset contains the library sources.

To verify a download in PowerShell, run `Get-FileHash -Algorithm SHA256` followed by the archive path and compare the result with the digest in the checksum file. License notices and build information accompany each published source bundle.

[Project website](https://n1viewer.com/video-player/) · [Third-party notices](https://n1viewer.com/video-player/licenses/)
