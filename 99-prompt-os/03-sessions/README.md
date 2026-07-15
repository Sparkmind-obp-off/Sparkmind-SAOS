# SPOS Sessions

> Status: Draft baseline SPOS-009 — folder instance session mengikuti Session Engine `In Review`.

## Tujuan

Menyimpan kontrak instance yang mengoperasionalkan [`../00-core/SESSION_ENGINE.md`](../00-core/SESSION_ENGINE.md) untuk satu unit kerja melalui identity, objective, type, lifecycle, state, scope, authority, dependency, deliverable, continuity, quality/governance gate, Git trace, report, dan closure.

## Artefak Aktif

- [`../00-core/SESSION_ENGINE.md`](../00-core/SESSION_ENGINE.md) — policy kanonik lifecycle, type, state, continuity, report, dan closure session.
- [`SESSION_TEMPLATE.md`](SESSION_TEMPLATE.md) — template instance untuk session SPOS dan session SAOS yang menggunakan SPOS.

## Aturan

- Satu session memiliki tepat satu objective utama, ID unik, primary type, state/history, owner, authority, scope, deliverable, success criteria, serta source of truth.
- State hanya menggunakan `Pending`, `Running`, `Blocked`, `Waiting for Approval`, `Review`, `Completed`, `Archived`, atau `Cancelled` beserta transisi yang diizinkan Session Engine.
- Session tidak memperluas authority upstream; `Completed` tidak berarti artefak otomatis `Approved`.
- Resume menggunakan continuity package, actual repository state, dan last safe checkpoint; session terminal dilanjutkan melalui successor ber-ID baru.
- Dependency, approval, atau gate kritis yang gagal menggunakan `Blocked`/`Waiting for Approval`, bukan false completion.
- Laporan hasil tetap disimpan di [`../../reports/sessions/`](../../reports/sessions/); folder ini menyimpan kontrak instance, bukan laporan historis atau policy tandingan.
