---
name: kompilasi-naskah
description: Prosedur kompilasi naskah LaTeX MKA (proposal/tesis) + pemeriksaan integritas — deteksi sitasi undefined (indikasi kunci salah/karangan), audit warning, regenerasi ZIP Overleaf, ekspor DOCX review via Pandoc. Gunakan saat diminta kompilasi naskah, cek error LaTeX, atau menyiapkan berkas untuk pembimbing/Overleaf.
---

# Kompilasi & Pemeriksaan Naskah

Proyek: `01 - Naskah/Proposal (LaTeX MKA)/` dan `01 - Naskah/Tesis (LaTeX MKA)/`. Main file: `LAPORAN_TESIS.tex`. Compiler: pdfLaTeX + BibTeX (natbib, APA-7).

## 0. Prasyarat

Cek dulu: `pdflatex --version`. Belum terpasang → dua jalur:
- **Lokal**: `winget install MiKTeX.MiKTeX` (setelahnya MiKTeX akan mengunduh paket on-the-fly saat kompilasi pertama — izinkan). Pandoc: `winget install JohnMacFarlane.Pandoc`.
- **Overleaf**: tanpa toolchain lokal, regenerasi ZIP (langkah 3) lalu pengguna unggah manual.

## 1. Urutan kompilasi (jalankan di folder proyek naskah)

```
pdflatex -interaction=nonstopmode LAPORAN_TESIS.tex
bibtex   LAPORAN_TESIS
pdflatex -interaction=nonstopmode LAPORAN_TESIS.tex
pdflatex -interaction=nonstopmode LAPORAN_TESIS.tex
```

## 2. Audit log (WAJIB setiap habis kompilasi)

Grep `LAPORAN_TESIS.log` dan `LAPORAN_TESIS.blg`:

| Pola | Arti | Tingkat |
|---|---|---|
| `Citation .* undefined` | Kunci \citep tanpa entri bib — salah ketik ATAU sitasi karangan | FATAL |
| `I didn't find a database entry` (.blg) | Sama seperti di atas, versi BibTeX | FATAL |
| `Reference .* undefined` | \ref/\label rusak | Tinggi |
| `There were multiply-defined labels` | Label ganda | Tinggi |
| `Overfull \hbox` > 30pt | Tata letak meluber | Rendah |

Nol `undefined` adalah syarat minimum sebelum naskah dikirim ke pembimbing. Laporkan tiap kunci bermasalah + file/baris pemakaiannya, lalu teruskan ke agen `auditor-sitasi` bila dicurigai kunci karangan.

## 3. ZIP Overleaf

Zip seluruh isi folder proyek KECUALI artefak build (`*.aux, *.log, *.out, *.toc, *.bbl, *.blg, *.synctex.gz`, dst — daftar lengkap di .gitignore) ke `01 - Naskah/_Overleaf (siap unggah)/<NamaProyek>_<YYYY-MM-DD>.zip`. Setelan Overleaf: compiler **pdfLaTeX**, main file **LAPORAN_TESIS.tex**.

## 4. DOCX review (Pandoc)

Untuk pembimbing yang mereview di Word:

```
pandoc LAPORAN_TESIS.tex --citeproc --bibliography=referensi.bib -o "Review_<YYYY-MM-DD>.docx"
```

Catatan wajib disampaikan: hasil Pandoc ≠ format final (LaTeX tetap otoritatif); persamaan/tabel kompleks bisa berubah bentuk. Bila bab tertentu saja yang direview, buat file .tex kecil yang meng-\input bab itu lalu konversi.
