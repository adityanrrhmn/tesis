# Workspace Tesis — Magister Kecerdasan Artifisial (UGM)

Repositori/vault terpadu untuk mengerjakan tesis dari awal hingga sidang: penulisan naskah, tinjauan literatur, manajemen sitasi, dan eksperimen AI/ML. Dirancang untuk dipakai bersama **Obsidian** (vault catatan), **template LaTeX resmi prodi MKA UGM** (naskah final), dan **Claude Code** (asisten riset & penulisan) melalui beberapa server MCP gratis.

> **Naskah final ditulis di LaTeX** (template prodi MKA, 7 bab) — lihat `01 - Naskah/Peta Naskah & Status.md` dan `99 - Template/Template Resmi UGM MIPA/Acuan Format UGM MIPA.md`. Obsidian dipakai untuk catatan riset, literatur, dan perencanaan.

## Cara membuka

1. **Obsidian** → `Open folder as vault` → pilih folder `d:\00 - Tesis`.
2. **Claude Code** → sudah aktif di folder ini. Server MCP dikonfigurasi di [.mcp.json](.mcp.json).
3. Belum selesai setup MCP? Ikuti **[SETUP MCP.md](SETUP%20MCP.md)** (install plugin Obsidian + kunci API, aktifkan Zotero local API).

## Struktur folder

| Folder | Isi |
|---|---|
| `00 - Dashboard` | Pusat kendali: progress, timeline, peta proyek |
| `01 - Naskah` | **Naskah final**: proyek LaTeX `Tesis (LaTeX MKA)` & `Proposal (LaTeX MKA)` + peta naskah + panduan kompilasi |
| `02 - Literatur` | Catatan baca (1 paper = 1 catatan), `references.bib`, PDF |
| `03 - Eksperimen` | Kode, dataset, model, hasil eksperimen AI/ML |
| `04 - Catatan Atomik` | Catatan konsep/ide ala Zettelkasten |
| `05 - Bimbingan` | Notula bimbingan dengan dosen pembimbing |
| `06 - Aset` | Gambar, diagram, grafik untuk naskah |
| `07 - Arsip` | Draf lama / versi yang sudah tidak dipakai |
| `99 - Template` | Template catatan (dipakai plugin Templates Obsidian) |

## Konvensi

- **Bahasa naskah:** Indonesia · **Gaya sitasi:** APA (edisi ke-7)
- **Sitasi dalam teks:** `[[@kunci-sitasi]]` atau `(Penulis, Tahun)` — sumber tunggal kebenaran ada di Zotero & `references.bib`.
- **Satu paper = satu catatan** di `02 - Literatur/Catatan Baca`, diberi tag `#literatur` dan dihubungkan ke konsep di `04 - Catatan Atomik`.
- Lihat **[CLAUDE.md](CLAUDE.md)** untuk aturan kerja Claude di vault ini.

## Server MCP yang terpasang

Obsidian · Zotero · arXiv · Paper Search · Web Fetch · Sequential Thinking — semuanya **gratis**. Rincian fungsi & status di **[SETUP MCP.md](SETUP%20MCP.md)**.
