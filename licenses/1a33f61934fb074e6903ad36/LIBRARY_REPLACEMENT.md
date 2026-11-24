# Using modified third-party libraries — N1 Video Player 2.14.79

Runtime ID: `1a33f61934fb074e6903ad36`. These instructions supplement BUILD_AND_REPLACE.md in the published [source archive](https://github.com/n1viewer/n1-video-player/releases/tag/runtime-1a33f61934fb074e6903ad36).

## Rights and ordinary Windows installation

You may modify the LGPL-covered components, use ABI-compatible modified versions, and reverse engineer the application as necessary to debug your modifications. This permission overrides conflicting proprietary terms. No developer permission, account or N1 signing key is required for ordinary DLL replacement.

Use the standalone installer for version 2.14.79 from the [official website](https://n1viewer.com/video-player/), once available. The corrected standalone and Store installations have the same 362 third-party binaries and the same source reference. Verify the runtime ID in `licenses/N1_SOURCE_REFERENCE.txt`.

1. Close N1 Video Player completely.
2. Keep a backup of the installed application directory, normally `C:\Program Files\N1 Video Player`.
3. Build compatible x64 VLC libraries from the matching modified source tree, build scripts, dependency sources and configuration in the source archive. For a modified statically linked dependency, rebuild the containing VLC plugin or library from the matching sources; replacing an unrelated standalone DLL is not sufficient.
4. Replace the corresponding `libvlc.dll`, `libvlccore.dll` or plugin DLL in its existing relative path under `plugins\`. Administrator permission may be needed for Program Files. Use compatible exports and ABI. Rebuild a consistent set of dependent DLLs if necessary. Recreate the plugin cache using the matching build's vlc-cache-gen.
5. Start the application normally. Restore the backed-up files if you wish to return to the distributed runtime.

Source inspection shows that VlcBackend::configureVlcRuntime adds the executable's directory and plugins directory to the DLL search path and sets VLC_PLUGIN_PATH. Runtime hash checks gate specific patched video enhancement paths, not the general LGPL library replacement permission. Modified builds can lose access to particular patch-dependent RTX enhancements, even when ordinary playback can initialize. Do not falsify the capability markers.

## Microsoft Store installation

Windows manages the installed MSIX files and protects package integrity. Do not edit WindowsApps in place. For a modified local MSIX, obtain the matching original package from a lawful accessible source or contact the publisher using the official website or repository issue tracker if the original package cannot be obtained. Unpack it using MakeAppx, perform the same DLL/plugin replacements, regenerate the plugin cache and prepare a separate local package identity and matching publisher. Regenerate resources.pri if the identity changes. Repack and sign using your own trusted local signing certificate; install the separate local package. No N1 private signing key is required for the separate local identity. The standalone edition is an additional route using the same runtime, not proof that the Store package can be replaced in place.

Microsoft documentation: [MakeAppx](https://learn.microsoft.com/windows/msix/package/create-app-package-with-makeappx-tool), [SignTool](https://learn.microsoft.com/windows/msix/package/sign-app-package-using-signtool).

## Scope

These are source-inspected instructions, not a record of a successful Windows replacement test. The ordinary installed binary inventory has been compared with the Store inventory. The repackaged MSIX procedure has not been executed with modified libraries. Compatibility of an arbitrary changed library is not guaranteed. The right to modify and use compatible libraries is not conditional on sending a test report to the publisher.
