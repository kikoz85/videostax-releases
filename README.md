<h1 align="left" style="border: none; padding: 0; margin: 0 0 16px 0;">
  <table style="border-collapse: collapse; border: none;">
    <tr>
      <td style="border: none; vertical-align: middle; padding: 0 18px 0 0; line-height: 0;">
        <img src="assets/logo.svg" alt="VideoSTAX logo" height="32" width="45" style="display: block;" />
      </td>
      <td style="border: none; vertical-align: middle; padding: 0; font-weight: 600; line-height: 1.25;">
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

**Current channel:** macOS **arm64** DMG (`VideoSTAX-v0.7.2-macOS.dmg` and newer). Linux and Windows packages appear on this page as they are published.

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

## 📄 Legal & third-party software

Bundled and invoked components (FFmpeg, MKVToolNix, VapourSynth, Flutter, Go, optional Rigaya encoders, etc.) are subject to their upstream licenses.

See **[THIRD_PARTY_LICENSES.md](THIRD_PARTY_LICENSES.md)** in this repository.

---

## ✉️ Contact

**Enrico Fanucchi** — [enricofanucchi@gmail.com](mailto:enricofanucchi@gmail.com) · [www.enricofanucchi.com](https://www.enricofanucchi.com)
