# Third-Party Open Source Licenses

VideoSTAX macOS release bundles or invokes the following third-party software.  
This document summarizes licensing for compliance and attribution. Full license texts are available from each upstream project.

---

## FFmpeg & FFprobe

- **Project:** [FFmpeg](https://ffmpeg.org/)
- **Use in VideoSTAX:** Transcoding, probing, remux (MP4/MOV/WebM), filters, VAAPI-related paths on supported platforms.
- **License:** FFmpeg is licensed under the **GNU Lesser General Public License (LGPL) version 2.1 or later**, and some optional components may be under **GPL**. Static builds distributed with VideoSTAX are built to comply with the license terms of the build used; source code and build instructions for corresponding FFmpeg versions are available from [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html).
- **Notice:** If you modify FFmpeg-linked binaries, you must comply with LGPL/GPL source-offer requirements.

---

## MKVToolNix (mkvmerge)

- **Project:** [MKVToolNix](https://mkvtoolnix.download/)
- **Use in VideoSTAX:** Multiplexing MKV outputs (chapters, sync, audio/video temp files).
- **License:** **GNU General Public License (GPL) version 2 or later.**
- **Source:** [https://gitlab.com/mbunkus/mkvtoolnix](https://gitlab.com/mbunkus/mkvtoolnix)

---

## Rigaya hardware encoders (QSVEncC, NVEncC, VCEEncC)

- **Projects:** [QSVEnc](https://github.com/rigaya/QSVEnc), [NVEnc](https://github.com/rigaya/NVEnc), [VCEEncC](https://github.com/rigaya/VCEEncC) (Rigaya)
- **Use in VideoSTAX:** Optional native hardware encoding on Windows and Linux when binaries are present and detected by the engine.
- **License:** Typically **MIT License** (verify per release tarball/binary you ship). See each repository’s `LICENSE` file for the exact text bundled with that version.
- **Note:** macOS builds in this release channel rely primarily on **VideoToolbox** via FFmpeg; Rigaya tools are not bundled in the standard macOS DMG unless explicitly stated in release notes.

---

## VapourSynth & related plugins

- **VapourSynth:** [https://www.vapoursynth.com/](https://www.vapoursynth.com/) — **LGPL 2.1+** (core).
- **Bundled plugins** (when present in a build, e.g. ffms2, MVTools, DFTTest, znedi3, havsfunc): each plugin carries its own license (commonly GPL/LGPL/MIT). Refer to the plugin source repositories shipped with or documented in the build script for that release.

---

## Flutter & Dart SDK

- **Project:** [Flutter](https://flutter.dev/)
- **Use in VideoSTAX:** Desktop UI (macOS, Windows, Linux).
- **License:** Flutter framework and Dart SDK components are distributed under **BSD-style licenses** (see [https://github.com/flutter/flutter/blob/master/LICENSE](https://github.com/flutter/flutter/blob/master/LICENSE) and `flutter/packages/flutter/LICENSE`).
- **Dependencies:** Additional packages in `pubspec.yaml` (e.g. Riverpod, easy_localization) have their own licenses in the Pub package cache or on [pub.dev](https://pub.dev).

---

## Go toolchain & VideoSTAX engine

- **Go:** [https://go.dev/](https://go.dev/) — **BSD 3-Clause License** ([https://go.dev/LICENSE](https://go.dev/LICENSE)).
- **VideoSTAX engine:** Proprietary application code © Enrico Fanucchi; it **links to and invokes** the third-party tools above at runtime. Engine source is maintained in the private VideoSTAX repository unless otherwise published.

---

## Trademarks

FFmpeg, MKVToolNix, Flutter, Go, Intel Quick Sync, NVIDIA, AMD, and other names are trademarks of their respective owners. VideoSTAX is not affiliated with or endorsed by those parties.

---

## Contact

For licensing questions regarding VideoSTAX releases: **Enrico Fanucchi** — [enricofanucchi@gmail.com](mailto:enricofanucchi@gmail.com)
