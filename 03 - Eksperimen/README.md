# 03 — Eksperimen

Kode, data, model, dan hasil eksperimen AI/ML untuk tesis. Tujuan utama: **reprodusibel** — setiap angka di BAB IV bisa ditelusuri ke kode + konfigurasi di sini.

## Struktur

| Folder | Isi | Di-git? |
|---|---|---|
| `src/` | Kode sumber (model, training, evaluasi) | ✅ ya |
| `notebooks/` | Notebook eksplorasi/analisis | ✅ ya |
| `data/` | Dataset mentah & olahan | ❌ tidak (lihat `.gitignore`) |
| `models/` | Bobot model / checkpoint | ❌ tidak |
| `results/` | Tabel, metrik, grafik hasil | ✅ ya (file kecil) |
| `logs/` | Log training (tensorboard/wandb) | ❌ tidak |

## Lingkungan

Disarankan pakai `uv` (sudah terpasang) atau `venv`:

```bash
# buat & aktifkan environment
uv venv
# .venv\Scripts\activate   (PowerShell: .venv\Scripts\Activate.ps1)

# pasang dependensi (sesuaikan)
uv pip install torch numpy pandas scikit-learn matplotlib jupyter
```

Simpan dependensi final di `requirements.txt` atau `pyproject.toml` agar reprodusibel.

## Konvensi reprodusibilitas

- **Selalu set seed** (numpy/torch/random) dan catat di catatan eksperimen.
- Satu eksperimen = satu catatan dari `99 - Template/Template - Eksperimen.md`.
- Catat **commit kode** yang menghasilkan tiap angka.
- Simpan konfigurasi (hyperparameter) sebagai file (mis. `config.yaml`), bukan hardcoded.
