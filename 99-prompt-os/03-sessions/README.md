# SPOS Sessions

> Status: Draft baseline SPOS-001.

## Tujuan

Menyimpan kontrak session yang membatasi satu unit kerja melalui objective, scope, dependency, deliverable, quality gate, Git trace, dan completion state.

## Artefak Aktif

- [`SESSION_TEMPLATE.md`](SESSION_TEMPLATE.md) — template standar untuk session SPOS dan session SAOS yang menggunakan SPOS.

## Aturan

- Satu session memiliki satu outcome utama dan satu source of truth.
- Session instance harus memiliki ID unik, status, owner, reviewer, dan success criteria.
- Session tidak boleh memperluas authority upstream.
- Session yang gagal memenuhi dependency atau Git Definition of Done wajib dilaporkan `Blocked` bila workflow tersebut diwajibkan.
- Laporan hasil tetap disimpan di [`../../reports/sessions/`](../../reports/sessions/); folder ini menyimpan kontrak eksekusi, bukan laporan historis.
