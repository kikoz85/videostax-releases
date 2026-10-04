<h1 style="border: none; margin: 0 0 16px 0; padding: 0;">
  <table border="0" cellspacing="0" cellpadding="0" role="presentation" style="border: none; border-collapse: collapse; border-spacing: 0;">
    <tr>
      <td style="border: none; vertical-align: middle; padding: 0 18px 0 0; line-height: 1;">
        <img src="assets/logo.svg" alt="VideoSTAX logo" width="44" height="34" style="display: block; border: none;" />
      </td>
      <td style="border: none; vertical-align: middle; padding: 0;">
        VideoSTAX — Releases &amp; Downloads
      </td>
    </tr>
  </table>
</h1>

[![Latest Release](https://img.shields.io/github/v/release/kikoz85/videostax-releases?style=flat-square&color=2b6cb0)](https://github.com/kikoz85/videostax-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/kikoz85/videostax-releases/total?style=flat-square&color=38a169)](https://github.com/kikoz85/videostax-releases/releases)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux%20%7C%20Windows-gray?style=flat-square)](#download-links)

Welcome to the official binary distribution repository for **VideoSTAX** — the high-performance cross-platform video encoding and batch processing studio.

Source code is maintained in a separate private repository; **this repo publishes only release binaries and compliance documentation.**

---

## 🚀 Download Links

Get the latest stable build for your operating system:

| Platform | Recommended Package | Direct Link |
| :--- | :--- | :--- |
| **macOS** *(Apple Silicon)* | `.dmg` installer | [📥 Download macOS build](https://github.com/kikoz85/videostax-releases/releases/latest) |
| **Linux** *(x86_64)* | `.AppImage` (portable) | [📥 Download Linux build](https://github.com/kikoz85/videostax-releases/releases/latest) |
| **Windows** *(64-bit)* | `.exe` / `.zip` archive | [📥 Download Windows build](https://github.com/kikoz85/videostax-releases/releases/latest) |

> 📌 **Looking for all releases?** View the full version history on the [GitHub Releases page](https://github.com/kikoz85/videostax-releases/releases).

**Latest v0.8.1 assets:** macOS `.dmg` (Apple Silicon, Native VT + **libswscale**, Apple AAC diagnostics, source channel layout) — [release page](https://github.com/kikoz85/videostax-releases/releases/tag/v0.8.1). Re-download if you installed an earlier 0.8.1 DMG. Linux AppImage and Windows zip for **v0.8.1** when built from `main`; older tags retain prior platform builds.

---

## 📋 System requirements

Requirements below describe what each **client build** expects on your machine. Optional items unlock hardware encoders or VapourSynth filters bundled with that release.

### macOS

| | Minimum | Recommended |
| :--- | :--- | :--- |
| **OS** | macOS 12 Monterey (Apple Silicon) | macOS 13 Ventura or later |
| **CPU** | Apple **M1** (arm64) | M2 / M3 / M4 series |
| **RAM** | 8 GB | 16 GB or more for VapourSynth + parallel jobs |
| **Disk** | ~500 MB for the app bundle | Fast SSD; free space ≥ 3× output size for temp mux/encode |
| **Display** | 1280×800 | 1920×1080 or higher |
| **GPU / encode** | VideoToolbox (built into Apple Silicon) | Same; no discrete GPU required |

**Notes:** Current public DMG builds are **arm64 only** (not Intel Mac). The `.app` ships **ffmpeg**, **ffprobe**, **mkvmerge**, **vspipe**, a bundled **VapourSynth** Python tree, and (v0.8+) optional **FFmpeg LGPL** libraries for the experimental **Native VideoToolbox** path (off by default in Settings → Performance)—no separate Homebrew install required for a standard release.

### Linux

| | Minimum | Recommended |
| :--- | :--- | :--- |
| **OS** | Recent **glibc** 64-bit distro (e.g. Ubuntu 22.04, Fedora 38+) | Ubuntu 24.04 LTS or equivalent |
| **CPU** | x86_64, 4 cores | 8+ cores for parallel queue |
| **RAM** | 8 GB | 16 GB+ with VapourSynth scripts |
| **Disk** | ~400 MB for portable bundle / AppImage | SSD; ample temp space for phased mux |
| **Display** | X11 or Wayland, 1280×800 | 1920×1080 |
| **GPU (optional)** | Intel/AMD/NVIDIA with working **VAAPI** (`/dev/dri/renderD*`) | Same + recent drivers for **QSVEncC** / **NVEncC** / **VCEEncC** when shipped in the build |

**Notes:** Release bundles expect **`LD_LIBRARY_PATH`** layout documented in release notes (engine + `bin/lib`). Flatpak/AppImage builds are self-contained when provided. Root is **not** required.

### Windows

| | Minimum | Recommended |
| :--- | :--- | :--- |
| **OS** | Windows 10 **64-bit** (21H2+) | Windows 11 64-bit |
| **CPU** | x64, 4 cores | 8+ cores |
| **RAM** | 8 GB | 16 GB+ |
| **Disk** | ~600 MB installed | SSD; temp space for intermediate video/audio files |
| **Display** | 1280×800 | 1920×1080 |
| **GPU (optional)** | Intel **QSV**, NVIDIA **NVENC**, or AMD **VCE/AMF** (driver-dependent) | Dedicated GPU with latest vendor drivers for **QSVEncC**, **NVEncC**, **VCEEncC** |

**Notes:** Keep the **`bin`** folder next to the UI executable (same layout as the release `.zip`). **Microsoft Visual C++** redistributables used by Flutter are included or installed by the setup when an installer is provided. Enable **Developer Mode** only for building from source, not for end-user installs.

---

## 🛠️ Installation & First Launch Notes

### macOS

1. Open the downloaded `.dmg` and drag **VideoSTAX** into **Applications**.
2. If macOS blocks launch because the app is from an unidentified developer:
   - Open **System Settings** → **Privacy & Security**.
   - In **Security**, click **Open Anyway** next to VideoSTAX, then confirm.

The bundle includes the VideoSTAX engine and tools (ffmpeg, ffprobe, mkvmerge, VapourSynth) under the app’s `Contents` layout.

### Linux

When an AppImage is provided for a release:

```bash
chmod +x VideoSTAX-*.AppImage
./VideoSTAX-*.AppImage
```

Ensure `ffmpeg`, `mkvmerge`, and optional VapourSynth plugins match the release notes for that version.

### Windows

When an installer or `.zip` is provided:

1. Extract or run the installer from the release asset.
2. Keep the `bin` folder next to the UI executable so the bundled **videostax** engine and tools resolve correctly.
3. Allow the app through Windows Defender / SmartScreen if prompted (unsigned or new publisher builds).

---

## 💖 Support the Project

VideoSTAX is independently developed and maintained. If you find the app helpful for your video encoding workflows and want to support ongoing development, optimizations, and new features, consider becoming a sponsor:

👉 **[Sponsor VideoSTAX on GitHub](https://github.com/sponsors/kikoz85)**

Your support helps keep the project active and continuously evolving!

---

## 📄 Legal & third-party software

Bundled and invoked components (FFmpeg, MKVToolNix, VapourSynth, Flutter, Go, optional Rigaya encoders, etc.) are subject to their upstream licenses.

See **[THIRD_PARTY_LICENSES.md](THIRD_PARTY_LICENSES.md)** in this repository.

---

## ✉️ Contact

**Enrico Fanucchi** — [enricofanucchi@gmail.com](mailto:enricofanucchi@gmail.com) · [www.enricofanucchi.com](https://www.enricofanucchi.com)
