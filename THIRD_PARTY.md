# Third-party software and licensing terms

N1 Video Player for Windows is independently developed by N1 Viewer. The proprietary application is not offered under an open-source license merely because this repository hosts its third-party source materials.

## Open-source components

The player uses the VideoLAN libVLC engine, including modified VLC modules, and FFmpeg and additional third-party libraries. The current development baseline uses VLC 4 at upstream revision `623d7b909226a79d09cb57cf9cec1026d75e6df5`. This is an upstream reference, not a substitute for the exact modified source corresponding to a distributed binary.

- VLC: [upstream project](https://code.videolan.org/videolan/vlc), [libVLC documentation](https://videolan.videolan.me/vlc/).
- FFmpeg: [upstream project](https://ffmpeg.org/), [licensing information](https://ffmpeg.org/legal.html).
- [GNU LGPL 2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html) and [GNU GPL 2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html): consult the individual source file headers and corresponding release notices for applicability. The full upstream source tree can contain code not distributed in the player runtime.

The unmodified VLC license and attribution texts from the pinned upstream revision are available here: [LGPL 2.1](licenses/vlc/COPYING.LIB), [GPL 2](licenses/vlc/COPYING) and [AUTHORS](licenses/vlc/AUTHORS). They do not constitute the complete release-specific set of notices for every dependency.

The exact component inventory, applicable licenses, copyright notices, dependency versions, patches and build settings are specific to each runtime. Release-specific materials accompany the matching source archive. The installed package also contains the applicable notices in its `licenses` directory. A general upstream link alone is not the complete corresponding source.

## User rights

Nothing in the N1 Video Player terms restricts the rights granted by the applicable third-party licenses, including the right to modify LGPL-covered libraries, use compatible modified versions for personal purposes, and reverse engineer the application as necessary to debug such modifications.

N1's contributions to the modified LGPL-covered VLC library, including helper code incorporated into that library, are offered under LGPL-2.1-or-later. Other third-party source files retain their own licenses and copyright notices.

The Windows Store installation is managed by Windows. Do not change the protected WindowsApps directory or disable integrity protections. Follow the release-specific build and local package instructions for compatible modified libraries. Those instructions must correspond to the actual release.

## Source materials

See [SOURCE_DOWNLOADS.md](SOURCE_DOWNLOADS.md) and the [Releases page](https://github.com/n1viewer/n1-video-player/releases). The [2.14.79 third-party source release](https://github.com/n1viewer/n1-video-player/releases/tag/runtime-1a33f61934fb074e6903ad36) is published. Its archive and checksum are available in Releases.

VLC, libVLC and FFmpeg are third-party projects. N1 Video Player is independently developed and is not endorsed by VideoLAN or the FFmpeg project.

Official website: https://n1viewer.com/video-player/licenses/
