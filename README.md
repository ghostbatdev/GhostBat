# GhostBat Launcher & Patcher

[![Version](https://img.shields.io/badge/version-v1.0.0-blue)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-CC--BY--NC--ND%204.0-lightgrey)](LICENSE.md)
[![Platform](https://img.shields.io/badge/platform-Windows%20x64-blue)](https://github.com/ghostbatdev/GhostBat/releases/download/v1.0.0/GhostBat_Windows-x64_v1.0.0.zip)
[![Guide](https://img.shields.io/badge/guida-Italian%20🇮🇹-green)](GUIDA.md)



**GhostBat** is a portable external launcher and patcher for RetroBat that allows advanced users to dynamically load ROMs, apply temporary patches, and launch systems — all **without modifying RetroBat’s original files**.

> ⚠️ GhostBat is not a replacement for RetroBat. It acts as a bridge, loading temporary content and managing system switching. Core emulation is always handled by RetroBat.

---

## ✨ Features

- Temporary ROM injection from remote links (`.zip`, `.chd`, `.cue`, `.7z`, etc.)
- Support for 200+ tested systems
- CSV editor with multiline entries and duplicate detection
- Automatic smart renaming based on file content
- Per-system or global patching in one click
- Manual CSV backup and restore
- Full cleanup and reversible patches
- USB & external disk compatible
- Optional ROM cache for quick relaunch
- Customizable interface (font size, layout)

---

## 🚀 How It Works

Before launching GhostBat, make sure **RetroBat is properly installed and configured**, including emulators, BIOS files, and system paths.

When GhostBat starts:
1. A **disclaimer prompt** appears — users can choose whether to continue or exit
2. Once accepted, GhostBat **scans local drives** for RetroBat’s root installation
3. If RetroBat is found, the user is asked whether to install the “mod” folder and a temporary ROM directory (`romstemp`)
4. A list of compatible systems is displayed in a **side panel** (DataGrid)
5. Users select systems to patch; GhostBat then temporarily updates `es_systems.cfg` to enable compatibility  
   ⏳ This is the **only file modified** in RetroBat

Once patched:
- Patched systems no longer accept standard ROM files — instead, they rely on **custom placeholder files**
- These files contain a direct download link, inserted by the user via the built-in CSV editor
- Systems not patched will behave as usual with regular ROMs

Using the ROM URL editor:
- Users input game titles and ROM URLs, which are stored in per-system `.csv` files
- These entries can be **injected** into RetroBat’s `roms/` folder
- Injected ROMs appear as playable entries inside RetroBat — even though no physical ROM is present

Behind the scenes:
- Each injected file is a **fake ROM-like placeholder** that contains a link to the real game
- When the user launches the title from RetroBat, GhostBat downloads the ROM temporarily, executes it, then removes it after use
- All injected content is fully reversible and non-destructive

Patch activity is logged inside the `log/` folder for reference and cleanup.

---

## 🧩 About Patched ROM Files

GhostBat does **not** include or download real ROMs into the RetroBat `roms/` folders.

Instead, patched entries create small placeholder files in system folders (e.g. `roms/megadrive/`) which contain direct download links.  
These placeholders simulate ROM presence to RetroBat, allowing launch while GhostBat fetches the actual content separately.

All patches are tracked and removable, preserving RetroBat’s native structure.

---

## 💻 Requirements

- Windows 10 or 11 (64-bit)
- [.NET Desktop Runtime 8.x – Windows x64](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)  
  👉 Be sure to download **“.NET Desktop Runtime (x64)”**, *not the base Runtime or SDK*
- RetroBat installed at the root of a drive (e.g. `C:\RetroBat`)
- Internet access for remote downloads
- Proper BIOS and emulator configuration within RetroBat

---

## 📁 Folder Structure (ZIP Package Contents)

| Path                                | Description |
|-------------------------------------|-------------|
| `GhostBat.exe`                      | Main launcher executable |
| `README_EN.txt`                     | Full documentation (English, offline use) |
| `README_IT.txt`                     | Full documentation (Italian) |
| `LICENSE.txt` / `LICENZA.txt`       | License and legal terms |
| `LICENSE.md`                        | Markdown version of the license |
| `DISCLAIMER.txt` / `note_legali.txt`| Legal disclaimers and usage limitations |
| `csv/`                              | Contains `README_csv.txt` — no pre-filled CSV files are distributed |
| `config/`                           | Contains configuration `.ini` files used by GhostBat |
| `mod/`                              | Contains the full GhostBat launcher and its dependencies — required for proper operation |
| `backup/`                           | Contains `README_backup.txt` — empty folder reserved for optional user-made CSV backups |
| `log/`                              | Runtime-only folder for temporary crash logs — empty on first install |

---

## ❓ Notes

- GhostBat **does not include** any ROMs, BIOS or emulators  
- GhostBat is **not affiliated with RetroBat**  
- No permanent changes are made to RetroBat or the host system  
- Only the `es_systems.cfg` file is temporarily updated to activate systems

---

## 🧾 Package Integrity

The SHA-256 checksum for each GhostBat release is available in the corresponding GitHub Release page and documented in the changelog.  
Always verify the official ZIP hash before trusting any build.

✅ GhostBat never includes ROMs or pre-filled CSVs.  
❌ If you received a version with embedded content or altered behavior, it has been modified and is not officially supported.

---

## ⚠️ Security Notice – Antivirus False Positives

GhostBat is **closed-source software**, and the ZIP package includes compiled executable files and libraries only.

Because the executables are **not digitally signed**, some antivirus programs — especially *Windows Defender* — may falsely flag GhostBat as a threat (e.g. `Sabsik.FL.A!ml`).  
This is a **false positive**, triggered by automatic heuristic scans — not due to actual malicious behavior.

GhostBat:

- ✅ Does not modify the Windows registry  
- ✅ Does not communicate with external servers  
- ✅ Does not install hidden services  
- ✅ Performs only local, reversible operations under user control

🛡️ The software is safe if downloaded from the [official GitHub release page](https://github.com/ghostbatdev/GhostBat/releases)

### 🔧 Recommended Exclusions

To ensure proper functionality and avoid false detections, we recommend manually excluding:

- The **main folder** where the ZIP contents were extracted (includes files such as `GhostBat.exe`, `GhostBat.dll`, etc.)
- The **`mod/` folder** generated inside **RetroBat**, if you choose to apply the mod (this folder is copied after user confirmation)

These folders contain executables and linked libraries that may be flagged by antivirus heuristics.  
Excluding the full folder ensures stable operation and prevents automatic quarantine or deletion.

---

## 🔐 License

GhostBat is licensed under [Creative Commons BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)  
✅ Free for personal and non-commercial use only  
❌ Commercial redistribution, modification, or bundling are prohibited  
📄 Full license terms available in [`LICENSE.md`](LICENSE.md)

---

## 🧩 Third-Party Notice

GhostBat includes one external component to support archive management:

- **Squid-Box.SevenZipSharp**  
  - **Description**: .NET wrapper for the 7-Zip library (`7z.dll`)  
  - **Purpose**: Used exclusively to extract compressed archive files inside the GhostBat launcher  
  - **License**: MIT License  
  - **Repository**: [https://github.com/adamhathcock/sevenzipsharp](https://github.com/adamhathcock/sevenzipsharp)

All rights belong to their respective authors.  
For the full license text, see the file `LICENSE-SevenZipSharp.txt` included in this package.

> This notice is provided to comply with third-party license terms and attribution requirements.

---

## 🌍 Languages

The main documentation is provided in English.  
An Italian version (`README_IT.txt`) is included inside the program ZIP.

---

## 🚀 GhostBat Release Info

📦 Download the latest version from the [GitHub Releases page](https://github.com/ghostbatdev/GhostBat/releases)  
📄 Full changelog: [`CHANGELOG.md`](CHANGELOG.md)  
🔐 License terms: [`LICENSE.md`](LICENSE.md)  
📘 User guide: [`GUIDA.md`](GUIDA.md) 🇮🇹 / [`GUIDE.md`](GUIDE.md) 🇬🇧


---
