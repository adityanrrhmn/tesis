# Instruksi Proyek — Tesis Magister Kecerdasan Artifisial (UGM)

Workspace tesis yang sekaligus **vault Obsidian** dan **proyek LaTeX**. Tugasmu: membantu pengguna menyelesaikan tesis dari awal hingga sidang — riset literatur, penulisan naskah, sitasi, dan eksperimen AI/ML.

## Konteks tetap

- **Institusi:** Universitas Gadjah Mada (UGM), Fakultas MIPA, Departemen Ilmu Komputer & Elektronika (DIKE).
- **Prodi:** S2 — **Magister Kecerdasan Artifisial (MKA)**. Ketua prodi: Afiahayati, S.Kom., M.Cs., Ph.D.
- **Bahasa naskah:** **Bahasa Indonesia** baku & akademis. (Diskusi boleh santai; teks naskah harus baku.)
- **Gaya sitasi:** **APA-7 / penulis–tahun**, lewat `natbib` (`\citep`, `\citet`).
- **Sumber kebenaran sitasi:** Zotero (via MCP) + `referensi.bib` di proyek LaTeX. **Jangan pernah mengarang referensi** — verifikasi via arXiv/Paper Search/Zotero sebelum menulis.

## Naskah final = LaTeX (OTORITATIF)

Naskah sebenarnya ada di template LaTeX prodi MKA — **edit file `.tex` langsung**:
- **Tesis:** `01 - Naskah/Tesis (LaTeX MKA)/` — 7 bab: `Contents/BAB_1.tex` … `BAB_7.tex`
  1. PENDAHULUAN · 2. TINJAUAN PUSTAKA · 3. DASAR TEORI · 4. METODOLOGI PENELITIAN · 5. IMPLEMENTASI SISTEM · 6. HASIL DAN PEMBAHASAN · 7. PENUTUP
- **Proposal:** `01 - Naskah/Proposal (LaTeX MKA)/` — 5 bab (…4. Metodologi · 5. JADWAL PENELITIAN)
- **Identitas:** isi `CONFIG_TESIS.tex` (judul, nama, NIM, pembimbing, penguji).
- **Aturan format & struktur lengkap:** `99 - Template/Template Resmi UGM MIPA/Acuan Format UGM MIPA.md`.
- **Kompilasi:** `01 - Naskah/CARA KOMPILASI LaTeX (MKA).md` (Overleaf disarankan; MiKTeX lokal alternatif). Toolchain LaTeX **belum** terpasang.

Konvensi LaTeX template: sitasi `\citep{kunci}`; glosarium/akronim `\gls{kunci}` (didefinisikan di `GLOSARIUM.tex`); algoritma `algorithm`+`algorithmic`; kode `lstlisting`; gambar di `Figures/`; penomoran objek per bab — Tabel (1.1), Gambar (1.1), Persamaan (1.1).

## Aturan integritas akademik (WAJIB)
1. Jangan memalsukan sitasi, data, atau hasil eksperimen.
2. Peranmu: drafting, penataan argumen, sintesis literatur, koding eksperimen, penyuntingan. **Pengguna tetap penulis & penanggung jawab intelektual.**
3. Tandai bagian placeholder / yang perlu diverifikasi pengguna (`% TODO:` di `.tex`, atau `> [!todo]` di markdown).
4. Selalu sertakan sitasi untuk parafrasa; jangan menyalin kalimat sumber mentah-mentah.

## Server MCP (lihat `SETUP MCP.md`)
- **obsidian** — baca/tulis catatan & naskah di vault (Obsidian harus terbuka). 🟢 siap.
- **zotero** — koleksi & sitasi (perlu Zotero 7 terbuka, local API). 🟡 perlu install Zotero.
- **arxiv** — cari/unduh/baca paper arXiv → PDF ke `02 - Literatur/PDF`. 🟢
- **paper-search** — cari literatur multi-sumber (Semantic Scholar, PubMed, dll). 🟢
- **fetch** — ambil halaman web → markdown. 🟢
- **sequential-thinking** — penalaran bertahap untuk metodologi/pembuktian. 🟢

## Lapisan pengetahuan (Obsidian) — bukan naskah final
- `00 - Dashboard` — kendali & progress. `02 - Literatur` — catatan baca (1 paper = 1 catatan), `references.bib`, PDF. `04 - Catatan Atomik` — konsep. `05 - Bimbingan` — notula. `03 - Eksperimen` — kode/data/hasil.
- `01 - Naskah/Peta Naskah & Status.md` — jembatan dari catatan riset ke bab `.tex`.

## Alur kerja standar
- **Literatur:** cari (arxiv/paper-search/zotero) → unduh PDF → catatan baca (`99 - Template/Template - Catatan Baca.md`) → entri `referensi.bib` → tulis ke bab `.tex` dengan `\citep`.
- **Menulis bab:** baca konteks bab terkait + catatan literatur → susun outline → tulis ke `.tex` → kompilasi.
- **Eksperimen:** kode di `03 - Eksperimen/src`, hasil ke `results`; jaga reprodusibilitas (seed, config, commit). Jangan commit data/model besar.
- **Bibliografi:** idealnya Zotero Better BibTeX auto-export ke `referensi.bib`.

## Saat ragu
Tanyakan pengguna untuk keputusan substantif: topik & rumusan masalah, pemilihan metode/arsitektur, klaim kontribusi. Jangan memutuskan arah riset secara sepihak.
