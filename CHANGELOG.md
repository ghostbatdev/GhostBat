# 📓 GhostBat — Changelog

Tutti i cambiamenti ufficiali al progetto **GhostBat** vengono documentati in questo file, a partire dalla versione iniziale `v1.0.0`.

---

## [v1.0.0] — 2025-07-11

🎉 **Initial Public Release**

### ✅ Added
- Prima versione pubblica del launcher GhostBat
- Supporto a oltre 200 sistemi RetroBat testati
- Editor CSV con rilevamento duplicati e gestione multilinea
- Meccanismo di patch reversibili con link ROM temporanei
- Esecuzione contenuti da URL remoti (`.zip`, `.chd`, `.cue`, ecc.)
- Interfaccia compatibile con dischi esterni USB
- Documentazione completa in inglese e italiano (`README_EN.txt`, `README_IT.txt`)
- File `LICENSE.md` (Creative Commons BY-NC-ND 4.0)
- File `GhostBat_Windows-x64_v1.0.0.zip` con struttura launcher portatile

### 🧩 Changed
- Configurazione automatica mod/romstemp nella struttura RetroBat
- Integrazione esterna non distruttiva con RetroBat (`es_systems.cfg` temporaneo)

### 📄 Documentation
- Creazione file `README.md` pubblico su GitHub
- Aggiunta sezione “Release Info” con changelog e link al pacchetto

### 🔐 Third-Party Components
- Inclusione di Squid-Box.SevenZipSharp (`7z.dll`)  
  Licenza: MIT — repository ufficiale [SevenZipSharp GitHub](https://github.com/adamhathcock/sevenzipsharp)

---

## 📌 Notes

- ✅ Nessun ROM, BIOS o contenuto sensibile incluso nel progetto
- ✅ Verifica SHA-256 disponibile nel file `README.md`
- ✅ Tutti i file rispettano le licenze Creative Commons e MIT
- ❌ GhostBat non modifica in modo permanente RetroBat o la configurazione di sistema