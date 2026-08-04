<p align="center">
  <img src="images/logo.svg" width="180" alt="Subtitle Edit Logo">
</p>
# SubtitleEdit AppImage (Portable Linux Build)

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


SubtitleEdit.AppImage.home


This ensures full portability.

---

## ⚙️ Build instructions

### Requirements

- bash
- wget or curl
- tar
- appimagetool (or included in repo)
- Linux x86_64 system

---

### Build

```bash
chmod +x build.sh
./build.sh

This will:

Download Subtitle Edit (official Linux release)
Extract files
Prepare AppDir structure
Build the AppImage

Output:

SubtitleEdit-x86_64.AppImage
📁 Portable mode

When you run the AppImage, it will automatically create:

SubtitleEdit.AppImage.home/
├── .config
├── .cache
└── .local

All settings are stored here instead of your system.

🌐 Language note

If Subtitle Edit does not save language changes from the top menu, use:

Options → Language → Apply → OK

This ensures the setting is saved correctly.

📦 Release

Prebuilt AppImages are available in the Releases section:

👉 https://github.com/rameshyatim/SubtitleEdit-AppImage/releases

⚠️ Notes
This project does NOT redistribute Subtitle Edit binaries in the repository
All binaries are downloaded from official sources during build
This ensures compliance and keeps the repository lightweight
🙌 Credits
Subtitle Edit by its original developers
AppImage tools by the AppImage community
Packaging and automation by this project
📜 License

This packaging script is released under MIT License.
Subtitle Edit itself follows its own upstream license.
Thanks to https://github.com/SubtitleEdit for porting it to Linux. 
