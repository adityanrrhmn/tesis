# PETA.md — Peta Navigasi untuk Claude (hemat konteks)

> Baca file ini SEBELUM menjelajah folder. Kalau jawabannya ada di sini, jangan Glob/scan lagi.
> Pengguna = kurator; Claude = pengerja naskah. Perbarui peta ini setiap menambah/memindah file penting.

## Butuh apa → buka apa

| Butuh | Lokasi persis |
|---|---|
| Menulis/merevisi BAB **tesis** | `01 - Naskah/Tesis (LaTeX MKA)/Contents/BAB_1.tex` … `BAB_7.tex` |
| Menulis/merevisi BAB **proposal** | `01 - Naskah/Proposal (LaTeX MKA)/Contents/BAB_1.tex` … `BAB_5.tex` (BAB_6/7 di folder ini = sisa template, TIDAK dipakai) |
| Abstrak | `Contents/Abstrak_ID.tex` & `Contents/Abstract_EN.tex` (per proyek naskah) |
| Menambah sitasi naskah | **`referensi.bib` DI DALAM folder proyek naskah ybs** — Proposal & Tesis punya bib masing-masing |
| Bib lapisan riset (Zotero/catatan) | `02 - Literatur/references.bib` — BUKAN yang dikompilasi LaTeX; jangan tertukar |
| Definisi istilah/akronim (`\gls`) | `GLOSARIUM.tex` per proyek naskah |
| Identitas (judul, NIM, pembimbing, penguji) | `CONFIG_TESIS.tex` per proyek naskah |
| Main file kompilasi | `LAPORAN_TESIS.tex` per proyek naskah (pdfLaTeX + BibTeX, natbib) |
| Gambar naskah | `Figures/` per proyek naskah (PDF vektor; sumber skrip di `03 - Eksperimen/src/figures/`) |
| Aturan format UGM (margin, penomoran, dll) | `99 - Template/Template Resmi UGM MIPA/Acuan Format UGM MIPA.md` |
| Cara kompilasi | `01 - Naskah/CARA KOMPILASI LaTeX (MKA).md` + skill `kompilasi-naskah` |
| Status per bab (apa yang belum selesai) | `01 - Naskah/Peta Naskah & Status.md` |
| Progress & timeline keseluruhan | `00 - Dashboard/Progress dan Timeline.md` · `00 - Dashboard/Dashboard Tesis.md` |
| Daftar paper + tautan unduh PDF | `02 - Literatur/Daftar Referensi & PDF.md` |
| Hasil audit sitasi proposal | `02 - Literatur/Audit Sitasi (Proposal).md` |
| Peta topik literatur (MOC) | `02 - Literatur/Peta Literatur (MOC).md` |
| Catatan baca per paper (1 paper = 1 file) | `02 - Literatur/Catatan Baca/` — template: `99 - Template/Template - Catatan Baca.md` |
| PDF paper (gitignored) | `02 - Literatur/PDF/` — MCP arxiv menyimpan ke sini |
| Kode / notebook / hasil eksperimen | `03 - Eksperimen/src` · `notebooks` · `results` (`data/`, `models/`, `logs/` gitignored) |
| Catatan konsep (Zettelkasten) | `04 - Catatan Atomik/` |
| Notula bimbingan | `05 - Bimbingan/` — template: `99 - Template/Template - Bimbingan.md` |
| PPT proposal (disetujui pembimbing) | `05 - Bimbingan/Presentasi/Tesis_SLM_LoRA_RAG.pptx` + `Analisis PPT Proposal.md` |
| Review DOCX proposal | `01 - Naskah/Proposal MKA - review.docx` |
| Draf lama 5-bab (arsip — JANGAN edit) | `07 - Arsip/draf-markdown-generik-5bab/` |
| Konfigurasi MCP | `.mcp.json` (kunci, gitignored) · `.mcp.json.example` (template) · `SETUP MCP.md` (panduan) |
| Agen & skill Claude | `.claude/agents/` (6 agen) · `.claude/skills/` (3 skill) — ringkasan di CLAUDE.md |

## Fakta yang sering dibutuhkan (jangan cari ulang)

- **Topik:** Optimasi Akurasi *Local Small Language Model* — *Fine-Tuning* LoRA + *Re-Ranked RAG* — *AI Agent Workflow Automation*. Penulis: Aditya Nurrohman, S2 MKA DIKE FMIPA UGM.
- **Proposal = 5 bab** (I Pendahuluan · II Tinjauan Pustaka · III Dasar Teori · IV Metodologi · V Jadwal) — status: LENGKAP, disetujui lanjut (notula `05 - Bimbingan/2026-06 Bimbingan - Persetujuan Lanjut Proposal.md`).
- **Tesis = 7 bab** (I Pendahuluan · II Tinjauan Pustaka · III Dasar Teori · IV Metodologi · V Implementasi Sistem · VI Hasil & Pembahasan · VII Penutup) — fokus kerja saat ini.
- **Sitasi:** natbib `\citep`/`\citet`, APA-7. Kunci HARUS sudah ada di `referensi.bib` proyek ybs; verifikasi eksistensi paper sebelum menambah entri (agen `auditor-sitasi` / `pencari-literatur`).
- **Objek per bab:** Tabel (1.1), Gambar (1.1), Persamaan (1.1); algoritma `algorithm`+`algorithmic`; kode `lstlisting`.

## Anti-pola (pemborosan konteks — hindari)

- Jangan membaca `LAPORAN_TESIS.tex` / `ugmtesis.cls` penuh — Grep/baca hanya bagian yang relevan.
- `referensi.bib` bisa panjang → Grep kunci spesifik, jangan baca penuh.
- Jangan scan `.obsidian/`, `02 - Literatur/PDF/`, atau `07 - Arsip/` tanpa alasan spesifik.
- Struktur folder sudah terpetakan di sini — tidak perlu `Get-ChildItem -Recurse` dari root.
