---
tags: [dashboard]
jenis: dashboard
---
# 🎓 Dashboard Tesis

> [!info] Identitas
> - **Nama / NIM:** Aditya Nurrohman / 25/574386/PPA/07244
> - **Judul:** Optimasi Akurasi *Local Small Language Model* Menggunakan *Fine-Tuning* LoRA dan *Re-Ranked Retrieval-Augmented Generation* pada *AI Agent Workflow Automation*
> - **Prodi:** S2 Magister Kecerdasan Artifisial — DIKE, FMIPA UGM
> - **Pembimbing 1:** Prof. Dr. Azhari, MT.
> - **Pembimbing 2:** Dr.techn. Guntur Budi Herwanto, S.Kom., M.Cs.
> - **Tahap:** Penyusunan proposal (disetujui pembimbing untuk lanjut)
> - **Target sidang:** _belum ditentukan_

## 📌 Status saat ini

> [!success] Sudah selesai
> - [x] Setup workspace + 8 MCP + template LaTeX MKA
> - [x] Bibliografi 38 paper terverifikasi (non-MDPI, 0 halusinasi)
> - [x] Draf proposal BAB I–V terkompilasi (PDF)

> [!todo] Langkah berikutnya
> - [ ] Lengkapi `% TODO` di `.tex`: dataset domain, model SLM final, GPU, hyperparameter
> - [ ] Perkuat justifikasi metode & ablation (sedang dikerjakan)
> - [ ] Finalisasi → ajukan seminar proposal

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
