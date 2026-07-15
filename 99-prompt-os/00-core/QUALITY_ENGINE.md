# SparkMind Quality Engine

> Status: In Review — quality governance baseline SPOS-007; activation as a binding standard requires the applicable human authority and eligible upstream versions.
>
> Owner: Founder
>
> Reviewer: Founder, Governance owner, Quality owner/steward, Security/Privacy owner, repository maintainer, Documentation owner, Knowledge Steward, dan domain owner yang ditunjuk
>
> Approver: Founder atau authority manusia yang didelegasikan secara tertulis untuk kebijakan kualitas non-konstitusional
>
> Version: 0.1.0
>
> Established: 2026-07-15
>
> Effective: setelah approval operasional yang sah dan dependency upstream terpenuhi
>
> Review trigger: amendment Constitution; perubahan Governance, Developer Mode, Session Engine, Execution Engine, Git Engine, Documentation Engine, Report Engine, Foundation, Knowledge System, atau SPOS Architecture; insiden kualitas material; perubahan risiko/capability; audit finding berulang; atau evidence bahwa gate dan metrik tidak lagi efektif

## 1. Kedudukan dan Tujuan

Quality Engine adalah standar permanen untuk mendefinisikan kualitas, validasi, review, audit, dan continuous improvement bagi seluruh artefak SparkMind, termasuk keputusan, dokumentasi, kode, konfigurasi, arsitektur, governance, knowledge, prompt, playbook, laporan, dan proses engineering.

Engine ini mengoperasionalkan [`CONSTITUTION.md`](CONSTITUTION.md), [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md), [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md), [`SESSION_ENGINE.md`](SESSION_ENGINE.md), [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md), [`GIT_ENGINE.md`](GIT_ENGINE.md), [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md), [`REPORT_ENGINE.md`](REPORT_ENGINE.md), dan [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md). Session Engine menjadi sumber lifecycle orchestration/state/continuity session; Execution Engine menjadi sumber prosedur eksekusi/checkpoint/completion; Quality Engine menjadi sumber kanonik definisi kualitas, urutan quality gate, Definition of Done, metrik, audit, corrective/preventive action, dan AI Quality Policy.

Quality Engine bukan aplikasi, test runner, CI/CD, dashboard, sertifikasi, pengganti Governance, atau izin bagi AI untuk menyetujui hasilnya sendiri. Test hijau, skor metrik tinggi, commit, publication, dan completion teknis tidak otomatis membuktikan approval, fitness for purpose, keamanan, atau kualitas keseluruhan.

Karena Constitution, Governance Engine, dan engine upstream masih `In Review`, dokumen ini juga `In Review`. Baseline dapat digunakan untuk kerja dan review, tetapi tidak menjadi standard binding sebelum activation record yang sah tersedia.

## 2. Scope dan Non-Scope

### 2.1 Scope

Engine berlaku untuk:

- seluruh artefak yang dibuat, diubah, direview, dipublikasikan, atau digunakan oleh manusia dan AI;
- quality planning sebelum eksekusi, assurance selama eksekusi, dan control sebelum completion;
- review objective, requirement, architecture, implementation, documentation, Git, security/privacy, governance, dan approval;
- Definition of Done lintas session;
- metrik kualitas, audit, finding, CAPA, lesson learned, dan improvement cycle;
- aktivitas manual maupun otomatis dengan evidence yang dapat ditelusuri.

### 2.2 Non-Scope

Engine tidak:

- menetapkan requirement produk, risk appetite, atau acceptance bisnis tanpa owner;
- menggantikan specialist review untuk security, privacy, legal, accessibility, domain, atau safety;
- menjamin zero defect atau mengubah absence of evidence menjadi evidence of absence;
- menetapkan approval, exception, atau risk acceptance tanpa authority manusia;
- membangun aplikasi, fitur produk, quality dashboard, CI/CD, test framework, atau automation runtime;
- menduplikasi prosedur rinci yang telah dimiliki engine atau domain lain.

## 3. Model Kualitas

Kualitas berarti artefak **fit for intended purpose**, benar berdasarkan evidence, konsisten dengan authority dan repository, aman digunakan dalam scope yang dinyatakan, dapat dipahami, ditelusuri, dipelihara, dan ditingkatkan.

Quality Assurance (QA) mencegah defect melalui standard, planning, review, dan process design. Quality Control (QC) mendeteksi defect pada output melalui inspection, test, dan verification. Keduanya wajib proporsional terhadap risiko dan tidak boleh saling menggantikan.

Setiap klaim kualitas harus menjawab:

1. **Apa** yang dinilai dan untuk tujuan/audience apa?
2. **Terhadap kriteria** serta versi requirement mana?
3. **Dengan evidence** aktual apa?
4. **Oleh siapa** dan dengan independence/kompetensi apa?
5. **Kapan** penilaian dilakukan dan apakah masih berlaku?
6. **Apa yang tidak diuji**, limitation, debt, dan residual risk-nya?
7. **Siapa** yang berwenang menyetujui atau menerima risiko?

## 4. Quality Principles

### 4.1 Truth Before Speed

Keadaan aktual, evidence, dan limitation harus dilaporkan sebelum mengejar kecepatan atau status selesai. Jangan memalsukan pass, menghilangkan failure, menurunkan gate, atau memilih validasi yang lebih lemah agar pekerjaan tampak cepat.

### 4.2 Quality Over Quantity

Outcome yang benar, berguna, dan dapat dipelihara lebih bernilai daripada banyak file, fitur, test, metrik, atau kata. Volume bukan proxy kualitas. Hapus duplikasi dan generated filler; prioritaskan coverage terhadap risiko material.

### 4.3 Documentation Completeness

Dokumentasi yang diperlukan untuk memahami, menggunakan, mereview, mengoperasikan, memigrasikan, memulihkan, atau mengaudit perubahan adalah bagian kualitas dan Definition of Done. Completeness bersifat proporsional, bukan kewajiban menambah dokumen tanpa kebutuhan.

### 4.4 Traceability

Objective, requirement, decision, perubahan, test, review, finding, approval, dan outcome harus dapat ditelusuri dua arah. Traceability menunjukkan hubungan dan coverage; tidak membuktikan correctness dengan sendirinya.

### 4.5 Consistency

Artefak harus konsisten dengan source of truth, terminology, architecture, interface, lifecycle, version, dan consumer yang berlaku. Konflik tidak diselesaikan dengan menyembunyikan perbedaan atau membuat SSOT tandingan.

### 4.6 Reliability

Hasil yang sama harus dapat diperoleh secara konsisten pada kondisi yang dinyatakan. Failure mode, boundary, dependency, retry, rollback, recovery, dan observability diuji sesuai risiko. Flaky evidence tidak dianggap pass tanpa diagnosis.

### 4.7 Simplicity

Gunakan solusi paling sederhana yang memenuhi objective dan constraint secara utuh. Simplicity mengurangi cognitive load dan failure surface, tetapi tidak boleh menghapus kontrol, evidence, atau penanganan kasus penting.

### 4.8 Maintainability

Artefak harus dapat dipahami, diubah, diuji, direview, dan dipulihkan oleh maintainer berikutnya tanpa hidden context. Ownership, modularity, naming, dependency, debt, dan change path harus jelas.

### 4.9 Reusability

Artefak reusable memiliki boundary, contract, prerequisite, limitation, version, example, dan owner yang jelas. Jangan memaksakan abstraksi dini; reuse hanya bernilai jika mengurangi duplikasi tanpa menciptakan coupling atau authority ambiguity.

### 4.10 Human-Centered Quality

Kualitas dinilai dari dampak pada manusia, bukan hanya kepatuhan teknis. Accessibility, usability, keselamatan, privasi, kejelasan, beban operasional, fairness, dan kemampuan manusia untuk memahami serta mengendalikan hasil wajib dipertimbangkan.

### 4.11 Continuous Improvement

Kualitas adalah sistem belajar. Finding, incident, review feedback, dan outcome diubah menjadi tindakan terukur melalui owner yang tepat. Improvement tidak boleh mengubah policy atau status approved secara otomatis.

### 4.12 Prinsip Pendukung

- **Risk-based rigor:** semakin tinggi dampak, semakin kuat evidence, independence, dan approval.
- **Shift left and verify right:** cegah defect sejak objective/requirement, lalu verifikasi outcome aktual.
- **Independent review where required:** self-review tidak menggantikan reviewer independen untuk risiko material.
- **Fail visibly and safely:** failure dicatat, dibatasi, dan dipulihkan; bukan disamarkan.
- **No quality theater:** checklist, test count, coverage, dan skor tidak boleh dipakai tanpa hubungan dengan risiko nyata.
- **Least disclosure:** evidence cukup untuk audit tanpa mengekspos secret atau data pribadi yang tidak perlu.

## 5. Authority, Peran, dan Independence

| Peran | Tanggung jawab | Batas |
| --- | --- | --- |
| **Founder** | Keputusan fundamental, ratifikasi, dan risk acceptance strategis | Tidak menggantikan evidence atau kewajiban hukum/keselamatan |
| **Governance owner** | Delegation, approval, exception, escalation, separation, dan audit authority sesuai Governance Engine | Tidak menyetujui domain correctness tanpa owner/reviewer yang tepat |
| **Quality owner/steward** | Menjaga standard, gate, metric definition, audit program, dan portfolio improvement | Tidak menyetujui correctness domain sendirian |
| **Domain/Product owner** | Menetapkan intended purpose, requirement, acceptance, dan domain correctness | Tidak melemahkan gate lintas domain tanpa authority |
| **Security/Privacy owner** | Review threat, data handling, access, dan residual security/privacy risk | Tidak menggantikan approval bisnis atau konstitusional |
| **Documentation owner** | Completeness, usability, lifecycle, dan publication quality | Tidak menetapkan fakta domain tanpa source/owner |
| **Repository maintainer** | Integritas repository, check, Git evidence, dan release readiness | Commit/merge tidak sama dengan approval kualitas |
| **Author/Executor** | Quality planning, implementation, self-review, evidence, dan remediation | Tidak self-approve perubahan yang memerlukan independence |
| **Reviewer/Auditor** | Evaluasi evidence, finding, severity, dan conformity secara objektif | Tidak approve di luar kompetensi/delegasi |
| **AI Agent** | Self-review, validation, cross-review, metric calculation, dan draft CAPA sesuai Section 10 | Bukan Founder, approver, auditor independen, atau risk owner |

Reviewer wajib memiliki kompetensi yang relevan dan conflict of interest yang dikelola. Untuk perubahan high/critical, perubahan normatif, security/privacy-sensitive, irreversible, atau berdampak lintas domain, author tidak boleh menjadi satu-satunya reviewer. Jika independence wajib tetapi tidak tersedia, gate berstatus `Blocked`.

## 6. Quality Planning dan Evidence Contract

Sebelum eksekusi material, quality plan minimum menetapkan:

- objective, intended purpose, audience, scope, non-scope, dan acceptance criteria;
- requirement ID/source/version serta traceability method;
- risk level, criticality, affected parties, dan failure impact;
- quality gate yang berlaku, owner, reviewer, approver, serta independence;
- validation method, positive/negative/boundary case, dan expected evidence;
- documentation, Git, security/privacy, governance, rollback, dan recovery impact;
- metric yang berguna beserta baseline/target; bukan target arbitrer;
- stop condition, exception path, dan residual-risk owner.

Evidence minimum harus:

- berasal dari state dan output aktual, bukan ingatan atau klaim;
- mengidentifikasi artefak, versi/commit, environment, waktu, serta metode bila relevan;
- reproducible atau menjelaskan mengapa tidak;
- mempertahankan failure dan limitation;
- aman menurut security, privacy, legal, dan retention;
- cukup untuk reviewer mengambil keputusan tanpa hidden context.

Evidence yang stale, flaky, berasal dari versi berbeda, tidak mencakup perubahan material, atau tidak dapat ditelusuri tidak boleh digunakan sebagai dasar `Pass` tanpa penjelasan dan revalidation.

## 7. Quality Gates

Quality gate dijalankan berurutan, tetapi perubahan material pada tahap berikutnya dapat mengembalikan pekerjaan ke gate sebelumnya. Setiap gate menghasilkan `Pass`, `Fail`, `Blocked`, atau `Not Applicable` disertai reviewer, evidence, waktu, dan alasan. `Not Applicable` memerlukan justifikasi; gate kritis `Fail`/`Blocked` mencegah completion.

### 7.1 Gate 1 — Objective Review

Verifikasi:

- satu objective utama, intended outcome, audience, dan value jelas;
- scope/non-scope, constraint, assumption, dependency, dan stop condition eksplisit;
- authority serta owner objective valid;
- outcome dapat diverifikasi dan tidak mengandung hidden objective;
- pekerjaan tidak membangun sesuatu yang dilarang atau tidak diperlukan.

**Exit:** objective cukup jelas, sah, feasible, dan dapat diturunkan menjadi requirement.

### 7.2 Gate 2 — Requirement Review

Verifikasi:

- requirement lengkap, konsisten, atomic bila perlu, testable, dan traceable;
- acceptance criteria mencakup positive, negative, boundary, failure, dan non-functional need sesuai risiko;
- requirement konflik, ambiguity, priority, source, version, dan owner diselesaikan;
- security, privacy, accessibility, legal, operational, migration, dan compatibility requirement dipetakan;
- perubahan requirement setelah review dikendalikan dan direview ulang.

**Exit:** requirement baseline dapat digunakan tanpa mengarang intent; gap kritis menjadi blocker.

### 7.3 Gate 3 — Architecture Review

Verifikasi:

- desain memenuhi requirement tanpa melanggar boundary atau authority;
- component, dependency, interface, data/control flow, dan source of truth jelas;
- trade-off, alternative, failure mode, scalability/reliability, security/privacy, maintainability, dan reversibility dinilai;
- reuse tidak menciptakan coupling/abstraction dini; simplicity dipertahankan;
- migration, compatibility, rollback/recovery, dan affected consumer tersedia;
- keputusan material dicatat pada Architecture/Design Decision/ADR yang tepat.

**Exit:** architecture fit for purpose, konsisten, dapat direview, dan memiliki mitigasi risiko.

### 7.4 Gate 4 — Implementation Review

Untuk kode maupun artefak non-code, verifikasi:

- implementasi sesuai requirement dan architecture yang direview;
- perubahan minimum, cohesive, readable, maintainable, dan tidak mengandung unrelated work;
- validation mencakup test/check semantik, teknis, positive/negative/boundary/regression sesuai risiko;
- error handling, observability, failure, rollback, dan recovery memadai;
- dependency, generated artifact, configuration, data/schema, prompt, dan compatibility direview;
- tidak ada placeholder, bypass, disabled control, dead path, atau debt material tanpa record.

**Exit:** implementation evidence lulus dan seluruh defect blocking diperbaiki atau pekerjaan tetap `Blocked`.

### 7.5 Gate 5 — Documentation Review

Ikuti [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) dan verifikasi:

- documentation impact assessment selesai;
- source kanonik, jenis, status, owner, metadata, lifecycle, link, index, changelog, handoff, dan consumer sinkron;
- fakta, keputusan, assumption, limitation, risk, debt, migration, operation, dan recovery dibedakan;
- dokumen dapat digunakan manusia dan AI tanpa hidden context;
- tidak ada documentation drift kritis, status palsu, secret, atau data sensitif yang tidak perlu.

**Exit:** dokumentasi wajib lengkap untuk penggunaan dan operasi aman.

### 7.6 Gate 6 — Git Review

Ikuti [`GIT_ENGINE.md`](GIT_ENGINE.md) dan verifikasi:

- branch, remote, upstream, working tree, protection, dan authority benar;
- diff penuh dan staged diff sesuai satu objective, tanpa unrelated change;
- whitespace, file lokal, secret/data, generated/binary, dan deletion direview;
- validation evidence terikat pada commit yang akan dikirim;
- commit, PR, reviewer, check, approval, merge, push, tag, dan release sesuai policy;
- hash lokal/remote dan status aktual diverifikasi bila push diwajibkan.

**Exit:** trace Git lengkap atau blocker Git dilaporkan jujur sesuai completion policy.

### 7.7 Gate 7 — Security & Privacy Review

Verifikasi sesuai risiko:

- asset/data, classification, threat, trust boundary, permission, dan attack surface dipetakan;
- least privilege, authentication/authorization, secret handling, encryption, retention, deletion, dan logging sesuai kebutuhan;
- data minimization, purpose limitation, consent/legal basis, user control, dan sensitive-data exposure ditinjau;
- abuse/misuse, prompt injection, supply-chain, dependency, dan incident path dinilai bila relevan;
- temuan memiliki severity, mitigation, owner, deadline, dan revalidation;
- residual risk diterima hanya oleh authority yang sah.

**Exit:** tidak ada critical/high finding yang belum diselesaikan atau diterima secara sah; exception terdokumentasi.

### 7.8 Gate 8 — Governance Review

Verifikasi:

- Constitution, Governance, policy, standard, delegation, owner, dan precedence dipatuhi;
- required human/domain/Founder review serta separation of duties terpenuhi;
- exception, bypass, conflict, risk acceptance, lifecycle, publication, dan archive memiliki authority serta audit trail;
- AI, author, reviewer, dan approver tidak melampaui batas perannya;
- keputusan material diterapkan pada source kanonik dan consumer yang tepat.

**Exit:** authority jelas dan semua approval wajib tersedia; ambiguity material tetap fail-closed.

### 7.9 Gate 9 — Final Approval

Final Approval mengagregasi evidence, bukan mengulang self-review. Verifikasi:

- Gate 1–8 yang berlaku memiliki status dan evidence valid;
- objective, requirement, deliverable, documentation, repository, dan report konsisten;
- defect, debt, exception, residual risk, dan limitation transparan;
- DoD terpenuhi;
- approver berwenang menyatakan `Approved`, `Completed`, `Release Ready`, `Blocked`, atau `Revision Required` sesuai scope;
- approval mengidentifikasi artefak/commit/version, tanggal, scope, dan condition.

**Exit:** keputusan final tercatat. AI tidak dapat memberi Final Approval jika approval manusia diwajibkan.

## 8. Definition of Done (DoD)

DoD adalah completion contract minimum setiap session. Domain boleh menambah kriteria yang lebih ketat tetapi tidak menghapus gate lintas sistem tanpa exception sah.

Session hanya `Completed` jika:

1. **Objective tercapai:** outcome utama dan seluruh deliverable wajib tersedia pada lokasi kanonik.
2. **Repository konsisten:** SSOT, architecture, interface, terminology, dependency, status, version, index, dan consumer tidak diketahui bertentangan.
3. **Dokumentasi diperbarui:** documentation impact assessment dan seluruh update wajib selesai sesuai Documentation Engine.
4. **Tidak ada inkonsistensi:** conflict, defect, drift, placeholder, disabled control, dan unrelated change material telah diselesaikan atau memblokir completion.
5. **Review selesai:** self-review dan seluruh independent/domain/human review yang diwajibkan selesai.
6. **Validasi selesai:** acceptance criteria, quality gate, check/test, negative path, security/privacy, recovery, dan cross-review relevan lulus dengan evidence aktual.
7. **Git workflow selesai:** diff/staged review, commit, PR/approval/merge/push/remote verification selesai bila diwajibkan dan capability tersedia; blocker tidak boleh disamarkan.
8. **Session Report selesai:** report akurat memuat outcome, evidence, branch/hash/push, finding, debt, residual risk, dan rekomendasi.

Tambahan wajib:

- tidak ada critical/high defect atau risk tanpa resolution/acceptance authority;
- exception aktif memiliki scope, owner, expiry, compensating control, dan audit trail;
- rollback/recovery tetap layak untuk perubahan berisiko;
- technical debt tidak menggantikan deliverable atau keselamatan;
- follow-up di luar objective dicatat, bukan dikerjakan diam-diam;
- completion teknis tidak diklaim sebagai approval normatif.

Jika satu syarat wajib tidak terpenuhi, status adalah `Blocked`, `In Review`, atau `Revision Required` sesuai keadaan—bukan `Completed`.

## 9. Quality Metrics

Metrik membantu keputusan; metrik bukan tujuan, approval, atau bukti tunggal kualitas. Setiap metrik wajib memiliki definisi, source, owner, periode, baseline, target/threshold, segmentation, limitation, dan tindakan ketika menyimpang.

### 9.1 Metrik Inti

| Metrik | Definisi operasional minimum | Interpretasi dan guardrail |
| --- | --- | --- |
| **Documentation Coverage** | Artefak/perubahan yang membutuhkan dokumentasi dan telah memiliki update valid ÷ seluruh artefak/perubahan yang membutuhkan dokumentasi | Jangan menghitung jumlah file; nilai completeness dan currentness |
| **Review Completion** | Required review yang selesai dengan evidence ÷ seluruh required review | Approval formalitas tanpa pembacaan/evidence tidak dihitung |
| **Requirement Traceability** | Requirement material dengan link dua arah ke implementation, validation, dan outcome ÷ seluruh requirement material | Link saja tidak membuktikan correctness |
| **Architecture Consistency** | Komponen/interface yang sesuai architecture baseline ÷ komponen/interface yang diperiksa, disertai daftar drift | Sampling dan baseline version wajib terlihat |
| **Repository Health** | Composite yang didefinisikan dari build/check, broken link, secret finding, stale dependency, protection, backup/restore, dan worktree/release integrity | Jangan membuat satu skor tanpa menampilkan komponen dan severity |
| **Technical Debt** | Inventory debt menurut severity, age, owner, impact, dan trend; termasuk debt created/resolved/overdue | Jumlah kecil dapat tetap kritis; severity dan aging lebih penting |
| **Reusability** | Artefak reusable yang berhasil digunakan dalam konteks valid dengan contract/limitation jelas, disertai reuse defect dan avoided duplication | Jangan memaksimalkan reuse atau abstraksi tanpa benefit |
| **Knowledge Completeness** | Topik/decision kritis dengan source, provenance, status, owner, confidence, link, dan review current ÷ scope knowledge kritis yang ditetapkan | Unknown yang dilabeli lebih baik daripada completeness palsu |

### 9.2 Metrik Pendukung

- gate pass/fail/blocked rate menurut gate dan severity;
- defect escape rate dan recurrence rate;
- mean time to detect, contain, remediate, dan verify;
- change failure/revert rate;
- flaky validation rate;
- audit finding aging serta CAPA overdue rate;
- exception volume, age, expiry breach, dan repeat use;
- accessibility/usability task success serta human-reported burden;
- review lead time tanpa mengorbankan finding quality;
- documentation/source drift rate.

### 9.3 Aturan Penggunaan Metrik

1. Tetapkan pertanyaan keputusan sebelum memilih metrik.
2. Gunakan trend dan segmentasi; hindari angka agregat yang menyembunyikan severity.
3. Validasi source, denominator, sampling, dan periode.
4. Bedakan leading indicator (misalnya review coverage) dari lagging outcome (misalnya incident).
5. Jangan memberi insentif hanya pada angka yang mudah dimanipulasi.
6. Metric target tidak boleh mendorong suppression finding, test dangkal, dokumentasi filler, atau klasifikasi risiko lebih rendah.
7. Perubahan definisi metrik memerlukan versioning; hasil sebelum/sesudah tidak dibandingkan tanpa normalisasi.
8. Data sensitif mengikuti least disclosure dan retention.
9. Jika metrik tidak menghasilkan keputusan atau tindakan, hentikan atau redesign.

## 10. AI Quality Policy

### 10.1 Kapan AI Wajib Melakukan Self-Review

AI wajib self-review:

- setelah setiap increment material sebelum melanjutkan ke dependency berikutnya;
- sebelum menyatakan deliverable selesai, staging, commit, push, publication, atau report final;
- setelah merge/conflict resolution, recovery, requirement/architecture change, atau perubahan reviewer feedback;
- ketika output dibuat/generate oleh AI, termasuk dokumentasi, kode, prompt, analisis, dan metrik;
- ketika evidence, source, environment, atau dependency berubah;
- saat menemukan inconsistency, uncertainty, failure, atau risk baru.

Self-review minimum mencakup objective, requirement, correctness, scope, authority, evidence, security/privacy, documentation, Git diff, negative path, limitation, debt, dan residual risk sesuai gate yang berlaku.

### 10.2 Kapan AI Wajib Meminta Review Founder

AI wajib meminta keputusan/review Founder untuk:

- perubahan Constitution, Kernel, identity, Vision, Mission, Values, Ethics, Canon, atau arah strategis;
- perubahan authority utama, governance hierarchy, ratification, atau amendment;
- penerimaan critical/material residual risk atau conflict konstitusional;
- exception yang dapat melemahkan quality gate fundamental;
- keputusan irreversible atau lintas ekosistem dengan dampak fundamental;
- milestone/release yang menyatakan ratification, status fundamental, atau aktivasi engine tanpa delegation lain yang sah.

Untuk perubahan domain, security/privacy/legal, release, atau operasi yang telah didelegasikan, AI meminta review authority manusia yang tepat; AI tidak boleh mengasumsikan delegation.

### 10.3 Kapan Pekerjaan Harus Dihentikan

AI wajib menghentikan area terdampak jika:

- objective/requirement/authority/source of truth kritis ambigu atau konflik;
- gate kritis `Fail`/`Blocked`, evidence hilang/stale/tidak dapat dipercaya, atau required reviewer tidak tersedia;
- critical/high security, privacy, legal, ethical, safety, atau data-integrity risk belum dimitigasi/diterima secara sah;
- perubahan di luar scope, irreversible tanpa recovery, atau dapat menimpa pekerjaan/evidence valid;
- test/check flaky atau gagal dan hasil tidak dapat dipastikan;
- completion memerlukan placeholder, bypass, disabled control, suppressed finding, atau klaim palsu;
- Git memerlukan force push/protection bypass atau remote state tidak dapat diverifikasi;
- dokumentasi wajib, migration, rollback, atau operational guidance belum aman;
- AI diminta self-approve, mengarang reviewer/evidence/metric, atau menurunkan kualitas demi kecepatan.

AI mempertahankan state aman, evidence, dan pekerjaan valid; lalu melaporkan blocker, dampak, opsi recovery, authority yang diperlukan, dan next action.

### 10.4 Larangan Mengorbankan Kualitas demi Kecepatan

AI dilarang:

- melewati, mengubah menjadi `N/A`, menurunkan threshold, atau menghapus gate tanpa alasan dan authority;
- memilih test dangkal, sampling bias, atau metric denominator yang membuat hasil tampak baik;
- menyembunyikan finding, failure, debt, limitation, atau uncertainty;
- menganggap banyak output, test count, coverage, checklist tercentang, atau skor sebagai kualitas;
- menutup pekerjaan parsial sebagai complete karena deadline atau credit/tool pressure;
- melakukan blind retry, mass rewrite, atau workaround yang menambah risiko;
- menggunakan technical debt atau “follow-up” untuk menunda kebutuhan yang wajib bagi keselamatan dan correctness.

Jika waktu terbatas, kurangi scope melalui owner yang berwenang, pertahankan kriteria kualitas untuk scope tersisa, dan nyatakan konsekuensinya. Jangan mengurangi kualitas secara diam-diam.

### 10.5 Batas AI pada Review dan Approval

AI boleh menyiapkan checklist, menjalankan check, menghitung metrik, melakukan self/cross-review, mengklasifikasikan finding sementara, mengusulkan CAPA, dan menyusun evidence. AI tidak boleh:

- menyebut self-review sebagai independent review;
- memberi Final Approval atau risk acceptance atas nama manusia;
- mengubah severity hanya agar gate lulus;
- menandai finding closed tanpa remediation dan verification evidence;
- mengubah policy approved berdasarkan lesson learned tanpa change process;
- mengarang audit sample, user feedback, test result, source, reviewer, atau approval.

## 11. Finding, Defect, Exception, dan Quality Debt

### 11.1 Severity

| Severity | Kriteria ringkas | Default gate effect |
| --- | --- | --- |
| **Critical** | Potensi harm besar, pelanggaran authority/hukum, compromise luas, irreversible loss, atau core objective salah | Stop; completion dilarang |
| **High** | Dampak material pada correctness, security/privacy, operability, atau banyak consumer | Block sampai resolved atau accepted oleh authority sah |
| **Medium** | Dampak terbatas dengan workaround/mitigation yang jelas | Wajib owner dan deadline; dapat memblokir sesuai context |
| **Low** | Masalah minor tanpa dampak material saat ini | Dapat dijadwalkan dengan record proporsional |

Severity mempertimbangkan impact, likelihood, detectability, exposure, reversibility, dan affected parties. AI dapat mengusulkan severity; owner/reviewer berwenang mengonfirmasi untuk temuan material.

### 11.2 Record Minimum

Setiap finding/debt material mencatat:

- ID, tanggal, source gate/audit, artefak/version;
- expected versus actual dan evidence;
- severity/rationale serta impact/consumer;
- root cause terverifikasi atau hypothesis berlabel;
- containment/mitigation sementara;
- corrective dan preventive action;
- owner, reviewer, due date, dependency;
- status, verification evidence, residual risk, dan closure authority.

### 11.3 Exception

Exception bukan pass. Exception wajib memiliki authority, alasan, scope, finding/gate terkait, risk assessment, compensating control, owner, start, expiry, review cadence, revocation condition, dan audit trail. AI tidak dapat memberi exception kepada dirinya sendiri. Expired exception otomatis memblokir penggunaan yang bergantung padanya sampai diperbarui atau ditutup secara sah.

## 12. Audit dan Continuous Improvement

### 12.1 Audit Berkala

Quality owner menyusun risk-based audit program yang mencakup:

- audit terjadwal untuk engine/core, artefak critical, dan area high-use;
- audit event-driven setelah incident, release material, repeated finding, major change, atau metric anomaly;
- scope, criteria, sample method, auditor competence/independence, evidence, dan report;
- review terhadap artefak serta efektivitas process/control, bukan checklist presence saja.

Cadence baseline yang disarankan:

| Kelas | Cadence maksimum | Trigger tambahan |
| --- | --- | --- |
| Critical/normative/security-sensitive | 3–6 bulan | Setiap perubahan material atau incident |
| High-use architecture/process | 6 bulan | Drift, defect escape, atau consumer change |
| Stable reference | 12 bulan | Source/dependency change |
| Historical evidence | Event-driven | Integrity, retention, atau legal trigger |

Governance/owner dapat menetapkan cadence lebih ketat. Audit overdue harus terlihat dan dinilai risikonya.

### 12.2 Pencatatan Temuan

Audit report memuat objective, scope, criteria, sample/limitation, evidence, conforming observation, finding, severity, owner, due date, dan residual risk. Temuan tidak dihapus karena tidak nyaman; duplicate finding dihubungkan ke root issue dan recurrence.

### 12.3 Corrective Action

Corrective action menghilangkan penyebab defect/finding yang terjadi:

1. contain dampak dan lindungi consumer;
2. verifikasi problem serta blast radius;
3. analisis root cause dan contributing factor;
4. pilih tindakan proporsional serta owner;
5. implementasikan incremental;
6. validasi fix dan regression;
7. verifikasi efektivitas setelah periode yang sesuai;
8. tutup hanya dengan evidence dan authority.

### 12.4 Preventive Action

Preventive action mengurangi kemungkinan defect serupa sebelum terjadi kembali melalui perubahan requirement, design, guardrail, test, review, documentation, training, ownership, monitoring, atau automation. Preventive action harus berbasis pola/evidence dan tidak menghasilkan process overhead tanpa benefit.

### 12.5 Lesson Learned

Lesson learned wajib membedakan fakta, cause, inference, dan recommendation; mengidentifikasi kondisi serta batas generalisasi; menentukan target Knowledge/Decision/Pattern/Anti-pattern/Standard/Playbook; memiliki source, owner, reviewer, dan lifecycle; serta tidak otomatis menjadi policy approved.

### 12.6 Continuous Improvement Cycle

```text
Observe evidence and outcomes
  → Measure and detect signal
  → Analyze root cause and system factors
  → Prioritize by risk and value
  → Plan corrective/preventive action
  → Implement incrementally
  → Validate and audit effectiveness
  → Standardize or rollback
  → Share reviewed learning
  → Monitor recurrence and new risk
```

Improvement berhasil hanya jika outcome/control effectiveness membaik tanpa harm atau beban yang tidak proporsional. Jika hasil memburuk, rollback atau redesign dilakukan dan evidence dipertahankan.

## 13. Failure dan Recovery

| Kondisi | Tindakan |
| --- | --- |
| Gate dilewati atau salah `Pass` | Hentikan promotion/completion, buka kembali gate, identifikasi consumer, revalidate, dan catat finding |
| Evidence palsu/stale/flaky | Invalidasi keputusan yang bergantung, preservasi evidence, ulangi dengan metode valid, dan review blast radius |
| Requirement/architecture drift | Hentikan implementasi terdampak, tentukan intended state, update baseline melalui authority, lalu re-review |
| Defect lolos ke consumer | Contain, communicate, rollback/correct, regression test, root-cause review, dan CAPA |
| Metric gaming atau salah definisi | Hentikan penggunaan metric untuk keputusan, koreksi data/definisi, komunikasikan impact, dan re-baseline |
| Reviewer/approval tidak sah | Turunkan status ke evidence aktual, lindungi consumer, minta review authority yang benar, dan audit perubahan terkait |
| Exception kedaluwarsa | Hentikan penggunaan bergantung, pulihkan control, remediate atau minta exception baru melalui authority |
| CAPA tidak efektif/berulang | Buka kembali finding, perluas root-cause/system review, naikkan escalation dan monitoring |

Recovery mengikuti Execution Engine: detect, stop propagation, preserve evidence, assess blast radius, stabilize, recover incrementally, revalidate, communicate, dan record learning.

## 14. Cross-System Alignment

| Sumber | Implementasi dalam Quality Engine | Boundary |
| --- | --- | --- |
| [`CONSTITUTION.md`](CONSTITUTION.md) | Truth over Assumption, Human First, quality, oversight, traceability, reversibility, accountability, dan Founder Authority | Engine tidak meratifikasi Constitution atau menerima risiko strategis |
| [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) | Read/plan/review before action, Continuous Validation, self-review, stop gate, rollback, dan human oversight | Quality Engine merinci quality standard tanpa memperluas otonomi AI |
| [`SESSION_ENGINE.md`](SESSION_ENGINE.md) | Lifecycle orchestration, state transition, Quality Review, Governance Check, report, dan closure | Session Engine mengorkestrasi gate; Quality Engine tetap sumber definisi quality/gate/metric/audit |
| [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) | Validate Results, enam validation checkpoint, failure/recovery, evidence, dan completion criteria | Execution Engine tetap sumber prosedur eksekusi; Quality Engine sumber definisi quality/gate/metric/audit |
| [`GIT_ENGINE.md`](GIT_ENGINE.md) | Diff/staged review, reviewer, check, audit trace, release readiness, dan recovery | Git event/check hijau tidak menjadi Final Approval kualitas |
| [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) | Documentation completeness, review, lifecycle, evidence, publication gate, dan debt | Documentation Engine tetap sumber detail dokumentasi |
| [`REPORT_ENGINE.md`](REPORT_ENGINE.md) | Quality/Audit report structure, claim-evidence mapping, validation result, finding/debt/risk disclosure, traceability, dan aggregation guardrail | Quality Engine menetapkan gate/finding/metric/audit; Report Engine menetapkan cara hasil dilaporkan |
| [`../../01-foundation/FOUNDATION_ARCHITECTURE.md`](../../01-foundation/FOUNDATION_ARCHITECTURE.md) | SSOT, evidence flow, ownership, lifecycle, feedback, learning, dan human oversight | Engine tidak mengambil ownership Foundation/domain |
| [`../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) | source quality, provenance, confidence, verification, lesson learned, dan review | Audit/metric output tidak otomatis menjadi approved knowledge/policy |
| [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) | authority, ownership, delegation, approval, exception, escalation, reviewer/auditor separation, dan risk acceptance | Quality Engine menilai evidence; Governance menetapkan decision rights |
| [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) | modular contract, traceability, quality gates, bounded execution, report, dan feedback | Engine adalah kontrak dokumentasi, bukan QA runtime/dashboard |
| [`../03-sessions/SESSION_TEMPLATE.md`](../03-sessions/SESSION_TEMPLATE.md) | dependency, quality plan, gate evidence, cross-review, DoD, dan report | Template menginstansiasi engine dan tidak menjadi policy tandingan |

### 14.1 Resolusi Cross-Review SPOS-007

- Sembilan gate SPOS-007 menjadi urutan quality review kanonik; enam Validation Gates Execution Engine tetap checkpoint lifecycle dan mendelegasikan detail kualitas ke engine ini.
- DoD SPOS-007 memperkuat, bukan mengganti, DoD Execution Engine; konflik memakai requirement yang lebih ketat sesuai authority.
- Documentation Review mendelegasikan detail ke Documentation Engine; Git Review ke Git Engine; Security/Privacy serta Governance tetap memerlukan owner/authority domain.
- Quality metrics digunakan sebagai decision support dan dilarang menjadi approval otomatis atau target yang mendorong gaming.
- AI self-review wajib tetapi tidak dianggap independent review atau Final Approval.
- Audit finding, gate result, metric, dan CAPA dilaporkan mengikuti Report Engine; reporting tidak mengubah severity, gate, approval, atau closure authority.
- Audit finding dan lesson learned mengalir ke Knowledge/Decision/Pattern/Standard owner melalui review; tidak mengubah source approved secara otomatis.
- Governance Engine SPOS-008 menetapkan role dan decision-right policy. Sampai activation, delegation, serta human role acceptance aktual tersedia, Quality owner, auditor independence, exception, risk acceptance, dan Final Approval yang ambigu tetap fail-closed.
- Brief SPOS-007 menetapkan Quality Engine meskipun report/handoff SPOS-006 merekomendasikan Governance Engine; deviasi historis dicatat, dan Governance Engine kemudian dibangun melalui SPOS-008.

## 15. Activation dan Change Control

Aktivasi sebagai standard binding memerlukan:

- Constitution dengan status operasional sah atau keputusan Founder yang secara eksplisit mengizinkan baseline sementara;
- Developer Mode, Execution Engine, Git Engine, dan Documentation Engine yang kompatibel;
- Governance Engine yang approved/active beserta role, delegation, independence, exception, escalation, audit, dan risk-acceptance record;
- Quality owner/steward serta reviewer/auditor delegation;
- approval eksplisit, version, effective date, scope, dan audit trail;
- consumer migration, gate mapping, metric definitions, audit cadence, dan evidence retention yang dapat diverifikasi.

Activation record:

- Approver: `<authorized human>`
- Decision: `<approved / rejected / revision required>`
- Effective date: `<YYYY-MM-DD>`
- Version approved: `<version>`
- Constitution dependency: `<version and status>`
- Developer Mode dependency: `<version and status>`
- Execution Engine dependency: `<version and status>`
- Git Engine dependency: `<version and status>`
- Documentation Engine dependency: `<version and status>`
- Governance/Quality decision: `<relative-link>`
- Consumer migration evidence: `<reference>`
- Audit/metric baseline: `<reference>`
- Commit hash: `<hash>`

AI tidak boleh mengisi field approval atas nama manusia. Perubahan material pada prinsip, gate, DoD, severity, metric, AI boundary, exception, audit, atau approval memerlukan impact analysis, versioning, changelog, review, migration, dan approval sesuai authority.

## 16. Quality Engine Review Checklist

- [x] Truth Before Speed, Quality Over Quantity, Documentation Completeness, Traceability, Consistency, Reliability, Simplicity, Maintainability, Reusability, Human-Centered Quality, dan Continuous Improvement terdokumentasi.
- [x] Objective, Requirement, Architecture, Implementation, Documentation, Git, Security & Privacy, Governance, dan Final Approval gate memiliki checks serta exit criteria.
- [x] Definition of Done mencakup objective, repository consistency, documentation, inconsistency resolution, review, validation, Git workflow, dan Session Report.
- [x] Documentation Coverage, Review Completion, Requirement Traceability, Architecture Consistency, Repository Health, Technical Debt, Reusability, dan Knowledge Completeness didefinisikan dengan anti-gaming guardrail.
- [x] Audit berkala, finding record, corrective action, preventive action, lesson learned, CAPA, dan continuous improvement cycle terdokumentasi.
- [x] AI self-review, Founder/human review, automatic stop, quality-over-speed, dan approval boundary terdokumentasi.
- [x] Finding severity, quality debt, exception, evidence, failure, dan recovery terdokumentasi.
- [x] Alignment dengan Constitution, Governance, Developer Mode, Session Engine, Execution Engine, Git Engine, Documentation Engine, Report Engine, Foundation, Knowledge System, SPOS Architecture, dan Session Template dipetakan.
- [x] Scope tidak membangun aplikasi, fitur produk, dashboard, CI/CD, test framework, atau automation runtime.
- [ ] Constitution diratifikasi atau baseline interim diizinkan secara eksplisit.
- [ ] Seluruh upstream engine, termasuk Session dan Report Engine, serta Quality Engine memperoleh approval operasional dan activation record yang kompatibel.
- [ ] Governance Engine memperoleh approval/activation; Quality owner, auditor delegation/independence, exception, dan risk-acceptance authority diterapkan serta diterima manusia terkait.
- [ ] Consumer migration, metric baseline, audit operation, CAPA registry, evidence retention, dan conformance automation diterapkan serta diverifikasi.
