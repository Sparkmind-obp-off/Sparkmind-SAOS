# SparkMind Git Engine

> Status: In Review — Git governance baseline SPOS-005; activation as a binding standard requires the applicable human authority and eligible upstream versions.
>
> Owner: Founder
>
> Reviewer: Founder, Governance owner, repository owner/maintainer, Security owner bila relevan, dan domain owner yang ditunjuk
>
> Approver: Founder atau authority manusia yang didelegasikan secara tertulis untuk kebijakan Git non-konstitusional
>
> Version: 0.1.0
>
> Established: 2026-07-15
>
> Effective: setelah approval operasional yang sah dan dependency upstream terpenuhi
>
> Review trigger: amendment Constitution, perubahan Governance/Developer Mode/Execution Engine, insiden repository, perubahan hosting atau protection capability, perubahan release model, atau evidence bahwa workflow tidak lagi aman dan efektif

## 1. Kedudukan dan Tujuan

Git Engine adalah standar permanen pengelolaan version control untuk seluruh AI Agent, repository, dan proyek dalam ekosistem SparkMind. Engine menetapkan branch strategy, commit policy, Pull Request dan review, merge, push, release, repository protection, audit, recovery, serta batas otomatisasi AI.

Engine ini mengoperasionalkan [`CONSTITUTION.md`](CONSTITUTION.md), [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md), [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md), dan [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md). Constitution menetapkan prinsip dan authority; Developer Mode menetapkan perilaku; Execution Engine menetapkan lifecycle session; Git Engine menjadi sumber kanonik untuk proses Git pada tahap **Perform Git Workflow**. Dokumentasi yang menyertai branch, commit, review, release, dan audit mengikuti [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md); quality plan, gate, DoD, metric, finding, dan audit kualitas mengikuti [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md).

Git Engine bukan layanan hosting Git, CI/CD, aplikasi, fitur produk, atau izin untuk mengubah histori tanpa batas. Capability teknis tidak sama dengan authority. Commit, push, merge, tag, dan release tidak dengan sendirinya merupakan approval normatif, ratifikasi, atau penerimaan risiko.

Karena Constitution, Developer Mode, dan Execution Engine masih `In Review` serta Governance substantif belum tersedia, dokumen ini juga `In Review`. Dokumen dapat digunakan sebagai baseline kerja dan bahan review, tetapi penggunaan berulang tidak menjadikannya `Approved`.

## 2. Prinsip Git

Seluruh workflow Git wajib mengikuti prinsip berikut:

1. **Repository First:** repository aktif dan remote terverifikasi adalah sumber keadaan teknis, bukan ingatan atau percakapan.
2. **One change, one trace:** setiap perubahan dapat ditelusuri dari objective ke branch, diff, review, commit, dan release bila berlaku.
3. **Atomic and reviewable:** perubahan dipisahkan menurut satu tujuan logis dan selalu dapat direview.
4. **Protect shared history:** shared history tidak ditulis ulang untuk kenyamanan.
5. **Fail closed on ambiguity:** target, authority, ownership, atau divergence yang ambigu memblokir operasi berisiko.
6. **Approval is not a Git event:** commit, push, merge, atau tag tidak menggantikan approval manusia yang diwajibkan.
7. **Preserve evidence:** histori, review, keputusan, dan hasil validasi dipertahankan sesuai security dan least disclosure.
8. **Reversible by default:** pilih perubahan, merge, dan release yang dapat dipulihkan melalui revert atau versi koreksi.
9. **Least privilege:** credential, permission, dan bypass digunakan hanya sesuai scope serta durasi yang sah.
10. **Truth over completion:** jangan mengarang branch, hash, reviewer, approval, push, merge, tag, release, atau status remote.

## 3. Authority dan Peran

| Peran | Tanggung jawab Git | Batas |
| --- | --- | --- |
| **Founder** | Menetapkan arah fundamental, ratifikasi, dan keputusan risiko/authority material | Tidak menghapus evidence atau mengesampingkan hukum dan keselamatan |
| **Governance owner** | Menetapkan delegation, approval, exception, escalation, dan lifecycle | Governance substantif masih menjadi dependency terbuka |
| **Repository owner/maintainer** | Mengelola akses, default branch, ruleset, reviewer, merge method, dan release operation | Tidak dapat menyetujui perubahan di luar delegasi domain |
| **Domain owner** | Memastikan correctness dan dampak domain | Tidak menggantikan Security/Founder review bila gate tersebut berlaku |
| **Reviewer** | Memeriksa diff, risiko, evidence, dan acceptance criteria secara independen | Tidak boleh memberi approval tanpa kompetensi atau konflik kepentingan yang dikelola |
| **Author/executor** | Menyusun perubahan, self-review, validasi, commit, dan respons review | Tidak self-approve perubahan yang membutuhkan review independen |
| **AI Agent** | Menjalankan operasi terbatas sesuai Section 10 dan menyajikan evidence | Tidak menjadi Founder, approver, risk owner, atau exception authority |

Jika satu orang memegang beberapa peran, separation of duties tetap diterapkan pada perubahan strategis, security-sensitive, irreversible, atau berisiko tinggi. Ketika reviewer independen tidak tersedia, perubahan tersebut tetap `Blocked` atau menunggu exception tertulis dari authority yang sah.

## 4. Branch Strategy

### 4.1 Branch Utama

#### `main`

`main` adalah default branch dan SSOT integrasi yang harus selalu konsisten, dapat direproduksi, serta siap digunakan sesuai maturity repository. Semua release tag berasal dari commit yang telah terintegrasi ke `main`.

Aturan:

- tidak boleh force push atau rewrite history;
- perubahan normal masuk melalui branch dan Pull Request bila platform serta workflow kolaborasi tersedia;
- perubahan langsung hanya boleh dilakukan jika owner mengizinkan, risiko rendah, scope tunggal, seluruh gate lulus, dan tidak ada review/approval wajib yang dilewati;
- perubahan normatif, strategis, security-sensitive, release, atau berisiko tinggi wajib melalui branch terpisah dan review yang sesuai.

#### `develop` — opsional

`develop` hanya dibuat jika repository benar-benar membutuhkan integration branch untuk beberapa aliran perubahan paralel atau release train. Jangan membuatnya secara default.

Jika digunakan:

- keberadaan, owner, cadence, merge target, dan protection-nya harus terdokumentasi;
- branch harus mengikuti protection setara `main` sesuai risikonya;
- release candidate tetap diverifikasi sebelum dipromosikan ke `main`;
- `develop` tidak boleh menjadi SSOT tandingan atau branch permanen tanpa kebutuhan aktif.

### 4.2 Working Branch

Format kanonik:

```text
<type>/<lowercase-kebab-case-description>
```

| Prefix | Digunakan untuk |
| --- | --- |
| `feature/*` | Fitur atau capability baru yang mengubah perilaku pengguna/sistem |
| `fix/*` | Perbaikan defect atau inkonsistensi terverifikasi |
| `docs/*` | Dokumentasi tanpa perubahan perilaku produk |
| `refactor/*` | Restrukturisasi yang mempertahankan perilaku atau makna |
| `research/*` | Eksperimen atau evidence gathering yang memang perlu branch; hasil tidak otomatis menjadi policy/feature |
| `chore/*` | Pemeliharaan repository, tooling, dependency, atau housekeeping |
| `release/*` | Stabilisasi versi, release note, version bump, dan validasi rilis |
| `hotfix/*` | Perbaikan produksi mendesak yang diotorisasi dan mengikuti jalur review dipercepat |

Alias `feat/*` boleh dipertahankan pada repository yang sudah menggunakannya, tetapi repository baru menggunakan `feature/*`. Prefix `ci/*` atau `test/*` hanya ditambahkan melalui policy repository jika volume pekerjaan membenarkannya; jika tidak, gunakan `chore/*` atau prefix outcome primer.

Contoh:

```text
docs/spos-git-engine
fix/broken-session-links
refactor/knowledge-index
research/release-signing-options
release/0.2.0
hotfix/credential-redaction
```

### 4.3 Lifecycle Branch

1. Verifikasi remote, default branch, working tree, dan authority.
2. Sinkronkan dari `main` terbaru tanpa menimpa pekerjaan lokal.
3. Buat satu working branch untuk satu objective.
4. Lakukan perubahan dan commit atomik.
5. Push normal ke remote yang diizinkan.
6. Buat Pull Request dan selesaikan review/gate.
7. Integrasikan dengan merge method yang disetujui.
8. Verifikasi target branch dan automation pascamerge.
9. Hapus branch setelah perubahan aman terintegrasi dan tidak menyimpan commit unik.

### 4.4 Larangan Branch

- branch tanpa owner, objective, atau lifecycle;
- nama generik seperti `test`, `new`, `temp`, `final`, atau nama individu saja;
- mencampur beberapa objective independen;
- menggunakan `hotfix/*` untuk melewati review normal tanpa insiden nyata;
- menghapus branch yang masih memiliki commit unik;
- rebase atau force push pada branch bersama tanpa koordinasi dan authority;
- mempertahankan `develop`, `release/*`, atau branch eksperimen lebih lama dari kebutuhan aktif.

## 5. Commit Policy

### 5.1 Format Conventional Commits

```text
<type>(<scope>): <description>

[optional body]

[optional footer]
```

Type minimum:

| Type | Penggunaan | Contoh |
| --- | --- | --- |
| `feat` | Capability atau fitur baru | `feat(agent): add bounded task retry` |
| `fix` | Perbaikan defect | `fix(spos): correct engine dependency link` |
| `docs` | Perubahan dokumentasi | `docs(spos): establish Git Engine` |
| `refactor` | Restrukturisasi tanpa perubahan perilaku/makna | `refactor(knowledge): simplify index hierarchy` |
| `chore` | Pemeliharaan repository/tooling | `chore(repository): normalize editor settings` |
| `test` | Test atau validation fixture | `test(engine): cover blocked execution state` |
| `ci` | Workflow continuous integration | `ci(repository): add markdown link check` |

Type tambahan yang diizinkan: `build`, `revert`, `perf`, dan `style` jika benar-benar akurat. Gunakan scope stabil berdasarkan domain, bukan nama individu.

### 5.2 Aturan Pesan

- subject menggunakan bahasa Inggris, imperative mood, dan lowercase setelah titik dua;
- subject menjelaskan outcome, bukan aktivitas generik;
- subject disarankan maksimal 72 karakter dan tanpa titik di akhir;
- body menjelaskan alasan, konteks, trade-off, risiko, dan migration bila tidak jelas dari diff;
- footer mencatat issue, decision, approval, co-author, atau `BREAKING CHANGE` bila relevan;
- jangan menggunakan pesan `update`, `fix`, `wip`, `final`, atau generated message tanpa konteks.

### 5.3 Atomic Commit

Satu commit wajib:

- memiliki satu tujuan logis;
- dapat direview, divalidasi, dan di-revert secara masuk akal;
- tidak mencampur formatting massal dengan perubahan makna;
- tidak memasukkan secret, credential, data sensitif, binary lokal, atau artefak sementara;
- menyertakan dokumentasi/test yang merupakan bagian langsung dari perubahan;
- tidak mengklaim completion jika state commit sebenarnya parsial.

Commit parsial diperbolehkan hanya jika workflow secara eksplisit mengizinkan checkpoint lokal/private, statusnya jelas, dan commit tersebut tidak dipromosikan sebagai hasil selesai. Shared branch tidak boleh menjadi tempat menyimpan `WIP` tanpa kesepakatan.

### 5.4 Review Sebelum Commit

Minimum:

1. `git status` dan branch benar;
2. seluruh diff serta file baru dibaca;
3. scope, unintended deletion, format, link, test/build, dan security diperiksa;
4. `git diff --check` lulus;
5. hanya file dalam scope di-stage;
6. staged diff direview ulang;
7. secret/data-sensitive scan proporsional dijalankan;
8. pesan commit sesuai perubahan aktual.

Jangan menggunakan `git add .` tanpa memeriksa status dan staged diff. Jangan mengubah author atau histori untuk menyembunyikan provenance.

## 6. Pull Request dan Review Policy

### 6.1 Kapan Pull Request Wajib

Pull Request wajib jika platform mendukung dan salah satu kondisi berikut berlaku:

- perubahan normatif, strategis, arsitektural, atau lintas domain;
- perubahan security, privacy, legal, permission, credential flow, atau protection;
- perubahan ke Constitution, Governance, engine inti, policy, atau standard;
- feature, bug fix material, migration, release, hotfix, atau perubahan irreversible;
- repository memiliki lebih dari satu contributor aktif atau branch protection mensyaratkannya;
- owner/session instruction secara eksplisit mewajibkan review.

Perubahan langsung yang diizinkan ke `main` tetap harus memiliki self-review, validation evidence, dan audit trail. Ketiadaan fitur PR tidak menghapus review/approval yang diwajibkan; gunakan review record lain yang sah atau tandai `Blocked`.

### 6.2 Isi Pull Request

PR minimum memuat:

- objective dan alasan;
- scope serta non-scope;
- ringkasan perubahan dan file/domain terdampak;
- dependency, keputusan, dan approval yang relevan;
- risk level, security/privacy impact, dan reversibility;
- validation evidence;
- rollback/recovery plan;
- breaking change, migration, technical debt, dan residual risk;
- issue/session/decision link serta checklist yang berlaku.

PR Draft digunakan untuk kolaborasi awal dan tidak boleh digabung sampai seluruh gate wajib lulus.

### 6.3 Reviewer

Reviewer dipilih berdasarkan ownership dan risiko:

- repository maintainer untuk integritas repository;
- domain owner untuk correctness domain;
- Governance/Founder untuk authority atau perubahan normatif;
- Security owner untuk security/privacy/credential/protection;
- release owner untuk release readiness.

Author tidak boleh menjadi satu-satunya approver pada perubahan yang memerlukan review independen. Perubahan oleh AI membutuhkan reviewer manusia bila gate manusia berlaku. Approval lama menjadi stale jika perubahan baru mengubah area yang telah direview secara material.

### 6.4 Checklist Review

Reviewer memeriksa:

- objective, scope, dan acceptance criteria;
- correctness, terminology, dan keselarasan authority;
- diff penuh, termasuk generated/deleted files;
- test, link, lint, build, compatibility, dan negative path yang relevan;
- security, privacy, secret, permission, legal/license, dan data handling;
- architecture, upstream/downstream, migration, rollback, dan blast radius;
- dokumentasi, metadata/lifecycle, changelog, versioning, release note, publication impact, dan audit evidence sesuai Documentation Engine;
- commit quality serta absence of unrelated changes;
- unresolved comment, blocker, risk owner, dan approval wajib.

### 6.5 Approval dan Merge Policy

- Semua required checks, required reviews, dan conversation resolution harus selesai.
- `Changes requested` memblokir merge sampai reviewer yang tepat menyatakan resolusi memadai.
- Jangan merge dengan check merah, conflict unresolved, approval palsu, atau bypass tanpa exception sah.
- **Squash merge** adalah default untuk working branch agar `main` tetap ringkas, kecuali commit terpisah memiliki nilai audit/migrasi yang perlu dipertahankan.
- **Merge commit** digunakan untuk release/integration branch atau rangkaian commit yang struktur historinya memang penting.
- **Rebase merge** hanya jika repository owner memilih linear history dan seluruh commit sudah bersih serta tidak merusak traceability.
- Merge method repository wajib konsisten; perubahan metode memerlukan owner review.

### 6.6 Conflict Resolution

1. Fetch state remote terbaru dan identifikasi sumber divergence.
2. Pahami intent kedua sisi, owner, status, serta dependency; jangan memilih `ours/theirs` secara massal tanpa review.
3. Selesaikan konflik pada working branch, bukan dengan force push ke protected branch.
4. Jalankan ulang seluruh check yang dipengaruhi konflik.
5. Minta review ulang jika resolusi mengubah makna atau area yang telah disetujui.
6. Catat keputusan material pada PR/decision record.
7. Jika intent atau authority tidak dapat dipastikan, hentikan merge dan eskalasikan.

## 7. Push Workflow

### 7.1 Kapan Push Dilakukan

Push dilakukan setelah commit lokal:

- telah direview dan tervalidasi;
- berada pada branch serta remote yang benar;
- tidak mengandung secret atau file lokal;
- tidak menimpa shared history;
- diperlukan untuk PR, backup kolaboratif, integrasi, atau deliverable session;
- diizinkan oleh owner, policy, dan credential scope.

Push checkpoint ke private working branch boleh dilakukan untuk backup/kolaborasi jika statusnya jelas. Push ke protected branch atau remote publik tidak boleh dilakukan hanya karena credential tersedia.

### 7.2 Verifikasi Sebelum Push

1. `git status --short --branch` bersih atau hanya memuat worktree yang sengaja belum diikutkan.
2. `git log` dan commit target benar.
3. upstream serta remote URL diverifikasi tanpa mengekspos credential.
4. local branch tidak tertinggal/divergen secara berbahaya.
5. validation, staged review, dan secret scan telah lulus.
6. target branch serta permission sesuai authority.
7. operasi adalah normal push; non-fast-forward membutuhkan penghentian dan resolusi, bukan force.

### 7.3 Verifikasi Setelah Push

- periksa exit status push;
- bandingkan hash lokal dengan ref remote yang dituju;
- pastikan branch/PR/check platform muncul sesuai harapan;
- jangan menyatakan berhasil hanya karena command dijalankan;
- catat branch, full commit hash, remote, waktu bila relevan, dan status check pada Session Report.

Jika push gagal, pertahankan commit lokal, klasifikasikan error, dan ikuti failure policy. Jangan melakukan blind retry atau memintas protection.

## 8. Release Workflow

### 8.1 Persiapan Release

Release hanya dibuat dari commit `main` yang:

- telah direview dan memenuhi release criteria;
- memiliki versi sesuai [`../../docs/standards/VERSIONING_CONVENTION.md`](../../docs/standards/VERSIONING_CONVENTION.md);
- memiliki `CHANGELOG.md` dan release note akurat;
- lulus test/check, security review, compatibility, dan migration review yang relevan;
- memiliki owner, approver, rollback plan, serta known issue/residual risk;
- tidak mengklaim status `Approved` untuk artefak yang belum disahkan.

Gunakan `release/<version>` hanya jika stabilisasi membutuhkan beberapa commit. Jangan menambah fitur baru ke release branch kecuali keputusan release owner yang terdokumentasi.

### 8.2 Tagging

- gunakan annotated tag `vMAJOR.MINOR.PATCH`, contoh `v0.2.0`;
- tag menunjuk commit terverifikasi di `main`;
- tag message mencantumkan versi dan ringkasan;
- published tag bersifat immutable dan tidak dipindahkan atau ditimpa;
- signing digunakan bila capability, key governance, dan verification path tersedia;
- AI tidak membuat atau mempublikasikan tag tanpa instruksi/delegasi release yang eksplisit.

### 8.3 Changelog dan Release Note

- perubahan penting dicatat di `Unreleased` selama pengembangan;
- saat release, pindahkan entry yang benar ke heading versi dan tanggal ISO 8601;
- kelompokkan `Added`, `Changed`, `Fixed`, `Deprecated`, `Removed`, dan `Security` sesuai kebutuhan;
- release note menjelaskan highlight, breaking change, migration, compatibility, known issue, dan rollback/recovery;
- changelog hanya mencakup commit yang benar-benar ada pada release.

### 8.4 Publikasi dan Verifikasi

1. Verifikasi commit release, version metadata, changelog, dan approval.
2. Buat annotated tag secara lokal.
3. Push tag tanpa force/update.
4. Buat release platform bila workflow menggunakannya.
5. Verifikasi tag remote, release asset/checksum bila ada, dan consumer path.
6. Catat evidence serta status final.

### 8.5 Rollback Release

Published history tidak dihapus atau ditulis ulang. Gunakan urutan:

1. hentikan promosi/distribusi yang menambah dampak;
2. preservasi evidence dan identifikasi blast radius;
3. `git revert` commit yang bermasalah atau siapkan corrective release;
4. terbitkan versi baru untuk koreksi; jangan memindahkan published tag;
5. perbarui changelog/release note dengan status dan mitigasi;
6. verifikasi state consumer;
7. jalankan incident/lesson-learned review sesuai risiko.

Yank/deprecate release hanya dilakukan jika platform mendukung dan authority mengizinkan; tindakan tersebut tetap tidak menghapus audit trail.

## 9. Repository Protection

### 9.1 Baseline Protection

Untuk `main`, dan `develop` bila digunakan, ruleset yang direkomendasikan:

- block force push dan branch deletion;
- require Pull Request untuk perubahan non-rutin sesuai Section 6;
- require minimal satu approval independen; tambah Code Owner/domain/Security review sesuai risiko;
- dismiss stale approval atau require approval ulang setelah perubahan material;
- require conversation resolution;
- require status checks dan branch up to date jika check tersedia;
- restrict bypass serta direct push kepada peran minimum yang terdokumentasi;
- require signed commit/tag hanya bila key lifecycle dan recovery sudah dikelola;
- aktifkan secret scanning, dependency/security alerts, dan audit log bila capability tersedia.

Ruleset platform adalah kontrol operasional eksternal; dokumentasi repository tidak boleh mengklaim konfigurasi aktif sebelum diverifikasi. Perubahan protection dicatat dengan actor, alasan, before/after, approval, waktu, dan expiry bila sementara.

### 9.2 Larangan dan Exception

Dilarang:

- force push ke `main` atau protected shared branch;
- memindahkan/menghapus published tag untuk menyembunyikan kesalahan;
- menonaktifkan check, review, atau protection agar merge cepat;
- menggunakan admin bypass tanpa exception tertulis;
- menghapus audit log, PR, branch, atau commit yang dibutuhkan sebagai evidence;
- menyimpan credential di remote URL, commit, log, issue, atau PR.

Exception protection harus memiliki authority, alasan, scope, branch/ref, durasi/expiry, compensating control, recovery plan, dan audit trail. AI tidak dapat menerbitkan exception untuk dirinya sendiri.

### 9.3 Backup Strategy

Git remote utama bukan satu-satunya backup. Repository owner menetapkan:

- remote utama dan mirror/backup terotorisasi;
- jadwal backup sesuai criticality;
- cakupan branch, tag, Git LFS/object, release artifact, issue/PR/export, dan configuration/ruleset;
- encryption, access control, retention, serta storage owner;
- restore test berkala dan recovery time objective bila relevan.

Backup tidak boleh dibuat ke lokasi pribadi/tidak terotorisasi. AI hanya boleh membuat backup bila tujuan, lokasi, data classification, retention, dan authority jelas.

### 9.4 Audit History dan Traceability

Trace minimum untuk perubahan material:

```text
Objective / Issue / Session
  → Branch
  → Commit(s)
  → Pull Request / Review
  → Approval / Decision
  → Merge commit
  → Tag / Release (jika ada)
  → Outcome / Incident / Revert
```

Audit record mempertahankan full hash, author, reviewer, approver, timestamp, validation evidence, exception, dan keputusan material sesuai risiko. Gunakan least disclosure: jangan memasukkan secret atau data pribadi yang tidak diperlukan.

## 10. AI Git Automation Policy

### 10.1 AI Boleh Commit Otomatis Jika

Semua kondisi berikut terpenuhi:

- objective dan instruksi session secara eksplisit meminta atau mengizinkan perubahan repository;
- working tree awal, branch, remote, dan unrelated work telah diperiksa;
- perubahan berada dalam scope, reversible, dan tidak membutuhkan approval yang belum tersedia;
- seluruh validation gate wajib lulus;
- diff dan staged diff telah direview;
- secret/data-sensitive scan proporsional lulus;
- commit atomik dan Conventional Commits digunakan;
- commit tidak digunakan untuk mengklaim approval normatif.

AI boleh membuat lebih dari satu commit hanya jika setiap commit memiliki tujuan logis berbeda dan pemisahan tersebut memperbaiki review atau rollback.

### 10.2 AI Boleh Push Otomatis Jika

Selain syarat commit:

- session secara eksplisit mewajibkan push atau policy yang sah memberi delegasi push normal;
- credential dan remote telah terverifikasi tanpa mengekspos token;
- target branch diizinkan dan push tidak memintas PR/protection;
- push bersifat fast-forward normal;
- tidak ada divergence, check kritis gagal, atau required approval yang belum tersedia;
- AI dapat memverifikasi ref remote setelah push dan melaporkan hasil aktual.

Instruksi SPOS session yang secara eksplisit meminta “commit dan push jika akses tersedia” menjadi delegasi untuk **normal push** hasil session yang tervalidasi, bukan izin force push, merge, release, protection change, atau history rewrite.

### 10.3 AI Wajib Meminta Persetujuan Founder

Founder decision wajib sebelum AI:

- mengubah atau merilis Constitution, Kernel, authority, identitas, nilai, etika, atau arah strategis;
- menerima risiko material atau konflik konstitusional;
- mengubah ownership/authority utama repository tanpa delegation yang telah disahkan;
- melemahkan protection branch utama, mengizinkan force push/history rewrite, atau menghapus evidence material;
- membuat release/tag yang menyatakan milestone fundamental, ratifikasi, atau status `1.0.0` tanpa approval;
- mempublikasikan repository private, data sensitif, atau artefak proprietary ke akses yang lebih luas;
- menjalankan operasi Git material yang Governance tetapkan eksklusif bagi Founder.

Jika Founder telah mendelegasikan operasi non-konstitusional secara tertulis, AI meminta approval kepada delegate dalam scope delegasi; AI tetap tidak dapat mengasumsikan delegasi.

### 10.4 AI Wajib Meminta Approval Manusia/Domain

Approval authority yang tepat diperlukan untuk:

- merge perubahan yang mensyaratkan review independen;
- security/privacy/legal/permission/credential changes;
- migration, destructive operation, hotfix, dan release publik;
- perubahan branch protection, repository visibility, access, webhook, integration, atau secret;
- conflict resolution yang mengubah intent pihak lain;
- backup/export ke sistem eksternal;
- bypass atau exception apa pun.

### 10.5 Kondisi Penghentian Otomatis

AI wajib menghentikan area Git terdampak jika:

- repository, target branch, remote, atau owner tidak dapat diverifikasi;
- working tree memiliki unrelated work yang berisiko tertimpa;
- secret/data sensitif ditemukan pada diff atau histori yang akan dipush;
- required validation, review, approval, atau protection gagal;
- non-fast-forward, divergence, conflict, atau unexpected remote state terjadi;
- operasi memerlukan force push, reset destruktif, rebase shared history, branch/tag deletion, atau protection bypass tanpa approval sah;
- credential/permission gagal atau tampak terlalu luas/tidak sah;
- commit/tag/release berpotensi membuat klaim approval, ratifikasi, atau status palsu;
- rollback/recovery tidak layak untuk operasi berisiko;
- instruksi bertentangan dengan hukum, keselamatan, Constitution, Governance, atau policy yang lebih tinggi.

AI mempertahankan pekerjaan valid, evidence yang aman, dan commit lokal bila sesuai; kemudian melaporkan blocker, risiko, dan recovery path tanpa mengarang completion.

## 11. Failure dan Recovery

| Kegagalan | Tindakan |
| --- | --- |
| Push ditolak/non-fast-forward | Jangan force push; fetch, analisis divergence, sinkronkan secara aman atau eskalasikan |
| Conflict | Selesaikan berdasarkan intent kedua sisi, revalidate, dan minta re-review bila material |
| Commit salah belum dipush | Buat perbaikan terkontrol; amend hanya bila branch private dan belum dibagikan |
| Commit salah sudah dipush | Gunakan `git revert` atau corrective commit; jangan rewrite shared history |
| Secret ter-commit belum dipush | Hentikan, rotasi/revoke bila perlu, bersihkan secara aman dengan Security owner |
| Secret ter-push | Anggap incident; revoke/rotate dahulu, batasi exposure, preservasi evidence aman, lalu lakukan remediation terotorisasi |
| Tag salah belum dipush | Hapus/perbaiki lokal setelah verifikasi |
| Published tag salah | Jangan pindahkan diam-diam; buat versi koreksi dan catat status |
| Protection/check gagal | Jangan bypass; perbaiki penyebab atau dapatkan exception tertulis |
| Akses GitHub gagal | Simpan commit lokal, laporkan blocker, dan jangan mengklaim push/merge |

Retry mengikuti [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md): diagnosis dahulu, maksimum satu retry default untuk error transient non-kritis, tanpa blind loop. Permission, authority, invalid input, deterministic check failure, dan conflict tidak diselesaikan dengan retry.

## 12. Cross-System Alignment

| Sumber | Implementasi dalam Git Engine | Boundary |
| --- | --- | --- |
| [`CONSTITUTION.md`](CONSTITUTION.md) | Repository First, Truth over Assumption, transparency, human oversight, traceability, reversibility, dan audit | Git event tidak menjadi ratifikasi atau approval |
| [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) | Review before commit, commit before push, push before report, small changes, rollback, dan autonomy gates | Git Engine merinci workflow tanpa memperluas otonomi |
| [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) | Perform Git Workflow, validation, evidence, failure/recovery, dan Definition of Done | Git Engine adalah sumber kanonik detail Git; Execution Engine tetap sumber lifecycle session |
| [`DOCUMENTATION_ENGINE.md`](DOCUMENTATION_ENGINE.md) | Versioned/traceable documentation, change history, review, changelog, release notes, publication, dan archive | Git menyediakan history/evidence; Git event tidak mengubah status approval dokumen |
| [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) | Git Review gate, traceability, evidence integrity, review independence, finding, release readiness, dan Final Approval | Check/merge/push hijau tidak menjadi approval kualitas atau risk acceptance |
| [`../../01-foundation/FOUNDATION_ARCHITECTURE.md`](../../01-foundation/FOUNDATION_ARCHITECTURE.md) | SSOT, ownership, evidence flow, approved lifecycle, dan Git history | Engine tidak mengambil ownership Foundation/domain |
| [`../../01-foundation/governance/README.md`](../../01-foundation/governance/README.md) | approval, delegation, exception, escalation, dan audit | Governance substantif belum tersedia; ambiguity tetap fail-closed |
| [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) | traceable component flow, bounded execution, report, dan feedback | Engine adalah kontrak dokumentasi, bukan Git hosting/automation runtime |
| [`../../CONTRIBUTING.md`](../../CONTRIBUTING.md) | contribution flow, review, branch, commit, dan sensitive handling | Contributing merujuk engine; tidak menjadi policy Git tandingan |
| [`../../docs/standards/BRANCH_CONVENTION.md`](../../docs/standards/BRANCH_CONVENTION.md) dan [`../../docs/standards/COMMIT_CONVENTION.md`](../../docs/standards/COMMIT_CONVENTION.md) | Bentuk nama branch dan commit untuk penggunaan repository | Standards adalah profil repository yang tunduk pada engine |
| [`../../docs/standards/VERSIONING_CONVENTION.md`](../../docs/standards/VERSIONING_CONVENTION.md) | SemVer, annotated tag, immutable release history, dan changelog | Versi tidak otomatis mengubah status authority |

### 12.1 Resolusi Cross-Review SPOS-005

- Prefix kanonik branch baru distandarkan menjadi `feature/*`, sementara `feat/*` dipertahankan sebagai alias kompatibilitas repository lama.
- `develop` dinyatakan opsional agar tidak menciptakan branch permanen tanpa kebutuhan.
- Direct commit ke `main` dipertahankan hanya sebagai exception workflow berisiko rendah yang diizinkan owner; perubahan material wajib melalui PR/review.
- Git Engine menjadi sumber kanonik detail Git; standar branch/commit/versioning tetap menjadi profil bentuk repository dan wajib merujuk engine.
- Commit/push allowance Developer Mode dipersempit secara eksplisit oleh syarat branch protection, approval, dan normal fast-forward push.
- Governance gap tidak diisi dengan self-approval AI; operasi authority-sensitive tetap fail-closed.

## 13. Validation Checklist Git

Sebelum Git workflow dinyatakan selesai:

- [ ] Repository, branch, working tree, remote, dan upstream terverifikasi.
- [ ] Objective dan scope tunggal dapat ditelusuri ke diff.
- [ ] Tidak ada unrelated work, secret, data sensitif, atau file lokal dalam commit.
- [ ] Diff, staged diff, dan `git diff --check` telah direview.
- [ ] Test/check dan documentation gate yang relevan lulus.
- [ ] Commit atomik serta Conventional Commits dipatuhi.
- [ ] Required reviewer, approval, PR, check, dan conversation resolution selesai.
- [ ] Merge/push tidak memintas protection atau menulis ulang shared history.
- [ ] Hash lokal dan remote diverifikasi setelah push.
- [ ] Tag/release/changelog diverifikasi bila berlaku.
- [ ] Failure, exception, rollback, technical debt, dan residual risk dicatat.
- [ ] Session Report menyatakan branch, hash, remote, dan status aktual.

## 14. Activation dan Change Control

Dokumen ini disusun pada SPOS-005 sebagai baseline Git governance. Aktivasi sebagai standard binding memerlukan:

- Constitution dengan status operasional sah atau keputusan Founder yang secara eksplisit mengizinkan baseline sementara;
- Developer Mode dan Execution Engine yang kompatibel;
- review Governance, repository owner, Security owner bila relevan, dan authority lain yang ditunjuk;
- approval eksplisit, versi, tanggal efektif, dan audit trail;
- penerapan ruleset/protection pada platform serta verifikasi bahwa konfigurasi aktual sesuai policy;
- propagasi melalui referensi kanonik tanpa membuat salinan rule tandingan.

Activation record:

- Approver: `<authorized human>`
- Decision: `<approved / rejected / revision required>`
- Effective date: `<YYYY-MM-DD>`
- Version approved: `<version>`
- Constitution dependency: `<version and status>`
- Developer Mode dependency: `<version and status>`
- Execution Engine dependency: `<version and status>`
- Governance/repository decision: `<relative-link>`
- Platform protection evidence: `<reference>`
- Commit hash: `<hash>`

AI tidak boleh mengisi field approval atas nama manusia. Perubahan material pada branch strategy, review/merge gate, release, protection, AI authority, backup, atau audit policy memerlukan impact analysis, versioning, changelog, review, dan approval sesuai authority.

## 15. Git Engine Review Checklist

- [x] Branch strategy untuk `main`, `develop`, working branch, release, dan hotfix terdokumentasi.
- [x] Conventional Commits, format pesan, atomic commit, dan contoh type wajib terdokumentasi.
- [x] Pull Request, reviewer, checklist, approval, merge, dan conflict resolution terdokumentasi.
- [x] Push timing, verifikasi pre/post-push, tagging, changelog, release, dan rollback terdokumentasi.
- [x] Branch protection, force-push prohibition, backup, audit history, dan traceability terdokumentasi.
- [x] AI commit/push permission, Founder/human approval, dan automatic stop conditions terdokumentasi.
- [x] Alignment dengan Constitution, Developer Mode, Execution Engine, Documentation Engine, Quality Engine, Foundation, Governance, SPOS Architecture, dan repository standards dipetakan.
- [x] Scope tidak membangun aplikasi, fitur produk, Git hosting, CI/CD, atau runtime automation.
- [ ] Constitution diratifikasi atau baseline interim diizinkan secara eksplisit.
- [ ] Developer Mode, Execution Engine, dan Git Engine memperoleh approval operasional serta activation record.
- [ ] Governance substantif, repository role delegation, dan authority matrix tersedia.
- [ ] Platform branch protection, backup, audit retention, dan release authority dikonfigurasi serta diverifikasi.
