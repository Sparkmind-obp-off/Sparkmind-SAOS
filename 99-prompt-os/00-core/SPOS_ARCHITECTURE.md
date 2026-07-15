# SPOS Architecture

> Status: Draft baseline SPOS-001 — architecture contract untuk review, bukan engine aktif.

## Tujuan

Mendefinisikan posisi, komponen, dependency, lifecycle, execution flow, dan boundary SparkMind Prompt Operating System (SPOS) agar workflow AI dapat dibangun secara modular tanpa mengambil alih otoritas Kernel, Foundation, Knowledge, Governance, SAOS, Engineering, atau Products.

## Sasaran Arsitektur

1. **Modular:** rule stabil, template, session, playbook, dan prompt dipisahkan menurut tanggung jawab.
2. **Traceable:** setiap instruksi dapat ditelusuri ke sumber, status, owner, dan hasil validasi.
3. **Derived, not duplicated:** SPOS merujuk sumber upstream dan tidak membuat salinan normatif.
4. **Deterministic assembly:** input, precedence, output, dan stop condition dinyatakan sebelum eksekusi.
5. **Human-governed:** AI dapat menyusun, mengeksekusi dalam batas, dan memberi evidence; authority manusia tetap berlaku.
6. **Vendor-agnostic:** kontrak inti tidak bergantung pada model atau tool tertentu.
7. **Fail-closed on authority conflicts:** konflik otoritas menghentikan bagian eksekusi yang terdampak sampai terselesaikan.

## Posisi Arsitektur

```text
┌───────────────────────────────────────────┐
│ 00-kernel                                 │
│ Fundamental authority and constraints     │
└────────────────────┬──────────────────────┘
                     ▼
┌───────────────────────────────────────────┐
│ 01-foundation                             │
│ Governance, knowledge, decisions, guidance│
└────────────────────┬──────────────────────┘
                     ▼
┌───────────────────────────────────────────┐
│ SAOS                                      │
│ SparkMind AI ecosystem operating model    │
│   └─ 99-prompt-os / SPOS                  │
│      AI workflow and prompt contracts     │
└───────────────┬───────────────────────────┘
                ▼
        AI Agents / Engineering
                ▼
             Products
                │
                └─ evidence & feedback ──► Foundation / SPOS review
```

SPOS berada di bawah operating model SAOS dan menggunakan Kernel serta Foundation sebagai upstream. Nomor folder `99` menyatakan lapisan operasional lintas domain, bukan tingkat authority tertinggi.

## Komponen SPOS

| Komponen | Tanggung jawab | Input | Output |
| --- | --- | --- | --- |
| `00-core/` | Mendefinisikan architecture dan engine contracts | Kernel, Foundation, SAOS constraints | Execution model dan engine specifications |
| `01-templates/` | Menyediakan struktur artefak reusable | Rule dan metadata contract | Draft artefak yang konsisten |
| `02-rules/` | Menyimpan aturan atomik dan precedence | Authority serta governance approved | Constraint dan quality gate terkomposisi |
| `03-sessions/` | Membatasi satu unit kerja | Objective, scope, dependency, acceptance criteria | Deliverable, evidence, dan session report |
| `04-playbooks/` | Mengurutkan prosedur untuk pekerjaan berulang | Rules, templates, approved patterns | Langkah eksekusi dan checklist |
| `05-prompts/` | Merakit kontrak system, user, dan task | Rules, session, playbook, context | Prompt package untuk executor |

## Dependency

### Dependency normatif

```text
Kernel authority
  └─ Foundation governance and approved interpretation
       └─ SAOS operating model
            └─ SPOS rules and engines
                 └─ Session / playbook / prompt instance
                      └─ Product-specific execution
```

Dependency hanya mengalir ke bawah untuk authority dan constraint. Feedback mengalir ke atas sebagai evidence, bukan sebagai perubahan aturan otomatis.

### Precedence minimum

Jika dua instruksi bertentangan, urutan acuan adalah:

1. hukum, keamanan, dan batas platform yang berlaku;
2. Kernel approved;
3. Foundation governance dan keputusan approved;
4. SAOS policy approved;
5. SPOS core engine dan rule approved;
6. playbook yang dipilih;
7. session contract;
8. task dan prompt instance;
9. preferensi implementasi lokal.

Baseline ini tidak menetapkan bahwa dokumen yang belum approved memiliki authority. Status dokumen selalu diperiksa sebelum precedence diterapkan.

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

Perubahan status mengikuti governance upstream. Commit atau keberadaan file tidak sama dengan approval.

### Lifecycle session

```text
Intake
  → Resolve dependencies
  → Define objective and scope
  → Select rules, templates, and playbooks
  → Assemble prompt package
  → Preflight quality gate
  → Execute bounded work
  → Validate and cross-review
  → Deliver and report
  → Capture feedback and close / block
```

Session berstatus `Blocked` jika dependency wajib hilang, authority conflict belum selesai, akses yang diperlukan tidak tersedia, atau quality gate kritis gagal.

## Execution Flow

1. **Intake:** terima objective, context, constraint, dan expected outcome.
2. **Classify:** tentukan domain, risiko, reversibility, dan authority yang diperlukan.
3. **Resolve upstream:** muat sumber kanonik Kernel, Foundation, Governance, Knowledge, dan SAOS yang relevan beserta statusnya.
4. **Create session contract:** kunci scope, non-scope, deliverable, success criteria, dan stop condition.
5. **Select modules:** pilih engine, rule, template, dan playbook yang approved serta sesuai versi.
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
| Kernel | Vision, Mission, Philosophy, Values, Principles, Ethics, Doctrine, Canon, Terminology fundamental | SPOS tidak menetapkan ulang sumber normatif |
| Foundation | Governance, knowledge, decisions, patterns, cross-domain guidance | SPOS tidak memberi approval atau memindahkan ownership |
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

## Review Checklist SPOS-001

- [x] Tujuan, komponen, dependency, lifecycle, dan execution flow terdokumentasi.
- [x] Posisi SPOS terhadap SAOS dijelaskan.
- [x] Boundary terhadap Kernel, Foundation, Knowledge, Governance, Engineering, dan Products eksplisit.
- [x] Folder `99` tidak ditafsirkan sebagai authority tertinggi.
- [x] Prompt template diposisikan sebagai assembly boundary, bukan sumber normatif.
- [x] Baseline tidak mengklaim engine atau automation yang belum dibangun.
