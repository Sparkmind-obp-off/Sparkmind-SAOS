# SparkMind SAOS

SparkMind AI Operating System (SAOS) adalah repository dokumentasi yang menjadi Single Source of Truth (SSOT) untuk fondasi, identitas, standar, dan pengetahuan operasional SparkMind.

> Status repository: Foundation Architecture, Knowledge System, dan SPOS baseline terdokumentasi. Constitution SPOS-002, Developer Mode SPOS-003, Execution SPOS-004, Git SPOS-005, Documentation SPOS-006, Quality SPOS-007, Governance SPOS-008, serta Session Engine SPOS-009 berstatus `In Review`; Kernel Session 001 masih berupa kerangka terstruktur.

## Tujuan

Repository ini dirancang untuk:

- menjaga satu sumber kebenaran bagi keputusan dan dokumen SparkMind;
- memisahkan prinsip fundamental dari aturan operasional dan implementasi produk;
- memastikan perubahan dapat direview, dilacak, dan dipelihara;
- menyediakan fondasi vendor-agnostic bagi manusia dan AI yang bekerja untuk SparkMind.

## Ruang Lingkup Saat Ini

### Selesai

- Kernel awal dengan 10 dokumen terstruktur.
- Dokumentasi root repository.
- Standar penamaan, folder, Markdown, dokumentasi, commit, branch, dan versioning.
- Pedoman kontribusi, keamanan, dukungan, dan perilaku komunitas.
- Struktur lengkap `01-foundation/` dengan 13 domain terdokumentasi.
- Foundation Architecture, dependency, alur informasi, dan boundary antarlapisan.
- Knowledge System dengan sembilan domain, arsitektur pengetahuan, lifecycle, governance, dan ownership model.
- Baseline SparkMind Prompt Operating System (SPOS) dengan Constitution, Governance, Developer Mode, Session, Execution, Git, Documentation, Quality Engine, architecture, session framework, dan prompt templates.

### Belum Diimplementasikan

- Isi final dokumen Kernel dan persetujuan Founder.
- Isi substantif serta approval artefak pada setiap domain Foundation dan Knowledge System.
- Ratifikasi Founder atas Constitution SPOS.
- Approval operasional dan activation record Governance, Developer Mode, Session, Execution, Git, Documentation, serta Quality Engine.
- Report Engine dan engine substantif SPOS lainnya.
- Spesifikasi atau implementasi produk, termasuk Hifz AI.
- Kode aplikasi, database, deployment, dan CI/CD.

## Struktur Repository

```text
sparkmind-saos/
├── 00-kernel/             # Dokumen fundamental dan normatif
├── 01-foundation/         # Pengetahuan, governance, library, dan playbook
├── 99-prompt-os/          # Kontrak workflow, session, dan prompt AI
├── docs/
│   └── standards/         # Standar pengelolaan repository
├── reports/
│   └── sessions/          # Laporan hasil setiap session
├── README.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── CHANGELOG.md
├── LICENSE
├── SECURITY.md
└── SUPPORT.md
```

Direktori baru hanya ditambahkan ketika memiliki tujuan, owner, dan dokumen indeks yang jelas. Konvensi lengkap tersedia di [`docs/standards/FOLDER_CONVENTION.md`](docs/standards/FOLDER_CONVENTION.md).

## Indeks Dokumentasi

### Kernel

- [`00-kernel/README.md`](00-kernel/README.md) — kedudukan dan indeks Kernel.
- [`00-kernel/VISION.md`](00-kernel/VISION.md) — arah jangka panjang.
- [`00-kernel/MISSION.md`](00-kernel/MISSION.md) — mandat utama.
- [`00-kernel/PHILOSOPHY.md`](00-kernel/PHILOSOPHY.md) — pandangan dasar.
- [`00-kernel/PRINCIPLES.md`](00-kernel/PRINCIPLES.md) — prinsip pengarah.
- [`00-kernel/VALUES.md`](00-kernel/VALUES.md) — nilai inti.
- [`00-kernel/ETHICS.md`](00-kernel/ETHICS.md) — batas etis.
- [`00-kernel/DOCTRINE.md`](00-kernel/DOCTRINE.md) — cara berpikir stabil.
- [`00-kernel/CANON.md`](00-kernel/CANON.md) — hierarki sumber normatif.
- [`00-kernel/TERMINOLOGY.md`](00-kernel/TERMINOLOGY.md) — kosakata terkontrol.

### Foundation

- [`01-foundation/README.md`](01-foundation/README.md) — indeks 13 domain Foundation.
- [`01-foundation/FOUNDATION_ARCHITECTURE.md`](01-foundation/FOUNDATION_ARCHITECTURE.md) — peran, dependency, alur informasi, dan boundary.
- [`01-foundation/knowledge/README.md`](01-foundation/knowledge/README.md) — indeks Knowledge System.
- [`01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md`](01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md) — alur, lifecycle, role, dan dependency pengetahuan.
- [`01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) — naming, versioning, review, approval, deprecation, archiving, dan cross-reference.
- [`01-foundation/governance/README.md`](01-foundation/governance/README.md) — indeks governance Foundation dan record yang diturunkan dari Governance Engine.

### Prompt Operating System

- [`99-prompt-os/README.md`](99-prompt-os/README.md) — tujuan, posisi, struktur, boundary, dan status SPOS.
- [`99-prompt-os/00-core/CONSTITUTION.md`](99-prompt-os/00-core/CONSTITUTION.md) — authority konstitusional SPOS, prinsip dasar, hierarchy, decision principles, dan amendment policy.
- [`99-prompt-os/00-core/GOVERNANCE_ENGINE.md`](99-prompt-os/00-core/GOVERNANCE_ENGINE.md) — control plane authority, ownership, decision, delegation, lifecycle governance, compliance, audit, escalation, exception, dan AI Governance Policy.
- [`99-prompt-os/00-core/DEVELOPER_MODE_ENGINE.md`](99-prompt-os/00-core/DEVELOPER_MODE_ENGINE.md) — standar perilaku operasional AI, decision gates, autonomy boundary, repository policy, rollback, dan validation.
- [`99-prompt-os/00-core/SESSION_ENGINE.md`](99-prompt-os/00-core/SESSION_ENGINE.md) — identity, lifecycle orchestration, type, state, continuity, dependency antarsession, report, closure, dan AI Session Policy.
- [`99-prompt-os/00-core/EXECUTION_ENGINE.md`](99-prompt-os/00-core/EXECUTION_ENGINE.md) — prosedur eksekusi, task classification, validation checkpoints, failure/recovery, evidence, dan Definition of Done.
- [`99-prompt-os/00-core/GIT_ENGINE.md`](99-prompt-os/00-core/GIT_ENGINE.md) — branch, commit, Pull Request/review, merge, push, release, protection, audit, recovery, dan AI Git automation.
- [`99-prompt-os/00-core/DOCUMENTATION_ENGINE.md`](99-prompt-os/00-core/DOCUMENTATION_ENGINE.md) — prinsip, jenis, lifecycle, metadata, versioning, ownership, review, publication, archive, dan AI Documentation Policy.
- [`99-prompt-os/00-core/QUALITY_ENGINE.md`](99-prompt-os/00-core/QUALITY_ENGINE.md) — prinsip kualitas, sembilan quality gate, Definition of Done, metrik, audit, CAPA, continuous improvement, dan AI Quality Policy.
- [`99-prompt-os/00-core/SPOS_ARCHITECTURE.md`](99-prompt-os/00-core/SPOS_ARCHITECTURE.md) — komponen, dependency, lifecycle, execution flow, dan quality gates.
- [`99-prompt-os/03-sessions/SESSION_TEMPLATE.md`](99-prompt-os/03-sessions/SESSION_TEMPLATE.md) — kontrak standar session.
- [`99-prompt-os/05-prompts/README.md`](99-prompt-os/05-prompts/README.md) — placeholder System, User, dan Task Prompt.

### Repository

- [`CONTRIBUTING.md`](CONTRIBUTING.md) — alur kontribusi dan review.
- [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) — standar perilaku.
- [`CHANGELOG.md`](CHANGELOG.md) — riwayat perubahan terkurasi.
- [`SECURITY.md`](SECURITY.md) — pelaporan kerentanan dan informasi sensitif.
- [`SUPPORT.md`](SUPPORT.md) — jalur bantuan dan pertanyaan.
- [`docs/standards/README.md`](docs/standards/README.md) — indeks standar repository.
- [`reports/sessions/README.md`](reports/sessions/README.md) — indeks laporan session.

## Panduan Penggunaan

1. Mulai dari dokumen ini untuk memahami ruang lingkup repository.
2. Baca [`00-kernel/README.md`](00-kernel/README.md) sebelum mengusulkan perubahan fundamental.
3. Baca [`01-foundation/README.md`](01-foundation/README.md) dan arsitekturnya sebelum menambah pengetahuan atau playbook.
4. Ikuti [`01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) sebelum membuat atau memperbarui artefak Knowledge System.
5. Baca [`99-prompt-os/00-core/CONSTITUTION.md`](99-prompt-os/00-core/CONSTITUTION.md), [`99-prompt-os/00-core/GOVERNANCE_ENGINE.md`](99-prompt-os/00-core/GOVERNANCE_ENGINE.md), [`99-prompt-os/00-core/DEVELOPER_MODE_ENGINE.md`](99-prompt-os/00-core/DEVELOPER_MODE_ENGINE.md), [`99-prompt-os/00-core/SESSION_ENGINE.md`](99-prompt-os/00-core/SESSION_ENGINE.md), [`99-prompt-os/00-core/EXECUTION_ENGINE.md`](99-prompt-os/00-core/EXECUTION_ENGINE.md), [`99-prompt-os/00-core/GIT_ENGINE.md`](99-prompt-os/00-core/GIT_ENGINE.md), [`99-prompt-os/00-core/DOCUMENTATION_ENGINE.md`](99-prompt-os/00-core/DOCUMENTATION_ENGINE.md), [`99-prompt-os/00-core/QUALITY_ENGINE.md`](99-prompt-os/00-core/QUALITY_ENGINE.md), dan [`99-prompt-os/README.md`](99-prompt-os/README.md) sebelum menyusun workflow atau session AI; gunakan hanya artefak dengan status dan authority yang sesuai.
6. Ikuti [`CONTRIBUTING.md`](CONTRIBUTING.md) dan seluruh standar di `docs/standards/`.
7. Bedakan isi berstatus draft, verified, approved, deprecated, atau superseded.
8. Gunakan issue atau jalur privat yang sesuai sebelum mengirim perubahan sensitif.

## Data dan Teknologi

Repository ini hanya berisi Kernel, Foundation, SPOS, dan dokumentasi tata kelola repository. Tidak ada data model aplikasi, database, layanan penyimpanan, API, runtime, atau tech stack yang dipilih pada tahap ini.

## URL dan Status

- **Repository remote:** <https://github.com/Sparkmind-obp-off/Sparkmind-SAOS>
- **Production:** Belum tersedia; deployment berada di luar ruang lingkup Foundation.
- **Platform target:** Belum ditetapkan.
- **Status:** Foundation, Knowledge System, dan SPOS-009 baseline aktif sebagai dokumentasi; Constitution, Governance, Developer Mode, Session, Execution, Git, Documentation, serta Quality Engine menunggu approval yang sah dan repository belum berupa aplikasi.
- **Terakhir diperbarui:** 2026-07-15.

## Lisensi

Repository ini bersifat proprietary. Tidak ada hak penggunaan, penyalinan, modifikasi, atau distribusi yang diberikan tanpa izin tertulis. Lihat [`LICENSE`](LICENSE).
