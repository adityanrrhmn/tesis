---
tags: [literatur, moc]
jenis: moc
---
# 🗺️ Peta Literatur (MOC)

> *Map of Content* — pintu masuk ke seluruh literatur. Kelompokkan paper per tema agar BAB II mudah disintesis.

## Alur kerja menambah literatur
1. Cari paper (minta Claude pakai **arXiv MCP** / **Paper Search MCP** / **Zotero MCP**).
2. Unduh PDF ke `02 - Literatur/PDF`.
3. Buat catatan dari `99 - Template/Template - Catatan Baca.md` di folder `Catatan Baca`.
4. Tambahkan entri BibTeX ke `references.bib` (atau impor dari Zotero).
5. Daftarkan di peta ini, di bawah tema yang sesuai.

## Tema A — _judul tema_
- [ ] [[ ]]

## Tema B — _judul tema_
- [ ] [[ ]]

## Tema C — _judul tema_
- [ ] [[ ]]

## Semua catatan baca

```dataview
TABLE penulis AS "Penulis", tahun AS "Tahun", status AS "Status", rating AS "★"
FROM "02 - Literatur/Catatan Baca"
WHERE jenis = "catatan-baca"
SORT tahun DESC
```

> [!note] Tabel di atas butuh plugin **Dataview** (opsional).
