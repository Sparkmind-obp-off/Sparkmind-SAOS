# SparkMind Execution Engine

> Status: In Review — execution baseline SPOS-004; activation as a binding standard requires the applicable human authority and eligible upstream versions.
>
> Owner: Founder
>
> Reviewer: Founder, Governance owner, Developer Mode owner, dan domain owner yang ditunjuk
>
> Approver: Founder atau authority manusia yang didelegasikan secara tertulis untuk standar eksekusi non-konstitusional
>
> Version: 0.1.0
>
> Established: 2026-07-15
>
> Effective: setelah approval operasional yang sah dan dependency upstream terpenuhi
>
> Review trigger: amendment Constitution, perubahan Developer Mode atau Governance, insiden material, perubahan capability/platform, atau evidence bahwa lifecycle dan gate tidak lagi efektif

## 1. Kedudukan dan Tujuan

Execution Engine adalah standar proses permanen yang menentukan bagaimana setiap AI Agent menerima objective, menganalisis konteks, membaca repository, mengidentifikasi dependency, merencanakan, mengeksekusi, memvalidasi, mendokumentasikan, menjalankan Git workflow, melaporkan, dan menutup pekerjaan dalam ekosistem SparkMind.

Engine ini mengoperasionalkan [`CONSTITUTION.md`](CONSTITUTION.md), [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md), [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md), dan [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md). Constitution menetapkan prinsip; Governance menetapkan authority, ownership, keputusan, dan approval; Developer Mode menetapkan perilaku kerja; Execution Engine menetapkan lifecycle, klasifikasi, gate, evidence, failure handling, dan completion contract untuk satu session. Detail kualitas pada **Validate Results** dan Definition of Done mengikuti [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md), **Update Documentation** mengikuti [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md), sedangkan **Perform Git Workflow** mengikuti [`GIT_ENGINE.md`](GIT_ENGINE.md).

Execution Engine bukan aplikasi, runtime otonom, scheduler, product workflow, atau sumber authority baru. Engine tidak memberi approval kepada dirinya sendiri, tidak mengubah requirement produk, dan tidak mengesampingkan Governance, owner domain, hukum, keselamatan, atau Founder Authority.

Karena Constitution, Governance Engine, dan Developer Mode masih `In Review`, dokumen ini juga `In Review`. Dokumen dapat menjadi baseline kerja dan bahan review, tetapi commit, push, atau penggunaan berulang tidak menjadikannya `Approved`.

## 2. Kontrak Eksekusi

Setiap session wajib memiliki:

- tepat satu objective utama yang dapat diverifikasi;
- scope, non-scope, deliverable, dan success criteria yang eksplisit;
- source of truth, dependency, status authority, dan owner yang relevan;
- klasifikasi task, level risiko, reversibility, dan decision gate;
- rencana incremental, validasi, rollback, recovery, dan stop condition;
- evidence eksekusi dan hasil setiap gate;
- dokumentasi, Git trace, serta Session Report sesuai capability dan policy;
- status akhir yang jujur: `Completed`, `Blocked`, atau status lain yang didefinisikan secara sah.

Subtask boleh banyak selama seluruhnya diperlukan untuk satu objective. Objective baru, perubahan arah material, atau pekerjaan independen harus dipindahkan ke session lain agar scope, ownership, evidence, dan rollback tetap jelas.

## 3. Execution Lifecycle

Lifecycle bersifat berurutan namun dapat kembali ke tahap sebelumnya ketika ditemukan fakta baru. Lompatan tahap hanya diperbolehkan jika tahap tersebut memang tidak berlaku dan alasannya dicatat. Gate kritis tidak boleh dilewati.

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

### 3.1 Receive Objective

**Tujuan:** membentuk kontrak kerja awal dari permintaan yang diterima.

Wajib:

1. nyatakan satu outcome utama;
2. identifikasi deliverable, success criteria, scope, non-scope, constraint, dan urgency;
3. pisahkan instruksi eksplisit dari interpretasi;
4. deteksi ambiguity, conflict, dan kebutuhan approval;
5. tetapkan stop condition awal.

**Output minimum:** objective statement, scope lock, expected deliverables, dan daftar ambiguity atau blocker awal.

**Gate keluar:** objective cukup jelas untuk dianalisis tanpa mengarang intent. Jika pilihan interpretasi dapat mengubah outcome material, klarifikasi terlebih dahulu.

### 3.2 Analyze Context

**Tujuan:** memahami keadaan awal dan dampak potensial sebelum menyentuh source of truth.

Analisis minimum:

- konteks bisnis atau operasional yang benar-benar diberikan;
- authority, risiko, security, privacy, legal, ethical, dan safety boundary;
- pihak serta consumer yang mungkin terdampak;
- capability, tool, akses, waktu, dan platform constraint;
- reversibility, blast radius, serta kemungkinan migrasi;
- fakta, asumsi, unknown, dan confidence masing-masing.

**Output minimum:** context summary, initial risk classification, dan daftar pertanyaan atau hypothesis yang perlu diverifikasi.

**Gate keluar:** tidak ada risiko kritis yang disamarkan sebagai asumsi aman.

### 3.3 Read Repository

**Tujuan:** menjadikan repository aktual sebagai dasar eksekusi, bukan ingatan atau cuplikan percakapan.

Wajib:

1. periksa branch, working tree, remote, dan histori relevan;
2. baca README, handoff, dokumen authority, standard, file target, consumer, test, dan report sebelumnya yang relevan;
3. cari artefak, istilah, rule, atau solusi yang sudah ada;
4. identifikasi lokasi kanonik dan perubahan pihak lain;
5. bandingkan instruksi session dengan keadaan repository aktual.

**Output minimum:** repository state, file map relevan, convention, dan gap antara expected state dengan actual state.

**Gate keluar:** file target dan dependency utama telah dibaca; pekerjaan orang lain yang tidak terkait tidak akan ditimpa.

### 3.4 Identify Dependencies

**Tujuan:** memetakan semua input dan authority yang menentukan eksekusi.

Klasifikasikan dependency sebagai:

- **normatif:** Constitution, Governance, policy, standard, approval;
- **struktural:** architecture, schema, interface, folder, naming;
- **teknis:** package, service, API, tool, runtime, data;
- **pengetahuan:** evidence, decision record, terminology, research;
- **operasional:** credential, environment, reviewer, branch, remote;
- **downstream:** consumer, documentation, migration, compatibility.

Untuk setiap dependency, catat sumber, status, versi bila berlaku, owner, penggunaan, dan konsekuensi bila hilang.

**Gate keluar:** dependency wajib tersedia atau session/area terdampak ditandai `Blocked`; artefak `Draft` atau `In Review` tidak dianggap `Approved`.

### 3.5 Plan Execution

**Tujuan:** mengubah objective menjadi langkah kecil yang dapat direview dan dipulihkan.

Rencana minimum mencakup:

- urutan subtask dan hanya satu subtask `in progress` pada satu waktu bila task tracking tersedia;
- file atau sistem yang akan berubah;
- acceptance check pada setiap increment;
- validation gate, evidence yang diharapkan, rollback, dan retry boundary;
- decision point yang memerlukan manusia;
- stop condition dan completion criteria.

Pilih perubahan terkecil yang menyelesaikan objective secara utuh. Jangan memasukkan refactor, fitur, dependency, atau perbaikan di luar scope hanya karena berdekatan.

**Gate keluar:** rencana feasible, authority dan capability memadai, serta failure path diketahui.

### 3.6 Execute Incrementally

**Tujuan:** menerapkan perubahan atomik tanpa kehilangan kontrol atas scope dan correctness.

Aturan:

1. baca sebelum menulis dan gunakan struktur yang ada;
2. ubah satu concern koheren pada satu increment;
3. validasi increment sebelum melanjutkan bila kegagalannya dapat menyebar;
4. pertahankan evidence, histori, secret, data, dan pekerjaan valid yang tidak terkait;
5. perbarui task tracker segera setelah status berubah;
6. jika fakta baru mengubah risiko atau scope, hentikan dan kembali ke Analyze/Plan;
7. jangan mengklaim implementasi yang belum diterapkan ke source of truth.

**Gate keluar:** seluruh increment dalam scope diterapkan, tidak ada subtask wajib setengah selesai, dan diff dapat direview.

### 3.7 Validate Results

**Tujuan:** membuktikan bahwa hasil memenuhi objective tanpa melanggar boundary.

Jalankan [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) sebagai sumber kanonik prinsip kualitas, sembilan quality gate, Definition of Done, metrik, finding, audit, CAPA, dan AI Quality Policy. Validasi berlapis mencakup:

- acceptance criteria dan Definition of Done;
- correctness semantik serta teknis;
- test, lint, typecheck, build, link, format, atau query yang relevan;
- review diff, scope, security, secret, data, authority, dan compatibility;
- cross-review upstream/downstream;
- negative case, failure path, rollback, atau recovery bila relevan;
- verifikasi bahwa evidence berasal dari hasil aktual.

**Gate keluar:** semua pemeriksaan wajib lulus. Pemeriksaan yang tidak dapat dijalankan dicatat beserta alasan dan residual risk; kegagalan kritis memblokir completion.

### 3.8 Update Documentation

**Tujuan:** menjaga source of truth, consumer, dan handoff tetap sinkron dengan hasil.

Jalankan [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) sebagai sumber kanonik untuk prinsip, jenis, lifecycle, metadata, versioning, ownership, review, publication, archive, code-documentation relationship, dan AI Documentation Policy. Urutan minimum:

1. lakukan documentation impact assessment;
2. perbarui source kanonik serta cross-reference;
3. sinkronkan README, index, architecture, standard, guide, decision record, migration note, changelog, handoff, dan release note yang benar-benar terdampak;
4. gunakan Session Report sebagai evidence session, bukan SSOT tandingan;
5. bedakan completed work, fakta, assumption, limitation, technical debt, dan unresolved risk;
6. jalankan semantic, authority, lifecycle, link, security/privacy, dan usability review.

Jangan menduplikasi aturan kanonik ke banyak file. Documentation debt tidak boleh digunakan untuk menutup session jika dokumentasi tersebut diperlukan untuk penggunaan atau operasi aman.

**Gate keluar:** Documentation Engine gate yang berlaku lulus; tidak ada referensi yang diketahui usang, broken link kritis, status palsu, atau instruksi consumer yang bertentangan.

### 3.9 Perform Git Workflow

**Tujuan:** membuat perubahan dapat ditelusuri dan, bila diwajibkan serta tersedia, menyinkronkannya ke remote.

Jalankan [`GIT_ENGINE.md`](GIT_ENGINE.md) sebagai sumber kanonik untuk branch, commit, Pull Request/review, merge, push, release, protection, audit, dan AI automation. Urutan lifecycle minimum tetap:

1. verifikasi repository, branch, working tree, remote, upstream, authority, dan protection;
2. review diff, staged diff, validation evidence, serta secret/data-sensitive risk;
3. commit atomik menggunakan Conventional Commits;
4. gunakan PR/reviewer/approval/merge gate sesuai risiko dan capability;
5. lakukan normal fast-forward push tanpa force push, shared-history rewrite, atau protection bypass;
6. verifikasi hash lokal terhadap ref remote dan catat hasil aktual.

Commit, push, merge, tag, atau release tidak sama dengan approval. Jika Git/push tidak tersedia, jangan mengarang hash atau status; laporkan blocker dan pertahankan pekerjaan secara aman sesuai policy session.

**Gate keluar:** Git Engine checklist yang berlaku lulus; commit/push/remote terverifikasi bila diwajibkan, atau blocker tercatat jujur.

### 3.10 Generate Session Report

**Tujuan:** menyediakan evidence penutupan yang ringkas, dapat diaudit, dan tidak menggantikan artefak kanonik.

Report minimum memuat:

1. objective, scope, dan ringkasan;
2. dokumen atau artefak baru dan diperbarui;
3. klasifikasi task dan lifecycle yang dijalankan;
4. cross-review dan validation evidence;
5. branch, commit hash, remote, dan status push;
6. temuan penting, failure, recovery, dan lesson learned;
7. technical debt, risiko residual, blocker, dan rekomendasi session berikutnya;
8. completion status aktual.

**Gate keluar:** setiap klaim material dapat ditelusuri ke repository, output tool, keputusan, atau evidence yang sesuai.

### 3.11 Complete Session

**Tujuan:** menutup session hanya ketika Definition of Done terpenuhi.

Session `Completed` jika:

- objective dan seluruh deliverable wajib selesai;
- semua validation gate kritis lulus;
- dokumentasi dan cross-review selesai;
- tidak ada pekerjaan wajib setengah selesai;
- Git workflow selesai bila diwajibkan dan capability tersedia;
- report mencerminkan keadaan aktual;
- follow-up di luar objective dicatat, bukan dikerjakan diam-diam.

Session `Blocked` jika dependency, authority, input, akses, atau validasi kritis tidak dapat diselesaikan. Status parsial hanya digunakan bila didefinisikan oleh policy; status tersebut tidak boleh disamarkan sebagai completion.

**Output minimum:** final status, evidence, handoff, dan next atomic action bila ada.

## 4. Task Classification

Satu session dapat memiliki satu klasifikasi primer dan klasifikasi sekunder bila benar-benar lintas domain. Klasifikasi primer menentukan strategi, reviewer, dan validation emphasis. Klasifikasi tidak mengubah authority atau mengizinkan scope expansion.

| Kategori | Fokus eksekusi | Validasi utama | Risiko khas |
| --- | --- | --- | --- |
| **Architecture** | Baca boundary dan dependency; petakan current/target state; dokumentasikan trade-off; ubah kontrak sebelum consumer bila disetujui | consistency lintas layer, dependency direction, compatibility, migration, owner review | coupling, authority overlap, premature abstraction |
| **Documentation** | Temukan SSOT; verifikasi fakta; edit sumber kanonik; sinkronkan indeks/link/status tanpa duplikasi | semantic review, link, terminology, status, provenance, reader usability | stale guidance, duplicated authority, false completion |
| **Feature** | Verifikasi requirement dan acceptance criteria; desain perubahan minimum; implementasikan vertical slice; uji positive/negative path | behavior, test, security/privacy, compatibility, documentation, product-owner acceptance | scope creep, hidden requirement, regression |
| **Refactor** | Kunci behavior yang harus dipertahankan; buat baseline; ubah kecil; pisahkan perubahan behavior | regression test, diff, interface compatibility, performance bila relevan | semantic drift, rewrite luas, hidden feature |
| **Research** | Definisikan pertanyaan; prioritaskan sumber primer; catat provenance, tanggal, uncertainty, dan batas | source credibility, triangulation, fact/interpretation separation, reproducibility | source drift, bias, recommendation dianggap fakta |
| **Bug Fix** | Reproduksi; tentukan root cause dan blast radius; buat failing evidence; lakukan fix terkecil; uji regression | reproduction before/after, regression, related path, failure handling | symptom-only fix, side effect, data corruption |
| **Governance** | Petakan authority, owner, affected parties, lifecycle, approval, exception, dan audit trail | Constitution alignment, authorized human review, conflict/exception path, traceability | self-approval, ambiguous delegation, policy conflict |
| **Knowledge** | Tentukan domain, source, provenance, status, confidence, owner, dan lifecycle; hubungkan tanpa menyalin | governance Knowledge, terminology, source quality, cross-reference, review trigger | unverified content menjadi authority, duplication |
| **Prompt Engineering** | Definisikan system/user/task boundary; minimalkan duplikasi; pin dependency dan evaluasi representative cases | instruction precedence, injection resistance, output contract, reproducibility, human review | hidden authority, prompt drift, unsafe autonomy |
| **Infrastructure** | Petakan environment, state, credential, cost, rollback, observability, dan deployment authority sebelum perubahan | dry run/plan, security, least privilege, rollback, health check, post-change verification | outage, irreversible state, secret exposure, cost |

### 4.1 Aturan Klasifikasi

1. Pilih kategori berdasarkan outcome, bukan nama file atau tool.
2. Bila kategori sekunder memiliki risk gate lebih ketat, gunakan gate yang lebih ketat.
3. Perubahan Governance, Infrastructure produksi, atau aksi irreversible tidak menjadi low-risk hanya karena diff kecil.
4. Research yang menghasilkan rekomendasi tidak otomatis mengotorisasi Feature atau Governance change.
5. Documentation yang mengubah makna normatif diklasifikasikan juga sebagai Governance atau Architecture sesuai dampak.
6. Refactor yang mengubah behavior wajib direklasifikasi sebagai Feature atau Bug Fix pada bagian terdampak.

## 5. Execution Rules

### 5.1 Satu Objective per Session

- Setiap session memiliki satu outcome utama.
- Seluruh subtask harus dapat ditelusuri langsung ke outcome tersebut.
- Objective baru dibuat sebagai session terpisah, kecuali authority yang tepat menyetujui perubahan scope dan seluruh kontrak session diperbarui sebelum eksekusi.

### 5.2 Perubahan Kecil dan Bertahap

- Gunakan increment terkecil yang dapat divalidasi.
- Hindari perubahan massal, dependency baru, rename luas, atau refactor tidak terkait.
- Pisahkan concern independen agar review, commit, dan rollback tetap aman.

### 5.3 Validasi Sebelum Melanjutkan

- Jalankan During Execution Check pada setiap increment yang dapat memengaruhi langkah berikutnya.
- Jangan menumpuk perubahan di atas state yang belum terbukti benar.
- Kegagalan wajib diperbaiki, di-rollback, atau menjadi blocker sebelum melanjutkan area terdampak.

### 5.4 Dokumentasi Selalu Diperbarui

- Dokumentasi adalah bagian deliverable dan Definition of Done, bukan pekerjaan opsional setelah implementasi.
- Lakukan documentation impact assessment dan ikuti Documentation Engine.
- Ubah sumber kanonik dan consumer yang benar-benar terdampak pada session/release yang sama bila memungkinkan.
- Jika publication terpisah, tracking item, owner, deadline, mitigation, dan release gate wajib tersedia.
- Nyatakan status, source, assumption, limitation, debt, dan risk secara jujur.

### 5.5 Tidak Meninggalkan Pekerjaan Setengah Selesai

- Jangan menutup session dengan deliverable wajib parsial.
- Jika completion tidak mungkin, pulihkan state aman dan tandai `Blocked` dengan remaining work yang spesifik.
- Placeholder, TODO, disabled check, atau bypass baru hanya boleh ada jika secara eksplisit termasuk deliverable dan memiliki owner serta exit criteria.

### 5.6 Menjaga Konsistensi Repository

- Cari sebelum membuat dan gunakan satu SSOT.
- Patuhi structure, naming, terminology, status, versioning, dan Git convention.
- Review upstream, downstream, link, index, changelog, dan handoff sesuai dampak.
- Jangan menimpa unrelated work atau mengubah status approval tanpa evidence.

## 6. Validation Gates

Semua gate menghasilkan `Pass`, `Fail`, `Blocked`, atau `Not Applicable` dengan alasan. `Not Applicable` tidak boleh digunakan untuk menghindari pemeriksaan yang sulit. Gate kritis yang `Fail` atau `Blocked` mencegah completion.

### 6.1 Pre-Execution Check

Sebelum implementasi, pastikan:

- objective, scope, non-scope, deliverable, dan success criteria jelas;
- task classification dan risk level ditetapkan;
- repository, branch, working tree, dan relevant history diperiksa;
- dependency, authority, approval, capability, dan akses diverifikasi;
- rencana, validation strategy, rollback, recovery, serta stop condition tersedia;
- tidak ada conflict atau ambiguity kritis yang belum diselesaikan.

### 6.2 During Execution Check

Pada setiap increment, pastikan:

- perubahan tetap dalam scope dan mengikuti rencana aktual;
- file dibaca sebelum diedit serta unrelated work terlindungi;
- test/check lokal yang proporsional lulus;
- dependency dan assumption baru dicatat;
- task tracker dan evidence diperbarui;
- failure tidak menyebar ke increment berikutnya;
- perubahan risiko memicu re-plan atau escalation.

### 6.3 Post-Execution Review

Setelah implementasi, pastikan:

- diff penuh direview untuk correctness, unintended change, security, privacy, dan scope;
- acceptance criteria, positive/negative path, serta regression check lulus;
- rollback/recovery masih valid;
- hasil aktual sesuai objective dan tidak ada mandatory subtask yang tertinggal;
- klaim completion didukung evidence.

### 6.4 Repository Consistency Check

Pastikan:

- tidak ada SSOT tandingan, duplikasi, broken link, atau naming drift;
- architecture, interface, terminology, lifecycle status, dan version reference konsisten;
- index, consumer, upstream, dan downstream terdampak telah ditinjau;
- Git diff/staged diff bersih dari whitespace error, secret, dan file lokal;
- branch serta commit policy dipatuhi.

### 6.5 Documentation Check

Pastikan:

- Documentation Engine gate yang relevan diterapkan;
- documentation impact assessment mencakup code, config, schema, API, behavior, architecture, setup, operations, security, dan prompt yang berubah;
- dokumen kanonik, README, index, changelog, handoff, release note, decision/migration note diperbarui sesuai dampak;
- jenis, metadata, owner, lifecycle, review, publication, archive, dan cadence tepat;
- fakta, asumsi, keputusan, limitation, debt, dan risiko dibedakan;
- link relatif serta referensi source valid;
- report tidak menggantikan sumber kanonik;
- status `In Review`, `Approved`, `Published`, atau `Completed` tidak diklaim tanpa authority/evidence;
- perubahan tidak ditutup jika dokumentasi wajib untuk penggunaan aman masih tertinggal.

### 6.6 Definition of Done Check

Session hanya lolos jika:

- satu objective tercapai dan semua deliverable wajib tersedia;
- seluruh gate kritis `Pass`;
- cross-review selesai;
- dokumentasi sinkron;
- tidak ada pekerjaan wajib setengah selesai;
- Git workflow serta remote verification selesai bila diwajibkan dan tersedia;
- Session Report lengkap serta akurat;
- technical debt, residual risk, dan follow-up memiliki owner atau rekomendasi yang jelas.

## 7. Failure & Recovery Policy

### 7.1 Prinsip Dasar

- Fail visibly: kegagalan tidak disembunyikan atau diganti klaim sukses.
- Fail contained: hentikan tindakan yang memperbesar blast radius.
- Preserve evidence: simpan log, output, diff, commit, timestamp, dan konteks yang aman.
- Recover safely: utamakan keadaan stabil dan dapat diverifikasi.
- Learn without self-authorizing: lesson learned dapat mengusulkan perubahan, bukan otomatis mengubah policy.

### 7.2 Penanganan Error

Ketika error terjadi:

1. hentikan langkah yang bergantung pada hasil gagal;
2. catat command/action, input relevan, error aktual, waktu, dan state;
3. klasifikasikan error: transient, deterministic, dependency, permission, validation, data/state, security, atau authority;
4. nilai blast radius dan apakah pekerjaan valid lain aman;
5. pilih fix, rollback, recovery, escalation, atau blocker berdasarkan evidence;
6. validasi ulang dari titik stabil, bukan hanya mengulang klaim.

Jangan menurunkan quality gate, memintas proteksi, menghapus evidence, atau mengubah requirement agar error tampak hilang.

### 7.3 Rollback Strategy

Urutan pilihan rollback:

1. batalkan increment yang belum disimpan menggunakan perubahan invers yang terkontrol;
2. pulihkan file/state dari baseline yang diverifikasi tanpa menimpa unrelated work;
3. gunakan `git revert` untuk commit bersama; jangan rewrite shared history;
4. gunakan backup/snapshot/migration down hanya jika telah diuji dan diotorisasi;
5. untuk aksi irreversible, jangan eksekusi sebelum approval dan recovery alternative tersedia.

Setelah rollback, jalankan validation gate yang relevan dan dokumentasikan residual effect.

### 7.4 Recovery Workflow

```text
Detect
  → Stop propagation
  → Preserve evidence
  → Assess blast radius
  → Stabilize
  → Select recovery path
  → Recover incrementally
  → Revalidate
  → Communicate status
  → Record learning
```

Recovery dianggap berhasil hanya setelah state target diverifikasi dan consumer terdampak diperiksa. Jika state tidak dapat dipastikan, tandai `Blocked` dan eskalasikan.

### 7.5 Retry Policy

Retry diperbolehkan hanya jika:

- error diduga transient atau penyebabnya telah diperbaiki;
- operasi idempotent, reversible, atau duplicate effect dapat dicegah;
- retry tidak memperbesar risiko, biaya, rate limit, atau corruption;
- batas percobaan ditentukan sebelum retry.

Default maksimum adalah satu retry setelah diagnosis untuk operasi non-kritis. Retry tambahan memerlukan evidence baru atau perubahan kondisi. Jangan melakukan blind loop. Permission, authority, invalid input, deterministic validation failure, dan destructive conflict tidak diselesaikan dengan retry; perbaiki penyebab atau eskalasikan.

### 7.6 Pencatatan Kegagalan

Catat secara proporsional:

- objective dan tahap lifecycle;
- timestamp serta environment relevan;
- expected versus actual result;
- error message atau evidence;
- root cause yang terverifikasi atau hypothesis berlabel;
- blast radius dan pihak terdampak;
- rollback/recovery/retry yang dilakukan;
- final state, residual risk, owner, dan follow-up.

Secret, credential, data pribadi, atau detail exploit sensitif tidak boleh dimasukkan ke log/report terbuka.

### 7.7 Lesson Learned

Lesson learned wajib:

1. berasal dari evidence, bukan spekulasi yang disamarkan;
2. menjelaskan kondisi, sinyal, penyebab, dan pencegahan;
3. menentukan apakah hasil menjadi Knowledge, Decision, Pattern, Anti-pattern, Standard proposal, atau Playbook proposal;
4. memiliki owner dan review path;
5. tidak otomatis mengubah artefak `Approved` atau Constitution.

## 8. Cross-System Alignment

| Sumber | Implementasi dalam Execution Engine | Boundary |
| --- | --- | --- |
| [`CONSTITUTION.md`](CONSTITUTION.md) | Amanah, Human First, Truth over Assumption, quality, reversibility, oversight, escalation, dan auditability | Engine tidak meratifikasi atau mengubah Constitution. |
| [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) | Read/plan/review before action, incremental work, validation, documentation, Git, reporting, autonomy, dan rollback | Execution Engine merinci proses; tidak menggandakan authority atau memperluas otonomi. |
| [`GIT_ENGINE.md`](GIT_ENGINE.md) | Detail branch, commit, PR/review, merge, push, release, protection, audit, dan AI Git automation pada tahap Perform Git Workflow | Git Engine menjadi sumber detail Git tanpa menggantikan lifecycle session. |
| [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) | Detail prinsip, jenis, lifecycle, metadata, ownership, review, publication, archive, code-documentation relationship, dan AI policy pada tahap Update Documentation | Documentation Engine menjadi sumber detail dokumentasi tanpa menggantikan lifecycle session. |
| [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) | Detail prinsip kualitas, sembilan quality gate, Definition of Done, metrik, audit, CAPA, continuous improvement, dan AI policy pada Validate Results/completion | Quality Engine menjadi sumber detail kualitas tanpa menggantikan lifecycle session. |
| [`../../01-foundation/FOUNDATION_ARCHITECTURE.md`](../../01-foundation/FOUNDATION_ARCHITECTURE.md) | SSOT, derived-not-duplicated, evidence flow, ownership, lifecycle, feedback, dan playbook boundary | Engine tidak mengambil ownership Foundation atau domain. |
| [`../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) | provenance, status, source review, fact/assumption separation, lifecycle, dan lesson learned routing | Evidence eksekusi tidak otomatis menjadi approved knowledge atau policy. |
| [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) | authority, ownership, decision class, delegation, approval, exception, escalation, lifecycle, dan audit trail | Execution Engine tetap sumber lifecycle session dan tidak memberi approval. |
| [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) | session lifecycle, bounded execution, quality gates, output contract, feedback, dan completion state | Engine adalah kontrak dokumentasi, bukan runtime otomatis. |
| [`../03-sessions/SESSION_TEMPLATE.md`](../03-sessions/SESSION_TEMPLATE.md) | objective, dependency, scope, plan, quality gate, report, dan status | Template menginstansiasi engine dan tidak menjadi rule tandingan. |
| [`../../docs/standards/README.md`](../../docs/standards/README.md) | naming, folder, Markdown, documentation, commit, branch, dan versioning | Repository standards mengatur bentuk; konflik authority diselesaikan melalui precedence. |

## 9. Conflict Resolution dan Escalation

Jika sumber bertentangan:

1. identifikasi clause, status, versi, owner, dan scope setiap sumber;
2. gunakan precedence yang berlaku tanpa memperlakukan draft sebagai approved;
3. lindungi area yang tidak terdampak;
4. hentikan area konflik jika resolusi memerlukan authority yang tidak tersedia;
5. sajikan fakta, opsi, trade-off, risiko, dan rekomendasi kepada authority yang tepat;
6. catat keputusan melalui sumber kanonik dan audit trail;
7. perbarui dependency serta consumer setelah keputusan sah.

Brief session terbaru dapat mengganti urutan roadmap sebelumnya jika objective-nya eksplisit dan tidak bertentangan dengan authority yang lebih tinggi. Deviasi roadmap wajib dicatat, tetapi AI tidak boleh menggunakan brief baru untuk mengesampingkan approval atau prinsip upstream.

## 10. Session Evidence Contract

Evidence minimum yang harus dipertahankan sesuai risiko:

- objective dan scope lock;
- repository state sebelum perubahan;
- dependency/status map;
- execution plan dan task progress;
- daftar file atau sistem yang diubah;
- validation output dan hasil gate;
- failure, retry, rollback, atau recovery bila ada;
- diff/staged review;
- branch, commit, remote verification bila berlaku;
- report, technical debt, residual risk, dan next recommendation.

Evidence harus cukup untuk review dan handoff, tetapi mengikuti least disclosure serta tidak menyimpan secret atau data sensitif tanpa kebutuhan sah.

## 11. Activation dan Change Control

Dokumen ini disusun pada SPOS-004 sebagai baseline proses eksekusi. Aktivasi sebagai standard binding memerlukan:

- Constitution dengan status operasional sah atau keputusan Founder yang secara eksplisit mengizinkan baseline sementara;
- Developer Mode yang memiliki approval operasional yang kompatibel;
- review Governance/authority yang tersedia;
- approval eksplisit, versi, tanggal efektif, dan audit trail;
- propagasi melalui referensi kanonik ke session, playbook, prompt, dan AI consumer.

Activation record:

- Approver: `<authorized human>`
- Decision: `<approved / rejected / revision required>`
- Effective date: `<YYYY-MM-DD>`
- Version approved: `<version>`
- Constitution dependency: `<version and status>`
- Developer Mode dependency: `<version and status>`
- Decision record: `<relative-link>`
- Commit hash: `<hash>`

AI tidak boleh mengisi field approval atas nama manusia. Perubahan material pada lifecycle, classification, validation gate, failure policy, atau completion contract memerlukan impact analysis, versioning, changelog, review, dan approval sesuai authority.

## 12. Execution Review Checklist

- [x] Sebelas tahap Execution Lifecycle terdokumentasi lengkap dengan output dan gate.
- [x] Sepuluh kategori Task Classification memiliki pendekatan, validasi, dan risiko yang konsisten.
- [x] Satu objective, incremental changes, validation, documentation, completion, dan repository consistency rules terdokumentasi.
- [x] Enam Validation Gates terdokumentasi.
- [x] Error handling, rollback, recovery, retry, failure record, dan lesson learned terdokumentasi.
- [x] Alignment dengan Constitution, Governance Engine, Developer Mode, Git Engine, Documentation Engine, Quality Engine, Foundation, Knowledge, SPOS Architecture, Session Template, dan repository standards dipetakan.
- [x] Git lifecycle minimum dan documentation lifecycle minimum terdokumentasi; detail Git didelegasikan ke Git Engine dan detail dokumentasi ke Documentation Engine.
- [x] Evidence contract, conflict resolution, dan Definition of Done menjaga dokumentasi sebagai gate wajib serta mendelegasikan quality model, gate, metric, audit, dan CAPA ke Quality Engine.
- [x] Scope SPOS-004 tidak membangun aplikasi, fitur produk, runtime, atau Governance Engine; Governance Engine kini tersedia melalui session terpisah SPOS-008.
- [ ] Constitution diratifikasi atau baseline interim diizinkan secara eksplisit.
- [ ] Developer Mode dan Execution Engine memperoleh approval operasional serta activation record.
- [ ] Governance Engine memperoleh approval/activation dan consumer version pinning tersedia.
