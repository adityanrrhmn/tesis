---
name: grafik-tesis
description: Membuat grafik/diagram kualitas publikasi untuk naskah tesis — matplotlib bergaya seragam, ekspor ganda PDF vektor (untuk LaTeX Figures/) + PNG 300 dpi (untuk DOCX/Word review). Gunakan setiap kali membuat chart, plot hasil eksperimen, atau diagram perbandingan yang akan masuk naskah atau dokumen review.
---

# Grafik Tesis (LaTeX + Word)

Prinsip: satu sumber kebenaran. Setiap gambar naskah dibuat oleh skrip Python di `03 - Eksperimen/src/figures/` dari data nyata di `results/` — bisa diregenerasi kapan pun.

## Gaya seragam (WAJIB)

- matplotlib murni (boleh + seaborn untuk statistik, tapi bukan tema default seaborn).
- Font serif menyamai naskah: `plt.rcParams["font.family"] = "serif"`; ukuran font efektif ≥ 9 pt pada lebar cetak akhir.
- Lebar figur = lebar teks tesis (~15 cm ≈ 5.9 in) atau setengahnya untuk gambar berdampingan. JANGAN membuat kecil lalu diskalakan besar di LaTeX.
- Ramah cetak hitam-putih & buta warna: bedakan seri dengan marker + linestyle, bukan hanya warna; palet aman (tab10 terpilih / viridis untuk sekuensial).
- Tanpa judul di dalam gambar — judul adalah caption LaTeX/Word. Label sumbu berbahasa Indonesia + satuan. Legend tanpa bingkai bila memungkinkan.
- Sebelum memilih bentuk chart & warna: baca juga skill bawaan `dataviz` bila tersedia; skill ini menambahkan aturan khusus naskah UGM di atasnya.

## Ekspor ganda (setiap gambar, dua format)

```python
fig.savefig(r"01 - Naskah/Tesis (LaTeX MKA)/Figures/nama_gambar.pdf", bbox_inches="tight")    # LaTeX: vektor
fig.savefig(r"03 - Eksperimen/results/figures/nama_gambar.png", dpi=300, bbox_inches="tight")  # Word: 300 dpi
```

- LaTeX: `\includegraphics[width=\linewidth]{Figures/nama_gambar}` — caption gambar di BAWAH, caption tabel di ATAS (Acuan Format UGM MIPA); penomoran per bab otomatis.
- Word/DOCX review: sisipkan PNG 300 dpi apa adanya; dilarang screenshot.

## Integritas data

- Data grafik HARUS dari hasil nyata (`results/`) atau sumber bersitasi. DILARANG mengarang angka untuk mengisi grafik.
- Placeholder terpaksa? Tulis watermark "DATA DUMMY" besar di gambar + `% TODO:` di .tex.
- Simpan pasangan (skrip, data, gambar) dengan nama sama agar mudah dilacak: `fig_akurasi_lora.py` → `fig_akurasi_lora.pdf/png`.
