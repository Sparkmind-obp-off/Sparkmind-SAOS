# SparkMind Prompt Operating System (`99-prompt-os`)

> Status: SPOS-009 baseline — Constitution, Governance, Developer Mode, Session, Execution, Git, Documentation, dan Quality Engine tersedia sebagai `In Review`; authority operasional menunggu approval yang sah.

## Apa Itu SPOS

SparkMind Prompt Operating System (SPOS) adalah lapisan dokumentasi operasional yang menerjemahkan arah, batas, dan pengetahuan SparkMind menjadi kontrak kerja AI yang modular. SPOS mengorganisasi architecture, template, rule, session, playbook, dan prompt agar pekerjaan AI dapat direncanakan, dieksekusi, direview, serta dilaporkan secara konsisten.

SPOS bukan produk, aplikasi, model AI, atau runtime vendor. Pada baseline ini SPOS juga belum mengeksekusi pekerjaan secara otomatis. Constitution, Governance, Developer Mode, Session, Execution, Git, Documentation, dan Quality Engine telah didokumentasikan sebagai `In Review`; semuanya bukan runtime otomatis atau bukti approval.

## Mengapa SPOS Ada

SPOS dibangun untuk:

- menghilangkan pengulangan aturan panjang pada setiap prompt;
- menyediakan satu lokasi kanonik bagi workflow AI Engineering;
- memisahkan aturan stabil dari objective session yang dinamis;
- membuat dependency, quality gate, keputusan, dan hasil eksekusi dapat ditelusuri;
- menjaga perilaku AI konsisten lintas tool, vendor, tim, dan produk;
- memungkinkan perubahan aturan dilakukan satu kali tanpa membuat salinan prompt tandingan.

## Posisi dan Hubungan

```text
Founder authority + 00-kernel source material
  │
  ▼
SPOS Constitution (highest authority within SPOS when ratified)
  │
  ▼
01-foundation governance, knowledge & approved guidance
  │
  ▼
SAOS
  │ operating model for the SparkMind AI ecosystem
  └── 99-prompt-os (SPOS)
         │ Governance + Developer Mode + Session + Execution + Git + Documentation + Quality contracts
         ▼
Engineering / AI Agents
         │ bounded execution
         ▼
Products
         └── evidence, outcomes, incidents & feedback ──► Foundation / SPOS review
```

### Hubungan dengan SAOS

SAOS adalah operating model yang lebih luas untuk ekosistem AI SparkMind. SPOS merupakan lapisan operasional prompt dan workflow di dalam SAOS: SPOS menentukan bagaimana instruksi dirakit dan dijalankan, tetapi tidak menggantikan identitas, governance, architecture, atau keputusan strategis SAOS.

### Hubungan dengan Constitution, Kernel, dan Foundation

[`00-core/CONSTITUTION.md`](00-core/CONSTITUTION.md) adalah authority tertinggi di dalam SPOS setelah ratifikasi Founder. Dokumen tersebut merakit prinsip fundamental dari Kernel menjadi batas konstitusional SPOS tanpa menghapus source history atau mengklaim approval otomatis.

Foundation mengelola ratification/source map, governance, knowledge, decision, pattern, standard, dan guidance. SPOS merujuk serta mengoperasionalkan artefak tersebut; SPOS tidak memberi approval kepada dirinya sendiri atau kepada artefak Kernel dan Foundation.

Jika isi SPOS berkonflik dengan Constitution atau authority yang lebih tinggi, eksekusi harus dihentikan pada batas terdampak, konflik dicatat, lalu dieskalasikan. Selama Constitution belum diratifikasi, consumer wajib memperlakukannya sebagai `In Review` dan menggunakan sumber approved yang benar-benar tersedia.

### Hubungan dengan Products

Products mengonsumsi hasil kerja AI yang dijalankan melalui SPOS sesuai konteks produknya. SPOS tidak memiliki requirement, logika bisnis, data, atau keputusan produk. Feedback, outcome, dan insiden dari Products menjadi input review; semuanya tidak otomatis mengubah rule SPOS tanpa proses perubahan yang sah.

## Struktur

```text
99-prompt-os/
├── README.md
├── 00-core/
│   ├── README.md
│   ├── CONSTITUTION.md
│   ├── DEVELOPER_MODE_ENGINE.md
│   ├── EXECUTION_ENGINE.md
│   ├── GIT_ENGINE.md
│   ├── DOCUMENTATION_ENGINE.md
│   ├── QUALITY_ENGINE.md
│   ├── GOVERNANCE_ENGINE.md
│   ├── SESSION_ENGINE.md
│   └── SPOS_ARCHITECTURE.md
├── 01-templates/
│   └── README.md
├── 02-rules/
│   └── README.md
├── 03-sessions/
│   ├── README.md
│   └── SESSION_TEMPLATE.md
├── 04-playbooks/
│   └── README.md
└── 05-prompts/
    ├── README.md
    ├── SYSTEM_TEMPLATE.md
    ├── USER_TEMPLATE.md
    └── TASK_TEMPLATE.md
```

## Komponen

| Komponen | Fungsi | Status terkini |
| --- | --- | --- |
| `00-core/` | Constitution, Governance, Developer Mode, Session, Execution, Git, Documentation, Quality Engine, arsitektur, lifecycle, dan engine inti | Seluruh engine inti `In Review`; architecture tersedia dan runtime belum dibangun |
| `01-templates/` | Kontrak artefak kerja yang dapat digunakan ulang | Kontrak folder tersedia |
| `02-rules/` | Rule modular dengan authority dan precedence eksplisit | Kontrak folder tersedia |
| `03-sessions/` | Instance identity, objective, type, state, scope, authority, dependency, lifecycle, continuity, deliverable, validation, report, dan closure | Session Template SPOS-009 tersedia |
| `04-playbooks/` | Prosedur terurut untuk kelas pekerjaan berulang | Kontrak folder tersedia |
| `05-prompts/` | Template assembly untuk system, user, dan task prompt | Tiga placeholder terstruktur tersedia |

## Aturan SSOT dan Boundary

1. Founder memegang ratifikasi dan amendment authority konstitusional.
2. Constitution adalah authority tertinggi di dalam SPOS setelah diratifikasi.
3. Kernel menyimpan source material fundamental; Foundation mengelola ratification/source map, governance, knowledge, keputusan, pattern, dan panduan lintas domain.
4. SPOS memiliki Constitution serta kontrak eksekusi AI, komposisi prompt, session, dan quality gate yang diturunkan.
5. Products tetap memiliki requirement dan logika bisnis masing-masing.
6. Satu aturan hanya memiliki satu lokasi kanonik; template dan prompt merujuk aturan tersebut, bukan menyalinnya.
7. Artefak `Draft` atau `In Review` tidak boleh diperlakukan sebagai aturan approved.
8. AI boleh menyusun dan mereview draft, tetapi tidak dapat meratifikasi Constitution atau amendment.

## Cara Menggunakan Baseline

1. Baca [`00-core/CONSTITUTION.md`](00-core/CONSTITUTION.md) dan periksa status ratifikasinya.
2. Baca [`00-core/DEVELOPER_MODE_ENGINE.md`](00-core/DEVELOPER_MODE_ENGINE.md) dan periksa status aktivasi serta authority-nya.
3. Baca [`00-core/EXECUTION_ENGINE.md`](00-core/EXECUTION_ENGINE.md) untuk lifecycle, classification, validation, recovery, evidence, dan Definition of Done.
4. Baca [`00-core/GIT_ENGINE.md`](00-core/GIT_ENGINE.md) sebelum branch, commit, Pull Request/review, merge, push, release, protection, backup, atau Git automation.
5. Baca [`00-core/DOCUMENTATION_ENGINE.md`](00-core/DOCUMENTATION_ENGINE.md) sebelum membuat, memperbarui, mereview, mempublikasikan, supersede, atau mengarsipkan dokumentasi.
6. Baca [`00-core/QUALITY_ENGINE.md`](00-core/QUALITY_ENGINE.md) untuk prinsip kualitas, sembilan gate, Definition of Done, metrik, audit, CAPA, dan AI Quality Policy.
7. Baca [`00-core/GOVERNANCE_ENGINE.md`](00-core/GOVERNANCE_ENGINE.md) untuk authority, ownership, decision, delegation, approval, exception, escalation, lifecycle governance, compliance, audit, dan AI Governance Policy.
8. Baca [`00-core/SESSION_ENGINE.md`](00-core/SESSION_ENGINE.md) untuk identity, lifecycle orchestration, type, state, continuity, dependency antarsession, report, closure, dan AI Session Policy.
9. Baca [`00-core/SPOS_ARCHITECTURE.md`](00-core/SPOS_ARCHITECTURE.md).
10. Susun session menggunakan [`03-sessions/SESSION_TEMPLATE.md`](03-sessions/SESSION_TEMPLATE.md).
11. Gunakan placeholder di `05-prompts/` hanya untuk merancang kontrak prompt; jangan menganggapnya engine aktif.
12. Cantumkan dependency, type/state, owner, reviewer, approver, decision class, delegation, quality gate, continuity, dan unresolved conflict.
13. Laporkan evidence dan feedback agar perubahan dapat direview melalui Foundation dan governance.

## Status Implementasi

### Selesai

**SPOS-001**

- Struktur awal enam komponen SPOS.
- Arsitektur, dependency, lifecycle, dan execution flow.
- Session Template standar.
- Placeholder terstruktur untuk System, User, dan Task Prompt.
- Boundary terhadap Kernel, Foundation, Knowledge, Governance, SAOS, dan Products.

**SPOS-002**

- Constitution Engine dengan Vision, Mission, Long-term Purpose, Core Values, Guiding Principles, Ethical Principles, dan Founder Authority.
- Governance Hierarchy, Decision Principles, Amendment Policy, versioning, changelog, audit trail, enforcement, dan source map.
- Cross-review terhadap Kernel, Foundation, Knowledge, Governance, serta SPOS Architecture.

**SPOS-003**

- Developer Mode Engine dengan operational principles, standard workflow, decision gates, autonomous execution, repository interaction, rollback, validation, Git workflow, dan reporting contract.
- Cross-review terhadap Constitution, Foundation, Knowledge, Governance, SPOS Architecture, serta repository standards.
- Activation boundary yang mempertahankan Founder Authority dan status `In Review`.

**SPOS-004**

- Execution Engine dengan lifecycle sebelas tahap, sepuluh task classification, execution rules, enam validation gates, failure/recovery policy, evidence contract, dan Definition of Done.
- Cross-review terhadap Constitution, Developer Mode, Foundation, Knowledge, Governance, SPOS Architecture, Session Template, serta repository standards.
- Penyelarasan precedence repository standards dan deviasi roadmap tanpa membangun Governance Engine atau fitur produk.

**SPOS-005**

- Git Engine dengan branch strategy, Conventional Commits, PR/review/merge policy, push/release workflow, protection, backup, audit, failure/recovery, dan AI Git Automation Policy.
- Cross-review terhadap Constitution, Developer Mode, Execution Engine, Foundation, Governance, SPOS Architecture, contributing flow, serta branch/commit/versioning standards.
- Penyelarasan Git Engine sebagai SSOT detail Git tanpa membangun hosting, CI/CD, protection platform, atau runtime automation.

**SPOS-006**

- Documentation Engine dengan sembilan prinsip utama, enam belas jenis, lifecycle Draft–Archived, struktur, metadata, versioning, cross-reference, ownership, review cadence, change history, code-documentation relationship, dan AI Documentation Policy.
- Cross-review terhadap Constitution, Developer Mode, Execution Engine, Git Engine, Foundation, Governance, Knowledge System, SPOS Architecture, serta repository documentation standards.
- Penyelarasan Documentation Engine sebagai SSOT policy lintas ekosistem tanpa membangun CMS, portal, publication platform, deployment, atau automation runtime.

**SPOS-007**

- Quality Engine dengan sebelas prinsip utama, sembilan quality gate, Definition of Done, delapan metrik inti, finding/severity, audit, CAPA, continuous improvement, dan AI Quality Policy.
- Cross-review terhadap Constitution, Developer Mode, Execution Engine, Git Engine, Documentation Engine, Governance, Foundation, Knowledge System, SPOS Architecture, serta Session Template.
- Penyelarasan Quality Engine sebagai SSOT kualitas lintas ekosistem tanpa membangun dashboard, CI/CD, test framework, atau automation runtime.

**SPOS-008**

- Governance Engine dengan sepuluh prinsip, delapan role authority, decision classification, delegation contract, ownership matrix, governance lifecycle, compliance/audit, violation/CAPA, escalation/exception, dan AI Governance Policy.
- Cross-review terhadap Constitution, Developer Mode, Execution, Git, Documentation, Quality Engine, Foundation, Knowledge System, SPOS Architecture, dan Session Template.
- Penyelarasan Governance sebagai control plane SSOT tanpa membangun IAM, dashboard, compliance platform, policy runtime, database, atau automation.

**SPOS-009**

- Session Engine dengan tiga belas tahap lifecycle, dua belas session type, delapan state beserta transition rules, continuity/resume/recovery, dependency antarsession, context preservation, handoff, closure, dan AI Session Policy.
- Cross-review terhadap Constitution, Governance, Developer Mode, Execution, Git, Documentation, Quality Engine, Foundation, Knowledge System, SPOS Architecture, dan Session Template.
- Penyelarasan Session Engine sebagai SSOT identity/lifecycle/state/continuity session tanpa membangun registry service, scheduler, queue, dashboard, database, agent memory, atau automation runtime.

### Belum Diimplementasikan

- Ratifikasi Founder atas Constitution.
- Approval operasional dan activation record Developer Mode Engine.
- Report Engine.
- Approval operasional dan activation record Governance, Session, Execution, Git, Documentation, serta Quality Engine.
- Rule substantif, template pekerjaan khusus, playbook, prompt compiler, atau runtime otomatis.
- Role/delegation/ownership/decision/exception/audit registry; session registry/index dan transition authority; human role acceptance; access enforcement; dan approval SPOS final.
- Integrasi vendor, aplikasi, database, deployment, atau CI/CD.

## Referensi

- [`../00-kernel/README.md`](../00-kernel/README.md)
- [`../01-foundation/README.md`](../01-foundation/README.md)
- [`../01-foundation/FOUNDATION_ARCHITECTURE.md`](../01-foundation/FOUNDATION_ARCHITECTURE.md)
- [`../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md`](../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md)
- [`../docs/standards/README.md`](../docs/standards/README.md)
