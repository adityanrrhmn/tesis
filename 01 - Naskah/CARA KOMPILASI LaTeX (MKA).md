---
tags: [latex, panduan]
jenis: panduan
---
# ⚙️ Cara Kompilasi Template LaTeX MKA

> Toolchain LaTeX **belum terpasang** di komputer ini. Ada dua jalur. Untuk tesis dengan banyak paket (glosarium, algoritma, listing, natbib), **Overleaf paling mudah** dan tanpa instalasi.

## Berkas inti tiap proyek
- `LAPORAN_TESIS.tex` — berkas utama (yang dikompilasi).
- `CONFIG_TESIS.tex` — identitas (judul, nama, NIM, pembimbing). **Isi ini dulu.**
- `ADDITIONAL_PACKAGES.tex` — paket tambahan.
- `ugmtesis.cls` — kelas dokumen UGM (jangan diubah kecuali paham).
- `GLOSARIUM.tex` — definisi istilah & singkatan.
- `Contents/BAB_*.tex` — isi tiap bab.
- `referensi.bib` — basis data sitasi (BibTeX).
- `natbib.bst` — gaya daftar pustaka (penulis–tahun).
- `Figures/` — gambar, logo UGM, form pengesahan.

## Jalur A — Overleaf (online, gratis, disarankan) ✅
1. Buat akun gratis di <https://www.overleaf.com>.
2. **New Project → Upload Project**. Kompres isi folder `Tesis (LaTeX MKA)` menjadi ZIP, lalu unggah. (Atau unggah ZIP asli yang sudah diarsipkan di `99 - Template/Template Resmi UGM MIPA/_arsip-zip`.)
3. Buka **Menu → Settings**:
   - *Compiler*: **pdfLaTeX**.
   - *Main document*: **LAPORAN_TESIS.tex**.
4. Klik **Recompile**. Glosarium & daftar pustaka biasanya otomatis di Overleaf (jika daftar istilah kosong, jalankan recompile dua kali).
5. Sinkronisasi balik: unduh hasil/PDF, atau hubungkan Overleaf ke GitHub (opsional) agar sinkron dengan vault ini.

> Kelebihan: tanpa instal, semua paket tersedia, mudah berbagi draf ke pembimbing.
> Kekurangan: butuh internet; akun gratis ada batas waktu kompilasi (cukup untuk tesis).

## Jalur B — Lokal dengan MiKTeX (Windows)
1. Pasang **MiKTeX**: <https://miktex.org/download> (atau lewat winget: `winget install MiKTeX.MiKTeX`). Saat instalasi pilih *"install missing packages on the fly: Yes"*.
2. Pasang **Perl** (dibutuhkan `makeglossaries`/`latexmk`): <https://strawberryperl.com> (atau `winget install StrawberryPerl.StrawberryPerl`).
3. (Opsional) Editor: **TeXstudio** (`winget install TeXstudio.TeXstudio`) atau ekstensi **LaTeX Workshop** di VS Code.
4. Kompilasi dari folder proyek (urutan untuk natbib + glosarium):
   ```powershell
   pdflatex LAPORAN_TESIS
   bibtex   LAPORAN_TESIS
   makeglossaries LAPORAN_TESIS
   pdflatex LAPORAN_TESIS
   pdflatex LAPORAN_TESIS
   ```
   Atau cukup: `latexmk -pdf LAPORAN_TESIS.tex` (mengulang otomatis).
5. Hasil: `LAPORAN_TESIS.pdf`.

> [!tip] Minta bantuan
> Saya (Claude) bisa menjalankan instalasi via winget dan menjalankan kompilasi untuk Anda — cukup minta. File `.tex` juga bisa saya sunting langsung.

## Catatan build & git
Berkas hasil kompilasi (`.aux`, `.log`, `.bbl`, `.glo`, dll.) sudah diabaikan git lewat `.gitignore`. Jangan commit berkas-berkas itu.
