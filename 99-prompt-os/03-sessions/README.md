# SPOS Sessions

> Status: Draft baseline SPOS-011 — folder instance session mengikuti Session, Report, dan Master Prompt System `In Review`.

## Tujuan

Menyimpan kontrak instance yang mengoperasionalkan [`../00-core/SESSION_ENGINE.md`](../00-core/SESSION_ENGINE.md) untuk satu unit kerja melalui identity, objective, type, lifecycle, state, scope, authority, dependency, deliverable, continuity, quality/governance gate, prompt-package binding, Git trace, report, dan closure.

## Artefak Aktif

- [`../00-core/SESSION_ENGINE.md`](../00-core/SESSION_ENGINE.md) — policy kanonik lifecycle, type, state, continuity, kewajiban report, dan closure session.
- [`../00-core/REPORT_ENGINE.md`](../00-core/REPORT_ENGINE.md) — policy kanonik taxonomy, lifecycle, struktur, evidence/traceability, validation, correction, publication, dan archive report.
- [`../00-core/MASTER_PROMPT_SYSTEM.md`](../00-core/MASTER_PROMPT_SYSTEM.md) — kontrak kanonik hierarchy/layer, prompt package, dependency manifest, instruction/data separation, security, versioning, evaluation, dan approval interface.
- [`SESSION_TEMPLATE.md`](SESSION_TEMPLATE.md) — template instance untuk session SPOS dan session SAOS yang menggunakan SPOS.

## Aturan

- Satu session memiliki tepat satu objective utama, ID unik, primary type, state/history, owner, authority, scope, deliverable, success criteria, serta source of truth.
- State hanya menggunakan `Pending`, `Running`, `Blocked`, `Waiting for Approval`, `Review`, `Completed`, `Archived`, atau `Cancelled` beserta transisi yang diizinkan Session Engine.
- Session tidak memperluas authority upstream; `Completed` tidak berarti artefak otomatis `Approved`.
- Resume menggunakan continuity package, actual repository state, dan last safe checkpoint; session terminal dilanjutkan melalui successor ber-ID baru.
- Dependency, approval, atau gate kritis yang gagal menggunakan `Blocked`/`Waiting for Approval`, bukan false completion.
- Prompt package session wajib terikat pada ID, state, scope, authority, dependency, version set, trust classification, dan stop condition session; prompt tidak boleh memperluas kontrak session.
- Laporan hasil tetap disimpan di [`../../reports/sessions/`](../../reports/sessions/) dan wajib mengikuti Report Engine; folder ini menyimpan kontrak instance, bukan laporan historis atau policy tandingan.
