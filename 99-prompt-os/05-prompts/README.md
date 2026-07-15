# SPOS Prompts

> Status: Draft baseline SPOS-001; seluruh template masih placeholder dan bukan prompt aktif.

## Tujuan

Menyediakan assembly boundary untuk prompt yang menghubungkan executor, intent pengguna, dan unit task tanpa menjadikan prompt sebagai sumber authority baru.

## Artefak Aktif

- [`SYSTEM_TEMPLATE.md`](SYSTEM_TEMPLATE.md) — role, authority, constraint, dan output contract stabil.
- [`USER_TEMPLATE.md`](USER_TEMPLATE.md) — intent, context, scope, deliverable, dan preference pengguna.
- [`TASK_TEMPLATE.md`](TASK_TEMPLATE.md) — objective eksekusi, langkah, output, validation, serta stop condition.

## Urutan Assembly

```text
Approved dependencies
  → System Template
  → User intent and context
  → Session-bounded Task
  → Preflight validation
  → Executor
```

## Aturan

- Muat hanya dependency yang relevan dan statusnya jelas.
- Jangan menyalin rule lengkap bila referensi kanonik cukup.
- Jangan meletakkan secret atau credential di prompt.
- Jangan mengklaim prompt placeholder sebagai engine atau policy approved.
- Output prompt wajib tetap tunduk pada scope session dan governance.
