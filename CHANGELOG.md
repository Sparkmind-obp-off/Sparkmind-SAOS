# Changelog

Seluruh perubahan penting pada SparkMind SAOS didokumentasikan dalam file ini.

Format mengikuti prinsip [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) dan versioning repository mengikuti [`docs/standards/VERSIONING_CONVENTION.md`](docs/standards/VERSIONING_CONVENTION.md).

## [Unreleased]

### Added

- Dokumentasi root repository: README, contribution guide, code of conduct, security policy, support policy, license, dan changelog.
- Standar repository untuk naming, folder, Markdown, dokumentasi, commit, branch, dan versioning.
- Struktur laporan session untuk menjaga ketertelusuran pekerjaan.
- Konfigurasi dasar editor dan Git ignore yang vendor-agnostic.
- Struktur lengkap `01-foundation/` dengan README untuk constitution, governance, knowledge, wisdom, principles, values, ethics, decision library, pattern library, anti-pattern library, terminology, research, dan playbooks.
- Dokumentasi Foundation Architecture yang menjelaskan peran, dependency, alur informasi, boundary, dan posisi terhadap Kernel, SAOS, Engineering, serta Products.
- Laporan Session 002 dan Session 003 untuk melengkapi traceability.
- SparkMind Knowledge System dengan sembilan domain: concepts, glossary, architecture, standards, best practices, decisions, references, learning, dan onboarding.
- Knowledge Architecture dan Knowledge Governance untuk alur, lifecycle, ownership, naming, versioning, review, approval, deprecation, archiving, serta referensi silang.
- Laporan Session 004 dan handoff lintas session.
- Baseline `99-prompt-os/` untuk SparkMind Prompt Operating System (SPOS), termasuk arsitektur, kontrak setiap komponen, Session Template, dan placeholder System/User/Task Prompt.
- Laporan SPOS-001 dan pembaruan handoff menuju pembangunan engine berikutnya.
- Constitution Engine SPOS-002 dengan Vision, Mission, Long-term Purpose, Core Values, Guiding Principles, Ethical Principles, Founder Authority, Governance Hierarchy, Decision Principles, Amendment Policy, enforcement, dan source map.
- Laporan SPOS-002 serta penyelarasan Canon, Foundation Constitution, Governance, SPOS Architecture, indeks, dan handoff.
- Developer Mode Engine SPOS-003 dengan operational principles, standard workflow, decision gates, autonomous execution policy, repository interaction policy, rollback, validation, Git workflow, failure handling, dan activation boundary.
- Laporan SPOS-003 serta penyelarasan SPOS Core, SPOS Architecture, indeks repository, dan handoff.
- Execution Engine SPOS-004 dengan lifecycle sebelas tahap, sepuluh task classification, execution rules, enam validation gates, failure/recovery policy, evidence contract, dan Definition of Done.
- Laporan SPOS-004 serta penyelarasan SPOS Core, SPOS Architecture, precedence repository standards, indeks repository, dan handoff.
- Git Engine SPOS-005 dengan branch strategy, Conventional Commits, Pull Request/review/merge policy, push/release workflow, repository protection, backup, audit, failure/recovery, dan AI Git Automation Policy.
- Laporan SPOS-005 serta penyelarasan Developer Mode, Execution Engine, SPOS Core/Architecture, Governance index, contributing flow, branch/commit/versioning standards, indeks repository, dan handoff.
- Documentation Engine SPOS-006 dengan sembilan prinsip dokumentasi, enam belas jenis, lifecycle Draft–Archived, struktur, metadata, versioning, cross-reference, ownership, review cadence, change history, code-documentation relationship, validation, publication, archive, dan AI Documentation Policy.
- Laporan SPOS-006 serta penyelarasan Developer Mode, Execution Engine, Git Engine, SPOS Core/Architecture, Governance, Knowledge Governance, Documentation Convention, repository index, dan handoff.
- Quality Engine SPOS-007 dengan sebelas prinsip, sembilan quality gate, Definition of Done, delapan metrik inti, evidence contract, finding/severity, exception, audit, CAPA, continuous improvement, dan AI Quality Policy.
- Laporan SPOS-007 serta penyelarasan Developer Mode, Execution Engine, Git Engine, Documentation Engine, SPOS Core/Architecture, Governance, Foundation, Knowledge Governance, Session Template, repository index, dan handoff.
- Governance Engine SPOS-008 dengan sepuluh prinsip, delapan role authority, decision classification, delegation, ownership matrix, governance lifecycle, compliance/audit, violation/CAPA, escalation/exception, dan AI Governance Policy.
- Laporan SPOS-008 serta penyelarasan seluruh engine, Foundation Governance, Knowledge Governance, SPOS Architecture, Session Template, repository index, dan handoff.

### Reviewed

- Struktur dan 10 dokumen Kernel hasil Session 001.
- Dokumentasi Repository Foundation hasil Session 002.
- Cross-review Session 001–003 untuk konflik, duplikasi, placeholder, dan konsistensi struktur.
- Cross-review Session 001–004 dengan boundary eksplisit antara Knowledge System, Kernel Terminology, Foundation Decision Library, patterns, wisdom, research, dan repository standards.
- Cross-review SPOS-001 terhadap Kernel, Foundation, Knowledge, Governance, SAOS, Engineering, Products, dan repository conventions.
- Cross-review SPOS-002 terhadap Kernel, Foundation, Knowledge, Governance, dan SPOS Architecture, termasuk resolusi interim lokasi instrumen Constitution dan batas ratifikasi Founder.
- Cross-review SPOS-003 terhadap Constitution, Foundation, Knowledge, Governance, SPOS Architecture, dan repository standards, termasuk batas otonomi serta dependency aktivasi.
- Cross-review SPOS-004 terhadap Constitution, Developer Mode, Foundation, Knowledge, Governance, SPOS Architecture, Session Template, dan repository standards, termasuk penyelarasan precedence Constitution.
- Cross-review SPOS-005 terhadap Constitution, Developer Mode, Execution Engine, Foundation, Governance, SPOS Architecture, contributing flow, serta branch/commit/versioning standards, termasuk pemisahan Git policy kanonik dari profile repository.
- Cross-review SPOS-006 terhadap Constitution, Developer Mode, Execution Engine, Git Engine, Foundation, Governance, Knowledge System, SPOS Architecture, serta documentation/Markdown standards, termasuk pemetaan lifecycle dan pemisahan Documentation Engine dari profile repository.
- Cross-review SPOS-007 terhadap Constitution, Developer Mode, Execution Engine, Git Engine, Documentation Engine, Foundation, Governance, Knowledge System, SPOS Architecture, dan Session Template, termasuk pemisahan quality gate kanonik dari checkpoint lifecycle.
- Cross-review SPOS-008 terhadap Constitution, Developer Mode, Execution Engine, Git Engine, Documentation Engine, Quality Engine, Foundation, Knowledge System, SPOS Architecture, dan Session Template, termasuk pemisahan governance control plane dari lifecycle session dan ownership domain.

## [0.1.0] - 2026-07-15

### Added

- Struktur awal `00-kernel/`.
- Kerangka `README.md`, `VISION.md`, `MISSION.md`, `PHILOSOPHY.md`, `PRINCIPLES.md`, `VALUES.md`, `ETHICS.md`, `DOCTRINE.md`, `CANON.md`, dan `TERMINOLOGY.md`.

[Unreleased]: https://github.com/Sparkmind-obp-off/Sparkmind-SAOS/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/Sparkmind-obp-off/Sparkmind-SAOS/releases/tag/v0.1.0
