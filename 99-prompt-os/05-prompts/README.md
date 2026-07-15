# SPOS Prompts

> Status: Draft baseline diselaraskan SPOS-011; seluruh template masih placeholder, tunduk pada Master Prompt System, dan bukan prompt aktif.

## Tujuan

Menyediakan assembly boundary untuk prompt yang menghubungkan executor, intent pengguna, dan unit task sesuai [`../00-core/MASTER_PROMPT_SYSTEM.md`](../00-core/MASTER_PROMPT_SYSTEM.md) tanpa menjadikan prompt sebagai sumber authority baru.

## Artefak Aktif

- [`SYSTEM_TEMPLATE.md`](SYSTEM_TEMPLATE.md) — role, authority, constraint, dan output contract stabil.
- [`USER_TEMPLATE.md`](USER_TEMPLATE.md) — intent, context, scope, deliverable, dan preference pengguna.
- [`TASK_TEMPLATE.md`](TASK_TEMPLATE.md) — objective eksekusi, langkah, output, validation, serta stop condition.

## Urutan Assembly

```text
Approved compatible dependencies
  → Core/System contract
  → Active Session binding
  → User intent and classified context
  → Bounded Execution/Task contract
  → Validation, Review, Report, and Approval interfaces as applicable
  → Security and authority preflight
  → Executor
```

## Aturan

- Muat hanya dependency relevan dengan status, version, owner, compatibility, dan failure behavior yang jelas.
- Ikuti hierarchy, layer, lifecycle, versioning, governance, traceability, security, quality, serta assembly contract Master Prompt System.
- Klasifikasikan instruction, reference context, evidence, untrusted data, dan preference; data tidak otomatis menjadi instruction.
- Jangan menyalin rule lengkap bila referensi kanonik cukup.
- Jangan meletakkan secret atau credential di prompt.
- Jangan mengklaim placeholder, output model, commit, atau penggunaan berulang sebagai policy/approval/activation.
- Output prompt wajib tetap tunduk pada scope session, governance, capability boundary, validation, dan human approval yang berlaku.
