---
tags: [naskah, moc, status]
jenis: peta-naskah
---
# 🧭 Peta Naskah & Status — Tesis MKA

> Jembatan antara **catatan riset** (Obsidian) dan **naskah final** (LaTeX). Naskah sebenarnya ada di file `.tex`; halaman ini untuk merencanakan, melacak status, dan menautkan literatur ke tiap bab. Aturan format: [[Acuan Format UGM MIPA]].

> [!info] Naskah final = LaTeX
> Edit isi bab langsung di file `.tex` (Claude bisa mengeditnya). Folder: `Tesis (LaTeX MKA)/Contents/`. Kompilasi: [[CARA KOMPILASI LaTeX (MKA)]].

## Tesis — 7 Bab

| Bab | Berkas | Status | Sub-bagian utama | Catatan/literatur |
|---|---|---|---|---|
| I Pendahuluan | `Tesis (LaTeX MKA)/Contents/BAB_1.tex` | 🔴 | Latar Belakang, Rumusan Masalah, Batasan, Tujuan, Manfaat | |
| II Tinjauan Pustaka | `BAB_2.tex` | 🔴 | Penelitian terdahulu / *related work* | [[Peta Literatur (MOC)]] |
| III Dasar Teori | `BAB_3.tex` | 🔴 | Teori & konsep pendukung | [[04 - Catatan Atomik]] |
| IV Metodologi | `BAB_4.tex` | 🔴 | Deskripsi Umum, Akuisisi Data, Rancangan Model, Rancangan Pengujian | |
| V Implementasi Sistem | `BAB_5.tex` | 🔴 | Detail implementasi, kode, eksperimen | `03 - Eksperimen` |
| VI Hasil & Pembahasan | `BAB_6.tex` | 🔴 | Hasil eksperimen, analisis, perbandingan | `03 - Eksperimen/results` |
| VII Penutup | `BAB_7.tex` | 🔴 | Kesimpulan, Saran | |
| Intisari / Abstract | `Contents/Abstrak_ID.tex`, `Abstract_EN.tex` | 🔴 | Tulis terakhir | |

> Legenda: 🔴 Belum · 🟡 Draf · 🟢 Selesai · ✅ Disetujui pembimbing

## Proposal — 5 Bab
`Proposal (LaTeX MKA)/`: I Pendahuluan · II Tinjauan Pustaka · III Dasar Teori · IV Metodologi · V **Jadwal Penelitian**.
> Proposal dikerjakan lebih dulu (Bab I–IV banyak dipakai ulang di tesis). Selesaikan proposal → seminar proposal → lanjut eksperimen → tesis penuh.

## Alur menulis (drafting → final)
1. **Riset & kumpulkan literatur** → catatan di `02 - Literatur/Catatan Baca`, konsep di `04 - Catatan Atomik`.
2. **Susun argumen/outline** per bab (boleh minta Claude pakai *sequential-thinking* untuk metodologi).
3. **Tulis prosa** langsung ke `.tex` bab terkait dengan sitasi `\citep{kunci}`.
4. **Tambah referensi** ke `referensi.bib` (idealnya auto-export Zotero).
5. **Kompilasi** & periksa hasil PDF.
6. Update status di tabel ini & di [[Dashboard Tesis]].

> [!todo] Langkah pertama
> - [ ] Isi `CONFIG_TESIS.tex` (judul, nama, NIM, pembimbing) di kedua proyek.
> - [ ] Tetapkan topik & isi Latar Belakang (BAB_1.tex).
> - [ ] Kumpulkan 15–20 paper kunci → BAB II.
