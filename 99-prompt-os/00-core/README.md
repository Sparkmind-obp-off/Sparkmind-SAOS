# SPOS Core

> Status: SPOS-005 baseline; Constitution, Developer Mode Engine, Execution Engine, dan Git Engine `In Review`, architecture tetap Draft sampai authority yang sah mengaktifkannya.

## Tujuan

Menyimpan Constitution, arsitektur, dan kontrak engine inti yang mengatur authority, lifecycle, precedence, execution flow, quality gate, reporting, dan integrasi komponen SPOS.

## Artefak Aktif

- [`CONSTITUTION.md`](CONSTITUTION.md) — authority tertinggi di dalam SPOS, prinsip dasar, governance hierarchy, decision principles, dan amendment policy.
- [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) — standar perilaku operasional AI, decision gates, autonomy boundary, repository policy, rollback, validation, dan reporting.
- [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) — standar proses eksekusi, lifecycle, task classification, validation gates, failure/recovery, evidence, dan Definition of Done.
- [`GIT_ENGINE.md`](GIT_ENGINE.md) — standar branch, commit, Pull Request/review, merge, push, release, protection, audit, recovery, dan otomatisasi Git AI.
- [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) — posisi, komponen, dependency, lifecycle, execution flow, dan boundary SPOS.

## Boundary

Constitution merakit sumber fundamental Kernel menjadi authority tertinggi di dalam SPOS setelah ratifikasi Founder. Foundation `constitution/` mengelola source map, ratification record, dan amendment record; Governance menerjemahkan Constitution tanpa mengubahnya.

Developer Mode menerjemahkan prinsip Constitution menjadi perilaku operasional AI; Execution Engine menerjemahkan perilaku tersebut menjadi lifecycle dan gate satu session; Git Engine menetapkan workflow version control pada tahap Git. Ketiganya tidak mengambil authority Governance atau domain owner. Core tidak dapat memberi approval kepada dirinya sendiri dan tidak memiliki requirement produk. Engine tambahan hanya dibuat melalui session terpisah dengan owner, status, dependency, dan review yang eksplisit.
