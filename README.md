 SubtitleEdit AppImage (Portable Linux Build)

This project provides a **portable AppImage packaging system** for Subtitle Edit on Linux.

It does NOT modify system files and keeps all user configuration inside a portable directory.

---

## 🚀 Features

- Portable execution (no installation required)
- Fully self-contained AppImage
- Uses `SubtitleEdit.AppImage.home` for isolated configuration
- Does not pollute `~/.config` or system directories
- Easy rebuild with a single script
- Based on official Subtitle Edit Linux release

---

## 📦 How it works

Subtitle Edit is downloaded from the official release tarball:

- `SubtitleEdit-Linux-x64.tar.gz`

Then it is packaged into an AppImage using `appimagetool`.

All configuration is redirected to:
