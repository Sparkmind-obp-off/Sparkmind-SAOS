# SPOS Architecture

> Status: Draft baseline SPOS-006 — diselaraskan dengan Constitution, Developer Mode Engine, Execution Engine, Git Engine, dan Documentation Engine `In Review`; bukan runtime aktif.

## Tujuan

Mendefinisikan posisi, komponen, dependency, lifecycle, execution flow, dan boundary SparkMind Prompt Operating System (SPOS) agar workflow AI dapat dibangun secara modular tanpa mengambil alih otoritas Kernel, Foundation, Knowledge, Governance, SAOS, Engineering, atau Products.

## Sasaran Arsitektur

1. **Constitution-led:** seluruh komponen SPOS menurunkan authority dari [`CONSTITUTION.md`](CONSTITUTION.md) setelah ratifikasi Founder.
2. **Modular:** rule stabil, template, session, playbook, dan prompt dipisahkan menurut tanggung jawab.
3. **Traceable:** setiap instruksi dapat ditelusuri ke sumber, status, owner, dan hasil validasi.
4. **Derived, not duplicated:** SPOS merujuk sumber upstream dan tidak membuat salinan normatif tandingan.
5. **Deterministic assembly:** input, precedence, output, dan stop condition dinyatakan sebelum eksekusi.
6. **Human-governed:** AI dapat menyusun, mengeksekusi dalam batas, dan memberi evidence; Founder memegang ratifikasi konstitusional.
7. **Vendor-agnostic:** kontrak inti tidak bergantung pada model atau tool tertentu.
8. **Fail-closed on authority conflicts:** konflik otoritas menghentikan bagian eksekusi yang terdampak sampai terselesaikan.

## Posisi Arsitektur

```text
Applicable law, safety obligations, and Founder authority
                     │
                     ▼
┌───────────────────────────────────────────┐
│ 00-kernel                                 │
│ Fundamental source material and history   │
└────────────────────┬──────────────────────┘
                     ▼
┌───────────────────────────────────────────┐
│ 99-prompt-os/00-core/CONSTITUTION.md      │
│ Highest authority within SPOS when ratified│
└────────────────────┬──────────────────────┘
                     ▼
┌───────────────────────────────────────────┐
│ 01-foundation + SAOS / SPOS               │
│ Records, governance, knowledge, workflows │
└───────────────┬───────────────────────────┘
                ▼
        AI Agents / Engineering
                ▼
             Products
                │
                └─ evidence & feedback ──► Foundation / SPOS review
```

SPOS berada di bawah operating model SAOS dan menggunakan Kernel serta Foundation sebagai sumber dan dependency. Di dalam SPOS, Constitution adalah authority tertinggi setelah ratifikasi Founder. Nomor folder `99` menyatakan lapisan operasional lintas domain, bukan authority di atas hukum, keselamatan, atau Founder.

## Komponen SPOS

| Komponen | Tanggung jawab | Input | Output |
| --- | --- | --- | --- |
| `00-core/` | Menyimpan Constitution, Developer Mode, Execution Engine, Git Engine, Documentation Engine, architecture, dan engine contracts | Founder authority, Kernel source material, Foundation, SAOS constraints | Constitutional boundaries, operational behavior, execution lifecycle, Git governance, documentation governance, dan engine specifications |
| `01-templates/` | Menyediakan struktur artefak reusable | Rule dan metadata contract | Draft artefak yang konsisten |
| `02-rules/` | Menyimpan aturan atomik dan precedence | Authority serta governance approved | Constraint dan quality gate terkomposisi |
| `03-sessions/` | Membatasi satu unit kerja | Objective, scope, dependency, acceptance criteria | Deliverable, evidence, dan session report |
| `04-playbooks/` | Mengurutkan prosedur untuk pekerjaan berulang | Rules, templates, approved patterns | Langkah eksekusi dan checklist |
| `05-prompts/` | Merakit kontrak system, user, dan task | Rules, session, playbook, context | Prompt package untuk executor |

## Dependency

### Dependency normatif

```text
Applicable law, safety obligations, and Founder authority
  └─ Kernel fundamental source material
       └─ SPOS Constitution (highest authority within SPOS after ratification)
            └─ Governance
                 └─ Policies
                      └─ Standards
                           └─ Playbooks
                                └─ Session Instructions
                                     └─ Prompt / task / local preference
```

Authority dan constraint mengalir ke bawah. Evidence dan feedback mengalir ke atas untuk review, bukan sebagai perubahan aturan otomatis. Foundation `constitution/` memelihara source map serta ratification/amendment record, sementara Governance mengatur penerapan Constitution.

### Precedence minimum

Jika dua instruksi bertentangan, urutan acuan adalah:

1. hukum, kewajiban keselamatan, dan batas platform yang berlaku;
2. authority serta keputusan Founder yang sah;
3. Constitution yang telah diratifikasi;
4. Governance approved;
5. Policies approved;
6. Standards approved;
7. Playbooks approved dan sesuai konteks;
8. Session Instructions;
9. task, prompt instance, dan preferensi implementasi lokal.

Hierarki internal SPOS pada butir 3–8 mengikuti [`CONSTITUTION.md`](CONSTITUTION.md). Kernel menyediakan sumber fundamental bagi Constitution dan tidak boleh dimanipulasi oleh artefak downstream. Dokumen yang belum approved tidak memiliki authority operasional hanya karena tersedia atau telah di-commit.

### Dependency antarkomponen

```text
00-core ──────► 02-rules ──────┐
    │                           │
    ├────────► 01-templates ────┤
    │                           ▼
    └────────► 04-playbooks ► 03-sessions
                                │
                                ▼
                           05-prompts
                                │
                                ▼
                             Executor
```

`05-prompts/` adalah assembly boundary, bukan sumber authority baru. Prompt hasil assembly harus mempertahankan referensi ke dependency kanoniknya.

## Lifecycle SPOS

### Lifecycle artefak

```text
Proposed → Draft → In Review → Approved → Deprecated → Archived
                              └──────────► Superseded
```

- **Proposed:** kebutuhan atau perubahan dicatat.
- **Draft:** kontrak sedang disusun dan belum berlaku.
- **In Review:** siap diperiksa authority, safety, consistency, dan operability.
- **Approved:** dapat digunakan sesuai scope dan versi yang dinyatakan.
- **Superseded:** digantikan artefak kanonik lain.
- **Deprecated:** masih tersedia untuk transisi, tidak untuk penggunaan baru.
- **Archived:** dipertahankan untuk audit atau histori.

Perubahan status mengikuti governance upstream. Mapping detail terhadap lifecycle `Draft → Review → Approved → Published → Updated → Archived`, termasuk state `In Review`, `Deprecated`, dan `Superseded`, mengikuti [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md). Commit atau keberadaan file tidak sama dengan approval.

### Lifecycle session

Lifecycle kanonik mengikuti [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md):

```text
Receive Objective
  → Analyze Context
  → Read Repository
  → Identify Dependencies
  → Plan Execution
  → Execute Incrementally
  → Validate Results
  → Update Documentation
  → Perform Git Workflow
  → Generate Session Report
  → Complete Session
```

Intake, module selection, prompt assembly, dan preflight tetap menjadi aktivitas arsitektural yang dipetakan ke tahap Receive/Analyze/Identify/Plan. Session berstatus `Blocked` jika dependency wajib hilang, authority conflict belum selesai, akses yang diperlukan tidak tersedia, atau quality gate kritis gagal.

## Execution Flow

1. **Intake:** terima objective, context, constraint, dan expected outcome.
2. **Classify:** tentukan domain, risiko, reversibility, dan authority yang diperlukan.
3. **Resolve upstream:** muat sumber kanonik Kernel, Foundation, Governance, Knowledge, dan SAOS yang relevan beserta statusnya.
4. **Create session contract:** kunci scope, non-scope, deliverable, success criteria, dan stop condition.
5. **Select modules:** pilih engine, rule, template, dan playbook yang approved serta sesuai versi; gunakan [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) sebagai baseline perilaku, [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) sebagai baseline proses, [`GIT_ENGINE.md`](GIT_ENGINE.md) sebagai baseline Git, dan [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) sebagai baseline dokumentasi hanya sesuai status serta authority aktualnya.
6. **Assemble prompts:** susun System → User → Task tanpa menduplikasi sumber authority.
7. **Preflight:** periksa konflik, missing input, security, capability, approval, dan rencana validasi.
8. **Execute:** lakukan pekerjaan hanya dalam scope serta rekam keputusan dan evidence.
9. **Validate:** jalankan acceptance criteria, quality gate, cross-review, dan pemeriksaan boundary.
10. **Deliver:** terapkan hasil pada source of truth yang ditetapkan; jangan mengganti hasil repository dengan artefak manual bila integrasi tersedia.
11. **Report:** catat outcome, perubahan, validation result, commit/push bila tersedia, kendala, dan technical debt.
12. **Feedback:** kirim gap, insiden, dan pembelajaran ke owner upstream untuk review; jangan mengubah rule secara otomatis.

## Kontrak Input dan Output

### Input minimum

- objective dan expected outcome;
- scope serta non-scope;
- source of truth dan dependency;
- constraint, risk, dan authority;
- deliverable dan acceptance criteria;
- capability serta akses yang tersedia.

### Output minimum

- deliverable pada lokasi kanonik;
- daftar perubahan dan keputusan;
- evidence validasi serta quality gate;
- unresolved issue, risk, dan technical debt;
- status completion atau blocked;
- session report dan trace Git bila tersedia.

## Quality Gates Baseline

Sebelum session ditutup, pastikan:

- dependency dan status sumber dapat ditelusuri;
- tidak ada duplikasi authority atau SSOT;
- scope dan non-scope dipatuhi;
- instruction conflict telah diselesaikan atau dilaporkan sebagai blocker;
- output memenuhi acceptance criteria;
- perubahan sensitif, strategis, atau irreversible memiliki approval yang tepat;
- laporan tidak mengklaim commit, push, deployment, atau approval yang belum terverifikasi.

## Boundary dan Ownership

| Layer | Memiliki | Tidak dimiliki SPOS |
| --- | --- | --- |
| Founder | Ratifikasi Constitution, amendment, dan resolusi konstitusional | SPOS dan AI tidak mengambil authority Founder |
| Kernel | Source material fundamental: Vision, Mission, Philosophy, Values, Principles, Ethics, Doctrine, Canon, Terminology | SPOS Constitution merakitnya tanpa menghapus histori atau mengklaim ratifikasi otomatis |
| Foundation | Ratification/source map, governance, knowledge, decisions, patterns, cross-domain guidance | SPOS tidak memberi approval kepada artefak Foundation atau memindahkan ownership |
| Knowledge System | Provenance, curation, lifecycle, discovery, learning | SPOS tidak mengubah knowledge menjadi policy otomatis |
| Governance | Authority, approval, escalation, exception | SPOS hanya mengeksekusi dan mencatat sesuai kebijakan |
| SAOS | Operating model ekosistem AI | SPOS tidak menggantikan keseluruhan SAOS |
| Engineering | Standar dan implementasi teknis | SPOS tidak memiliki keputusan teknis domain |
| Products | Requirement, data, logic, dan outcome produk | SPOS tidak menentukan kebutuhan bisnis |

## Failure dan Escalation

- Konflik authority: hentikan area terdampak dan eskalasikan dengan sumber yang bertentangan.
- Input wajib hilang: tandai `Blocked` dan sebutkan input yang diperlukan.
- Capability atau akses gagal: pertahankan pekerjaan yang valid, jangan memalsukan completion, dan laporkan recovery step.
- Quality gate gagal: perbaiki dalam scope atau tandai session belum selesai.
- Feedback produk: catat sebagai evidence; owner upstream memutuskan perubahan.

## Review Checklist SPOS-006

- [x] Tujuan, komponen, dependency, lifecycle, dan execution flow terdokumentasi.
- [x] Constitution menjadi authority tertinggi di dalam SPOS setelah ratifikasi Founder.
- [x] Governance hierarchy selaras dengan Constitution.
- [x] Posisi SPOS terhadap SAOS dijelaskan.
- [x] Boundary terhadap Founder, Kernel, Foundation, Knowledge, Governance, Engineering, dan Products eksplisit.
- [x] Folder `99` tidak ditafsirkan sebagai authority di atas hukum, keselamatan, atau Founder.
- [x] Prompt template diposisikan sebagai assembly boundary, bukan sumber normatif.
- [x] Developer Mode Engine diposisikan sebagai kontrak perilaku operasional, bukan runtime atau authority baru.
- [x] Execution Engine diposisikan sebagai kontrak proses kanonik untuk lifecycle, classification, validation, recovery, evidence, dan completion.
- [x] Git Engine diposisikan sebagai kontrak kanonik branch, commit, PR/review, merge, push, release, protection, audit, recovery, dan AI Git automation.
- [x] Documentation Engine diposisikan sebagai kontrak kanonik prinsip, jenis, lifecycle, metadata, versioning, ownership, review, publication, archive, dan AI Documentation Policy.
- [x] Decision gates, autonomy boundary, repository interaction, validation, rollback, documentation, Git, dan reporting selaras dengan execution flow.
- [x] Lifecycle arsitektural dan lifecycle Execution Engine dipetakan tanpa membuat dua sumber proses tandingan.
- [x] Update Documentation mendelegasikan detail ke Documentation Engine dan Perform Git Workflow mendelegasikan detail ke Git Engine tanpa membuat policy tandingan.
- [x] Lifecycle dokumentasi dipetakan terhadap lifecycle artefak SPOS tanpa menghapus status existing.
- [x] Baseline tidak mengklaim runtime, CMS, publication platform, hosting, platform protection, atau automation yang belum dibangun/diverifikasi.
