---
tags: [dashboard]
jenis: dashboard
---
# 🎓 Dashboard Tesis

> [!info] Identitas
> - **Judul (sementara):** _belum ditetapkan_
> - **Bidang:** Magister Kecerdasan Artifisial
> - **Pembimbing 1:** _—_
> - **Pembimbing 2:** _—_
> - **Target sidang:** _—_

## 📌 Status saat ini

> [!todo] Langkah berikutnya
> - [ ] Selesaikan setup MCP → lihat [[SETUP MCP]]
> - [ ] Tetapkan topik & rumusan masalah (BAB I)
> - [ ] Kumpulkan 15–20 paper kunci untuk tinjauan pustaka
> - [ ] Susun kerangka metodologi (BAB III)

## 🗂️ Navigasi cepat

- **Naskah final (LaTeX):** [[Peta Naskah & Status]] · folder `01 - Naskah/Tesis (LaTeX MKA)` & `Proposal (LaTeX MKA)`
- **Acuan format:** [[Acuan Format UGM MIPA]] · [[CARA KOMPILASI LaTeX (MKA)]]
- **Riset:** [[Peta Literatur (MOC)]] · [[Progress dan Timeline]]
- **Setup:** [[SETUP MCP]]

## 📈 Progress bab (Tesis — 7 bab)

| Bab | Berkas | Status |
|---|---|---|
| I Pendahuluan | `BAB_1.tex` | 🔴 Belum |
| II Tinjauan Pustaka | `BAB_2.tex` | 🔴 Belum |
| III Dasar Teori | `BAB_3.tex` | 🔴 Belum |
| IV Metodologi | `BAB_4.tex` | 🔴 Belum |
| V Implementasi Sistem | `BAB_5.tex` | 🔴 Belum |
| VI Hasil & Pembahasan | `BAB_6.tex` | 🔴 Belum |
| VII Penutup | `BAB_7.tex` | 🔴 Belum |
| Intisari / Abstract | `Abstrak_ID.tex` / `Abstract_EN.tex` | 🔴 Belum |

> Legenda: 🔴 Belum · 🟡 Draf · 🟢 Selesai · ✅ Disetujui pembimbing · Detail di [[Peta Naskah & Status]]

## 📚 Literatur terbaru

```dataview
TABLE penulis AS "Penulis", tahun AS "Tahun", status AS "Status"
FROM "02 - Literatur/Catatan Baca"
SORT file.mtime DESC
LIMIT 10
```

> [!note] Catatan: blok `dataview` di atas memerlukan plugin **Dataview** (opsional). Jika belum diinstal, abaikan — tabel tidak akan tampil.

## 🧪 Eksperimen terbaru

```dataview
TABLE status, tanggal
FROM "03 - Eksperimen"
WHERE jenis = "eksperimen"
SORT tanggal DESC
LIMIT 5
```
