\# 📘 GhostBat Usage Guide — Step-by-Step Tutorial



This guide describes the complete flow for using GhostBat as a selective patcher for RetroBat systems, via custom CSV files and direct ROM links.



---



\## ⚠️ 1. Initial Disclaimer Prompt



When launching GhostBat, a disclaimer is shown about the reversible functionality of the program.  

The user must click \*\*“Yes”\*\* to proceed.



!\[Disclaimer](img/1.png)



---



\## 🔎 2. RetroBat Detection and Mod Application Request



After accepting the disclaimer, GhostBat automatically checks if RetroBat is present in the root of the drive.



📌 If detected successfully, this message appears:



> ✅ RetroBat found! Would you like to apply the mod?



Select \*\*“Yes”\*\* to begin patching.



!\[RetroBat found](img/2.png)



---



\## ✅ 3. Mod Confirmation Message



GhostBat applies the necessary mod and displays:



> Mod successfully installed! You can now select compatible systems.



!\[Mod confirmation](img/3.png)



---



\## 🧩 4. Opening the Selective Patcher (`mod` folder)



The \*\*selective patcher\*\* located in the `mod` folder opens, allowing you to:



\- View the list of compatible RetroBat systems  

\- Select which systems to patch individually



!\[System list](img/4.png)



---



\## 🛠️ 5. Selecting Systems to Patch



✔️ You can:

\- Check only the systems you want  

\- Or select all



Click the \*\*System Patch\*\* button to apply changes.



!\[System Patch](img/5.png)



---



\## 🍃 6. Identifying Patched Systems



Successfully patched systems appear with a \*\*green row\*\* in the side list.  

This indicates they are active and ready for ROM injection.



!\[Patched systems](img/6.png)



---



\## 🌐 7. Opening the ROM URL Editor



Select a patched system and click \*\*Editor URL ROMS\*\* to open the interface for inserting remote ROM links.



!\[Editor URL ROMS](img/7.png)



---



\## 🌍 8. Inserting ROM Links and Adding to CSV Database



After opening the editor, you can manually add ROM entries for the selected system.



📌 Enter:

\- The \*\*ROM file name\*\* (e.g. `gamefile.extension`)  

\- The \*\*remote or local link\*\* (e.g. `http://192.168.1.118:8080/gamefile.extension`)



✅ Click \*\*“Add ROM link”\*\* to insert the entry.  

Each item is automatically saved in the `.csv` file for the selected system.



---



\### 🔎 Technical Requirements



> Both the \*\*ROM name\*\* and the \*\*URL\*\* must end with a valid extension (e.g. `.zip`, `.7z`, `.bin`, etc.)  

> ⚠️ Missing extensions may lead RetroBat to misinterpret files, causing errors.



📌 You can enable the \*\*“Auto Title”\*\* option to auto-generate the name based on the inserted link.



---



\### 📦 Handling Multi-file ROMs



Some advanced systems — like arcade or laserdisc emulators — require \*\*multiple files\*\* per game. GhostBat handles these cases smoothly.



📌 Examples:

\- \*\*MAME Naomi 2\*\*: `.zip` ROM + `.chd` files  

\- \*\*Daphne systems\*\*: primary `.zip` ROM + separate `.zip` with scripts/media



✔️ For these:

\- Insert the \*\*main ROM file\*\* (e.g. `.zip`)  

\- Add supporting files (e.g. `.chd`, media assets) right after  

\- Click “Add ROM link” for each entry



GhostBat will automatically associate them during launch, adapting to the selected emulator.



📣 No specific game examples are provided; users must understand their system’s file structure.



!\[Insert ROM](img/8.png)



---



\### 💿 Handling Multi-disc ROMs with M3U Generation



Some retro games — like \*\*PlayStation 1\*\* titles — span multiple discs (`CD1`, `CD2`, `CD3`, etc.).  

GhostBat supports combining these into a single virtual ROM using `.m3u` playlists.



📌 Steps:

1\. Insert disc links in the CSV list (`.chd`, `.iso`, `.bin`, etc.)  

2\. Select the files that belong to the same game  

3\. Click \*\*Generate Playlist .m3u\*\*



✅ GhostBat creates a `.m3u` file with the selected discs and patches it.  

RetroBat will show only one entry (e.g. `CD1`), but the launcher integrates all discs for accurate emulation.



⚠️ Important:

\- Multi-disc games are \*\*not auto-managed\*\* by “Patch all systems”  

\- Applying global patching before generating `.m3u` treats discs as separate games  

\- In that case, it's recommended to:

&nbsp; - Remove those entries from CSV  

&nbsp; - Reinsert manually and generate the `.m3u` playlist



📣 This feature works only on systems that support multi-disc via `.m3u`.



!\[Multi-disc selection and M3U generation](img/multidisco.png)



---



\## 🧃 9. ROM Selection and Patch Injection



Go to the \*\*ROM List\*\* tab to view your entries.



✔️ You may:

\- Select all ROMs  

\- Or patch them selectively



Click \*\*Inject to ROM\*\* to apply metadata.



📌 Patched ROMs will be highlighted in \*\*green rows\*\*, just like patched systems.



!\[Inject ROM](img/9.png)



---



\## ✅ 10. Final Confirmation and Patch File Generation



At the end, GhostBat shows:



> Completed.  

> 1 file generated in the 'roms' folder.



This confirms successful patch creation.



!\[Final confirmation](img/10.png)



---



\## 🛠️ Advanced Features Menu



GhostBat offers extra tools from the main menu.  

They’re optional but useful for expert users.



---



\### 📂 Advanced Commands



\- \*\*Apply patch to all systems and ROMs\*\*  

&nbsp; Automatically patches all supported systems and ROMs listed in `.csv` files.



\- \*\*Permanently remove mod\*\*  

&nbsp; Deletes:

&nbsp; - All patched systems  

&nbsp; - Injected ROMs  

&nbsp; - Files installed by GhostBat  

&nbsp; 📌 Restores RetroBat to its original state.



---



\### ⚙️ Launcher Configuration



\- \*\*Remember last launch\*\* (ON/OFF)  

&nbsp; If enabled, prevents re-downloading the same ROM if restarted consecutively.  

&nbsp; 📌 Saves the state of the last launched game.



---



\### 🎨 Interface Settings



\- \*\*Change ROM table font size\*\*  

&nbsp; Allows selecting text size in lists (default up to size `14`).



---



\### 🗂️ CSV Database Management



\- \*\*Save CSV backup ZIP\*\*  

&nbsp; Archives all `.csv` files into one `.zip`.



\- \*\*Load CSV backup ZIP\*\*  

&nbsp; Restores `.csv` files from a previously saved archive.



\- \*\*Clear CSV folder\*\*  

&nbsp; Deletes all `.csv` files created up to that point.



\- \*\*Open CSV folder\*\*  

&nbsp; Opens the directory containing all generated `.csv` files.



---



\### 📘 Info Section



\- \*\*View README\*\*  

\- \*\*View Disclaimer\*\*  

\- \*\*View License\*\*



📌 Documents are available in Italian and English.  

GhostBat is fully localized in Italian.



---



\## ℹ️ Technical Notes



\- All changes made via GhostBat are \*\*temporary and reversible\*\*  

\- Each patched system generates a `.csv` file containing ROM link entries  

\- After injection, GhostBat creates \*\*individual files in the `roms` folder\*\*, each named after the selected ROM and containing its assigned link



You can:

\- Add new ROMs anytime  

\- Remove entries from the CSV  

\- Re-run patches when needed



📌 `.csv` files must be \*\*created using GhostBat’s internal editor only\*\*  

Using externally edited CSVs may cause:

\- Multi-link errors  

\- Malfunctions in the patcher  

\- ROM duplication or conflicts



✅ The official editor ensures:

\- Correct syntax and link structure  

\- Automatic file cleanup and conflict detection  

\- Full compatibility with all launcher functions



🧠 For reliable performance, \*\*do not export or manually edit CSVs\*\* — always use the integrated editor.



---



Thank you for choosing GhostBat! 💻  

For support, visit the official GitHub repository or open an issue in the “Issues” tab.

