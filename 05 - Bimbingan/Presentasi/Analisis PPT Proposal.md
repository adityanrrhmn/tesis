---
tags: [bimbingan, analisis]
jenis: analisis
---
# 🔍 Analisis PPT Proposal — `Tesis_SLM_LoRA_RAG.pptx`

> Ekstraksi & analisis 9 slide presentasi yang sudah disetujui pembimbing, beserta pemetaan ke bab proposal LaTeX. **Sumber kebenaran arah riset = PPT ini.**

## Isi tiap slide
1. **Judul** — Optimasi Akurasi Local SLM via Fine-Tuning LoRA & Re-Ranked RAG pada AI Agent Workflow Automation (Aditya Nurrohman).
2. **Rumusan Masalah** — satu pertanyaan utama: *"Bagaimana mengoptimalkan akurasi local SLM menggunakan fine-tuning LoRA dan re-ranked RAG pada AI Agent untuk workflow automation?"*
3. **Variabel Penelitian** — X₁ = Fine-Tuning LoRA; X₂ = Re-Ranked RAG; **Y (akurasi)** diukur via: F1-Score, Exact Match (EM), ROUGE-L, Task Completion Rate, Response Latency (ms), Hallucination Rate.
4. **Studi Literatur Terdahulu** — tabel 8 paper (⚠️ **semuanya MDPI** — Electronics / Applied Sciences 2024–2025): SensiLoRA-RAG; Plant Protection QA; Hyundai Staria multimodal RAG; DocentGemma (sLLM+RAG); DS-RAG (BGE-Reranker); SDD-LawLLM; Sem-RAG; SLR Automation.
5. **Gap Penelitian** — **G1**: AI agent workflow automation dengan SLM masih terbatas (LEGOMem/AAMAS 2026, Flow/ICLR 2025 fokus multi-agent LLM besar; TinyAgent/EMNLP 2024 hanya function-calling tanpa RAG). **G2**: RAG re-ranking belum diintegrasikan dengan LoRA (Luo et al. 2026 = RAG+rerank tanpa LoRA; Saha et al. 2024 = RAG tanpa fine-tuning). → Tesis mengisi G1+G2 dengan pipeline terintegrasi.
6. **Contoh Data Training** — dataset **Alpaca** (`https://huggingface.co/datasets/tatsu-lab/alpaca`).
7. (kosong)
8. **Implementasi di n8n** — workflow automation direalisasikan via **n8n**.
9. **Rencana Penelitian** — Gantt 8 kegiatan, rentang **Mei–Februari**.

## Pemetaan ke proposal (LaTeX)
| Elemen PPT | Masuk ke | Status |
|---|---|---|
| Rumusan masalah tunggal | BAB I | ✅ diselaraskan |
| Variabel X₁/X₂/Y | BAB IV (Deskripsi Umum) | ✅ ditambahkan |
| Metrik (F1, EM, ROUGE-L, TCR, Latency, Hallucination) | BAB IV (Rancangan Pengujian) | ✅ diperbarui |
| Dataset Alpaca | BAB IV (Akuisisi Data) | ✅ ditambahkan |
| Implementasi n8n | BAB IV–V | ✅ ditambahkan |
| Gap G1/G2 | BAB I & II | ⏳ menunggu verifikasi sitasi |
| Jadwal Mei–Feb (8 kegiatan) | BAB V | ✅ diselaraskan |

## ⚠️ Catatan kritis — sumber literatur (MDPI)
Seluruh 8 paper acuan utama di PPT berasal dari **MDPI**, sedangkan preferensi tertulis Aditya adalah **menghindari MDPI**. Paper-paper rujukan (termasuk gap: TinyAgent, Flow, LEGOMem, Luo, Saha) sedang **diverifikasi keberadaannya** + dicarikan **alternatif non-MDPI bereputasi**. Daftar Pustaka proposal hanya akan memuat sumber **terverifikasi & non-MDPI** kecuali Aditya memutuskan lain. Lihat [[Audit Sitasi (Proposal)]].
