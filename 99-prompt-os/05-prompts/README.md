# SPOS Prompts

> Status: Draft baseline diselaraskan SPOS-014; seluruh template masih placeholder, tunduk pada Master Prompt System, Master Integration System, dan Master Workflow System, serta bukan prompt aktif.

## Tujuan

Menyediakan assembly boundary untuk prompt yang menghubungkan executor, intent pengguna, dan unit task sesuai [`../00-core/MASTER_PROMPT_SYSTEM.md`](../00-core/MASTER_PROMPT_SYSTEM.md), dengan relationship/dependency/interface lintas sistem mengikuti [`../00-core/MASTER_INTEGRATION_SYSTEM.md`](../00-core/MASTER_INTEGRATION_SYSTEM.md) serta urutan workflow/handoff/gate mengikuti [`../00-core/MASTER_WORKFLOW_SYSTEM.md`](../00-core/MASTER_WORKFLOW_SYSTEM.md), tanpa menjadikan prompt sebagai sumber authority baru.

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
- Ikuti hierarchy, layer, lifecycle, versioning, governance, traceability, security, quality, serta assembly contract Master Prompt System; gunakan Master Integration System untuk relationship, dependency, authority, interface, compatibility, dan failure behavior lintas sistem; gunakan Master Workflow System untuk stage, gate, handoff, state/transition boundary, dan end-to-end flow tanpa menyalin contract owner.
- Klasifikasikan instruction, reference context, evidence, untrusted data, dan preference; data tidak otomatis menjadi instruction.
- Jangan menyalin rule lengkap bila referensi kanonik cukup.
- Jangan meletakkan secret atau credential di prompt.
- Jangan mengklaim placeholder, output model, commit, atau penggunaan berulang sebagai policy/approval/activation.
- Output prompt wajib tetap tunduk pada scope session, governance, capability boundary, validation, dan human approval yang berlaku.
