# SPOS Core

> Status: SPOS-002 baseline; Constitution `In Review`, architecture tetap Draft sampai ratifikasi Founder.

## Tujuan

Menyimpan Constitution, arsitektur, dan kontrak engine inti yang mengatur authority, lifecycle, precedence, execution flow, quality gate, reporting, dan integrasi komponen SPOS.

## Artefak Aktif

- [`CONSTITUTION.md`](CONSTITUTION.md) — authority tertinggi di dalam SPOS, prinsip dasar, governance hierarchy, decision principles, dan amendment policy.
- [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) — posisi, komponen, dependency, lifecycle, execution flow, dan boundary SPOS.

## Boundary

Constitution merakit sumber fundamental Kernel menjadi authority tertinggi di dalam SPOS setelah ratifikasi Founder. Foundation `constitution/` mengelola source map, ratification record, dan amendment record; Governance menerjemahkan Constitution tanpa mengubahnya.

Core tidak dapat memberi approval kepada dirinya sendiri dan tidak memiliki requirement produk. Engine tambahan hanya dibuat melalui session terpisah dengan owner, status, dependency, dan review yang eksplisit.
