# 📓 GhostBat — Changelog

All official changes to the **GhostBat** project are documented in this file, starting from the initial release `v1.0.0`.

---

## [v1.0.0] — 2025-07-11

🎉 **Initial Public Release**

### ✅ Added  
- Initial release of the **GhostBat** launcher  
- Compatibility with over 200 tested RetroBat systems  
- Advanced CSV editor with multiline handling and duplicate detection  
- Reversible patching mechanism with temporary ROM links  
- Execution of remote content via URL (`.zip`, `.chd`, `.cue`)  
- Full support for external USB drives  
- Documentation and legal texts included in the ZIP package (`README_IT`, `README_EN`, license and disclaimer files)  
  → Main license: [Creative Commons BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)  
- Archive `GhostBat_Windows-x64_v1.0.0.zip` containing portable launcher, documentation, and runtime components

### 🧩 Changed  
- Automatic setup of `mod/romstemp` folder structure for RetroBat  
- Non-destructive external integration using temporary `es_systems.cfg` injection

### 📄 Documentation  
- Creation of public `README.md` file on GitHub  
- Addition of “Release Info” section with changelog and download link

### 🔐 Third-Party Components  
- Included: Squid-Box.SevenZipSharp (`7z.dll`)  
  License: MIT — official repository [SevenZipSharp GitHub](https://github.com/adamhathcock/sevenzipsharp)

### 📦 ZIP Integrity  
**File:** `GhostBat_Windows-x64_v1.0.0.zip`  
**SHA-256:** `3f076294d3dc7f76c4c6c7d34c9e4fb0f82e217b9beea6a4f6064d33c197e5f1`  

✅ This checksum verifies the authenticity of the distributed ZIP package.  
Compare it before using GhostBat to ensure the integrity of your copy.


---

## 📌 Notes  
- ✅ No ROMs, BIOS files or sensitive content included in the project  
- ✅ SHA-256 verification available in `README.md`  
- ✅ All files comply with Creative Commons and MIT licenses  
- ❌ GhostBat does not permanently modify RetroBat or system configuration
