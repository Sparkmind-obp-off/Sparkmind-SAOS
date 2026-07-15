# SparkMind Session Engine

> Status: In Review — session-governance baseline SPOS-009; activation as a binding standard requires Founder approval and eligible upstream versions.
>
> Owner: Founder
>
> Reviewer: Founder, Governance owner, AI Executive, Domain Owner, Knowledge Steward, Repository Maintainer, Quality owner, Documentation owner, dan pihak terdampak yang ditunjuk
>
> Approver: Founder atau authority manusia yang didelegasikan secara tertulis untuk session policy non-konstitusional
>
> Version: 0.1.0
>
> Established: 2026-07-15
>
> Effective: setelah approval operasional yang sah, activation record, dan dependency upstream terpenuhi
>
> Review trigger: amendment Constitution; perubahan Governance, Developer Mode, Execution, Git, Documentation, Quality, Foundation, Knowledge System, atau SPOS Architecture; perubahan model kerja AI; insiden session material; state/continuity failure berulang; atau evidence bahwa lifecycle tidak lagi efektif

## 1. Kedudukan dan Tujuan

Session Engine adalah standar permanen untuk mengelola satu unit kerja AI dari intake sampai closure. Engine ini menetapkan identitas dan kontrak session, lifecycle orkestrasi, jenis session, state machine, continuity, dependency, context preservation, handoff, report, serta kebijakan session AI di seluruh ekosistem SparkMind.

Engine ini mengoperasionalkan [`CONSTITUTION.md`](CONSTITUTION.md), [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md), [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md), dan [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md). [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) tetap menjadi sumber kanonik prosedur eksekusi incremental, validation checkpoint, failure/recovery, evidence, dan completion contract di dalam session. Session Engine menjadi sumber kanonik boundary, lifecycle orchestration, state, continuity, dan closure session. Detail Git, dokumentasi, dan kualitas masing-masing mengikuti [`GIT_ENGINE.md`](GIT_ENGINE.md), [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md), dan [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md).

Session Engine bukan aplikasi, orchestrator runtime, scheduler, queue, database, agent memory, workflow produk, atau izin otonomi tanpa batas. Dokumen, status, report, commit, push, atau output sukses tidak memberikan approval, delegation, risk acceptance, maupun authority baru.

Karena Constitution dan seluruh engine upstream masih `In Review`, Session Engine juga `In Review`. Baseline dapat dipakai untuk review dan kerja interim secara fail-closed, tetapi tidak menjadi bukti aktivasi atau approval.

## 2. Scope dan Non-Scope

### 2.1 Scope

Engine mengatur:

- satu objective utama, identitas unik, scope, deliverable, success criteria, owner, dan authority per session;
- lifecycle dari initialization, context loading, analysis, planning, execution, validation, dokumentasi, Git, review, reporting, sampai closure;
- kategori session dan output minimumnya;
- state `Pending`, `Running`, `Blocked`, `Waiting for Approval`, `Review`, `Completed`, `Archived`, dan `Cancelled` beserta transisi;
- dependency, predecessor/successor, continuity, resume, recovery, handoff, context preservation, dan supersession;
- evidence, quality/governance check, Session Report, dan closure record;
- batas AI dalam memulai, menjalankan, menunggu, melanjutkan, serta menutup session.

### 2.2 Non-Scope

Engine tidak:

- meratifikasi Constitution, menyetujui Governance, atau membuat delegation;
- menggantikan lifecycle artefak Governance, Documentation, Knowledge, atau release;
- menduplikasi prosedur teknis Execution, Git, Documentation, atau Quality Engine;
- menetapkan requirement, priority, correctness, atau acceptance milik Product/Domain Owner;
- menyediakan durable storage, queue, lock, timer, notification, dashboard, registry service, atau automation runtime;
- membangun aplikasi, fitur produk, database, deployment, CI/CD, atau integrasi vendor;
- menganggap context percakapan atau memory model sebagai source of truth.

## 3. Prinsip Session

1. **One Objective:** satu session memiliki tepat satu objective utama yang dapat diverifikasi; subtask harus langsung mendukungnya.
2. **Explicit Contract:** scope, non-scope, deliverable, success criteria, dependency, authority, risk, dan stop condition dinyatakan sebelum perubahan material.
3. **Repository and Source First:** repository serta sumber kanonik aktual mengalahkan ingatan, ringkasan, atau cuplikan percakapan.
4. **Bounded Execution:** tindakan dibatasi capability, akses, delegation, decision class, risk ceiling, waktu, dan scope aktual.
5. **State Integrity:** state hanya berubah melalui syarat masuk/keluar dan evidence yang sah; aktivitas teknis tidak otomatis mengubah state.
6. **Continuity by Evidence:** session dapat dilanjutkan dari artefak, commit, report, decision, dan handoff yang tersimpan, bukan hidden context.
7. **Continuous Validation:** objective, scope, dependency, hasil, risiko, dan gate diperiksa sepanjang session, bukan hanya di akhir.
8. **Documentation and Git Traceability:** perubahan source of truth disertai dokumentasi dan Git trace sesuai applicability serta capability.
9. **Human-Governed Approval:** AI dapat mengusulkan dan mengeksekusi dalam mandate, tetapi tidak mengarang approval atau menutup gate manusia.
10. **Honest Closure:** `Completed` hanya untuk objective yang benar-benar selesai; blocker, debt, limitation, dan residual risk dinyatakan.
11. **Recoverable by Design:** increment, checkpoint, safe state, rollback, dan next action disiapkan proporsional terhadap risiko.
12. **Least Disclosure:** continuity evidence cukup untuk audit tanpa menyimpan secret, credential, data pribadi, atau detail sensitif yang tidak diperlukan.

## 4. Kontrak dan Identitas Session

### 4.1 Identitas

Setiap session wajib memiliki ID unik dan stabil. Format repository default:

- `SPOS-NNN` untuk pembangunan engine atau fondasi SPOS;
- `SESSION-NNN` untuk session SAOS/Foundation umum;
- format domain lain hanya jika memiliki namespace owner, uniqueness rule, dan index kanonik.

ID tidak boleh dipakai ulang. Session yang diulang setelah `Completed`, `Archived`, atau `Cancelled` memperoleh ID baru dan merujuk predecessor.

### 4.2 Session Contract Minimum

Sebelum eksekusi material, catat:

| Field | Kewajiban |
| --- | --- |
| ID dan title | Unik, stabil, dan menjelaskan satu unit kerja |
| Objective | Tepat satu outcome utama yang dapat diverifikasi |
| Type | Satu primary type; secondary type hanya bila benar-benar diperlukan |
| State | Salah satu state kanonik beserta timestamp dan alasan |
| Owner/executor | Pihak accountable atas koordinasi dan pihak yang menjalankan |
| Reviewer/approver | Sesuai risiko, independence, dan Governance delegation |
| Authority | Source, decision class, delegation, risk ceiling, effective/expiry |
| Scope/non-scope | Batas perubahan dan larangan eksplisit |
| Deliverable | Nama, lokasi kanonik, dan acceptance criteria |
| Dependency | Source, version/status, owner, penggunaan, dan blocking behavior |
| Context baseline | Repository, branch, commit, environment, source, assumption, unknown |
| Plan | Subtask, gate, evidence, rollback, stop, dan escalation path |
| Continuity | Predecessor, successor bila diketahui, related session, checkpoint, resume point |
| Git | Branch/upstream, workflow, commit strategy, remote requirement |
| Closure | Final state, report, evidence, debt, risk, handoff, archive trigger |

Template implementasi berada di [`../03-sessions/SESSION_TEMPLATE.md`](../03-sessions/SESSION_TEMPLATE.md). Template menginstansiasi kontrak ini dan tidak boleh menjadi policy tandingan.

### 4.3 Session Record

Session record adalah manifest logis yang dapat direpresentasikan dalam Markdown, issue, atau sistem terotorisasi. Record minimum harus machine-checkable secara konseptual, tetapi SPOS-009 tidak membangun schema runtime atau registry service.

```text
session_id
objective
type
state + state_history
owner / executor / reviewer / approver
authority + decision_class + risk
scope / non_scope
deliverables + acceptance_criteria
dependencies + predecessor / related / successor
context_baseline + checkpoints
validation + quality_governance_results
git_trace
documentation_trace
report + closure_record
```

Perubahan material pada objective, scope, authority, risk, deliverable, dependency, atau expected outcome dicatat sebagai contract revision. Jika perubahan membentuk objective independen, buat session baru; jangan mengubah histori agar scope creep tampak sebagai rencana awal.

## 5. Session Lifecycle

Lifecycle ini adalah orkestrasi kanonik session. Tahap dapat kembali ke tahap sebelumnya ketika evidence baru muncul, tetapi gate kritis tidak boleh dilewati. Tahap yang tidak berlaku wajib diberi `Not Applicable` dengan alasan.

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

### 5.1 Session Initialization

**Tujuan:** membuka session yang unik, bounded, dan traceable.

Wajib:

1. tetapkan ID, title, primary type, initial state `Pending`, owner/executor, dan source request;
2. catat objective awal, expected deliverable, urgency, risk awal, dan source of truth;
3. identifikasi predecessor, duplicate session, active conflicting session, atau unrelated working-tree change;
4. tetapkan communication, evidence, dan session-record location;
5. jangan mulai tindakan material sebelum authority dan stop condition awal dinilai.

**Output:** session identity, initial contract, dan intake evidence.

**Exit:** session unik, bukan duplikasi tersembunyi, serta siap memuat context.

### 5.2 Context Loading

**Tujuan:** memuat seluruh context yang diperlukan tanpa menjadikan memory atau transcript sebagai authority.

Muat secara proporsional:

- brief lengkap, constraint, conversation attachment, dan expected outcome;
- Constitution, Governance, engine, policy, standard, playbook, decision, handoff, dan report relevan;
- status, version, owner, effective/expiry, serta conflict setiap sumber;
- fakta, asumsi, unknown, confidence, stakeholder, consumer, security/privacy/safety/legal boundary;
- capability, tool, skill, integration, credential availability, waktu, dan platform limitation.

**Output:** context manifest, source map, fact/assumption/unknown list, dan initial authority/risk map.

**Exit:** context material tersedia atau gap dicatat sebagai blocker/approval need.

### 5.3 Repository Analysis

**Tujuan:** memahami actual state sebelum menulis.

Ikuti Read Repository pada Execution Engine:

1. periksa path, branch, upstream, working tree, remote, dan histori relevan;
2. baca README, architecture, handoff, target, consumer, standard, test/check, serta report sebelumnya;
3. cari implementasi/istilah yang sudah ada dan tentukan lokasi kanonik;
4. identifikasi unrelated work, concurrent change, conflict, stale reference, dan migration impact;
5. catat baseline commit dan file map relevan.

**Output:** repository-state snapshot, baseline, affected map, convention, dan gap analysis.

**Exit:** target/dependency utama telah dibaca dan pekerjaan pihak lain terlindungi.

### 5.4 Objective Validation

**Tujuan:** membuktikan objective jelas, sah, tunggal, feasible, dan sesuai authority.

Validasi:

- satu outcome utama, intended purpose, audience, dan value;
- scope, non-scope, deliverable, acceptance criteria, constraint, serta stop condition;
- primary session type, decision class, risk, reversibility, blast radius, dan dependency;
- owner, reviewer, approver, authority/delegation, serta conflict of interest;
- keselarasan Constitution, Governance, roadmap, dan source of truth;
- tidak ada hidden objective, prohibited work, duplicate session, atau approval palsu.

**Output:** validated objective contract atau clarification/blocker record.

**Exit:** Objective Review `Pass`; session dapat berpindah `Pending → Running`. Jika approval objective wajib, state menjadi `Waiting for Approval`.

### 5.5 Planning

**Tujuan:** menurunkan objective menjadi rencana incremental yang dapat divalidasi dan dipulihkan.

Rencana minimum:

- urutan subtask dan hanya satu subtask aktif bila task tracker tersedia;
- file/system terdampak, dependency order, reviewer, dan decision point;
- expected evidence, quality gate, documentation impact, Git strategy, dan governance check;
- positive/negative/boundary check, rollback, recovery, retry limit, dan safe checkpoint;
- escalation, approval, cancellation, timeout/review trigger, dan completion criteria.

**Output:** execution/quality/continuity plan dan task tracker.

**Exit:** plan feasible, authority/capability memadai, failure path diketahui, dan tidak memperluas scope.

### 5.6 Execution

**Tujuan:** menghasilkan deliverable melalui increment atomik.

Execution mengikuti [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md): baca sebelum edit, ubah concern koheren, validasi increment, lindungi evidence/unrelated work, perbarui tracker, dan re-plan jika risiko berubah. Session state tetap `Running` selama tindakan sah berlangsung.

Tindakan yang memerlukan persetujuan mengubah state menjadi `Waiting for Approval`; dependency/error kritis mengubah state menjadi `Blocked`. AI tidak boleh tetap bertindak pada area yang seharusnya berhenti.

**Output:** deliverable increment, change/evidence log, updated checkpoint, serta failure/recovery record bila ada.

**Exit:** seluruh increment dalam scope selesai dan diff/state siap direview.

### 5.7 Continuous Validation

**Tujuan:** mencegah defect dan scope drift sejak awal hingga closure.

Continuous Validation bukan satu titik setelah Execution. Pada setiap tahap:

- bandingkan state aktual dengan objective, scope, plan, authority, dan acceptance criteria;
- jalankan check proporsional dan pertahankan output aktual;
- revalidate setelah context/dependency/risk/plan berubah, retry, rollback, atau recovery;
- buka kembali tahap/gate yang invalid; jangan mempertahankan `Pass` yang stale;
- klasifikasikan hasil `Pass`, `Fail`, `Blocked`, atau `Not Applicable` dengan alasan.

**Output:** validation history, finding, remediation, dan current confidence.

**Exit:** tidak ada critical failure tersembunyi; gate yang diperlukan untuk dokumentasi dan review siap.

### 5.8 Documentation Update

**Tujuan:** menyinkronkan source kanonik, consumer, dan continuity evidence.

Ikuti Documentation Engine:

1. lakukan impact assessment;
2. perbarui source kanonik dan cross-reference;
3. sinkronkan README, index, architecture, decision, changelog, handoff, migration/release note yang terdampak;
4. bedakan fakta, keputusan, assumption, limitation, debt, risk, dan proposal;
5. perbarui session checkpoint serta resume context;
6. jangan memakai Session Report sebagai SSOT tandingan.

**Output:** dokumentasi aktual, documentation trace, dan continuity package.

**Exit:** semantic, authority, lifecycle, link, security/privacy, dan usability check lulus.

### 5.9 Git Workflow

**Tujuan:** menjaga perubahan dapat ditelusuri dan disinkronkan sesuai policy.

Ikuti Git Engine:

- verifikasi branch/upstream/remote/protection/authority;
- review diff, staged diff, secret/sensitive-data risk, dan validation evidence;
- commit atomik dengan Conventional Commits;
- gunakan PR/reviewer/approval/merge gate sesuai risiko;
- push normal tanpa force atau shared-history rewrite;
- verifikasi hash lokal dan remote.

Jika Git tidak berlaku, catat `Not Applicable`. Jika diwajibkan tetapi capability/authority/access hilang, state menjadi `Blocked`; jangan mengarang hash atau status push.

**Output:** branch, commit/PR/merge/release trace yang aktual atau blocker record.

**Exit:** Git gate lulus atau blocker dilaporkan jujur.

### 5.10 Quality Review

**Tujuan:** menilai fitness for purpose dan Definition of Done sebelum closure.

Jalankan urutan Quality Engine: Objective, Requirement, Architecture, Implementation, Documentation, Git, Security & Privacy, Governance, dan Final Approval. Self-review AI wajib tetapi tidak menggantikan independent/human review. Temuan diperbaiki dalam scope, dikembalikan ke `Running`, atau menyebabkan `Blocked`/`Waiting for Approval`.

Saat paket siap direview, state berubah `Running → Review`.

**Output:** gate result, evidence, reviewer, finding/debt/exception, residual risk, dan remediation status.

**Exit:** seluruh gate kritis `Pass`; approval manusia tetap terpisah jika diwajibkan.

### 5.11 Governance Check

**Tujuan:** memastikan pekerjaan dan closure sah menurut authority serta governance.

Periksa:

- Constitution/Governance alignment, decision class, delegation, risk ceiling, dan effective/expiry;
- owner/executor/reviewer/approver identity, competence, separation, serta conflict of interest;
- scope, capability, data/access, exception, escalation, stop/rollback, dan audit trail;
- approval/risk acceptance yang diwajibkan dan statusnya;
- tidak ada self-approval, privilege expansion, hidden finding, atau false completion.

**Output:** governance result, approval/escalation/exception reference, dan unresolved authority gap.

**Exit:** Governance gate `Pass`; jika approval belum tersedia gunakan `Waiting for Approval`, jika authority conflict gunakan `Blocked`.

### 5.12 Session Report

**Tujuan:** menyediakan closure evidence yang ringkas dan dapat diaudit.

Report minimum memuat:

1. objective, type, scope, dan ringkasan;
2. lifecycle/state history serta dependency penting;
3. dokumen/artefak baru dan diperbarui;
4. cross-review, quality/governance result, dan validation evidence;
5. branch, commit hash, remote, serta status push;
6. failure, rollback, recovery, decision, exception, dan approval bila ada;
7. temuan, technical debt, residual risk, blocker, dan lesson learned;
8. predecessor/successor, continuity/handoff, rekomendasi berikutnya, dan proposed final state.

**Output:** report pada lokasi kanonik yang ditetapkan.

**Exit:** setiap klaim material dapat ditelusuri dan report tidak menggantikan artefak kanonik.

### 5.13 Session Closure

**Tujuan:** menutup session secara jujur, aman, dan dapat dilanjutkan/audit.

Closure wajib:

1. verifikasi satu objective dan seluruh deliverable/acceptance criteria;
2. pastikan tidak ada subtask wajib setengah selesai;
3. verifikasi documentation, Git, quality, governance, report, dan remote evidence yang berlaku;
4. tetapkan final state `Completed` atau `Cancelled`; gunakan `Blocked`/`Waiting for Approval` bila closure belum sah;
5. catat closure time, actor/authority, baseline/final commit, debt, residual risk, retention, dan archive trigger;
6. tetapkan next atomic action dan successor bila follow-up diperlukan;
7. lindungi evidence dan jangan mengubah histori state.

`Completed` menyatakan objective session selesai, bukan bahwa artefak otomatis `Approved` atau `Active`. Session `Archived` adalah state retensi setelah closure, bukan sinonim completion.

**Output:** closure record, final report, handoff, dan archive/retention instruction.

## 6. Pemetaan ke Execution Engine

Session Engine dan Execution Engine tidak membuat dua lifecycle tandingan. Pemetaan tanggung jawabnya:

| Session Lifecycle | Execution Engine | Ownership semantik |
| --- | --- | --- |
| Session Initialization | Receive Objective | Session Engine memiliki identity/intake/state; Execution memiliki cara membentuk kontrak objective |
| Context Loading | Analyze Context + Identify Dependencies | Session memiliki context manifest/continuity; Execution memiliki analisis dependency/risiko |
| Repository Analysis | Read Repository | Execution memiliki prosedur repository analysis; Session merekam baseline/checkpoint |
| Objective Validation | Receive Objective + Pre-Execution/Objective checks | Session memiliki admission dan state transition; Quality memiliki Objective Gate |
| Planning | Plan Execution | Execution memiliki planning procedure; Session memiliki plan record dan continuity |
| Execution | Execute Incrementally | Execution Engine adalah SSOT prosedur eksekusi |
| Continuous Validation | Validate Results + validation gates | Execution memiliki checkpoint; Quality Engine memiliki definisi gate/evidence |
| Documentation Update | Update Documentation | Documentation Engine memiliki detail standard |
| Git Workflow | Perform Git Workflow | Git Engine memiliki detail workflow |
| Quality Review | Validate Results + Definition of Done | Quality Engine memiliki quality model dan gate |
| Governance Check | authority/escalation/completion checks | Governance Engine memiliki decision rights dan approval |
| Session Report | Generate Session Report | Session Engine menetapkan closure/report continuity; Execution menetapkan evidence minimum |
| Session Closure | Complete Session | Session Engine memiliki final state/retention; Execution memiliki completion criteria |

Jika terdapat konflik, policy/domain engine yang memiliki semantik detail tetap menjadi SSOT; Session Engine hanya mengorkestrasi, merekam, dan menegakkan entry/exit tanpa menyalin seluruh rule.

## 7. Session Types

Setiap session memilih satu primary type. Secondary type dapat dicatat jika output benar-benar lintas domain; gate yang lebih ketat berlaku.

| Type | Tujuan | Karakteristik | Output minimum |
| --- | --- | --- | --- |
| **Foundation** | Membentuk atau memperbaiki fondasi lintas ekosistem | Authority-sensitive, durable, dependency luas, derived-not-duplicated | foundation artefact, source/dependency map, cross-domain review, decision/handoff |
| **Architecture** | Menetapkan atau mengubah boundary, component, interface, dependency, dan trade-off | Current/target state, compatibility, migration, reversibility, owner review | architecture document/decision, diagram/model, impact/migration plan |
| **Development** | Mengimplementasikan behavior atau capability yang telah diotorisasi | Requirement-led, incremental, testable, security/privacy-aware | working change, test/evidence, documentation, Git trace |
| **Documentation** | Membuat atau menyinkronkan dokumentasi kanonik | Source/provenance-first, semantic review, least duplication | canonical document/update, link/index synchronization, review evidence |
| **Research** | Menjawab pertanyaan melalui evidence | Source hierarchy, provenance, uncertainty, triangulation, reproducibility | research note, source list, findings, limitation, recommendation/proposal |
| **Governance** | Menetapkan atau mereview authority, policy, ownership, decision, exception, atau audit | Human approval, separation, auditability, conflict/escalation | governance artefact/record, authority matrix, decision/approval evidence |
| **Quality** | Menilai atau meningkatkan fitness, gate, metric, audit, dan CAPA | Risk-based, evidence-driven, independence, anti-gaming | quality plan/review, finding, audit/CAPA, effectiveness evidence |
| **Refactor** | Memperbaiki struktur tanpa intended behavior change | Baseline behavior, small increments, compatibility, regression focus | refactored artefact, before/after evidence, regression result, debt update |
| **Bug Fix** | Menghilangkan defect berdasarkan root cause | Reproduce first, smallest safe fix, blast-radius and regression review | reproduction, root cause, fix, before/after and regression evidence |
| **Release** | Menyiapkan dan mengotorisasi distribusi versioned artefact | Freeze/readiness, compatibility, migration, rollback, approval | release candidate, notes/changelog, approval, tag/release/verification trace |
| **Maintenance** | Menjaga health, dependency, lifecycle, access, atau operability | Routine/reversible, schedule/trigger, no hidden feature | maintenance change, check result, operational record, next review |
| **Knowledge** | Mengkurasi informasi reusable dengan provenance dan lifecycle | Status/confidence-aware, domain/steward review, no automatic policy | knowledge artefact/index, provenance, verification/status, review trigger |

### 7.1 Aturan Pemilihan Type

1. Pilih berdasarkan outcome, bukan file atau tool.
2. Perubahan dokumentasi normatif memakai primary `Governance` atau `Foundation` dengan secondary `Documentation` bila authority berubah.
3. Refactor yang mengubah behavior direklasifikasi menjadi `Development` atau `Bug Fix` pada bagian tersebut.
4. Research tidak otomatis memberi authority untuk Development, Governance, atau Release.
5. Release tidak boleh dipakai untuk menyamarkan development yang belum direview.
6. Session dapat dipecah jika dua type menghasilkan objective independen atau reviewer/rollback boundary berbeda.

## 8. Session State Management

### 8.1 Definisi State

| State | Makna | Syarat minimum |
| --- | --- | --- |
| **Pending** | Session terdaftar tetapi belum admitted untuk eksekusi material | identity/intake ada; objective/authority/dependency masih divalidasi |
| **Running** | Pekerjaan aktif dalam contract, authority, dan plan yang valid | objective valid, executor aktif, gate masuk lulus |
| **Blocked** | Progress aman tidak dapat dilanjutkan karena dependency, error, conflict, access, atau gate kritis | blocker, impact, safe state, owner, unblock condition, next action tercatat |
| **Waiting for Approval** | Pekerjaan berhenti pada decision gate manusia tertentu | approval needed, approver/authority, artefact/version, evidence, deadline tercatat |
| **Review** | Execution utama selesai dan paket sedang dinilai | deliverable/evidence siap; reviewer dan gate ditentukan; tidak ada execution diam-diam |
| **Completed** | Objective dan closure contract terpenuhi | gate wajib lulus, report/trace lengkap, final state terverifikasi |
| **Archived** | Session closed dipertahankan untuk retention/audit dan tidak aktif | closure record, retention, index, successor/reference tersedia |
| **Cancelled** | Session dihentikan sebelum completion melalui keputusan sah | reason/authority, impact, safe state, preserved evidence, successor bila ada |

### 8.2 Transisi yang Diizinkan

```text
Pending ───────────────► Running ───────────────► Review ───────────────► Completed ─► Archived
   │                       │  ▲                    │  │                      │
   │                       │  └──── remediation ───┘  └─ approval/blocker ──┐
   │                       ├────► Blocked ───────────────► Running           │
   │                       ├────► Waiting for Approval ──► Running/Review   │
   └──────────────────────► Cancelled ───────────────────────────────► Archived
                              ▲
                              └── dari state non-terminal dengan authority sah
```

Transisi eksplisit:

- `Pending → Running`: objective, contract, authority, dependency minimum, dan admission gate lulus.
- `Pending → Waiting for Approval`: admission memerlukan approval manusia.
- `Pending → Blocked`: input/dependency/authority kritis belum tersedia.
- `Pending → Cancelled`: duplicate, invalid, superseded, prohibited, atau tidak lagi diperlukan.
- `Running → Blocked`: dependency/error/conflict/gate kritis mencegah progress aman.
- `Running → Waiting for Approval`: decision/exception/risk gate manusia tercapai.
- `Running → Review`: deliverable dan evidence siap direview.
- `Review → Running`: remediation atau perubahan material diperlukan.
- `Review → Blocked`: finding/dependency kritis tidak dapat diselesaikan.
- `Review → Waiting for Approval`: review selesai tetapi Final Approval/risk acceptance belum ada.
- `Review → Completed`: seluruh gate dan closure criteria terpenuhi.
- `Blocked → Running/Review`: unblock condition terverifikasi; kembali ke tahap yang tepat, bukan otomatis ke posisi lama.
- `Blocked → Waiting for Approval`: blocker telah dipersempit menjadi keputusan manusia.
- `Waiting for Approval → Running/Review`: approval sah untuk artefak/version/scope terkait telah dicatat.
- state non-terminal `→ Cancelled`: authority sah menghentikan session dan safe closure selesai.
- `Completed/Cancelled → Archived`: retention/index/handoff selesai.

### 8.3 Transisi yang Dilarang

- `Pending → Completed` tanpa lifecycle/evidence;
- `Running → Completed` tanpa `Review`, quality/governance check, report, dan closure;
- `Blocked` atau `Waiting for Approval → Completed` dengan blocker/approval belum selesai;
- `Completed`, `Archived`, atau `Cancelled → Running`; gunakan successor session baru;
- state berubah hanya karena commit, push, merge, publication, timeout, message, atau tool selesai;
- AI mengubah `Waiting for Approval` menjadi `Running` dengan approval yang dibuatnya sendiri.

### 8.4 Transition Record

Setiap transisi mencatat:

- session ID, from/to state, timestamp, actor, dan authority;
- lifecycle phase/checkpoint;
- trigger, evidence, decision/approval reference, dan affected scope;
- blocker/finding/residual risk bila ada;
- next owner, next action, due/review time, serta rollback/resume point.

State history append-only secara semantik. Koreksi record mempertahankan nilai lama, alasan, actor, dan waktu; jangan menulis ulang histori.

### 8.5 Stale, Timeout, dan Supersession

Tidak ada auto-completion. Session tanpa aktivitas melewati review cadence tetap pada state aktual dan ditandai stale untuk triage. Triage dapat:

- meminta resume;
- mengubah ke `Blocked` bila dependency hilang;
- membatalkan dengan authority;
- membuat successor dan kemudian membatalkan/mengarsipkan predecessor;
- memperbarui deadline tanpa mengubah evidence.

Supersession tidak menghapus session lama. Record predecessor menyebut successor, alasan, carried context, unresolved work, dan ownership transfer.

## 9. Session Continuity

### 9.1 Continuity Package

Agar session dapat dilanjutkan tanpa hidden context, pertahankan:

- ID, objective, type, state/history, owner, authority, decision class, risk;
- scope/non-scope, deliverable, acceptance criteria, dan current progress;
- repository path, branch, baseline/current commit, working-tree state, remote;
- dependency/version/status, predecessor/related/successor, decision/approval/exception;
- file changed, command/check result, finding, failure, retry, rollback, recovery;
- last safe checkpoint, current blocker/approval, next atomic action;
- documentation/Git trace, Session Report draft/final, debt, residual risk;
- context yang sengaja tidak disimpan karena security/privacy.

Package disimpan pada source yang terotorisasi: repository artefact, issue/decision system, commit, report, dan handoff. Chat transcript boleh menjadi evidence tambahan, bukan satu-satunya context.

### 9.2 Melanjutkan Session Sebelumnya

Sebelum resume:

1. verifikasi session belum terminal dan actor memiliki authority;
2. baca continuity package, source kanonik, report/handoff, dan decision setelah checkpoint;
3. periksa branch, working tree, commit lokal/remote, dependency, access, approval, dan concurrent change;
4. bandingkan last known state dengan actual state;
5. revalidate objective, scope, risk, plan, gate, dan stale evidence;
6. catat resume timestamp, actor, context delta, invalidated assumption, dan next action;
7. lanjutkan dari last safe checkpoint, bukan sekadar pesan terakhir.

Jika session terminal, buat successor dengan objective baru/remaining work dan referensi predecessor.

### 9.3 Pemulihan Session Terhenti

Recovery mengikuti Execution Engine:

```text
Detect interruption
  → Freeze affected action
  → Preserve evidence
  → Reconstruct actual state
  → Assess blast radius
  → Stabilize safe state
  → Reconcile repository / remote / dependency
  → Select rollback, resume, re-plan, or cancel
  → Revalidate
  → Record recovery and communicate
```

Jangan blind retry. Operasi partial/unknown dianggap belum berhasil sampai diverifikasi. Jika state tidak dapat direkonstruksi, gunakan `Blocked`, sebutkan evidence yang hilang, dan eskalasikan.

### 9.4 Dependensi Antar-Session

Hubungan yang diizinkan:

- **predecessor/successor:** urutan continuity satu stream kerja;
- **blocks/blocked-by:** output session lain wajib sebelum progress;
- **related-to:** context relevan tanpa dependency completion;
- **supersedes/superseded-by:** pengganti yang mempertahankan histori;
- **parent/child:** hanya untuk decomposition satu objective; child memiliki ID, contract, owner, output, dan state sendiri.

Setiap dependency mencatat ID, output/version/commit yang dibutuhkan, state yang diterima, owner, expected date bila ada, fallback, dan behavior bila berubah. `Completed` pada dependency tidak membuktikan output `Approved`; status artefak tetap diperiksa.

Circular dependency memblokir session terdampak sampai dipecah atau diurutkan oleh owner yang berwenang.

### 9.5 Context Preservation

Context dibagi menjadi:

- **normative:** Constitution, Governance, policy, standard, approval;
- **objective:** brief, scope, deliverable, acceptance criteria;
- **repository:** path, branch, commit, diff, architecture, consumer;
- **decision:** options, rationale, dissent, approval, exception;
- **execution:** plan, progress, tool output, checkpoint, failure/recovery;
- **knowledge:** source, provenance, confidence, terminology;
- **continuity:** state, handoff, next action, debt, risk.

Simpan referensi dan ringkasan yang dapat diverifikasi, bukan copy seluruh sumber. Pin version/commit ketika drift berisiko. Secret, credential, personal data, dan exploit detail sensitif menggunakan reference/secure system, redaction, serta least disclosure.

### 9.6 Handoff

Handoff wajib ketika owner/executor berubah, session berhenti lama, state `Blocked`/`Waiting for Approval`, atau closure memiliki follow-up. Handoff memuat actual state, completed/remaining work, changed file, validation, decision, blocker, risk, next atomic action, serta source links. Penerima melakukan acceptance eksplisit; assignment tool atau mention tidak otomatis menjadi ownership acceptance.

## 10. AI Session Policy

### 10.1 Aturan Wajib

1. Satu objective utama per session.
2. Setiap session menghasilkan artefak/deliverable atau keputusan `Cancelled/Blocked` yang jelas dan traceable.
3. Setiap session memperbarui dokumentasi jika source, behavior, architecture, decision, workflow, setup, status, atau consumer terdampak.
4. Setiap session mengikuti Git Workflow bila ada perubahan pada repository dan capability/authority tersedia.
5. Setiap session menghasilkan Session Report sebelum `Completed` atau closure `Cancelled`; untuk `Blocked`/`Waiting for Approval`, report/checkpoint sementara wajib tersedia.
6. AI wajib memuat repository dan sumber kanonik sebelum perubahan.
7. AI wajib memelihara state, task progress, evidence, checkpoint, serta failure secara jujur.
8. AI wajib menghentikan area terdampak ketika authority, approval, scope, capability, evidence, atau safety boundary gagal.
9. AI tidak boleh self-approve, mengarang reviewer/hash/push/test, menghapus finding, atau menandai `Completed` untuk mandatory work parsial.
10. Objective baru, hidden feature, refactor independen, atau cleanup tidak terkait dipindahkan ke session lain.

### 10.2 Otonomi AI

AI boleh:

- membuat draft session contract, plan, checklist, context map, report, dan handoff;
- menjalankan D0/D1 yang eksplisit sesuai delegation, risk ceiling, dan tool policy;
- mengubah state operasional berdasarkan evidence untuk transisi yang tidak memerlukan approval manusia;
- merekomendasikan blocker, escalation, cancellation, successor, dan archive;
- melakukan self-review, check otomatis, recovery reversible, dan documentation/Git workflow yang diizinkan.

AI tidak boleh:

- memulai D2/D3 atau high/critical work tanpa authority/approval yang diwajibkan;
- menetapkan identity/authority/delegation/acceptance manusia;
- mengubah objective/scope/risk ceiling agar tindakan terlarang tampak sah;
- melanjutkan saat `Waiting for Approval` dengan asumsi silence equals consent;
- menutup `Blocked` sebagai `Completed`;
- memulihkan session terminal dengan mengubah histori; buat successor;
- menyimpan sensitive context di report terbuka untuk kemudahan resume.

### 10.3 Automatic Stop

AI wajib berhenti dan memperbarui state bila:

- objective ganda/materially ambiguous atau bertentangan dengan authority;
- source/dependency/version/owner kritis hilang atau conflict;
- required approval, review independence, access, capability, atau evidence tidak tersedia;
- scope/tool/data/risk ceiling akan terlampaui;
- concurrent/unrelated work berisiko tertimpa;
- destructive/irreversible/high-impact action tidak memiliki recovery dan approval;
- validation/gate kritis gagal atau actual state tidak dapat direkonstruksi;
- diminta self-approve, menyembunyikan failure, mengarang evidence, atau melanggar Constitution/Governance.

State menjadi `Blocked` untuk dependency/conflict/failure atau `Waiting for Approval` untuk decision gate yang jelas. Stop record mengikuti Governance Engine dan tidak menghalangi bagian independen yang terbukti aman.

## 11. Evidence, Report, dan Closure Contract

Evidence minimum per session:

- source request dan validated objective;
- initial/final repository state serta relevant commits;
- context/dependency/authority/risk map;
- plan, state history, checkpoint, dan progress;
- changed artefact dan decision trail;
- validation, quality, governance, documentation, serta Git result;
- failure/retry/rollback/recovery dan limitation;
- report, closure, handoff, debt, residual risk, dan next action.

Evidence mengikuti retention, security, privacy, dan least disclosure. Report merangkum evidence; report tidak menggantikan source, test output, decision record, atau approval record.

### 11.1 Definition of Session Closure

Session dapat `Completed` hanya jika:

- objective tunggal dan seluruh deliverable/acceptance criteria terpenuhi;
- lifecycle wajib selesai atau N/A terjustifikasi;
- state history serta transition evidence lengkap;
- dependency dan assumption material telah divalidasi;
- quality/governance gate kritis lulus;
- dokumentasi dan Git workflow selesai jika berlaku;
- required human review/approval tersedia;
- report dan continuity/handoff akurat;
- no mandatory partial work, hidden blocker, atau false claim;
- debt, limitation, residual risk, successor, serta archive trigger jelas.

## 12. Cross-System Alignment

| Sumber | Implementasi dalam Session Engine | Boundary |
| --- | --- | --- |
| [`CONSTITUTION.md`](CONSTITUTION.md) | Amanah, Human First, Repository First, Documentation First, Truth over Assumption, oversight, traceability, quality, dan escalation | Engine tidak meratifikasi Constitution atau mengambil Founder Authority |
| [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) | read/plan/review before action, bounded autonomy, tool use, validation, rollback, documentation, Git, reporting | Developer Mode memiliki perilaku AI; Session Engine memiliki unit/state/continuity kerja |
| [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) | execution procedure, task execution, validation checkpoint, failure/recovery, evidence, completion | Execution Engine tetap SSOT detail eksekusi; Session Engine mengorkestrasi lifecycle dan state |
| [`GIT_ENGINE.md`](GIT_ENGINE.md) | branch/commit/PR/push/release trace dan recovery | Git Engine tetap SSOT Git; Git event tidak otomatis mengubah state/approval |
| [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) | impact assessment, source update, status, report/handoff, archive | Documentation Engine tetap SSOT detail dokumentasi; session state bukan document status |
| [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) | objective/requirement/gate/DoD/evidence/finding/audit | Quality Engine tetap SSOT quality; session state bukan quality approval |
| [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) | authority, owner, delegation, decision class, separation, approval, exception, escalation, stop | Governance menetapkan siapa boleh memutus; Session Engine merekam dan menegakkan gate |
| [`../../01-foundation/FOUNDATION_ARCHITECTURE.md`](../../01-foundation/FOUNDATION_ARCHITECTURE.md) | SSOT, dependency, evidence/feedback, ownership, boundary, learning | Session tidak mengambil ownership Foundation/domain |
| [`../../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md`](../../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md) | provenance, status, confidence, review trigger, learning routing | Session evidence tidak otomatis menjadi approved knowledge |
| [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) | modular assembly, session boundary, lifecycle, input/output, bounded execution | Engine adalah kontrak dokumentasi, bukan runtime orchestrator |
| [`../03-sessions/SESSION_TEMPLATE.md`](../03-sessions/SESSION_TEMPLATE.md) | concrete session contract, plan, gate, state, continuity, report | Template menginstansiasi dan tidak menduplikasi policy |

### 12.1 Resolusi Cross-Review SPOS-009

- Session Engine menjadi SSOT untuk session identity, boundary, lifecycle orchestration, type, state machine, continuity, dependency antarsession, report, dan closure.
- Execution Engine tetap SSOT prosedur eksekusi incremental, validation checkpoint, failure/recovery, evidence, dan completion criteria; sebelas tahap lama dipetakan ke tiga belas tahap session tanpa menghapus semantics.
- Governance lifecycle mengatur policy/authority/ownership; Documentation lifecycle mengatur dokumen; Knowledge lifecycle mengatur knowledge; lifecycle tersebut tidak disamakan dengan state session.
- Quality gate menilai fitness; Governance menentukan decision rights; Git menjaga version trace; tidak satu pun eventnya otomatis mengubah session ke `Completed`.
- Session Template diperbarui agar menggunakan state, type, continuity, predecessor/successor, checkpoint, resume, cancellation, dan archive contract kanonik.
- Foundation dan Knowledge tetap menerima evidence/learning melalui review; Session Report tidak menjadi policy atau knowledge approved otomatis.
- Scope SPOS-009 documentation-only; tidak ada session registry service, scheduler, queue, dashboard, database, memory system, aplikasi, atau automation runtime yang dibangun.

## 13. Activation dan Change Control

Aktivasi memerlukan:

- Constitution diratifikasi atau Founder mengizinkan baseline interim secara eksplisit;
- Governance Engine dan engine dependency memiliki version/status yang kompatibel;
- Founder/authorized human menyetujui lifecycle, state machine, transition authority, continuity, report, serta closure contract;
- owner, reviewer, approver, session registry/index location, retention, dan security/privacy control ditetapkan;
- template, playbook, prompt, report, handoff, dan AI consumer dimigrasikan serta version-pinned;
- transition/recovery/continuity scenario diuji dan audit trail dapat diverifikasi.

Activation record:

- Approver: `<authorized human>`
- Decision: `<approved / rejected / revision required>`
- Effective date: `<YYYY-MM-DD>`
- Version approved: `<version>`
- Constitution dependency: `<version and status>`
- Governance dependency: `<version and status>`
- Engine compatibility set: `<versions and status>`
- Session registry/index: `<reference>`
- Template/consumer migration evidence: `<reference>`
- Retention/security control: `<reference>`
- Transition/recovery validation: `<reference>`
- Commit hash: `<hash>`

AI tidak boleh mengisi approval atau acceptance manusia. Perubahan material pada lifecycle, type, state/transition, closure, continuity, AI authority, report minimum, atau terminal-state semantics memerlukan impact analysis, versioning, migration, cross-review, dan approval sesuai Governance Engine.

## 14. Session Engine Review Checklist

- [x] Tiga belas tahap Session Lifecycle memiliki tujuan, output, dan gate yang jelas.
- [x] Foundation, Architecture, Development, Documentation, Research, Governance, Quality, Refactor, Bug Fix, Release, Maintenance, dan Knowledge didefinisikan dengan tujuan, karakteristik, serta output.
- [x] Pending, Running, Blocked, Waiting for Approval, Review, Completed, Archived, dan Cancelled memiliki definisi serta transisi eksplisit.
- [x] Resume, recovery, dependency antarsession, context preservation, checkpoint, handoff, stale/timeout, supersession, cancellation, dan archive terdokumentasi.
- [x] Satu objective, artefak jelas, documentation update, Git Workflow, dan Session Report menjadi AI Session Policy wajib.
- [x] Identity, contract, record, evidence, closure, dan activation contract terdokumentasi.
- [x] Alignment dengan Constitution, Developer Mode, Execution, Git, Documentation, Quality, Governance, Foundation, Knowledge System, SPOS Architecture, dan Session Template dipetakan.
- [x] Scope tidak membangun aplikasi, fitur produk, registry service, scheduler, queue, database, dashboard, agent memory, deployment, atau automation runtime.
- [ ] Constitution diratifikasi atau baseline interim diizinkan Founder secara eksplisit.
- [ ] Session Engine memperoleh approval operasional dan activation record.
- [ ] Session owner/reviewer/approver delegation, registry/index, retention, dan transition authority tersedia.
- [ ] Template/consumer migration, version pinning, continuity/recovery test, monitoring, dan conformance automation diterapkan serta diverifikasi.
