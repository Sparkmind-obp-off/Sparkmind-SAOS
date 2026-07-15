# Session Reports

## Tujuan

Folder ini menyimpan laporan hasil setiap session SparkMind SAOS untuk menjaga ketertelusuran objective, perubahan, evidence, validasi, keputusan, risiko, technical debt, lesson, dan rekomendasi berikutnya. Standard kanonik mengikuti [`../../99-prompt-os/00-core/REPORT_ENGINE.md`](../../99-prompt-os/00-core/REPORT_ENGINE.md).

## Aturan

- Gunakan nama `SESSION-NNN.md` untuk roadmap SAOS dan `SPOS-NNN.md` untuk roadmap Prompt Operating System, masing-masing dengan tiga digit.
- Satu laporan mewakili satu session yang telah dijalankan dan mengikuti lifecycle/status Report Engine.
- Laporan mencatat keadaan pada reporting period/as-of time, memiliki claim-evidence trace, dan tidak menggantikan dokumen kanonik.
- Keputusan penting yang ditemukan selama session harus diterapkan pada dokumen sumber yang tepat.
- Jangan memasukkan secret, credential, data pribadi, atau transcript mentah yang tidak diperlukan.
- Cantumkan repository, branch, baseline/final commit, status push, serta verifikasi lokal/remote jika Git tersedia.
- Setiap report wajib tervalidasi, dapat direproduksi secara proporsional, dan tidak memuat secret atau data sensitif yang tidak diperlukan.
- Correction, supersession, publication, retention, serta archive mengikuti Report Engine dan Documentation Engine.

## Struktur Minimum

1. Metadata, objective, scope, dan summary.
2. Deliverables serta dokumen dibuat/diperbarui.
3. Evidence dan validation results.
4. Decisions, risks, technical debt, dan lessons learned.
5. Branch, repository, commit, push, serta remote verification.
6. Next actions, approval/status, references, dan appendix bila diperlukan.

## Indeks

- Session 001 — Kernel foundation; tercatat dalam histori Git pada commit `7a2428e`.
- [`SESSION-002.md`](SESSION-002.md) — Repository Foundation & Project Identity.
- [`SESSION-003.md`](SESSION-003.md) — SparkMind Foundation Architecture.
- [`SESSION-004.md`](SESSION-004.md) — SparkMind Knowledge System.
- [`SPOS-001.md`](SPOS-001.md) — SparkMind Prompt Operating System Bootstrap.
- [`SPOS-002.md`](SPOS-002.md) — SparkMind Constitution Engine.
- [`SPOS-003.md`](SPOS-003.md) — SparkMind Developer Mode Engine.
- [`SPOS-004.md`](SPOS-004.md) — SparkMind Execution Engine.
- [`SPOS-005.md`](SPOS-005.md) — SparkMind Git Engine.
- [`SPOS-006.md`](SPOS-006.md) — SparkMind Documentation Engine.
- [`SPOS-007.md`](SPOS-007.md) — SparkMind Quality Engine.
- [`SPOS-008.md`](SPOS-008.md) — SparkMind Governance Engine.
- [`SPOS-009.md`](SPOS-009.md) — SparkMind Session Engine.
- [`SPOS-010.md`](SPOS-010.md) — SparkMind Report Engine.
