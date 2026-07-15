# SPOS Architecture

> Status: Draft baseline SPOS-012 — diselaraskan dengan Constitution, Foundation/Master Knowledge System, Governance, Developer Mode, Session, Execution, Git, Documentation, Quality, Report Engine, dan Master Prompt System `In Review`; bukan runtime aktif.

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
│ Governance control, records, knowledge    │
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
| `00-core/` | Menyimpan Constitution, Governance, Developer Mode, Session, Execution, Git, Documentation, Quality, Report Engine, Master Prompt System, architecture, dan engine contracts | Founder authority, Kernel source material, Foundation, SAOS constraints | Constitutional boundaries, governance control plane, operational behavior, session orchestration/state/continuity, execution procedure, Git/documentation/quality/reporting governance, prompt architecture/assembly governance, dan engine specifications |
| `01-templates/` | Menyediakan struktur artefak reusable | Rule dan metadata contract | Draft artefak yang konsisten |
| `02-rules/` | Menyimpan aturan atomik dan precedence | Authority serta governance approved | Constraint dan quality gate terkomposisi |
| `03-sessions/` | Menginstansiasi Session Engine untuk satu unit kerja | Objective, type, scope, authority, dependency, acceptance criteria | Session contract/state history, deliverable, evidence, continuity, closure, dan report |
| `04-playbooks/` | Mengurutkan prosedur untuk pekerjaan berulang | Rules, templates, approved patterns | Langkah eksekusi dan checklist |
| `05-prompts/` | Menginstansiasi template system, user, dan task sesuai Master Prompt System | Compatible rules, session, playbook, classified context, prompt-layer contract | Versioned prompt package untuk executor; bukan runtime atau authority baru |

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

Authority dan constraint mengalir ke bawah. Evidence dan feedback mengalir ke atas untuk review, bukan sebagai perubahan aturan otomatis. Foundation `constitution/` memelihara source map serta ratification/amendment record, sementara [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) mengatur penerapan Constitution melalui authority, ownership, decision, delegation, lifecycle, compliance, dan audit.

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

`05-prompts/` adalah assembly boundary, bukan sumber authority baru. [`MASTER_PROMPT_SYSTEM.md`](MASTER_PROMPT_SYSTEM.md) menjadi kontrak kanonik hierarchy, layer, Core/Session/Execution/Report/Validation/Review/Approval Prompt, assembly, dependency, lifecycle, versioning, governance, traceability, security, serta quality standard. Prompt hasil assembly harus mempertahankan referensi ke dependency kanonik, version set, trust classification, capability boundary, dan preflight evidence.

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

Lifecycle orchestration kanonik mengikuti [`SESSION_ENGINE.md`](SESSION_ENGINE.md):

```text
Session Initialization
  → Context Loading
  → Repository Analysis
  → Objective Validation
  → Planning
  → Execution
  → Continuous Validation
  → Documentation Update
  → Git Workflow
  → Quality Review
  → Governance Check
  → Session Report
  → Session Closure
```

Prosedur sebelas tahap [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) dipetakan ke lifecycle ini dan tetap menjadi SSOT untuk eksekusi incremental, validation checkpoint, failure/recovery, evidence, serta completion criteria. Session Engine memiliki identity, type, state, continuity, dependency antarsession, report, dan closure. Intake, module selection, prompt assembly, serta preflight dipetakan ke Initialization/Context/Objective Validation/Planning. State `Blocked` digunakan jika dependency wajib hilang, authority conflict belum selesai, akses diperlukan tidak tersedia, atau gate kritis gagal; state lain mengikuti Session Engine.

## Execution Flow

1. **Intake:** terima objective, context, constraint, dan expected outcome.
2. **Classify:** tentukan domain, risiko, reversibility, dan authority yang diperlukan.
3. **Resolve upstream:** muat sumber kanonik Kernel, Foundation, Governance, Master Knowledge System, dan SAOS yang relevan beserta version, status, provenance, confidence, applicability, classification, rights, contradiction, serta limitation yang material.
4. **Create session contract:** kunci scope, non-scope, deliverable, success criteria, dan stop condition.
5. **Select modules:** pilih engine, rule, template, dan playbook yang approved serta sesuai versi; gunakan [`../../01-foundation/knowledge/MASTER_KNOWLEDGE_SYSTEM.md`](../../01-foundation/knowledge/MASTER_KNOWLEDGE_SYSTEM.md) untuk claim/evidence, provenance/lineage, source assessment, taxonomy/relationship, curation, retrieval/consumption, knowledge security/rights, quality, serta learning; gunakan [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) untuk authority/ownership/decision, [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) untuk perilaku, [`SESSION_ENGINE.md`](SESSION_ENGINE.md) untuk unit/lifecycle/state/continuity, [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) untuk prosedur eksekusi, [`GIT_ENGINE.md`](GIT_ENGINE.md) untuk Git, [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) untuk dokumentasi, [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) untuk kualitas, [`REPORT_ENGINE.md`](REPORT_ENGINE.md) untuk taxonomy/lifecycle/struktur/evidence laporan, dan [`MASTER_PROMPT_SYSTEM.md`](MASTER_PROMPT_SYSTEM.md) untuk hierarchy/layer/assembly/dependency/security prompt hanya sesuai status serta authority aktualnya.
6. **Assemble prompts:** resolve compatible dependency manifest, muat Core, bind Session dan Execution, pasang Validation/Review/Report/Approval interface yang berlaku, klasifikasikan instruction/context/evidence/untrusted data, package knowledge dengan canonical source/version/status/provenance/confidence/applicability/classification/rights/limitation, lalu rekam package manifest; jangan menduplikasi sumber authority.
7. **Preflight:** periksa konflik, missing input, status/version/compatibility, prompt injection, context truncation, security, capability, approval, dan rencana validasi.
8. **Execute:** lakukan pekerjaan hanya dalam scope serta rekam keputusan dan evidence.
9. **Validate:** jalankan acceptance criteria, quality gate, cross-review, dan pemeriksaan boundary.
10. **Deliver:** terapkan hasil pada source of truth yang ditetapkan; jangan mengganti hasil repository dengan artefak manual bila integrasi tersedia.
11. **Report:** ikuti Report Engine untuk metadata, scope/objective, summary, deliverable, evidence, validation, decision, risk, debt, lesson, next action, approval, references, lifecycle, versioning, serta traceability.
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
- session report tervalidasi sesuai Report Engine dan trace Git bila tersedia.

## Quality Gates Baseline

Urutan review kanonik mengikuti [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md): Objective → Requirement → Architecture → Implementation → Documentation → Git → Security & Privacy → Governance → Final Approval. Execution Engine tetap menentukan checkpoint lifecycle dan completion state.

Sebelum session ditutup, pastikan dependency/status dapat ditelusuri, tidak ada SSOT tandingan, scope dipatuhi, konflik diselesaikan atau menjadi blocker, acceptance criteria serta gate yang berlaku lulus, approval yang tepat tersedia, dan laporan tidak membuat klaim tanpa evidence.

## Boundary dan Ownership

| Layer | Memiliki | Tidak dimiliki SPOS |
| --- | --- | --- |
| Founder | Ratifikasi Constitution, amendment, dan resolusi konstitusional | SPOS dan AI tidak mengambil authority Founder |
| Kernel | Source material fundamental: Vision, Mission, Philosophy, Values, Principles, Ethics, Doctrine, Canon, Terminology | SPOS Constitution merakitnya tanpa menghapus histori atau mengklaim ratifikasi otomatis |
| Foundation | Ratification/source map, governance, knowledge, decisions, patterns, cross-domain guidance | SPOS tidak memberi approval kepada artefak Foundation atau memindahkan ownership |
| Master Knowledge System | Claim/evidence, provenance/lineage, source assessment, curation, taxonomy/relationship, lifecycle, discovery/retrieval, consumption, traceability, protection, quality, learning, dan AI Knowledge Policy | SPOS/prompt/retrieval tidak mengubah knowledge menjadi instruction, decision, policy, atau approval otomatis |
| Governance | Authority, ownership, delegation, decision, approval, escalation, exception, lifecycle, audit, dan AI governance | Engine lain mengeksekusi serta mencatat tanpa mengambil authority |
| Master Prompt System | Hierarchy/layer prompt, package assembly, dependency, lifecycle, versioning, traceability, security, evaluation, dan approval interface | Tidak menciptakan authority, keputusan manusia, runtime, atau ownership domain |
| SAOS | Operating model ekosistem AI | SPOS tidak menggantikan keseluruhan SAOS |
| Engineering | Standar dan implementasi teknis | SPOS tidak memiliki keputusan teknis domain |
| Products | Requirement, data, logic, dan outcome produk | SPOS tidak menentukan kebutuhan bisnis |

## Failure dan Escalation

- Konflik authority: hentikan area terdampak dan eskalasikan dengan sumber yang bertentangan.
- Input wajib hilang: tandai `Blocked` dan sebutkan input yang diperlukan.
- Capability atau akses gagal: pertahankan pekerjaan yang valid, jangan memalsukan completion, dan laporkan recovery step.
- Quality gate gagal: perbaiki dalam scope atau tandai session belum selesai.
- Feedback produk: catat sebagai evidence; owner upstream memutuskan perubahan.

## Review Checklist SPOS-012

- [x] Tujuan, komponen, dependency, lifecycle, dan execution flow terdokumentasi.
- [x] Constitution menjadi authority tertinggi di dalam SPOS setelah ratifikasi Founder.
- [x] Governance hierarchy dan Governance Engine selaras dengan Constitution.
- [x] Posisi SPOS terhadap SAOS dijelaskan.
- [x] Boundary terhadap Founder, Kernel, Foundation, Knowledge, Governance, Engineering, dan Products eksplisit.
- [x] Folder `99` tidak ditafsirkan sebagai authority di atas hukum, keselamatan, atau Founder.
- [x] Prompt template diposisikan sebagai assembly boundary, bukan sumber normatif.
- [x] Developer Mode Engine diposisikan sebagai kontrak perilaku operasional, bukan runtime atau authority baru.
- [x] Session Engine diposisikan sebagai kontrak kanonik identity, lifecycle orchestration, type, state, continuity, dependency antarsession, report, dan closure.
- [x] Execution Engine diposisikan sebagai kontrak proses kanonik untuk prosedur eksekusi, classification, validation checkpoint, recovery, evidence, dan completion criteria.
- [x] Git Engine diposisikan sebagai kontrak kanonik branch, commit, PR/review, merge, push, release, protection, audit, recovery, dan AI Git automation.
- [x] Documentation Engine diposisikan sebagai kontrak kanonik prinsip, jenis, lifecycle, metadata, versioning, ownership, review, publication, archive, dan AI Documentation Policy.
- [x] Quality Engine diposisikan sebagai kontrak kanonik prinsip kualitas, sembilan quality gate, Definition of Done, metrik, audit, CAPA, continuous improvement, dan AI Quality Policy.
- [x] Governance Engine diposisikan sebagai control plane kanonik untuk authority, ownership, delegation, decision, approval, exception, escalation, lifecycle, compliance, audit, dan AI governance.
- [x] Report Engine diposisikan sebagai kontrak kanonik taxonomy, report lifecycle, struktur, evidence/traceability, validation, correction, publication, archive, aggregation, dan AI Reporting Policy.
- [x] Master Prompt System diposisikan sebagai kontrak kanonik hierarchy/layer, prompt package assembly, dependency, lifecycle, versioning, governance, traceability, security, quality, dan approval interface tanpa menjadi runtime atau authority baru.
- [x] Master Knowledge System diposisikan sebagai kontrak integratif claim/evidence, provenance/lineage, source assessment, taxonomy/relationship, lifecycle, curation, retrieval/consumption, protection, quality, learning, dan AI Knowledge Policy tanpa mengambil authority domain atau membangun runtime.
- [x] Core, Session, Execution, Report, Validation, Review, dan Approval Prompt dipetakan ke engine owner masing-masing tanpa SSOT tandingan.
- [x] Decision gates, autonomy boundary, repository interaction, validation, rollback, documentation, quality, Git, dan reporting selaras dengan execution flow.
- [x] Tiga belas tahap lifecycle Session Engine dan sebelas tahap prosedur Execution Engine dipetakan tanpa membuat dua sumber proses tandingan.
- [x] Continuous Validation/Quality Review mendelegasikan detail ke Quality Engine, Documentation Update ke Documentation Engine, Git Workflow ke Git Engine, Governance Check ke Governance Engine, dan Session Report ke Report Engine tanpa membuat policy tandingan.
- [x] Lifecycle dokumentasi dipetakan terhadap lifecycle artefak SPOS tanpa menghapus status existing.
- [x] Baseline tidak mengklaim prompt compiler/registry service, knowledge/search/retrieval service, RAG, vector/graph database, crawler, agent memory/runtime, quality/reporting dashboard, analytics platform, report generator, test framework, CI/CD, CMS, publication platform, hosting, platform protection, atau automation yang belum dibangun/diverifikasi.
