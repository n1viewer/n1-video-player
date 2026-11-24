# N1 Video Player — Free Windows Video Player with RTX VSR & RTX HDR

**Give old movies new life.** Rediscover a favorite DVD rip on a larger screen, watch a film in HDR, or pick up an episode where you left off. N1 Video Player plays local video on Windows x64. It’s free, with no ads, subscriptions, paid features, or account requirement.

[Official website](https://n1viewer.com/video-player/) · [Releases](https://github.com/n1viewer/n1-video-player/releases) · [Report an issue](https://github.com/n1viewer/n1-video-player/issues)

## Picture quality

- **NVIDIA RTX Video Super Resolution (VSR)** sharpens upscaled video and reduces visible compression artifacts. It’s especially useful when a lower-resolution movie fills a larger screen.
- **NVIDIA RTX Video HDR** converts SDR video to HDR for richer highlights, contrast, and color on an HDR display. VSR and RTX HDR have separate switches, so you can use either enhancement on its own or enable both.
- **10-bit HDR playback** supports HDR10 (PQ) and HLG video. The player uses hardware-accelerated Direct3D 11 rendering and DirectComposition.
- **GPU selection** lets you choose your discrete or integrated GPU and see which device is active.

RTX Video enhancements require a compatible NVIDIA RTX GPU and supported drivers.

## Your video library

Open **Library** to continue an unfinished movie from its saved position, revisit your watch history, or browse recently added and previously discovered videos. Mark favorite films, episodes, and clips for quick access. To browse by location, use the integrated folder explorer and thumbnail **Gallery**.

## Playback controls

- Choose a borderless **Modern** window or a **Classic** window with a standard frame. Fullscreen controls hide automatically.
- Use **Fit** to see the whole frame or **Fill** to crop the edges and fill the screen.
- Switch audio and subtitle tracks or open an external subtitle file. Audio details include codec, channel count, sample rate, and bitrate when the file provides them.
- Press **Space** to play or pause, **F** for fullscreen, or **← / →** to seek back or forward 30 seconds. Standard media keys are also supported.

## Media compatibility

**25 recognized video file extensions**

MP4, MKV, MOV, AVI, WEBM, M4V, WMV, TS, MTS, M2TS, M2T, MXF, 3GP, 3G2, MPG, MPEG, MPE, MPV, M2V, VOB, ASF, DIVX, FLV, F4V, OGV.

**Audio tracks in video files**

AAC, MP3, MPEG Audio, Vorbis, Opus, WMA, Dolby Digital (AC-3), Dolby Digital Plus (E-AC-3), DTS, Dolby TrueHD, FLAC, ALAC, and PCM. Playback depends on the codecs inside each file.

## Bug reports and feature requests

For playback issues, include the player version, Windows version, GPU, and steps to reproduce. For RTX or HDR issues, also mention your display and which enhancements were enabled. [Open a GitHub issue](https://github.com/n1viewer/n1-video-player/issues)

## Third-party sources and licenses

N1 Video Player is proprietary. This repository also hosts release-specific source bundles for its open-source components, including the modified VLC runtime. Each component retains its own license.

1. Find the **Runtime ID** in `licenses/N1_SOURCE_REFERENCE.txt` in the installed package. Builds with the same application version can use different runtimes.
2. Find the matching Runtime ID in [Releases](https://github.com/n1viewer/n1-video-player/releases).
3. Under **Assets**, download `N1VP-third-party-source-<Runtime ID>.zip` and its matching `.zip.sha256` file. The named ZIP contains the library sources. GitHub’s automatic **Source code** downloads contain the files tracked in this repository.

To verify a download in PowerShell, run `Get-FileHash -Algorithm SHA256` followed by the archive path and compare the result with the digest in the checksum file. License notices and build information accompany each published source bundle. [Third-party notices](https://n1viewer.com/video-player/licenses/)
