# SparkMind Governance Engine

> Status: In Review — governance control-plane baseline SPOS-008; activation as binding governance requires Founder approval and eligible upstream versions.
>
> Owner: Founder
>
> Reviewer: Founder, AI Executive, Domain Owner, Knowledge Steward, Repository Maintainer, Quality owner, Security/Privacy owner, dan pihak terdampak yang ditunjuk
>
> Approver: Founder; authority non-konstitusional tertentu dapat didelegasikan secara tertulis sesuai dokumen ini
>
> Version: 0.1.0
>
> Established: 2026-07-15
>
> Effective: setelah approval Founder, activation record, dan dependency upstream yang berlaku terpenuhi
>
> Review trigger: amendment Constitution; perubahan authority, ownership, organisasi, hukum, risiko, capability AI, Session Engine, Report Engine/engine SPOS lain, atau arsitektur; insiden governance material; audit/reporting failure berulang; dan evidence bahwa kontrol tidak efektif

## 1. Kedudukan dan Tujuan

Governance Engine adalah control plane permanen untuk tata kelola ekosistem SparkMind. Engine ini menerjemahkan [`CONSTITUTION.md`](CONSTITUTION.md) menjadi model authority, ownership, keputusan, approval, lifecycle, compliance, audit, escalation, dan batas AI yang dapat ditelusuri bagi AI Agent, repository, knowledge, dokumentasi, prompt, policy, standard, architecture, product, serta konfigurasi AI Agent.

Urutan normatif tetap: hukum dan kewajiban keselamatan yang berlaku → Founder Authority → Constitution yang diratifikasi → Governance → Policies → Standards → Playbooks → Session Instructions → prompt/task/preferensi lokal. Governance tidak dapat mengubah Constitution, menggantikan evidence, atau menciptakan authority yang tidak diberikan.

Governance Engine bukan aplikasi, layanan identity/access management, organisasi hukum, workflow produk, dashboard, enforcement runtime, atau pengganti owner domain. Capability teknis, kepemilikan akun, akses repository, commit, merge, publication, atau output AI tidak dengan sendirinya memberikan authority normatif.

Karena Constitution dan engine SPOS terkait masih `In Review`, Governance Engine juga `In Review`. Baseline dapat dipakai untuk review dan pengendalian interim secara fail-closed, tetapi tidak menjadi bukti approval, delegation, atau aktivasi.

## 2. Scope dan Non-Scope

### 2.1 Scope

Engine mengatur:

- authority, delegation, accountability, separation of responsibility, dan least privilege;
- ownership untuk repository, knowledge, dokumentasi, prompt, policy, standard, architecture, product, dan konfigurasi AI Agent;
- keputusan otomatis, keputusan dengan persetujuan, escalation, exception, conflict resolution, dan final authority;
- lifecycle governance dari proposal sampai retirement;
- compliance review, audit, violation handling, corrective/preventive action, serta kewajiban Governance Report sesuai [`REPORT_ENGINE.md`](REPORT_ENGINE.md);
- batas kewenangan AI, penggunaan capability/automation, serta automatic stop;
- hubungan control-plane dengan seluruh engine SPOS dan domain Foundation.

### 2.2 Non-Scope

Engine tidak:

- meratifikasi atau mengamendemen Constitution;
- mengambil alih requirement, correctness, atau operasi harian milik domain/product owner;
- menggantikan review legal, security, privacy, safety, agama, finance, atau ahli domain;
- memberi AI status manusia, legal person, Founder, atau risk owner;
- membangun aplikasi, fitur produk, IAM, policy engine, database, dashboard, CI/CD, atau automation runtime;
- menganggap governance lengkap hanya karena dokumen, checklist, atau matriks tersedia.

## 3. Governance Principles

### 3.1 Constitution First

Seluruh keputusan dan kontrol harus sesuai Constitution yang berlaku. Konflik material menghentikan area terdampak; exception Governance tidak dapat mengesampingkan Constitution.

### 3.2 Human Stewardship

Manusia berwenang memegang tanggung jawab akhir atas keputusan material. AI membantu analisis dan eksekusi terbatas, bukan menggantikan penilaian, consent, atau akuntabilitas manusia.

### 3.3 Founder Authority

Founder memegang ratifikasi konstitusional, arah fundamental, penunjukan authority utama, dan final authority untuk konflik strategis. Delegasi operasional tidak memindahkan authority konstitusional.

### 3.4 Amanah

Authority, data, akses, waktu, pengetahuan, dan kepercayaan digunakan hanya untuk tujuan, scope, serta durasi yang diberikan. Pemegang peran wajib melindungi pihak terdampak dan melaporkan penyimpangan.

### 3.5 Transparency

Sumber, status, decision rationale, conflict, delegation, exception, dissent, limitation, dan outcome material harus dapat diperiksa pihak berwenang dengan least disclosure untuk secret dan data sensitif.

### 3.6 Accountability

Setiap keputusan material memiliki human accountable owner, decision maker, evidence, due date bila relevan, dan jalur koreksi. Delegasi tugas tidak menghapus accountability pemberi delegasi.

### 3.7 Auditability

Authority, proposal, review, approval, implementasi, perubahan, exception, violation, dan retirement harus memiliki record yang immutable secara proporsional dan dapat dihubungkan ke artefak/version/commit.

### 3.8 Least Privilege

Berikan capability, akses, data, dan decision right minimum yang diperlukan, untuk scope serta durasi minimum. Akses teknis yang lebih luas daripada authority wajib dibatasi dengan kontrol dan monitoring.

### 3.9 Separation of Responsibility

Proposer, executor, reviewer, approver, auditor, dan risk acceptor dipisahkan sesuai risiko. Self-review tidak menjadi independent review; pihak yang memperoleh manfaat langsung tidak boleh menjadi satu-satunya approver keputusan material.

### 3.10 Continuous Governance

Governance dipantau berdasarkan outcome, incident, perubahan konteks, metric, dan audit. Pembelajaran mengusulkan perbaikan melalui lifecycle sah; tidak mengubah policy otomatis.

### 3.11 Prinsip Pendukung

- **Evidence before authority exercise:** keputusan harus didukung evidence yang cukup.
- **Proportionality:** rigor, review, dan segregation meningkat bersama risiko dan irreversibility.
- **Subsidiarity:** keputusan dibuat pada level kompeten terendah yang memiliki authority, lalu dieskalasikan bila batas terlampaui.
- **No silent delegation:** delegation, acting authority, dan proxy wajib eksplisit.
- **Fail closed:** ambiguity material pada authority, identity, approval, atau conflict of interest memblokir tindakan terdampak.
- **Reversibility and recovery:** keputusan berisiko memiliki rollback, expiry, atau recovery path bila mungkin.

## 4. Authority Model

Authority adalah hak terbatas untuk mengambil jenis keputusan tertentu dalam scope, batas risiko, durasi, dan kondisi yang terdokumentasi. Satu orang dapat memegang beberapa peran hanya jika separation-of-responsibility tetap terpenuhi.

### 4.1 Matriks Peran

| Peran | Hak | Tanggung jawab | Batas kewenangan |
| --- | --- | --- | --- |
| **Founder** | Ratifikasi Constitution; menetapkan arah fundamental; menunjuk/mencabut authority utama; memutus konflik strategis; menerima risiko strategis yang lawful | Menjaga purpose, amanah, human interest, dan audit trail keputusan fundamental | Tidak dapat mengubah fakta, menghapus audit trail, mengesampingkan hukum/keselamatan/hak, atau mendelegasikan ratifikasi final kepada AI |
| **AI Executive** | Mengoordinasikan AI Agent dan portfolio execution dalam mandate tertulis; mengusulkan keputusan dan prioritas; mengeksekusi keputusan approved | Menjaga scope, dependency, evidence, escalation, serta konsistensi lintas agent | Bukan Founder, legal officer, human approver, atau risk owner; tidak dapat self-delegate, self-approve, mengubah Governance, atau menerima risiko material |
| **Domain Owner** | Menetapkan intended purpose, requirement, priority, lifecycle, acceptance, dan risk recommendation domain | Menjaga correctness, outcome, stakeholder, consumer, dan debt domain | Tidak dapat mengubah Constitution/Governance atau menyetujui di luar domain/delegation; tidak boleh melemahkan control lintas sistem sendirian |
| **Knowledge Steward** | Mengelola curation, provenance, confidence, verification, lifecycle, dan discovery knowledge lintas domain | Menjaga Knowledge System bebas dari SSOT tandingan dan status palsu | Tidak menetapkan fakta domain tanpa source/owner; verification bukan approval policy atau keputusan strategis |
| **Repository Maintainer** | Mengelola integritas repository, branch/PR/merge/release sesuai delegation, access request, dan recovery teknis | Menjaga history, protection, traceability, availability, serta least privilege | Akses admin, commit, merge, tag, atau release bukan authority normatif, approval konten, atau risk acceptance |
| **Reviewer** | Memeriksa artefak/evidence, memberi finding, rekomendasi, dan review decision dalam kompetensi/delegation | Menyatakan conflict of interest, limitation, dan rationale; menjaga independence | Tidak mengubah artefak diam-diam, approve di luar kompetensi, atau menggantikan approver kecuali delegation eksplisit |
| **Contributor** | Mengusulkan dan membuat perubahan dalam scope akses; merespons review; menyediakan evidence | Mematuhi source, standard, security, documentation, quality, dan Git workflow | Tidak dapat menetapkan status Approved, memberi exception, mengubah ownership, atau mengklaim authority karena authorship |
| **Observer** | Membaca informasi yang diizinkan, memberikan feedback, dan melaporkan concern | Menjaga confidentiality dan menggunakan jalur escalation yang benar | Tidak memiliki write, approval, delegation, operational instruction, atau access-escalation right secara default |

### 4.2 Hubungan Antarperan

- Founder menunjuk atau mengesahkan authority manusia utama dan dapat mencabut delegation.
- Domain Owner accountable atas outcome domain; Contributor/AI Executive dapat menjadi executor, Reviewer memberi assurance, dan Repository Maintainer menjaga integritas teknis.
- Knowledge Steward menjaga kualitas knowledge lintas domain tanpa mengambil ownership domain.
- Approver adalah peran keputusan yang dipegang oleh Founder atau manusia yang didelegasikan; `Reviewer` tidak otomatis `Approver`.
- Observer dapat mengangkat concern tanpa retaliation, tetapi concern tidak otomatis mengubah keputusan.
- Untuk high/critical, proposer/executor tidak boleh menjadi satu-satunya reviewer, approver, auditor, atau risk acceptor.

### 4.3 Delegation Contract

Delegation wajib mencatat:

- delegator, delegate, role, dan kompetensi;
- decision rights yang diizinkan dan yang dilarang;
- scope domain/repository/artefak, risk ceiling, dan financial/data boundary bila relevan;
- effective time, expiry, review cadence, serta revocation trigger;
- required reviewer/approver, separation of duties, dan escalation path;
- evidence, decision-log location, serta fallback ketika delegate tidak tersedia.

Delegation tidak boleh tersirat dari job title, akses teknis, historical behavior, silence, atau output sukses. Sub-delegation dilarang kecuali diizinkan eksplisit. Expired/revoked delegation menghentikan tindakan baru; tindakan terdahulu direview bila validitasnya terdampak.

## 5. Decision Governance

### 5.1 Klasifikasi Keputusan

| Kelas | Contoh | Default authority |
| --- | --- | --- |
| **D0 — deterministic/automatic** | Format, lint, link check, calculation, routing yang sepenuhnya mengikuti rule approved dan reversible | Automation/AI sesuai mandate; hasil dicatat bila material |
| **D1 — routine delegated** | Editorial non-semantik, maintenance low-risk, tindakan reversible dalam playbook approved | Delegate manusia; AI dapat mengeksekusi jika eksplisit diizinkan |
| **D2 — domain material** | Perubahan requirement, architecture, policy domain, publication, release, access, atau medium/high risk | Domain Owner + review/approval yang diwajibkan |
| **D3 — strategic/fundamental** | Constitution, identity, Vision/Mission/Values, governance hierarchy, authority utama, irreversible/high-impact cross-domain, critical risk acceptance | Founder; expert/human review wajib sesuai konteks |
| **Emergency** | Tindakan containment segera untuk melindungi manusia, data, integritas, atau service | Authority manusia on-call yang ditunjuk; scope minimum, expiry, post-review wajib |

Automation hanya boleh memutus D0 dan bagian D1 yang rule, input, threshold, rollback, owner, monitoring, dan stop condition-nya approved. Uncertainty, exception, material impact, atau rule conflict menaikkan kelas dan memerlukan manusia.

### 5.2 Decision Record Minimum

Keputusan material mencatat ID, tanggal, status, proposer, decision owner, reviewer, approver, scope, class/risk, sumber authority, opsi/trade-off, evidence, conflict/dissent, keputusan/rationale, condition, residual risk/risk owner, effective/expiry, affected artefact/consumer, implementation/rollback, dan verification.

### 5.3 Keputusan yang Memerlukan Persetujuan

Persetujuan manusia eksplisit wajib untuk:

- D2/D3, high/critical risk, irreversible action, atau dampak lintas domain material;
- perubahan policy, standard normatif, architecture baseline, ownership, delegation, access privilege, publication/release material, atau konfigurasi AI berisiko;
- exception, bypass, residual-risk acceptance, archive/destruction evidence, dan penggunaan data sensitif baru;
- tindakan yang diwajibkan Constitution, Governance, law, security/privacy, atau owner domain;
- keputusan dengan conflict of interest yang tidak dapat dimitigasi tanpa reviewer/approver independen.

### 5.4 Escalation Path

Default escalation:

```text
Contributor / Observer / AI Agent
  → Repository Maintainer, Knowledge Steward, atau Reviewer terkait
  → Domain Owner
  → AI Executive untuk koordinasi (bukan approval manusia)
  → Founder untuk D3, conflict antar-owner, atau authority gap
```

Security, privacy, legal, safety, ethics, atau suspected abuse menggunakan jalur specialist/private lebih dahulu dan dapat langsung ke Founder. Escalation record memuat trigger, urgency, affected scope, evidence, action yang sudah diambil, decision needed, deadline, dan safe state.

### 5.5 Exception Handling

Exception bukan approval umum atau pass. Exception wajib memiliki source rule, authority manusia, alasan, scope sempit, risk assessment, compensating control, owner, start, expiry, review cadence, consumer notice, revocation condition, dan audit trail. Exception terhadap Constitution dilarang. Repeated exception memicu policy/control review; expiry menghentikan penggunaan bergantung sampai resolution sah.

### 5.6 Conflict Resolution

1. Hentikan area terdampak dan pertahankan safe state/evidence.
2. Identifikasi sumber, status, versi, specificity, authority, dan pihak terdampak.
3. Terapkan precedence normatif.
4. Minta review owner/ahli dan nyatakan conflict of interest.
5. Gunakan aturan lebih ketat sementara jika lawful dan proporsional.
6. Eskalasikan konflik setingkat ke authority bersama yang lebih tinggi.
7. Founder menjadi final authority internal untuk konflik strategis/konstitusional, tanpa mengesampingkan hukum atau keselamatan.
8. Catat keputusan, dissent, migration, serta verification; jangan menyelesaikan konflik dengan duplikasi SSOT.

### 5.7 Final Authority dan Final Approval

Founder adalah final authority internal untuk Constitution, arah fundamental, authority hierarchy, dan konflik strategis. Domain Owner dapat menjadi final approver domain hanya dalam delegation serta risk ceiling yang sah. Final Approval mengidentifikasi artefak/version/commit, scope, evidence/gate, condition, residual risk, tanggal, dan approver. AI Executive/AI Agent tidak dapat memberi Final Approval yang memerlukan manusia.

## 6. Ownership Model

Ownership adalah akuntabilitas pemeliharaan dan keputusan, bukan kepemilikan legal otomatis. Setiap artefak memiliki satu accountable owner; co-owner hanya digunakan dengan decision boundary eksplisit.

| Objek | Accountable owner default | Decision rights | Review/approval minimum | Boundary |
| --- | --- | --- | --- | --- |
| **Repository** | Repository Maintainer yang ditunjuk; Founder accountable untuk penunjukan utama | Access, protection, branch/release process, integrity, recovery | Content owner untuk makna; Founder untuk transfer/admin authority material | Maintainer tidak memiliki seluruh konten |
| **Domain Knowledge** | Domain Owner; Knowledge Steward menjaga sistem lintas domain | Source, confidence, verification, lifecycle, consumer | Steward + affected owner untuk lintas domain | Knowledge tidak otomatis menjadi policy |
| **Documentation** | Owner artefak/domain; Documentation Steward untuk standard | Accuracy, completeness, lifecycle, publication | Reviewer sesuai risiko; approver untuk status normatif | Publisher tidak otomatis owner fakta |
| **Prompt** | Owner workflow/domain | Intent, input/output contract, allowed tools/data, version | AI/security/privacy/domain review sesuai risiko | Prompt tidak menjadi authority baru |
| **Policy** | Governance/Domain Owner yang ditetapkan | Rule wajib, scope, exception, enforcement, review | Founder untuk fundamental; human authority yang didelegasikan untuk domain | AI tidak approve policy |
| **Standard** | Standard/Quality owner yang ditetapkan | Criteria, testability, version, conformance | Affected domain + Quality/Governance review | Standard tidak mengubah policy |
| **Architecture** | Architecture/Domain Owner yang ditetapkan | Baseline, interface, dependency, trade-off, migration | Affected owners; Founder untuk fundamental cross-ecosystem | Maintainer/executor tidak self-approve material drift |
| **Product** | Product/Domain Owner manusia | Purpose, requirement, priority, release acceptance, outcome | Stakeholder dan specialist review sesuai risiko | SPOS/AI tidak memiliki kebutuhan bisnis |
| **AI Agent Configuration** | Human Domain Owner; AI Executive mengoordinasikan sesuai mandate | Model/tool/data access, system instruction, autonomy, limits, monitoring, rollback | Governance, security/privacy, quality, dan Founder untuk high-impact | AI tidak mengubah authority/autonomy-nya sendiri |

Ownership record minimum: object/scope, owner, backup/delegate, rights, obligations, risk ceiling, dependencies, review cadence, effective/expiry, transfer/succession, dan decision-log location. Transfer ownership memerlukan acceptance eksplisit, access update, handoff, unresolved-risk disclosure, dan consumer notification.

## 7. Governance Lifecycle

### 7.1 Proposal

Catat masalah, proposer, intended outcome, scope/non-scope, affected authority/owner, evidence, urgency, risk, dan candidate decision class.

### 7.2 Review

Validasi source, Constitution alignment, stakeholder, options, impact, conflict of interest, security/privacy/legal/safety, ownership, resource, migration, reversibility, dan quality evidence. Dissent dipertahankan.

### 7.3 Approval

Approver memverifikasi authority, review completeness, conditions, residual risk, effective date, version, expiry/review trigger, serta implementation owner. Silence, commit, merge, atau penggunaan tidak menjadi approval.

### 7.4 Implementation

Terapkan perubahan secara incremental pada source kanonik; perbarui access, configuration, documentation, consumer, training, dan rollback plan. Executor tidak boleh memperluas keputusan.

### 7.5 Monitoring

Pantau adoption, compliance, outcome, incident, exception, metric, drift, unintended impact, dan owner availability. Monitoring harus menghasilkan action threshold yang jelas.

### 7.6 Audit

Periksa desain serta efektivitas governance, sample keputusan, authority, ownership, evidence, exception, access, lifecycle, dan outcome dengan auditor kompeten/independen sesuai risiko.

### 7.7 Improvement

Temuan, root cause, feedback, dan perubahan konteks menghasilkan corrective/preventive proposal. Improvement mengikuti lifecycle penuh bila mengubah makna atau authority.

### 7.8 Retirement

Cabut authority/access yang tidak lagi perlu, tandai deprecated/superseded/retired, migrasikan consumer, pertahankan evidence sesuai retention, komunikasikan effective date, dan verifikasi tidak ada dependency aktif yang yatim.

### 7.9 State dan Re-entry

State minimum: `Proposed → Draft → In Review → Approved → Active → Suspended → Retired/Archived`, dengan `Rejected`, `Superseded`, dan `Revoked` bila relevan. Perubahan material, incident, audit failure, atau dependency change mengembalikan artefak ke review. Status teknis tidak boleh disamakan dengan status normatif.

## 8. Compliance dan Audit

### 8.1 Governance Audit

Program audit risk-based mencakup:

- authority/delegation validity dan least privilege;
- ownership coverage, succession, serta orphaned artefact;
- decision classification, review, approval, dissent, dan traceability;
- separation of responsibilities serta conflict of interest;
- exception, access, AI autonomy, risk acceptance, dan lifecycle;
- implementation effectiveness serta consumer impact, bukan checklist presence saja.

Audit event-driven wajib setelah suspected abuse, unauthorized approval, critical incident, material authority change, repeated exception, stale owner, or metric anomaly. Auditor tidak mengaudit keputusan materialnya sendiri sebagai satu-satunya assurance.

### 8.2 Compliance Review

Compliance review memetakan requirement → control → owner → evidence → status → gap → action. Status: `Conformant`, `Partially Conformant`, `Non-Conformant`, `Not Applicable` dengan rationale, atau `Blocked`. `N/A` tidak boleh digunakan untuk menghindari control.

### 8.3 Policy Violation Handling

1. Deteksi dan validasi signal tanpa retaliation.
2. Hentikan propagation/harm dan lindungi pihak terdampak.
3. Preservasi evidence dengan least disclosure.
4. Nilai severity, blast radius, dan notification duty.
5. Cabut/suspend access atau automation bila diperlukan.
6. Investigasi oleh pihak kompeten dan cukup independen.
7. Terapkan remediation, restoration, communication, dan accountability proporsional.
8. Verifikasi efektivitas, tutup dengan authority, serta record lesson learned.

Proses harus fair, menjaga confidentiality, tidak menghapus due process, dan tidak menggunakan AI sebagai satu-satunya penentu sanksi material.

### 8.4 Corrective dan Preventive Action

Corrective action menangani violation/finding aktual melalui containment, root cause, remediation, regression check, dan effectiveness verification. Preventive action memperbaiki role design, delegation, access, training, review, policy, standard, monitoring, atau automation berdasarkan pola evidence. Owner, due date, severity, reviewer, residual risk, serta closure authority wajib jelas.

### 8.5 Governance Reporting

Report periodik memuat:

- active/expired/revoked delegation dan ownership gap;
- keputusan menurut kelas, overdue approval, dissent, dan escalation;
- exception volume/age/expiry/recurrence;
- violation/finding/CAPA status dan aging;
- access/AI autonomy change serta least-privilege review;
- audit scope, limitation, effectiveness, residual risk, dan trend;
- keputusan/dukungan yang dibutuhkan dari Founder atau owner.

Metric bukan approval. Agregasi tidak boleh menyembunyikan critical finding, conflict, atau pihak terdampak.

## 9. AI Governance Policy

### 9.1 Batas Kewenangan AI

AI boleh membaca sumber yang diizinkan, menganalisis, mengusulkan, membuat draft, mengeksekusi D0/D1 yang eksplisit, melakukan self/cross-review, menjalankan check, menyusun evidence, mendeteksi conflict, serta merekomendasikan escalation/CAPA.

AI tidak boleh:

- menjadi Founder, human accountable owner, approver, auditor independen, atau risk acceptor;
- meratifikasi/amend Constitution atau mengubah Governance/authority/ownership/delegation;
- memperluas tool, data, permission, autonomy, scope, atau expiry-nya sendiri;
- memberi exception, bypass, Final Approval, sanksi material, atau destructive/irreversible authorization;
- mengarang identity, consent, reviewer, approval, evidence, decision, atau compliance;
- menyembunyikan uncertainty, conflict, violation, limitation, atau human-impact risk.

### 9.2 Pekerjaan yang Wajib Meminta Persetujuan Founder

AI wajib meminta Founder untuk:

- Constitution, Kernel fundamental, identity, Vision, Mission, Values, Ethics, Canon, dan arah strategis;
- governance hierarchy, authority model utama, penunjukan/pencabutan role utama, atau delegation setara Founder;
- D3, critical residual risk, exception fundamental, atau konflik antar-Domain Owner yang tidak terselesaikan;
- high-impact AI autonomy, deployment lintas ekosistem, irreversible action, atau penggunaan sensitif yang mengubah risk posture secara fundamental;
- aktivasi/retirement engine inti atau klaim status fundamental tanpa delegation lain yang sah.

### 9.3 Capability dan Automation

Sebelum capability/automation aktif, wajib ada owner manusia, purpose, allowed input/output/action, data/access scope, risk class, approval, test/evidence, monitoring, rate/impact limit, human override, stop condition, rollback, audit log, dan expiry/review trigger. Default adalah deny untuk capability yang tidak disebutkan.

AI menggunakan least privilege dan melakukan preflight sebelum tindakan material. Chained automation dinilai berdasarkan dampak akhir, bukan langkah individual. Automation yang mengubah policy, role, permission, model/tool source, atau safety control memerlukan re-review.

### 9.4 Automatic Stop

AI/automation wajib menghentikan area terdampak, mempertahankan safe state, dan eskalasi jika:

- instruksi bertentangan dengan Constitution/Governance, hukum, keselamatan, atau authority yang lebih tinggi;
- identity, authority, delegation, consent, ownership, source, atau decision class material ambigu;
- required approval/reviewer tidak tersedia atau conflict of interest belum dikelola;
- scope/tool/data access akan terlampaui, privilege escalation diperlukan, atau secret/data sensitif terpapar;
- tindakan destructive, irreversible, high/critical risk, atau lintas domain tidak memiliki persetujuan;
- evidence hilang/tidak dapat dipercaya, control gagal, audit log tidak tersedia, atau automation berperilaku di luar expected boundary;
- AI diminta self-approve, menyembunyikan finding, menghapus evidence, atau mengklaim completion palsu.

AI boleh melanjutkan bagian independen yang aman hanya jika dependency dan blast radius jelas. Laporan stop memuat trigger, tindakan yang dihentikan, state aman, evidence, impact, authority yang dibutuhkan, dan recovery option.

## 10. Cross-System Alignment

| Sumber | Implementasi Governance | Boundary |
| --- | --- | --- |
| [`CONSTITUTION.md`](CONSTITUTION.md) | Constitution First, Founder Authority, hierarchy, human oversight, amanah, transparency, accountability, exception prohibition | Governance tidak meratifikasi/mengubah Constitution |
| [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) | Decision gates, autonomy, approval, stop, rollback, repository behavior, dan reporting | Governance menetapkan siapa berwenang; Developer Mode menetapkan perilaku AI |
| [`SESSION_ENGINE.md`](SESSION_ENGINE.md) | Session identity, lifecycle orchestration, state-transition authority, continuity, closure, cancellation, dan archive | Governance menetapkan decision rights; Session Engine merekam serta menegakkan gate per unit kerja |
| [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) | Authority check, execution checkpoint, escalation, evidence, completion criteria | Execution Engine tetap sumber prosedur eksekusi di dalam session |
| [`GIT_ENGINE.md`](GIT_ENGINE.md) | Repository role, access, review/approval separation, merge/release authority, audit/recovery | Git event dan admin access bukan authority normatif |
| [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) | Documentation ownership, approval, publication/archive, lifecycle, audit trail | Documentation Engine tetap sumber detail dokumentasi |
| [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) | Quality role, reviewer/auditor independence, Governance Review, Final Approval, finding/CAPA, risk acceptance | Quality Engine menilai kualitas; Governance menetapkan authority |
| [`REPORT_ENGINE.md`](REPORT_ENGINE.md) | Governance/Audit/Decision/Incident/Executive reporting, evidence/traceability, approval, publication, correction, dan aggregation guardrail | Governance menetapkan authority/decision rights; Report Engine menetapkan standard representasi laporan |
| [`../../01-foundation/FOUNDATION_ARCHITECTURE.md`](../../01-foundation/FOUNDATION_ARCHITECTURE.md) | Ownership, SSOT, evidence/feedback flow, decision, lifecycle, dan domain boundary | Governance tidak mengambil ownership domain |
| [`../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) | Domain Owner/Knowledge Steward, verification, approval, provenance, lifecycle | Knowledge tidak otomatis menjadi policy/authority |
| [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) | Hierarchy, control plane, module selection, conflict resolution, bounded execution | Governance adalah kontrak dokumentasi, bukan enforcement runtime |
| [`../03-sessions/SESSION_TEMPLATE.md`](../03-sessions/SESSION_TEMPLATE.md) | Authority/delegation, decision class, owner/reviewer/approver, exception, escalation, evidence | Template menginstansiasi, bukan menduplikasi policy |

### 10.1 Resolusi Cross-Review SPOS-008

- Governance Engine menjadi SSOT lintas sistem untuk authority, ownership, delegation, approval, exception, escalation, lifecycle governance, conflict resolution, Final Authority, dan AI governance.
- Constitution tetap authority tertinggi di dalam SPOS setelah ratifikasi; Governance tidak mengisi atau meniru ratification.
- Session Engine memiliki lifecycle orchestration/state/continuity session; Execution Engine memiliki prosedur eksekusi/checkpoint/completion; Governance lifecycle mengatur kebijakan/authority/ownership dan tidak membuat workflow session tandingan.
- Quality Engine tetap memiliki quality gate, DoD, metric, audit-quality, dan CAPA; Governance menetapkan reviewer/auditor independence, decision right, exception, serta risk-acceptance authority.
- Report Engine menetapkan taxonomy/lifecycle/structure/evidence laporan; Governance tetap menetapkan siapa yang boleh review, approve, publish, memberi exception, menerima risiko, atau mengarsipkan report.
- Git, Documentation, Knowledge, Architecture, dan Product owner mempertahankan detail domain. Governance menetapkan hak/batas/relasi, bukan mengambil correctness domain.
- Foundation governance README menjadi indeks/domain pointer ke dokumen ini, bukan SSOT tandingan.
- AI Executive adalah role koordinasi AI yang selalu berada di bawah human authority; nama role tidak memberi status eksekutif manusia atau approval right otomatis.
- Scope SPOS-008 documentation-only; tidak ada IAM, dashboard, compliance platform, policy runtime, produk, atau automation yang dibangun.

## 11. Activation dan Change Control

Aktivasi memerlukan:

- Constitution diratifikasi atau Founder mengizinkan baseline interim secara eksplisit;
- Founder menyetujui version, scope, effective date, dan hierarchy Governance;
- manusia yang disebut sebagai role/owner menerima penunjukan dan delegation tertulis;
- mapping consumer, access, role, risk ceiling, decision class, exception, escalation, audit, dan record location;
- review kompatibilitas seluruh engine serta migration dari ambiguity fail-closed;
- monitoring, review cadence, evidence retention, emergency path, dan revocation process yang dapat diverifikasi.

Activation record:

- Approver: `<Founder>`
- Decision: `<approved / rejected / revision required>`
- Effective date: `<YYYY-MM-DD>`
- Version approved: `<version>`
- Constitution dependency: `<version and status>`
- Role/delegation registry: `<reference>`
- Ownership registry: `<reference>`
- Decision/exception/audit registry: `<reference>`
- Consumer migration evidence: `<reference>`
- Review/expiry trigger: `<reference>`
- Commit hash: `<hash>`

AI tidak boleh mengisi approval/acceptance atas nama manusia. Perubahan material pada authority, role, ownership, decision class, delegation, exception, conflict resolution, lifecycle, audit, AI boundary, atau Final Authority memerlukan proposal, impact analysis, review, versioning, migration, dan Founder approval sesuai tingkatnya.

## 12. Governance Engine Review Checklist

- [x] Constitution First, Human Stewardship, Founder Authority, Amanah, Transparency, Accountability, Auditability, Least Privilege, Separation of Responsibility, dan Continuous Governance terdokumentasi.
- [x] Founder, AI Executive, Domain Owner, Knowledge Steward, Repository Maintainer, Reviewer, Contributor, dan Observer memiliki hak, tanggung jawab, batas, serta hubungan eksplisit.
- [x] Automatic/delegated/domain/strategic/emergency decision, approval, escalation, exception, conflict resolution, Final Authority, dan decision record terdokumentasi.
- [x] Ownership Repository, Domain Knowledge, Documentation, Prompt, Policy, Standard, Architecture, Product, dan AI Agent Configuration terdokumentasi.
- [x] Proposal, Review, Approval, Implementation, Monitoring, Audit, Improvement, dan Retirement terdokumentasi.
- [x] Governance audit, compliance review, violation handling, corrective/preventive action, dan reporting terdokumentasi.
- [x] AI authority boundary, Founder approval, capability/automation guardrail, dan automatic stop terdokumentasi.
- [x] Alignment dengan Constitution, Developer Mode, Session Engine, Execution Engine, Git Engine, Documentation Engine, Quality Engine, Report Engine, Foundation, Knowledge System, SPOS Architecture, dan Session Template dipetakan.
- [x] Scope tidak membangun aplikasi, fitur produk, IAM, governance dashboard, compliance platform, policy runtime, database, deployment, atau automation.
- [ ] Constitution diratifikasi atau baseline interim diizinkan Founder secara eksplisit.
- [ ] Governance Engine memperoleh Founder approval dan activation record.
- [ ] Role/delegation/ownership/decision/exception/audit registry serta human role acceptance tersedia.
- [ ] Access enforcement, Session Engine transition authority/registry, Report Engine ownership/classification/retention/publication controls, consumer migration, monitoring, evidence retention, emergency operation, dan conformance automation diterapkan serta diverifikasi.
