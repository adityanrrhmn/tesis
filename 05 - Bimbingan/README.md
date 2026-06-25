# 05 — Bimbingan

Notula setiap pertemuan dengan dosen pembimbing. Buat catatan baru dari `99 - Template/Template - Bimbingan.md`, beri nama mis. `2026-06-25 Bimbingan.md`.

```dataview
TABLE pembimbing AS "Pembimbing", file.mtime AS "Diperbarui"
FROM "05 - Bimbingan"
WHERE jenis = "bimbingan"
SORT tanggal DESC
```

> [!note] Tabel butuh plugin **Dataview** (opsional).
