---
tags: [acuan, format, ugm, mka]
jenis: acuan-format
---
# 📐 Acuan Format & Struktur — Tesis MKA UGM

> **Sumber kebenaran format & struktur.** Diekstrak langsung dari template resmi prodi. Saat menulis naskah final, semua aturan di bawah harus dipenuhi. Konfirmasikan detail terbaru ke dosen pembimbing / koordinator prodi — peraturan bisa berubah.

## Dua tingkat template (keduanya tersimpan di vault)

| Template | Lokasi | Status | Untuk apa |
|---|---|---|---|
| **MKA LaTeX (prodi)** ⭐ | `01 - Naskah/Tesis (LaTeX MKA)` & `Proposal (LaTeX MKA)` | **PRIMER — pakai ini** | Naskah final tesis & proposal Magister Kecerdasan Artifisial |
| Fakultas MIPA `.ott` | `99 - Template/Template Resmi UGM MIPA/*.ott` | Sekunder/acuan | Versi generik LibreOffice/Word (jika tidak memakai LaTeX) |

Template LaTeX diadaptasi dari `template-skripsi-mipa` (Yusuf Syaifudin) dan disesuaikan untuk prodi MKA. Kelas dokumen: **`ugmtesis.cls`**.

## Struktur naskah (LaTeX MKA — OTORITATIF)

### Tesis — 7 bab (`Tesis (LaTeX MKA)/LAPORAN_TESIS.tex`)
1. **BAB I — PENDAHULUAN** → `Contents/BAB_1.tex`
   Latar Belakang · Rumusan Masalah · Batasan Masalah · Tujuan Penelitian · Manfaat Penelitian
2. **BAB II — TINJAUAN PUSTAKA** → `BAB_2.tex` (penelitian terdahulu / *related work*)
3. **BAB III — DASAR TEORI** → `BAB_3.tex` (teori & konsep pendukung)
4. **BAB IV — METODOLOGI PENELITIAN** → `BAB_4.tex`
   Deskripsi Umum Penelitian · Akuisisi Data · Rancangan Model · Rancangan Pengujian
5. **BAB V — IMPLEMENTASI SISTEM** → `BAB_5.tex`
6. **BAB VI — HASIL DAN PEMBAHASAN** → `BAB_6.tex`
7. **BAB VII — PENUTUP** → `BAB_7.tex` (Kesimpulan · Saran)

### Proposal — 5 bab (`Proposal (LaTeX MKA)/LAPORAN_TESIS.tex`)
1. PENDAHULUAN · 2. TINJAUAN PUSTAKA · 3. DASAR TEORI · 4. METODOLOGI PENELITIAN · 5. **JADWAL PENELITIAN**

### Bagian Awal (front matter, otomatis dari `.cls`)
Cover · Halaman Judul · Halaman Persetujuan/Pengesahan · Pernyataan Bebas Plagiasi · Prakata · (Motto opsional) · Daftar Isi · Daftar Tabel · Daftar Gambar · **Daftar Algoritma** · **Daftar Kode Program** · **Daftar Istilah (glosarium)** · **Daftar Singkatan (akronim)** · **Intisari** (ID) · **Abstract** (EN).

### Bagian Akhir
Daftar Pustaka (otomatis dari `referensi.bib`) · Lampiran (opsional, via `\appendix`).

## Identitas dokumen — `CONFIG_TESIS.tex`
Isi field berikut (jangan ubah struktur, hanya nilainya):
`\titleind` (judul ID) · `\titleeng` (judul EN) · `\fullname` (nama) · `\idnum` (NIM) · `\examdate` · `\degree` (Master of Computer Science (AI)) · `\yearsubmit` · `\program{Kecerdasan Artifisial}` · `\headprogram{Afiahayati, S.Kom., M.Cs., Ph.D}` · `\dept{Ilmu Komputer dan Elektronika}` · `\firstsupervisor` · `\firstexaminer` · `\secondexaminer`.

## Tata halaman & huruf (berlaku untuk LaTeX & `.ott`)
| Aspek | Ketentuan |
|---|---|
| Kertas | **A4** (210 × 297 mm) |
| Margin | **kiri 4 cm · atas 4 cm · kanan 3 cm · bawah 3 cm** |
| Font isi | **Times New Roman / Liberation Serif, 12 pt** |
| Spasi | **1,5** |
| Kode program | Font monospace (Courier/LMTypewriter) |
| Orientasi | Portrait; Landscape diizinkan untuk tabel/gambar lebar |

## Sitasi & Daftar Pustaka
- **Mesin sitasi LaTeX:** `natbib` + gaya `natbib.bst` → format **penulis–tahun** (mis. `(Finnen, 1987)`). **Kompatibel dengan APA-7** (pilihan tesis ini).
- Perintah: `\citep{kunci}` → (Penulis, Tahun); `\citet{kunci}` → Penulis (Tahun).
- Sumber: file **`referensi.bib`** di dalam folder proyek LaTeX. Idealnya di-*auto-export* dari **Zotero (Better BibTeX)** agar selalu sinkron.
- Kategori sumber: Buku, Jurnal, Prosiding, Skripsi/Tesis/Disertasi, Laporan Penelitian, Surat Kabar, Artikel Internet.

## Fitur khas template (gunakan bila relevan untuk tesis AI)
- **Algoritma/pseudocode**: lingkungan `algorithm` + `algorithmic` (lihat contoh di `BAB_4.tex`).
- **Kode program**: `lstlisting` (otomatis masuk Daftar Kode Program).
- **Glosarium & singkatan**: definisikan di `GLOSARIUM.tex`, panggil dengan `\gls{kunci}` (akronim auto-reset tiap bab).
- **Gambar contoh ML** tersedia: `loss_plot.pdf`, `learning_rate_plot.pdf`, `grad_norm_plot.pdf` di `Figures/` (ganti dengan hasil eksperimenmu).

## Penomoran objek (per bab)
Tabel (1.1) — keterangan **di atas** · Gambar (1.1) — keterangan **di bawah** · Persamaan (1.1) · Teorema/Lemma/Definisi (1.1).

> Cara kompilasi LaTeX: lihat [[CARA KOMPILASI LaTeX (MKA)]].
