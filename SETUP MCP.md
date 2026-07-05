# 🔌 Setup MCP — Status & Langkah

Workspace ini memakai 8 server MCP **gratis** (konfigurasi di `.mcp.json`). Berikut status & yang masih perlu Anda lakukan.

> [!important] Aktifkan di Claude Code
> Setelah `.mcp.json` ada, **restart Claude Code** (atau jalankan `/mcp`) dan **setujui (trust)** server MCP proyek saat diminta. Server berbasis `uvx`/`npx` akan mengunduh paket saat pertama dijalankan (10–60 detik), lalu di-cache.

## Ringkasan status

| Server | Fungsi | Status | Yang perlu dilakukan |
|---|---|---|---|
| **obsidian** | Baca/tulis vault | 🟢 **Siap** | Plugin Local REST API aktif, API key sudah terpasang, endpoint HTTPS:27129 teruji (200) |
| **zotero** | Sitasi & referensi | 🟡 **Perlu Zotero** | Install Zotero 7 + aktifkan local API (lihat di bawah) |
| **arxiv** | Cari/unduh paper arXiv | 🟢 Siap | PDF tersimpan ke `02 - Literatur/PDF`. Unduh paket saat pertama dipakai |
| **paper-search** | Cari literatur multi-sumber | 🟢 Siap | Butuh `git` (ada). Opsional: API key Semantic Scholar (sudah diajukan 2026-07, menunggu email) untuk rate limit lebih tinggi |
| **fetch** | Web → markdown | 🟢 Siap | — |
| **sequential-thinking** | Penalaran bertahap | 🟢 Siap | — |
| **huggingface** | Cari model/dataset/paper HF Hub | 🟢 Siap | Token read terpasang di `.mcp.json` |
| **context7** | Dokumentasi API library terkini | 🟢 Siap | API key terpasang di `.mcp.json` |

## 1. Obsidian — SELESAI ✅
- Plugin **Local REST API** sudah terpasang & aktif di vault ini.
- API key sudah otomatis dimasukkan ke `.mcp.json` (dibaca dari config plugin).
- Endpoint aktif di mesin ini: **HTTP `127.0.0.1:27128`** (teruji auth OK). `OBSIDIAN_API_KEY` diisi key **polos tanpa awalan `Bearer`** — client `mcp-obsidian` menambahkannya otomatis (kalau ditulis "Bearer <key>" hasilnya 401).
- **Syarat pakai:** Obsidian harus **terbuka** dengan vault ini saat MCP dipakai.
- *Alternatif HTTPS:* aktifkan server HTTPS di setelan plugin, lalu set `"OBSIDIAN_PROTOCOL":"https"` + port-nya (mis. `27129`).

## 2. Zotero — PERLU DIPASANG 🟡
Server `zotero` memakai paket **`zotero-mcp-server`** (oleh 54yyyu — punya pencarian semantik; **bukan** `zotero-mcp` biasa). Mode **lokal gratis** (tanpa akun/API key):
1. Pasang **Zotero 7+**: <https://www.zotero.org/download/> (atau `winget install Zotero.Zotero`).
2. Buka Zotero → **Edit → Settings → Advanced**. Centang **"Allow other applications on this computer to communicate with Zotero"** dan **"Enable local API"** (API lokal di `http://localhost:23119`).
3. Biarkan Zotero **tetap terbuka** saat memakai MCP.
4. (Opsional, gratis) Pencarian semantik lokal: di PowerShell jalankan `uv tool install "zotero-mcp-server[semantic]"` lalu (Zotero terbuka) `zotero-mcp update-db`. Model embedding `all-MiniLM-L6-v2` berjalan lokal, tanpa biaya.
5. (Sangat disarankan) Pasang **Better BibTeX** (<https://retorque.re/zotero-better-bibtex/>) dan atur **auto-export** koleksi tesis ke `referensi.bib` proyek LaTeX → sitasi & daftar pustaka selalu sinkron.

## 3–6. arXiv / Paper Search / Fetch / Sequential Thinking — Siap
Tidak perlu kredensial. Akan aktif otomatis setelah Claude Code restart. arXiv menyimpan PDF ke `02 - Literatur/PDF`.

## 7. Hugging Face — SELESAI ✅
Server MCP resmi HF (remote `https://huggingface.co/mcp`): cari model, dataset, paper, dan dokumentasi Hub — inti untuk topik SLM lokal + LoRA. Autentikasi via token **read** (gratis) di `.mcp.json`. Kelola token: <https://huggingface.co/settings/tokens>.

## 8. Context7 — SELESAI ✅
Dokumentasi API library terkini (transformers, peft, trl, dsb.) agar kode eksperimen tidak memakai API usang. Remote `https://mcp.context7.com/mcp`; API key gratis dari <https://context7.com/dashboard>, tersimpan di `.mcp.json`.

## Uji cepat setelah aktif
Minta saya (atau coba sendiri):
- *"Pakai arxiv: cari 5 paper terbaru soal [topik]."*
- *"Pakai obsidian: baca [[Dashboard Tesis]]."*
- *"Pakai paper-search: cari di Semantic Scholar tentang [topik]."*
- (Setelah Zotero siap) *"Pakai zotero: cari item di koleksiku tentang [topik]."*

## Keamanan
- `.mcp.json` (berisi API key Obsidian) **diabaikan git** (lihat `.gitignore`). Berbagi konfigurasi via `.mcp.json.example` (tanpa kunci).
- Semua server berjalan **lokal**; tidak ada layanan berbayar. arXiv/paper-search/fetch mengakses internet publik tanpa kredensial.

> Toolchain LaTeX untuk menyusun naskah final: lihat [[CARA KOMPILASI LaTeX (MKA)]].
