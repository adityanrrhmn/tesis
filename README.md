# Tesis — Magister Kecerdasan Artifisial (UGM)

Workspace tesis terpadu: **vault Obsidian** (catatan riset & literatur) + **proyek LaTeX** (naskah final, template prodi MKA UGM) + integrasi **Claude Code** via server MCP gratis.

- **Topik:** Optimasi Akurasi *Local Small Language Model* menggunakan *Fine-Tuning* LoRA dan *Re-Ranked Retrieval-Augmented Generation* pada *AI Agent Workflow Automation*.
- **Penulis:** Aditya Nurrohman — S2 MKA, DIKE FMIPA UGM.
- **Naskah final:** LaTeX, 7 bab (lihat `01 - Naskah/`). Proposal sudah lengkap & terkompilasi.

---

## ⬇️ Clone

```bash
git clone https://github.com/adityanrrhmn/tesis.git
cd tesis
```

> [!IMPORTANT] Beberapa berkas **sengaja TIDAK disertakan** di repo (lihat `.gitignore`) demi keamanan & ukuran:
> - **`.mcp.json`** (berisi API key Obsidian) → pakai **`.mcp.json.example`** sebagai acuan.
> - **PDF paper** (`02 - Literatur/PDF/`) → daftar + tautan unduh ada di `02 - Literatur/Daftar Referensi & PDF.md`.
> - **Plugin Obsidian** (`.obsidian/plugins/`) → install ulang (lihat di bawah).
> - **Artefak build LaTeX** (`*.pdf` hasil, `*.aux`, dll.) & **data/model** eksperimen.

## 🧰 Prasyarat

| Alat | Untuk | Catatan |
|---|---|---|
| **Git** | version control | wajib |
| **Obsidian** | vault catatan | wajib; <https://obsidian.md> |
| **Node.js** + **Python 3.11+** + **uv** | menjalankan server MCP | untuk integrasi Claude Code |
| **Zotero 7** | sitasi | aktifkan *local API* |
| **LaTeX** | kompilasi naskah | **Overleaf** (online, mudah) atau **MiKTeX** (lokal) |
| **Pandoc** | ekspor DOCX | opsional |

## 🚀 Setup setelah clone

1. **Buka sebagai vault Obsidian:** `Open folder as vault` → pilih folder hasil clone.
2. **Install plugin community** (karena tidak ikut di repo). Lewat Obsidian *Settings → Community plugins → Browse*, pasang:
   `Local REST API`, `Dataview`, `Templater`, `Kanban`, `Excalidraw`, `Mind Map`, `Citations`, `Zotero Integration`, `Annotator`.
3. **Aktifkan Obsidian MCP:**
   - Di plugin **Local REST API**: set port **27124**, lalu salin **API Key**-nya.
   - `cp .mcp.json.example .mcp.json` (Windows: salin manual), buka `.mcp.json`, tempel API key ke `OBSIDIAN_API_KEY`, pastikan `OBSIDIAN_PORT` = `27124`.
4. **Zotero:** install Zotero 7 → *Edit → Settings → Advanced* → centang *Allow other applications* & *Enable local API*. (Detail lengkap: **[SETUP MCP.md](SETUP%20MCP.md)**.)
5. **LaTeX / naskah:**
   - **Overleaf:** unggah ZIP di `01 - Naskah/_Overleaf (siap unggah)/` (regenerate bila perlu), set compiler **pdfLaTeX**, main file **LAPORAN_TESIS.tex**.
   - **MiKTeX lokal:** lihat **[CARA KOMPILASI LaTeX (MKA)](01%20-%20Naskah/CARA%20KOMPILASI%20LaTeX%20%28MKA%29.md)**.
6. **PDF referensi:** tidak ikut di repo — unduh lewat daftar di `02 - Literatur/Daftar Referensi & PDF.md` (mayoritas arXiv/ACL, otomatis).

## 📁 Struktur folder

| Folder | Isi |
|---|---|
| `00 - Dashboard` | Progress, timeline, peta proyek |
| `01 - Naskah` | **Naskah final** LaTeX: `Tesis (LaTeX MKA)` & `Proposal (LaTeX MKA)` + peta naskah + panduan kompilasi + DOCX review |
| `02 - Literatur` | `referensi.bib`, indeks & PDF paper, audit sitasi |
| `03 - Eksperimen` | Kode, dataset, model, hasil AI/ML |
| `04 - Catatan Atomik` | Konsep/ide (Zettelkasten) |
| `05 - Bimbingan` | Notula bimbingan + presentasi |
| `06 - Aset` · `07 - Arsip` · `99 - Template` | Aset, arsip, template |

## 📝 Konvensi

- **Bahasa naskah:** Indonesia · **Gaya sitasi:** APA-7 (natbib `\citep`/`\citet`).
- **Sumber kebenaran sitasi:** Zotero + `referensi.bib`. **Integritas akademik:** tidak ada sitasi/data yang dikarang — lihat `02 - Literatur/Audit Sitasi (Proposal).md`.
- Aturan kerja asisten Claude: **[CLAUDE.md](CLAUDE.md)**.

## 🔌 Server MCP

Obsidian · Zotero · arXiv · Paper Search · Web Fetch · Sequential Thinking — semuanya gratis. Status & cara aktif: **[SETUP MCP.md](SETUP%20MCP.md)**.
