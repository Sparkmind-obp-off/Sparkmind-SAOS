# SPOS Core

> Status: SPOS-009 baseline; Constitution, Governance, Developer Mode, Session, Execution, Git, Documentation, dan Quality Engine `In Review`, architecture tetap Draft sampai authority yang sah mengaktifkannya.

## Tujuan

Menyimpan Constitution, arsitektur, dan kontrak engine inti yang mengatur authority, lifecycle, precedence, execution flow, quality gate, reporting, dan integrasi komponen SPOS.

## Artefak Aktif

- [`CONSTITUTION.md`](CONSTITUTION.md) — authority tertinggi di dalam SPOS, prinsip dasar, governance hierarchy, decision principles, dan amendment policy.
- [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) — standar perilaku operasional AI, decision gates, autonomy boundary, repository policy, rollback, validation, dan reporting.
- [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) — standar proses eksekusi, lifecycle, task classification, validation gates, failure/recovery, evidence, dan Definition of Done.
- [`GIT_ENGINE.md`](GIT_ENGINE.md) — standar branch, commit, Pull Request/review, merge, push, release, protection, audit, recovery, dan otomatisasi Git AI.
- [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) — standar prinsip, jenis, lifecycle, metadata, versioning, ownership, review, publication, archive, dan kebijakan dokumentasi AI.
- [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) — standar prinsip kualitas, sembilan quality gate, Definition of Done, metrik, audit, CAPA, continuous improvement, dan kebijakan kualitas AI.
- [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) — control plane authority, ownership, decision, delegation, lifecycle, compliance, audit, escalation, exception, dan tata kelola AI.
- [`SESSION_ENGINE.md`](SESSION_ENGINE.md) — standar identity, lifecycle orchestration, type, state, continuity, dependency antarsession, report, closure, dan kebijakan session AI.
- [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) — posisi, komponen, dependency, lifecycle, execution flow, dan boundary SPOS.

## Boundary

Constitution merakit sumber fundamental Kernel menjadi authority tertinggi di dalam SPOS setelah ratifikasi Founder. Foundation `constitution/` mengelola source map, ratification record, dan amendment record; Governance menerjemahkan Constitution tanpa mengubahnya.

Governance Engine menerjemahkan Constitution menjadi authority, ownership, decision, delegation, lifecycle governance, compliance, dan AI governance. Developer Mode menetapkan perilaku operasional AI; Session Engine menetapkan unit kerja, lifecycle orchestration, state, continuity, report, dan closure; Execution Engine menetapkan prosedur eksekusi, checkpoint, recovery, evidence, serta completion criteria; Git Engine menetapkan workflow version control; Documentation Engine menetapkan tata kelola dokumentasi; Quality Engine menetapkan quality gate, DoD, metrik, audit kualitas, dan continuous improvement. Seluruh engine mempertahankan ownership domain dan tidak dapat memberi approval kepada dirinya sendiri. Core tidak memiliki requirement produk; engine tambahan hanya dibuat melalui session terpisah dengan owner, status, dependency, dan review eksplisit.
