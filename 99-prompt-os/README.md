# SparkMind Prompt Operating System (`99-prompt-os`)

> Status: SPOS-002 baseline — Constitution tersedia sebagai `In Review`; authority operasional menunggu ratifikasi Founder.

## Apa Itu SPOS

SparkMind Prompt Operating System (SPOS) adalah lapisan dokumentasi operasional yang menerjemahkan arah, batas, dan pengetahuan SparkMind menjadi kontrak kerja AI yang modular. SPOS mengorganisasi architecture, template, rule, session, playbook, dan prompt agar pekerjaan AI dapat direncanakan, dieksekusi, direview, serta dilaporkan secara konsisten.

SPOS bukan produk, aplikasi, model AI, atau runtime vendor. Pada baseline ini SPOS juga belum mengeksekusi pekerjaan secara otomatis. Constitution Engine telah didokumentasikan, sedangkan runtime dan engine operasional lainnya belum dibangun.

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
00-kernel
  │ authority & constraints
  ▼
01-foundation
  │ governance, knowledge & approved guidance
  ▼
SAOS
  │ operating model for the SparkMind AI ecosystem
  └── 99-prompt-os (SPOS)
         │ AI execution contracts, sessions & prompts
         ▼
Engineering / AI Agents
         │ bounded execution
         ▼
Products
         └── evidence, outcomes, incidents & feedback ──► Foundation
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
| `00-core/` | Constitution, arsitektur, lifecycle, execution model, dan engine inti | Constitution `In Review` dan architecture tersedia; runtime belum dibangun |
| `01-templates/` | Kontrak artefak kerja yang dapat digunakan ulang | Kontrak folder tersedia |
| `02-rules/` | Rule modular dengan authority dan precedence eksplisit | Kontrak folder tersedia |
| `03-sessions/` | Objective, scope, deliverable, validasi, dan laporan eksekusi | Session Template tersedia |
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
2. Baca [`00-core/SPOS_ARCHITECTURE.md`](00-core/SPOS_ARCHITECTURE.md).
3. Susun session menggunakan [`03-sessions/SESSION_TEMPLATE.md`](03-sessions/SESSION_TEMPLATE.md).
4. Gunakan placeholder di `05-prompts/` hanya untuk merancang kontrak prompt; jangan menganggapnya engine aktif.
5. Cantumkan dependency, status, owner, reviewer, quality gate, dan unresolved conflict.
6. Laporkan evidence dan feedback agar perubahan dapat direview melalui Foundation dan governance.

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

### Belum Diimplementasikan

- Ratifikasi Founder atas Constitution.
- Developer Mode, Execution, Git, Documentation, Quality, Session, dan Report Engine.
- Rule substantif, template pekerjaan khusus, playbook, prompt compiler, atau runtime otomatis.
- Authority matrix dan approval SPOS final.
- Integrasi vendor, aplikasi, database, deployment, atau CI/CD.

## Referensi

- [`../00-kernel/README.md`](../00-kernel/README.md)
- [`../01-foundation/README.md`](../01-foundation/README.md)
- [`../01-foundation/FOUNDATION_ARCHITECTURE.md`](../01-foundation/FOUNDATION_ARCHITECTURE.md)
- [`../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md`](../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md)
- [`../docs/standards/README.md`](../docs/standards/README.md)
