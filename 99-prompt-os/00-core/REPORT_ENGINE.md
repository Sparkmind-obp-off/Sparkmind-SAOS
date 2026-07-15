# SparkMind Report Engine

> Status: In Review — reporting-governance baseline SPOS-010; activation as a binding standard requires Founder approval and eligible upstream versions.
>
> Owner: Founder
>
> Reviewer: Founder, Governance owner, Report owner/steward, Session owner, Quality owner, Documentation owner, Knowledge Steward, Repository Maintainer, Domain Owner, dan pihak terdampak yang ditunjuk
>
> Approver: Founder atau authority manusia yang didelegasikan secara tertulis untuk reporting policy non-konstitusional
>
> Version: 0.1.0
>
> Established: 2026-07-15
>
> Effective: setelah approval operasional yang sah, activation record, dan dependency upstream terpenuhi
>
> Review trigger: amendment Constitution; perubahan Governance, Developer Mode, Session, Execution, Git, Documentation, Quality, Foundation, Knowledge System, atau SPOS Architecture; perubahan kewajiban audit/retensi/klasifikasi; insiden pelaporan material; report drift berulang; atau evidence bahwa standard tidak lagi efektif

## 1. Kedudukan dan Tujuan

Report Engine adalah standar permanen dan single source of truth untuk bentuk, lifecycle, bukti, keterlacakan, validasi, publikasi, versioning, koreksi, serta pengarsipan laporan di seluruh ekosistem SparkMind. Engine memastikan aktivitas, perubahan, keputusan, validasi, insiden, audit, dan pembelajaran dapat ditelusuri, diperiksa, direproduksi secara proporsional, dan digunakan kembali tanpa menjadikan laporan sebagai sumber authority tandingan.

Engine ini mengoperasionalkan [`CONSTITUTION.md`](CONSTITUTION.md), [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md), [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md), [`SESSION_ENGINE.md`](SESSION_ENGINE.md), [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md), [`GIT_ENGINE.md`](GIT_ENGINE.md), [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md), [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md), dan [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md). Report Engine memiliki taxonomy, report lifecycle, struktur baku, evidence/traceability contract, serta reporting policy. Engine domain tetap memiliki semantik sumber: Governance untuk authority/approval, Quality untuk gate/audit/finding, Git untuk version trace, Documentation untuk tata kelola dokumen, Session untuk orkestrasi dan closure, serta Knowledge untuk curation/provenance.

Report Engine bukan dashboard, database, reporting service, analytics platform, log aggregator, workflow runtime, generator otomatis, aplikasi, atau fitur produk. Report, commit, publication, signature, atau status `Completed` tidak menciptakan approval, authority, correctness, risk acceptance, maupun pengetahuan approved.

Karena Constitution dan seluruh engine dependency masih `In Review`, Report Engine juga `In Review`. Baseline dapat digunakan untuk drafting, review, dan pengendalian interim secara fail-closed, tetapi tidak menjadi bukti activation atau approval.

## 2. Scope dan Non-Scope

### 2.1 Scope

Engine mengatur:

- taxonomy laporan dan aturan pemilihan jenis;
- lifecycle dari initialization sampai archival dan traceability;
- struktur baku, metadata, status, identitas, serta hubungan antar-report;
- evidence, claim, source, commit, branch, repository, session, decision, artefak, dan audit trail;
- reproducibility, validation, review, approval, publication, versioning, correction, supersession, retention, dan archive;
- confidentiality, privacy, least disclosure, redaction, access, serta sensitive-data handling;
- agregasi, executive summary, metric, dan anti-misrepresentation guardrail;
- kewajiban laporan per session dan batas AI dalam menyusun serta memvalidasi laporan;
- referensi silang laporan dengan seluruh engine SPOS, Foundation, dan Knowledge System.

### 2.2 Non-Scope

Engine tidak:

- mengubah source artefak, keputusan, test, audit evidence, atau approval record menjadi isi report semata;
- menetapkan fakta domain, requirement produk, decision right, quality gate, retention legal, atau risk appetite tanpa owner;
- menggantikan audit independen, specialist review, incident response, release authorization, atau governance decision;
- menganggap semua report boleh dipublikasikan atau memiliki audience yang sama;
- membangun dashboard, database, API, automation runtime, data warehouse, telemetry pipeline, notification, deployment, atau fitur produk;
- mewajibkan penyimpanan transcript mentah, secret, credential, data pribadi, atau bukti sensitif di repository publik;
- menjadikan jumlah report, panjang report, atau metric agregat sebagai proxy otomatis kualitas.

## 3. Prinsip Pelaporan

1. **Truth Before Narrative:** actual state, failure, limitation, unknown, dissent, dan residual risk lebih penting daripada narasi yang tampak sukses.
2. **Evidence Before Claim:** klaim material memiliki evidence atau diberi label assumption, inference, estimate, recommendation, maupun unverified.
3. **Single Source of Truth:** report merangkum dan merujuk sumber kanonik; report tidak menyalin atau menggantikan policy, decision, artefact, test output, atau approval record.
4. **Traceability by Design:** objective, scope, deliverable, change, evidence, validation, decision, risk, actor, waktu, version, serta outcome dapat dihubungkan dua arah secara proporsional.
5. **Reproducible in Context:** pembaca berwenang dapat memahami input, version, environment, method, dan limitation untuk mengulang atau memverifikasi klaim yang memang dapat direproduksi.
6. **Lifecycle Integrity:** status report, status session, status artefak, quality result, governance approval, dan Git event adalah dimensi terpisah.
7. **Proportional Completeness:** detail mengikuti risiko, longevity, audience, dan kebutuhan audit; ringkas tidak boleh menghilangkan fakta material, panjang tidak boleh menjadi filler.
8. **Least Disclosure:** report menyimpan bukti minimum yang cukup, dengan reference/redaction/access control untuk material sensitif.
9. **Human Accountability:** laporan menyatakan owner, reviewer, approver, serta batas AI; AI tidak menjadi approver, auditor independen, atau risk acceptor.
10. **Preserve Failure and Dissent:** failure, rollback, unresolved finding, dissent, exception, dan corrective action tidak dihapus untuk membuat hasil tampak bersih.
11. **Correctable, Not Rewritten:** koreksi mempertahankan versi lama, alasan, actor, tanggal, impact, serta link ke versi pengganti.
12. **Audience and Action Oriented:** laporan menjelaskan siapa yang perlu mengetahui apa, keputusan/tindakan apa yang diperlukan, owner, dan waktunya.

## 4. Authority, Ownership, dan Identitas Report

### 4.1 Peran

| Peran | Tanggung jawab | Batas |
| --- | --- | --- |
| **Founder** | Approval fundamental, arah reporting lintas ekosistem, serta risk acceptance strategis | Tidak dapat mengubah fakta atau menghapus audit trail |
| **Governance owner** | Delegation, publication/retention authority, exception, escalation, dan auditability | Tidak menetapkan correctness domain sendirian |
| **Report owner/steward** | Taxonomy, struktur, lifecycle, registry/index, quality portfolio, dan consistency | Tidak mengambil ownership isi domain atau self-approve material report |
| **Domain/Session owner** | Akurasi scope, outcome, deliverable, decision, risk, dan next action domain/session | Tidak mengubah policy reporting tanpa process sah |
| **Evidence owner/custodian** | Integritas, akses, retention, provenance, dan availability evidence | Custody tidak sama dengan approval isi |
| **Author** | Mengumpulkan evidence, drafting, cross-reference, self-review, dan correction | Tidak mengarang bukti atau menyatakan independent review |
| **Reviewer** | Memeriksa claim-evidence, completeness, consistency, risk, reproducibility, dan disclosure | Tidak approve di luar kompetensi/delegation |
| **Approver** | Menyetujui report/version untuk audience dan purpose tertentu | Approval report tidak menyetujui seluruh artefak sumber |
| **Repository Maintainer** | Integritas file, Git trace, index, dan publication path repository | Commit/push tidak sama dengan approval report |
| **Knowledge Steward** | Menilai routing lesson/knowledge dan mencegah report menjadi knowledge SSOT | Laporan tidak otomatis menjadi approved knowledge |
| **AI Agent** | Drafting, extraction, cross-check, link/format/coverage validation, dan summary sesuai Section 12 | Bukan human approver, independent auditor, evidence source tanpa output aktual, atau risk owner |

Setiap report material memiliki satu accountable owner. Reviewer dan approver ditentukan berdasarkan taxonomy, risk, audience, classification, serta authority. Untuk report high/critical, incident, audit, governance, release, atau perubahan normatif, author/executor tidak boleh menjadi satu-satunya reviewer dan approver.

### 4.2 ID dan Penamaan

Report harus memiliki ID stabil atau hubungan langsung dengan ID sumber:

- Session Report: `SPOS-NNN` atau `SESSION-NNN` mengikuti session;
- report lain: namespace domain yang memiliki uniqueness rule dan registry/index, misalnya `AUDIT-NNN`, `INCIDENT-NNN`, atau `RELEASE-NNN`;
- nama file repository menggunakan ID stabil atau `UPPER_SNAKE_CASE.md` sesuai [`../../docs/standards/NAMING_CONVENTION.md`](../../docs/standards/NAMING_CONVENTION.md);
- ID tidak dipakai ulang; koreksi/version baru mempertahankan lineage dan tidak menyamarkan report lama.

### 4.3 Status Report

Status minimum:

- `Draft`: sedang disusun dan belum tervalidasi;
- `In Review`: siap atau sedang direview;
- `Approved`: content/version disetujui authority untuk purpose/scope tertentu;
- `Published`: tersedia melalui channel resmi untuk audience yang ditetapkan;
- `Corrected`: memiliki koreksi terotorisasi dan menunjuk versi current;
- `Superseded`: diganti report/version lain;
- `Archived`: tidak current dan dipertahankan untuk retention/audit.

Status report tidak menyiratkan status session atau artefak. Report dapat `Published` untuk transparency dengan finding terbuka; report dapat `Approved` sementara artefak sumber tetap `In Review`; session dapat `Completed` sementara Report Engine tetap belum aktif.

## 5. Report Taxonomy

Satu report memiliki primary type. Secondary type hanya dicatat jika satu artefak benar-benar memenuhi dua kebutuhan tanpa mencampur authority, audience, retention, atau approval path. Jika boundary berbeda material, buat report terpisah dengan cross-reference.

| Kategori | Tujuan | Isi minimum khusus | Kapan digunakan |
| --- | --- | --- | --- |
| **Session Report** | Merekam objective, pekerjaan, evidence, state, closure, dan continuity satu session | session ID/type/state history, deliverable/change, validation, Git trace, blocker/debt/risk, handoff/successor | Setiap session; final sebelum `Completed/Cancelled`, interim untuk `Blocked/Waiting for Approval` |
| **Governance Report** | Menilai authority, ownership, delegation, decision, exception, compliance, dan control effectiveness | authority/delegation state, decision/escalation, exception, violation/CAPA, ownership gap, residual risk | Review governance berkala, perubahan material, atau concern/violation |
| **Quality Report** | Menyajikan quality plan, gate, finding, metric, CAPA, dan outcome | criteria/version, gate result, evidence, severity, trend/limitation, corrective/preventive action | Quality review, readiness, portfolio health, atau effectiveness review |
| **Documentation Report** | Menilai completeness, currentness, lifecycle, link, ownership, publication, dan debt dokumentasi | inventory/sampling, source drift, broken links, stale owner/status, publication/deprecation action | Documentation audit/review, migration, atau major update |
| **Git Report** | Merekam integritas branch/commit/PR/merge/push/release/protection dan recovery | repository/branch/hash, diff scope, reviewer/check, remote verification, tag/release/recovery | Perubahan/release material, repository audit, migration, atau Git incident |
| **Audit Report** | Memberi assurance terhadap criteria melalui evidence dan sample yang jelas | objective/scope/criteria, auditor independence, method/sample, evidence, finding/severity, limitation, action | Audit terjadwal/event-driven atau compliance assurance |
| **Architecture Report** | Menjelaskan current/target state, review, drift, trade-off, dan migration readiness | boundary/component/dependency, decision links, conformance/drift, risk, migration/rollback | Architecture review, major design change, drift assessment, atau readiness |
| **Knowledge Report** | Merangkum provenance, coverage, confidence, gap, curation, dan knowledge lifecycle | source/provenance, verification/confidence, gap, status, affected consumer, curation recommendation | Knowledge review, research synthesis routing, onboarding/coverage assessment |
| **Decision Report** | Menyajikan satu atau sekumpulan keputusan material dan implementasi/outcome-nya | decision IDs, owner/class/authority, options/trade-off, rationale/dissent, implementation, verification | Decision review, portfolio synthesis, atau outcome follow-up; bukan pengganti decision record |
| **Incident Report** | Menjaga timeline faktual, impact, containment, recovery, cause, dan follow-up | severity, affected parties/system, timeline, evidence, containment, root cause status, CAPA, notification/lessons | Setelah incident atau near miss sesuai severity dan policy |
| **Release Report** | Menilai serta mencatat readiness, content, approval, publication, verification, dan rollback release | version/tag/commit, scope/change, gate, compatibility/migration, known issue, approval, rollout/rollback | Setiap release material atau release readiness decision |
| **Executive Summary** | Memberi view ringkas bagi decision maker tanpa menyembunyikan material detail | period/scope/source reports, key outcome, exceptions, critical risk, trend/limitation, decision/action needed | Portfolio/periodic review atau keputusan eksekutif; selalu merujuk report sumber |

### 5.1 Aturan Pemilihan

1. Pilih berdasarkan primary purpose dan decision need, bukan berdasarkan folder atau author.
2. Session Report selalu wajib; report domain tambahan dibuat jika risiko, audience, policy, atau audit need menuntut.
3. Audit Report memerlukan criteria dan independence; self-review biasa tidak boleh diberi label audit independen.
4. Incident Report mempertahankan timeline dan impact; jangan mengubahnya menjadi retrospective sanitasi.
5. Executive Summary tidak boleh menjadi satu-satunya record bagi critical finding, dissent, exception, atau source evidence.
6. Decision Report merangkum; decision record pada source kanonik tetap authoritative.
7. Knowledge Report memberi input curation; tidak otomatis mempromosikan klaim menjadi `Verified` atau `Approved`.
8. Report yang memiliki classification, retention, atau audience berbeda wajib dipisah atau memiliki controlled annex.

## 6. Report Lifecycle

Lifecycle kanonik:

```text
Report Initialization
  → Evidence Collection
  → Validation
  → Drafting
  → Review
  → Approval
  → Publication
  → Versioning
  → Archival
  → Traceability
```

`Traceability` adalah kewajiban lintas lifecycle dan gate penutup, bukan hanya langkah terakhir. Lifecycle dapat kembali ke Evidence Collection, Validation, atau Drafting ketika claim/source berubah. Tahap yang tidak berlaku diberi `Not Applicable` dengan alasan dan authority yang sesuai.

### 6.1 Report Initialization

**Tujuan:** membentuk report contract yang unik, bounded, dan purpose-driven.

Wajib tetapkan:

- report ID, title, taxonomy, objective, audience, owner, author, reviewer, approver;
- scope/non-scope, period/as-of time, source session/decision/incident/release, dan expected use;
- classification, publication channel, retention, legal/security/privacy constraint;
- claim/evidence plan, materiality, quality criteria, dependency, serta completion gate;
- lokasi kanonik, version baseline, predecessor/supersession, dan conflict check.

**Output:** report contract dan source/evidence plan.

**Exit:** tujuan, owner, scope, source, audience, serta handling rule jelas.

### 6.2 Evidence Collection

**Tujuan:** mengumpulkan evidence aktual yang cukup dan aman.

Wajib:

1. gunakan source kanonik dan output aktual terlebih dahulu;
2. catat source owner, location, version/commit, time, environment, method, scope, serta classification;
3. pertahankan positive, negative, failure, dissent, limitation, dan counter-evidence;
4. hash/reference bukti immutable bila risikonya memerlukan;
5. bedakan observed fact, derived calculation, testimony, assumption, estimate, dan recommendation;
6. jangan menyalin secret/data sensitif jika reference terkendali cukup.

**Output:** evidence manifest dan initial claim-evidence map.

**Exit:** setiap klaim material memiliki bukti kandidat atau gap eksplisit.

### 6.3 Validation

**Tujuan:** membuktikan evidence relevan, authentic secara proporsional, current, complete, dan cukup untuk klaim.

Validasi mencakup:

- source/version/time/environment sesuai claim;
- method dan expected result dapat diperiksa;
- completeness terhadap objective/scope/material risk;
- conflict, anomaly, stale evidence, sampling bias, dan missing denominator;
- reproducibility atau alasan non-reproducibility;
- security/privacy/classification dan redaction quality;
- cross-check terhadap repository, remote, decision, approval, report terkait, serta actual state.

Hasil per check: `Pass`, `Fail`, `Blocked`, atau `Not Applicable` dengan evidence, actor, time, dan rationale.

**Output:** validation record, gap/finding, dan claim status.

**Exit:** tidak ada klaim material yang disajikan sebagai fact tanpa evidence valid atau label keterbatasan.

### 6.4 Drafting

**Tujuan:** menyusun narasi akurat dari evidence tervalidasi.

Wajib:

- gunakan struktur Section 7 secara proporsional;
- pisahkan fakta, keputusan, interpretation, assumption, risk, debt, lesson, dan recommendation;
- tautkan evidence/source alih-alih menyalin seluruhnya;
- nyatakan as-of time, limitation, excluded scope, unresolved conflict, dan confidence bila relevan;
- gunakan bahasa yang dapat dipahami tanpa hidden conversation context;
- hindari generated filler, success bias, metric theater, dan unsupported causal claim.

**Output:** Draft report dan updated traceability matrix.

**Exit:** self-review completeness, link, terminology, sensitivity, dan consistency lulus.

### 6.5 Review

**Tujuan:** memeriksa correctness, evidence, authority, completeness, usability, dan risk.

Review minimum:

- owner/domain review untuk factual/domain correctness;
- Quality review untuk criteria, method, finding, dan limitation;
- Governance review untuk authority, approval, exception, publication, dan risk;
- Documentation review untuk struktur, lifecycle, source, index, dan usability;
- security/privacy/legal/specialist review sesuai classification dan impact;
- independence check untuk audit, high/critical, incident, governance, dan release report.

Komentar material diselesaikan, ditolak dengan rationale, atau dicatat sebagai blocker/dissent.

**Output:** review record, finding, remediation, dan recommendation.

**Exit:** report siap approval atau kembali ke tahap yang diperlukan.

### 6.6 Approval

**Tujuan:** authority manusia menyetujui report/version untuk purpose, scope, audience, dan publication tertentu.

Approval record minimum:

- approver identity dan source delegation;
- report ID, version/commit/content reference;
- decision, date/time, scope, audience, publication channel;
- condition, limitation, exception, residual risk, effective/expiry;
- dependency dan review trigger.

Approval report tidak sama dengan approval artefak sumber, release, risk, policy, atau session kecuali decision record eksplisit menyatakan scope tersebut. AI tidak dapat memberi approval manusia.

**Output:** approval/revision/rejection record.

**Exit:** keputusan sah tersedia atau report tetap `In Review`/`Blocked`.

### 6.7 Publication

**Tujuan:** membuat versi yang tepat tersedia bagi audience yang tepat.

Syarat:

- source version, approval, classification, redaction, access, dan channel benar;
- index/discovery dan cross-reference diperbarui;
- sensitive annex dipisah dan dilindungi;
- publication timestamp, publisher, version, audience, serta withdrawal/correction path dicatat;
- consumer tidak diarahkan ke Draft/Superseded tanpa label.

Publication tidak membuktikan approval, truth, atau completeness melebihi record. Draft boleh dibagikan untuk review hanya dengan label dan akses yang tepat.

**Output:** publication record dan discoverable report reference.

**Exit:** audience dapat menemukan current version tanpa exposure tidak sah.

### 6.8 Versioning

**Tujuan:** mempertahankan histori dan applicability ketika report berubah.

- Git adalah version history default untuk report repository.
- Editorial correction dapat memakai patch/revision kecil sesuai delegation.
- Perubahan klaim, scope, conclusion, finding, decision, risk, atau evidence bersifat material dan memerlukan revalidation/review; approval lama menjadi stale untuk bagian terdampak.
- Report periodik memperoleh ID/period baru, bukan menimpa histori.
- Correction dan supersession menyediakan link dua arah serta impact statement.
- Nama `final`, `latest`, `new`, `v2`, atau salinan manual tidak boleh menggantikan version control.

**Output:** version/change record, compatibility/impact, dan current-version pointer.

**Exit:** pembaca dapat membedakan current, historical, corrected, dan superseded version.

### 6.9 Archival

**Tujuan:** mempertahankan report non-current sesuai retention tanpa membingungkan consumer.

Wajib:

- authority, reason, date, retention, classification, hold, dan destruction eligibility jelas;
- index current menunjuk pengganti bila ada;
- evidence/report relation dan audit metadata dipertahankan;
- access dapat diperketat setelah operational need berakhir;
- secret/data pribadi tidak dipertahankan hanya untuk kenyamanan;
- deletion mengikuti legal/security/privacy authority dan tidak dipakai untuk menyembunyikan failure.

**Output:** archive record dan replacement/retention reference.

**Exit:** report tidak lagi dipakai sebagai current source tetapi tetap dapat diaudit sesuai izin.

### 6.10 Traceability

**Tujuan:** membuktikan lineage end-to-end dan memastikan closure report dapat diverifikasi.

Gate traceability memeriksa:

```text
objective / requirement
  ↕
session / decision / authority
  ↕
deliverable / change / commit / version
  ↕
evidence / validation / finding
  ↕
report claim / conclusion / recommendation
  ↕
approval / publication / action / outcome
```

Setiap link harus menunjuk source/version yang tepat. Broken lineage, missing evidence, conflicting status, atau unowned action menjadi finding dan dapat memblokir publication/closure sesuai materiality.

**Output:** final traceability matrix, audit trail, dan closure evidence.

**Exit:** klaim material dapat ditelusuri dua arah dan limitation tersisa terlihat.

## 7. Report Structure Standard

Struktur baku berikut wajib dipertimbangkan. Heading dapat digabung atau diberi `Not Applicable` dengan alasan untuk report sederhana; field material tidak boleh dihilangkan hanya agar report ringkas.

### 7.1 Metadata

Metadata minimum:

| Field | Requirement |
| --- | --- |
| Report ID dan title | Unik, stabil, deskriptif |
| Type | Satu primary taxonomy; secondary bila justified |
| Status | Draft/In Review/Approved/Published/Corrected/Superseded/Archived |
| Version / commit | Version yang sedang dilaporkan atau Git reference |
| Owner / author | Accountable owner dan penyusun |
| Reviewer / approver | Sesuai risk, competence, independence, dan delegation |
| Created / reporting period / as-of | ISO 8601; bedakan waktu kejadian, pengumpulan, dan publikasi |
| Audience / purpose | Siapa menggunakan dan untuk keputusan/tindakan apa |
| Classification / access | Public/Internal/Restricted atau taxonomy approved |
| Sources / dependencies | Artefak, session, decision, policy, evidence, dan version |
| Repository / branch / baseline | Bila Git berlaku |
| Supersedes / superseded by | Bila lineage ada |
| Retention / review trigger | Sesuai policy dan risk |

### 7.2 Scope

Nyatakan included/excluded system, organization, period, artefact, population/sample, environment, audience, serta known boundary. Perubahan scope setelah evidence collection dicatat dan direview.

### 7.3 Objective

Nyatakan pertanyaan atau outcome yang harus dijawab report, criteria keberhasilan, dan decision/action yang hendak didukung. Objective report tidak boleh diam-diam memperluas objective session atau audit.

### 7.4 Summary

Berikan status dan outcome utama, critical finding, blocker, residual risk, decision/action needed, serta limitation material. Summary tidak boleh lebih optimistis daripada evidence detail.

### 7.5 Deliverables

Daftar artefak baru/diperbarui, lokasi, owner, status, version/commit, acceptance result, dan relationship. Report bukan pengganti deliverable.

### 7.6 Evidence

Sajikan evidence manifest atau referensi: ID, claim terkait, source/location, owner, version/commit, time/environment, method, classification, validity, dan limitation. Gunakan controlled reference untuk bukti sensitif.

### 7.7 Validation Results

Catat criteria, method/check, expected/actual, status `Pass/Fail/Blocked/N/A`, evidence, actor/reviewer, timestamp, scope, serta limitation. Jangan hanya menulis “semua tes lulus”.

### 7.8 Decisions

Tautkan decision record dan nyatakan decision ID, owner/approver, class/authority, options/trade-off, outcome, rationale, dissent, effective/expiry, implementation, dan verification. Report tidak boleh membuat keputusan material seolah sudah approved.

### 7.9 Risks

Catat risk ID, condition/cause/consequence, likelihood/impact/severity, affected party, mitigation/control, owner, due/review date, residual risk, dan acceptance authority. Unresolved high/critical risk tidak boleh disembunyikan dalam appendix.

### 7.10 Technical Debt

Bedakan debt dari defect/blocker. Catat location, reason, impact, severity, owner, mitigation, due/review trigger, dependency, dan exit criteria. Debt tidak boleh menggantikan deliverable wajib atau safety/correctness requirement.

### 7.11 Lessons Learned

Bedakan observation, root cause/factor, inference, lesson, condition/batas generalisasi, recommendation, target Knowledge/Decision/Pattern/Playbook, source, owner, dan review status. Lesson belum otomatis menjadi policy atau approved knowledge.

### 7.12 Next Actions

Setiap action memiliki outcome, owner, priority, due/review trigger, dependency, evidence of completion, dan destination session/decision. Recommendation tanpa owner atau route diberi label proposal, bukan commitment.

### 7.13 Approval

Catat decision approval report sesuai Section 6.6. Bila belum tersedia, tulis `Pending/Not Required` dengan rationale dan jangan memakai label `Approved`.

### 7.14 References

Gunakan link langsung ke source kanonik, engine, artefact, session, decision, commit/PR/release, serta report terkait. Hindari temporary URL, local absolute path, credential-bearing URL, atau salinan yang tidak terkontrol.

### 7.15 Appendix

Gunakan untuk detail pendukung seperti command output terkurasi, table panjang, methodology, sample, glossary, timeline, atau controlled-evidence index. Appendix tetap mengikuti classification, validation, dan retention; critical fact tidak boleh hanya muncul di appendix.

## 8. Evidence dan Traceability Standard

### 8.1 Evidence Record Minimum

Setiap evidence material mencatat:

- evidence ID dan related claim/finding/decision;
- type: source document, repository state, diff, commit, tool output, test/check, observation, interview/testimony, metric, log, approval, atau external source;
- location/custodian dan access/classification;
- producer/source owner serta collector;
- artefact/version/commit/hash dan repository/branch bila berlaku;
- event time, collection time, environment/context, dan method;
- expected versus actual bila evidence memvalidasi sesuatu;
- integrity/authenticity check proporsional;
- scope, limitation, confidence, retention, dan expiry/staleness trigger.

### 8.2 Claim–Evidence Mapping

Klaim material diberi salah satu status:

- `Observed`: langsung didukung output atau source aktual;
- `Derived`: hasil calculation/transformation dengan method dan input;
- `Corroborated`: didukung beberapa sumber independen/relevan;
- `Assumed`: belum terbukti dan memiliki validation owner/path;
- `Estimated`: memakai model/interval/asumsi yang dinyatakan;
- `Disputed`: ada counter-evidence atau dissent belum selesai;
- `Unverified`: evidence tidak cukup atau tidak dapat diakses.

Kesimpulan tidak boleh memiliki confidence lebih tinggi daripada evidence terlemah yang material terhadapnya tanpa rationale.

### 8.3 Git dan Repository Evidence

Jika repository berlaku, report mencatat:

- repository canonical URL/name;
- branch aktif dan upstream;
- baseline commit dan final/implementation/report-finalization commit;
- changed artefact atau diff scope;
- PR/review/merge/tag/release references bila ada;
- push status dan hash lokal/remote aktual;
- working-tree state pada checkpoint penting;
- command/method verifikasi serta timestamp.

Commit hash hanya valid untuk content yang benar-benar ada pada commit tersebut. Report finalization commit tidak dapat mereferensikan hash dirinya sendiri di dalam content yang sama; final hash dicatat melalui Git history, closure output, signed external record, atau successor correction yang tidak mengklaim circular proof.

### 8.4 Session, Decision, dan Artefak

Trace minimum:

- session ID, type, state, predecessor/successor, dan report;
- objective, deliverable, acceptance criteria, serta closure;
- decision/approval/exception ID, authority, scope, version, dan expiry;
- artefak source/current status, owner, version/commit, dan consumer;
- related report dan relationship: `evidence for`, `summarizes`, `corrects`, `supersedes`, atau `derived from`.

### 8.5 Audit Trail

Audit trail bersifat append-only secara semantik dan mencakup initialization, evidence add/remove/redaction, validation, authoring, review comment/resolution, approval, publication, access/classification change, correction, supersession, archive, serta deletion authorization. Koreksi tidak menghapus siapa melakukan apa, kapan, mengapa, dan terhadap version mana.

### 8.6 Reproducibility Package

Untuk klaim yang dapat direproduksi, sediakan secara proporsional:

- input/source dan pinned version;
- environment/configuration dan relevant dependency;
- method, command, query, criteria, sample, atau calculation;
- expected result dan tolerance;
- actual output/reference;
- known nondeterminism, limitation, access prerequisite, dan safety constraint;
- verifier serta waktu revalidation.

Jika reproducibility tidak aman, lawful, feasible, atau relevan, jelaskan sebab dan alternative assurance. Jangan mengekspos secret atau data pribadi demi reproduksi.

## 9. Reporting Policy

### 9.1 Kewajiban per Session

1. Setiap session wajib menghasilkan Session Report.
2. Session Report final tersedia sebelum state `Completed` atau closure `Cancelled`.
3. Session `Blocked` atau `Waiting for Approval` memiliki interim report/checkpoint bila continuity, handoff, audit, atau keputusan memerlukannya.
4. Report harus mencerminkan final state aktual; Git success atau deliverable presence tidak cukup.
5. Report mencatat objective, scope, deliverable, evidence, validation, decision, risk, debt, lesson, next action, Git trace, dan approval sesuai applicability.
6. Report disimpan pada lokasi kanonik/index yang ditetapkan dan dirujuk dari session record.

### 9.2 Reproducibility

- Klaim yang dapat diulang wajib memiliki context dan method yang cukup.
- Klaim yang tidak dapat diulang harus memiliki source, limitation, alternative verification, serta reason.
- Evidence stale atau dari version/environment berbeda tidak boleh digunakan tanpa disclosure dan revalidation.
- “Berhasil”, “identik”, “lulus”, “selesai”, dan “tidak ada” memerlukan method serta scope pemeriksaan.

### 9.3 Sensitive Data

Report dilarang memuat secret, credential, private key, exploit detail sensitif, personal data, confidential business data, atau transcript mentah yang tidak diperlukan. Gunakan minimization, redaction, pseudonymization, aggregate, controlled annex, secure evidence system, dan reference token yang tidak membuka akses.

Redaction harus:

- menjaga makna audit yang diperlukan;
- menyatakan bahwa content direduksi dan atas dasar apa;
- tidak membocorkan nilai melalui filename, URL, command, diff, metadata, atau appendix;
- direview untuk re-identification dan inference risk;
- tidak digunakan untuk menyembunyikan finding atau conflict.

### 9.4 Validation dan Cross-Reference

Setiap report wajib:

- menjalani self-review dan review sesuai risk;
- memvalidasi claim-evidence, scope, status, version, link, terminology, completeness, security/privacy, serta reproducibility;
- merujuk engine, artefak, session, decision, commit, dan evidence terkait;
- mempertahankan single source of truth dan tidak copy-paste rule kanonik;
- menyebut gap serta unresolved conflict sebagai finding/blocker, bukan mengarang resolution.

### 9.5 Correction dan Retraction

Jika report salah atau menyesatkan:

1. hentikan penggunaan/publikasi yang berisiko;
2. preservasi versi/evidence;
3. nilai impact dan consumer;
4. koreksi klaim/source/status dan tandai version lama;
5. lakukan revalidation/review/approval sesuai materiality;
6. beritahu audience terdampak;
7. hubungkan correction/retraction dua arah;
8. catat root cause dan preventive action.

Retraction tidak sama dengan deletion. Penghapusan hanya melalui authority retention/security/privacy/legal yang sah.

### 9.6 Aggregation dan Executive Summary

Agregasi wajib:

- menyebut source report, period, scope, denominator, filter, missing data, dan methodology;
- mempertahankan severity dan tidak merata-ratakan critical/high finding;
- membedakan count, rate, trend, forecast, dan qualitative judgement;
- mencegah double counting, survivorship bias, stale data, dan mixed definitions;
- menampilkan exception, dissent, uncertainty, serta residual risk material;
- memungkinkan drill-down konseptual ke source report sesuai access.

Executive Summary tidak boleh menandai portfolio “green” jika critical blocker tersembunyi atau source coverage tidak cukup.

## 10. Validation dan Quality Gates Report

### 10.1 Gate Isi

- taxonomy, objective, audience, scope, period, dan classification tepat;
- seluruh section material tersedia atau N/A beralasan;
- fakta, decision, assumption, estimate, inference, recommendation, dan status dibedakan;
- summary konsisten dengan detail dan tidak menghilangkan material adverse information.

### 10.2 Gate Evidence

- setiap claim material memiliki valid evidence/reference;
- source/version/time/environment/method sesuai;
- counter-evidence, failure, limitation, sample, dan missing data terlihat;
- integrity, custody, retention, serta access proporsional.

### 10.3 Gate Traceability

- objective → artefact/change → evidence → validation → report claim → decision/action dapat ditelusuri;
- branch/hash/repository/session/decision/artifact references benar;
- local link dan source target tersedia;
- current, historical, corrected, dan superseded version tidak ambigu.

### 10.4 Gate Reproducibility

- input, context, method, expected/actual, dan limitation cukup;
- nondeterminism dan inaccessible/sensitive prerequisite dinyatakan;
- verifier dapat mengulang atau menggunakan alternative assurance tanpa hidden context.

### 10.5 Gate Governance dan Quality

- owner/reviewer/approver/authority/delegation valid;
- independence dan conflict of interest dikelola;
- quality finding/severity/CAPA konsisten dengan Quality Engine;
- decision/approval/exception/risk acceptance konsisten dengan Governance Engine;
- publication, retention, classification, dan archive sah.

### 10.6 Gate Security, Privacy, dan Usability

- no secret/unnecessary sensitive data;
- redaction dan access sesuai audience;
- struktur dapat dipindai, terminology konsisten, link deskriptif, dan action jelas;
- report dapat dipahami manusia serta AI tanpa transcript tersembunyi;
- detail cukup tetapi tidak berisi dump/log/transcript tanpa kurasi.

Critical gate `Fail/Blocked` mencegah approval/publication atau session closure yang bergantung. `Not Applicable` memerlukan rationale. Self-review AI tidak menjadi independent/human approval.

## 11. Failure, Conflict, dan Recovery

| Kondisi | Tindakan |
| --- | --- |
| Klaim tidak memiliki evidence | Turunkan menjadi assumption/unverified, kumpulkan bukti, atau hapus klaim dengan impact review |
| Source/version salah atau stale | Invalidasi claim terdampak, pin source benar, revalidate, dan koreksi consumer |
| Report dan artefak kanonik konflik | Artefak/decision source yang sah tetap acuan; hentikan propagasi dan koreksi report |
| Summary menyembunyikan finding | Tarik/koreksi summary, identifikasi audience terdampak, dan review aggregation control |
| Hash/push/test/approval palsu | Tandai failure material, preservasi evidence, turunkan status, audit blast radius, dan eskalasi |
| Data sensitif terekspos | Batasi akses, ikuti incident response, revoke/rotate bila secret, lakukan remediation histori terotorisasi |
| Reviewer/approver tidak sah | Invalidasi approval, pertahankan versi, minta authority tepat, dan review penggunaan report |
| Evidence hilang/rusak | Hentikan klaim bergantung, rekonstruksi dari source sah, dokumentasikan gap, dan eskalasi retention failure |
| Correction menimpa histori | Pulihkan version history, buat correction append-only, dan perbaiki index/current pointer |
| Report terlambat atau tidak dibuat | Session tidak boleh `Completed` jika report wajib; catat blocker, owner, mitigation, dan next action |

Recovery mengikuti Execution Engine: detect, stop propagation, preserve evidence, reconstruct actual state, assess impact, stabilize, correct/recover incrementally, revalidate, communicate, dan record learning.

## 12. AI Reporting Policy

### 12.1 AI Boleh

AI boleh:

- membuat report contract, evidence manifest, claim-evidence matrix, Draft, summary, dan appendix;
- mengekstrak fakta dari source yang diizinkan dan menyertakan provenance;
- menjalankan link, heading, coverage, consistency, Git, secret-pattern, dan terminology check;
- membandingkan local/remote hash melalui output aktual;
- mengusulkan taxonomy, status, finding, severity, risk, debt, lesson, dan next action dengan label yang tepat;
- melakukan self-review/cross-review serta menyiapkan correction;
- meredaksi berdasarkan rule approved tanpa menghapus material finding.

### 12.2 AI Dilarang

AI tidak boleh:

- mengarang evidence, command output, source, timestamp, identity, reviewer, approval, hash, push, test, metric, incident, atau user feedback;
- menyebut self-review sebagai independent audit/review;
- memberi approval, risk acceptance, exception, closure authority, atau publication authority atas nama manusia;
- menaikkan confidence/status atau menurunkan severity agar report terlihat sukses;
- menyalin data sensitif ke report karena lebih mudah daripada controlled reference;
- menyembunyikan failure, dissent, blocker, limitation, scope gap, atau residual risk;
- mengubah source kanonik hanya agar cocok dengan narasi report yang salah;
- membuat report baru yang menduplikasi report current tanpa lineage dan purpose berbeda;
- mengklaim reproduksi bila method/context/output aktual tidak tersedia.

### 12.3 Automatic Stop

AI wajib menghentikan area reporting terdampak jika:

- source of truth, owner, scope, period, taxonomy, atau authority material ambigu;
- evidence kritis hilang, conflict, stale, unverifiable, atau berasal dari version salah;
- required reviewer/approver/independence tidak tersedia;
- publication dapat mengekspos secret, personal/confidential data, atau memperluas audience;
- summary/aggregation berisiko menyembunyikan critical finding atau misleading conclusion;
- report memerlukan fabricated evidence, circular proof, atau status yang tidak didukung;
- correction/archive/delete melanggar retention, legal, security, privacy, atau audit trail;
- AI diminta self-approve, memalsukan pass, atau menutup session tanpa report wajib.

State session mengikuti Session Engine: `Blocked` untuk evidence/authority/conflict failure atau `Waiting for Approval` untuk decision gate manusia yang jelas.

## 13. Cross-System Alignment

| Sumber | Implementasi dalam Report Engine | Boundary |
| --- | --- | --- |
| [`CONSTITUTION.md`](CONSTITUTION.md) | Truth over Assumption, Repository/Documentation First, Amanah, transparency, accountability, traceability, human oversight | Report tidak meratifikasi Constitution atau mengambil Founder Authority |
| [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) | Evidence-based reporting, review before claim, bounded tool use, honest failure, validation, final communication | Developer Mode memiliki perilaku AI; Report Engine memiliki standard laporan |
| [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) | evidence, validation, completion, failure/recovery, dan Generate Session Report | Execution memiliki prosedur kerja; Report Engine memiliki taxonomy/lifecycle/structure/traceability |
| [`GIT_ENGINE.md`](GIT_ENGINE.md) | repository, branch, commit, PR, merge, push, release, remote verification, audit trace | Git Engine tetap SSOT Git; report tidak menciptakan hash atau approval |
| [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) | document lifecycle, metadata, SSOT, link, publication, correction/archive, security | Documentation Engine mengatur dokumen umum; Report Engine memberi profil khusus report |
| [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) | quality gate, evidence validity, finding/severity, audit, metric, CAPA, DoD | Quality Engine tetap SSOT quality; report menyajikan hasil tanpa mengubah gate |
| [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) | authority, owner, delegation, review/approval, exception, auditability, risk acceptance | Governance menentukan decision rights; report merekam, bukan memberi authority |
| [`SESSION_ENGINE.md`](SESSION_ENGINE.md) | Session Report wajib, lifecycle/state/continuity/closure, predecessor/successor, report checkpoint | Session Engine menentukan kapan dan state; Report Engine menentukan bentuk serta lifecycle report |
| [`../../01-foundation/FOUNDATION_ARCHITECTURE.md`](../../01-foundation/FOUNDATION_ARCHITECTURE.md) | evidence/outcome/incident/feedback flow, SSOT, ownership, learning routing | Report tidak mengambil ownership Foundation/domain |
| [`../../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md`](../../01-foundation/knowledge/KNOWLEDGE_ARCHITECTURE.md) | provenance, confidence, source, curation, learning, review trigger | Report/lesson tidak otomatis menjadi verified/approved knowledge |
| [`../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) | naming, metadata, versioning, review, lifecycle, cross-reference, archive | Knowledge-specific verification/approval tetap dimiliki Knowledge Governance |
| [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) | Report Engine sebagai core contract, report stage/output, evidence-feedback loop, modular SSOT | Engine adalah kontrak dokumentasi, bukan reporting runtime |
| [`../../reports/sessions/README.md`](../../reports/sessions/README.md) | lokasi dan indeks Session Report repository | Index menginstansiasi policy dan tidak menjadi source normatif tandingan |

### 13.1 Resolusi Cross-Review SPOS-010

- Report Engine menjadi SSOT taxonomy, report lifecycle, structure, evidence/traceability, validation, correction, aggregation, dan reporting policy.
- Session Engine tetap SSOT identity/lifecycle/state/continuity/closure session serta mewajibkan Session Report; Report Engine merinci bentuk dan lifecycle report.
- Documentation Engine tetap SSOT tata kelola dokumen umum; report adalah document profile khusus yang memakai lifecycle/metadata/publication rule Documentation Engine tanpa membuat lifecycle tandingan.
- Quality Engine tetap SSOT quality gate, finding, severity, metric, audit, dan CAPA; report hanya menyajikan hasil serta evidence sesuai version.
- Governance Engine tetap SSOT authority, ownership, delegation, approval, exception, risk acceptance, serta audit right; approval report tidak menjadi approval artefak/source.
- Git Engine tetap SSOT branch/commit/PR/push/release; hash dan remote verification dicatat dari output aktual, termasuk batas circular self-reference pada finalization commit.
- Executive Summary dan aggregation tidak boleh menyembunyikan critical finding, dissent, exception, missing denominator, atau source coverage gap.
- Foundation/Knowledge menerima evidence, learning, dan recommendation melalui review; laporan tidak otomatis menjadi decision, pattern, playbook, policy, atau approved knowledge.
- `reports/sessions/` tetap lokasi current Session Report repository dan indeksnya diturunkan dari engine ini.
- Scope SPOS-010 documentation-only; tidak ada dashboard, database, API, analytics platform, report generator, deployment, atau automation runtime yang dibangun.

## 14. Activation dan Change Control

Activation memerlukan:

- Constitution diratifikasi atau Founder mengizinkan baseline interim secara eksplisit;
- Governance, Session, Documentation, Quality, Git, Execution, dan Developer Mode version/status kompatibel;
- Founder/authorized human menyetujui taxonomy, lifecycle, structure, evidence/traceability, classification, retention, correction, publication, aggregation, dan AI boundary;
- Report owner/steward, reviewer, approver, evidence custodian, registry/index, classification, retention, serta publication authority ditetapkan;
- template/index/consumer/AI dimigrasikan dan version-pinned;
- representative reproducibility, correction, sensitive-data, traceability, dan archival scenario diuji.

Activation record:

- Approver: `<authorized human>`
- Decision: `<approved / rejected / revision required>`
- Effective date: `<YYYY-MM-DD>`
- Version approved: `<version>`
- Constitution dependency: `<version and status>`
- Governance/Session/Documentation/Quality dependency: `<versions and status>`
- Report ownership/delegation: `<reference>`
- Registry/index and naming: `<reference>`
- Classification/retention/publication controls: `<reference>`
- Consumer migration evidence: `<reference>`
- Validation/scenario evidence: `<reference>`
- Commit hash: `<hash>`

AI tidak boleh mengisi approval manusia. Perubahan material pada taxonomy, lifecycle, status, structure minimum, evidence/claim semantics, approval/publication, correction/retention/archive, aggregation guardrail, sensitive-data policy, atau AI authority memerlukan impact analysis, versioning, cross-review, migration, dan approval sesuai Governance Engine.

## 15. Report Engine Review Checklist

- [x] Session, Governance, Quality, Documentation, Git, Audit, Architecture, Knowledge, Decision, Incident, Release Report, dan Executive Summary memiliki tujuan, isi minimum, serta trigger penggunaan.
- [x] Report Initialization, Evidence Collection, Validation, Drafting, Review, Approval, Publication, Versioning, Archival, dan Traceability terdokumentasi dengan output/gate.
- [x] Metadata, Scope, Objective, Summary, Deliverables, Evidence, Validation Results, Decisions, Risks, Technical Debt, Lessons Learned, Next Actions, Approval, References, dan Appendix menjadi struktur baku.
- [x] Evidence record, claim status, repository/branch/commit, session/decision/artefact relation, audit trail, dan reproducibility package terdokumentasi.
- [x] Setiap session wajib menghasilkan report; reproducibility, sensitive-data prohibition, validation, dan cross-reference policy eksplisit.
- [x] Correction/retraction, versioning, publication, classification, retention, archive, aggregation, serta Executive Summary guardrail terdokumentasi.
- [x] AI permission/prohibition, automatic stop, human approval boundary, dan honest reporting terdokumentasi.
- [x] Alignment dengan Constitution, Developer Mode, Execution, Git, Documentation, Quality, Governance, Session, Foundation, Knowledge System, SPOS Architecture, serta session-report index dipetakan.
- [x] Scope tidak membangun aplikasi, dashboard, database, API, analytics/reporting platform, generator, deployment, atau automation runtime.
- [ ] Constitution diratifikasi atau baseline interim diizinkan Founder secara eksplisit.
- [ ] Report Engine memperoleh approval operasional dan activation record.
- [ ] Report owner/reviewer/approver/evidence-custodian delegation, registry/index, classification, retention, publication, correction, dan archive authority tersedia.
- [ ] Template/consumer migration, version pinning, representative scenario test, monitoring, dan conformance automation diterapkan serta diverifikasi.
