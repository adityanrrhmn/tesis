---
tags: [literatur, audit, sitasi]
jenis: audit-sitasi
---
# 🛡️ Audit Sitasi — Proposal (Anti-Halusinasi)

> Bukti bahwa **setiap sitasi di proposal merujuk paper NYATA**. Tiap entri ditemukan via MCP (OpenAlex / DBLP / arXiv) dan diverifikasi pengenal stabilnya (DOI atau arXiv-id). Audit otomatis: 29 sitasi dipakai = 29 entri `referensi.bib`, **0 menggantung**.

**Tanggal audit:** 2026-06-25 · **Berkas:** `01 - Naskah/Proposal (LaTeX MKA)/referensi.bib`

| # | Key sitasi | Penulis (Tahun) | Venue | DOI / arXiv | Status |
|---|---|---|---|---|---|
| 1 | hu2022lora | Hu dkk. (2022) | ICLR | arXiv:2106.09685 | ✅ |
| 2 | zhang2024tinyllama | Zhang dkk. (2024) | arXiv | arXiv:2401.02385 | ✅ |
| 3 | abdin2024phi3 | Abdin dkk. (2024) | arXiv (tech report) | arXiv:2404.14219 | ✅ |
| 4 | qwen2024qwen25 | Qwen dkk. (2024) | arXiv (tech report) | arXiv:2412.15115 | ✅ |
| 5 | wang2025slmsurvey | Wang dkk. (2025) | ACM TIST (Q1) | 10.1145/3768165 | ✅ |
| 6 | xia2023sheared | Xia dkk. (2023) | ICLR/arXiv | arXiv:2310.06694 | ✅ |
| 7 | minaee2024llmsurvey | Minaee dkk. (2024) | arXiv | arXiv:2402.06196 | ✅ |
| 8 | dettmers2023qlora | Dettmers dkk. (2023) | NeurIPS | arXiv:2305.14314 | ✅ |
| 9 | ding2023delta | Ding dkk. (2023) | Nature Machine Intelligence (Q1) | 10.1038/s42256-023-00626-4 | ✅ |
| 10 | mao2024lorasurvey | Mao dkk. (2024) | Frontiers of Computer Science (Q2) | 10.1007/s11704-024-40663-9 | ✅ |
| 11 | valipour2023dylora | Valipour dkk. (2023) | EACL | 10.18653/v1/2023.eacl-main.239 | ✅ |
| 12 | hu2023llmadapters | Hu dkk. (2023) | EMNLP | 10.18653/v1/2023.emnlp-main.319 | ✅ |
| 13 | zheng2024llamafactory | Zheng dkk. (2024) | ACL (Demos) | 10.18653/v1/2024.acl-demos.38 | ✅ |
| 14 | lewis2020rag | Lewis dkk. (2020) | NeurIPS | arXiv:2005.11401 | ✅ |
| 15 | gao2023ragsurvey | Gao dkk. (2023) | arXiv | arXiv:2312.10997 | ✅ |
| 16 | ram2023incontext | Ram dkk. (2023) | TACL (Q1) | 10.1162/tacl_a_00605 | ✅ |
| 17 | ren2021rocketqav2 | Ren dkk. (2021) | EMNLP | 10.18653/v1/2021.emnlp-main.224 | ✅ |
| 18 | sun2023rankgpt | Sun dkk. (2023) | EMNLP | 10.18653/v1/2023.emnlp-main.923 | ✅ |
| 19 | ma2023lrl | Ma dkk. (2023) | arXiv | arXiv:2305.02156 | ✅ |
| 20 | pradeep2023rankvicuna | Pradeep dkk. (2023) | arXiv | arXiv:2309.15088 | ✅ |
| 21 | pradeep2023rankzephyr | Pradeep dkk. (2023) | arXiv | arXiv:2312.02724 | ✅ |
| 22 | liu2024lostmiddle | Liu dkk. (2024) | TACL (Q1) | 10.1162/tacl_a_00638 | ✅ |
| 23 | jiang2023activerag | Jiang dkk. (2023) | EMNLP | 10.18653/v1/2023.emnlp-main.495 | ✅ |
| 24 | chen2024ragbench | Chen dkk. (2024) | AAAI | 10.1609/aaai.v38i16.29728 | ✅ |
| 25 | es2024ragas | Es dkk. (2024) | EACL (Demos) | 10.18653/v1/2024.eacl-demo.16 | ✅ |
| 26 | wang2024agentsurvey | Wang dkk. (2024) | Frontiers of Computer Science (Q2) | 10.1007/s11704-024-40231-1 | ✅ |
| 27 | schick2023toolformer | Schick dkk. (2023) | NeurIPS | arXiv:2302.04761 | ✅ |
| 28 | yao2023tot | Yao dkk. (2023) | NeurIPS | arXiv:2305.10601 | ✅ |
| 29 | park2023generativeagents | Park dkk. (2023) | UIST (ACM) | 10.1145/3586183.3606763 | ✅ |

## Catatan verifikasi
- **Tidak ada penerbit MDPI / jurnal predator.** Venue = konferensi top AI (NeurIPS, ICLR, ACL, EMNLP, EACL, AAAI, UIST) & jurnal Q1/Q2 Scopus (TACL, Nature Machine Intelligence, ACM TIST, Frontiers of Computer Science).
- Status indeks **Scopus** untuk jurnal sebaiknya dikonfirmasi final via SJR/Scopus sebelum sidang.
- Cara cek ulang otomatis: jalankan audit di repo (mencocokkan `\citep/\citet` ↔ entri `referensi.bib`). Hasil terakhir: **0 sitasi menggantung**.
- Untuk entri arXiv yang kemudian terbit di venue resmi, perbarui `referensi.bib` dengan DOI venue tersebut.
