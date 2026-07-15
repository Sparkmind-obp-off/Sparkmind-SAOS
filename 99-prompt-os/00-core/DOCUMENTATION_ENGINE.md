# SparkMind Documentation Engine

> Status: In Review — documentation governance baseline SPOS-006; activation as a binding standard requires the applicable human authority and eligible upstream versions.
>
> Owner: Founder
>
> Reviewer: Founder, Governance owner, Documentation owner/steward, Knowledge Steward, repository maintainer, dan domain owner yang ditunjuk
>
> Approver: Founder atau authority manusia yang didelegasikan secara tertulis untuk kebijakan dokumentasi non-konstitusional
>
> Version: 0.1.0
>
> Established: 2026-07-15
>
> Effective: setelah approval operasional yang sah dan dependency upstream terpenuhi
>
> Review trigger: amendment Constitution; perubahan Governance, Developer Mode, Session Engine, Execution Engine, Git Engine, Foundation, Knowledge System, atau SPOS Architecture; perubahan struktur repository atau consumer; insiden akibat dokumentasi usang; atau evidence bahwa standard tidak lagi efektif

## 1. Kedudukan dan Tujuan

Documentation Engine adalah standar permanen untuk seluruh dokumentasi yang dibuat atau dipelihara oleh manusia dan AI di ekosistem SparkMind. Engine menetapkan prinsip, kategori, lifecycle, struktur, metadata, versioning, referensi silang, ownership, review cadence, change history, validation, serta kebijakan dokumentasi AI.

Engine ini mengoperasionalkan [`CONSTITUTION.md`](CONSTITUTION.md), [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md), [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md), [`SESSION_ENGINE.md`](SESSION_ENGINE.md), [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md), [`GIT_ENGINE.md`](GIT_ENGINE.md), [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md), dan [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md). Constitution menetapkan prinsip dan authority; Developer Mode menetapkan perilaku kerja; Session Engine menetapkan lifecycle orchestration/state/continuity session; Execution Engine menetapkan prosedur eksekusi; Git Engine menjaga histori perubahan; Documentation Engine menjadi sumber kanonik bagi tata kelola dokumentasi lintas domain.

Documentation Engine bukan aplikasi, content management system, generator otomatis, pengganti Governance, atau izin bagi AI untuk menetapkan fakta dan approval. Dokumen menjelaskan keadaan, keputusan, atau prosedur; keberadaan file, commit, publication, atau penggunaan berulang tidak otomatis menjadikan isinya benar, approved, atau berlaku.

Karena Constitution, Governance Engine, dan engine upstream masih `In Review`, dokumen ini juga `In Review`. Dokumen dapat digunakan sebagai baseline kerja dan bahan review, tetapi tidak boleh diperlakukan sebagai standard binding sebelum aktivasi yang sah.

## 2. Scope dan Non-Scope

### 2.1 Scope

Engine berlaku untuk dokumentasi:

- AI Agent, repository, produk, arsitektur, API, governance, knowledge, prompt, dan proses engineering;
- dalam repository maupun sistem dokumentasi eksternal yang diotorisasi;
- yang dibuat manual, dihasilkan AI, atau disusun bersama;
- sepanjang lifecycle dari draft hingga archived;
- yang bersifat normatif, informatif, prosedural, operasional, atau evidensial.

### 2.2 Non-Scope

Engine tidak:

- menetapkan requirement atau keputusan produk;
- meratifikasi Constitution, Governance, policy, atau keputusan strategis;
- menggantikan source code, schema, test, telemetry, atau evidence teknis;
- mengatur isi substantif setiap domain tanpa owner domain;
- membangun portal dokumentasi, search engine, application, deployment, atau automation runtime;
- memberi authority kepada AI untuk menyetujui hasilnya sendiri.

## 3. Prinsip Dokumentasi

### 3.1 Documentation First

Dokumentasi dimulai saat objective, constraint, interface, atau keputusan material dibentuk, bukan setelah perubahan selesai. Sebelum implementasi, dokumentasikan intent dan acceptance criteria secara proporsional. Selama implementasi, sinkronkan keputusan serta dampak. Sebelum completion, pastikan consumer memiliki panduan aktual.

Documentation First tidak berarti membuat dokumen panjang untuk setiap perubahan. Kedalaman harus proporsional terhadap risiko, longevity, complexity, dan jumlah consumer.

### 3.2 Single Source of Truth

Satu definisi, keputusan, policy, atau prosedur memiliki satu sumber kanonik. Dokumen lain merujuk sumber tersebut dan hanya memberi konteks lokal yang tidak mengubah makna. Jika dua sumber mengklaim authority yang sama, hentikan propagasi dan selesaikan ownership serta precedence.

### 3.3 Living Documentation

Dokumentasi dipelihara selama subject-nya masih digunakan. Perubahan kode, architecture, workflow, ownership, status, dan dependency harus memicu review dokumen terdampak. Living documentation tidak menghapus histori; current state dan historical evidence dipisahkan melalui versioning serta lifecycle.

### 3.4 Versioned Documentation

Perubahan dokumentasi ditelusuri melalui Git atau version control yang disetujui. Dokumen kontraktual dapat memiliki versi independen jika memiliki owner, compatibility rule, dan approval path. Status lifecycle tidak sama dengan versi, dan commit baru tidak otomatis mengubah status authority.

### 3.5 Traceable Documentation

Setiap klaim material dapat ditelusuri ke source, decision, owner, version, commit, evidence, atau authority yang relevan. Dokumen harus membedakan fakta, interpretasi, asumsi, rekomendasi, dan keputusan. Laporan session tidak menjadi sumber kanonik tandingan.

### 3.6 Readable by Humans and AI

Dokumen menggunakan struktur semantik, heading deskriptif, metadata eksplisit, istilah konsisten, link langsung, serta bahasa yang tidak bergantung pada konteks percakapan tersembunyi. Tabel dipakai untuk perbandingan ringkas; prosedur memakai langkah berurutan; constraint dan exception dinyatakan eksplisit.

### 3.7 Consistency Over Personal Preference

Konvensi repository dan domain mengalahkan preferensi gaya individu selama tidak bertentangan dengan authority lebih tinggi. Perubahan format massal tanpa manfaat semantik dihindari. Jika format perlu diubah, tetapkan migration plan dan perbarui consumer secara konsisten.

### 3.8 Evidence Before Assumption

Klaim tentang keadaan sistem, approval, hasil test, user behavior, atau external fact memerlukan evidence yang sesuai. Asumsi diberi label, owner, dampak, dan validation path. AI tidak boleh mengisi celah dengan narasi yang tampak meyakinkan.

### 3.9 Explicit Over Implicit

Status, scope, owner, audience, prerequisite, constraint, exception, risk, dan next action dinyatakan bila penting bagi penggunaan yang benar. Jangan mengandalkan nama file, lokasi folder, kebiasaan tim, atau konteks percakapan sebagai satu-satunya penjelasan.

### 3.10 Prinsip Pendukung

- **Least duplication:** ringkas dan rujuk; jangan copy-paste rule kanonik.
- **Proportionality:** effort dokumentasi sebanding dengan risiko dan kebutuhan consumer.
- **Accessibility:** gunakan bahasa, struktur, link label, dan format yang dapat diakses.
- **Security and least disclosure:** dokumentasi tidak memuat secret atau data sensitif yang tidak diperlukan.
- **Reversibility:** perubahan makna dapat dibandingkan, direview, dan dipulihkan.
- **Human accountability:** owner manusia memegang approval ketika authority manusia diwajibkan.

## 4. Authority, Ownership, dan Peran

| Peran | Tanggung jawab | Batas |
| --- | --- | --- |
| **Founder** | Ratifikasi fundamental, arah strategis, dan keputusan authority material | Tidak menggantikan kebutuhan evidence atau kewajiban hukum/keselamatan |
| **Governance owner** | Delegation, approval, exception, escalation, dan lifecycle policy sesuai Governance Engine | Tidak menetapkan correctness domain atau mengubah Constitution |
| **Documentation owner/steward** | Standard, information architecture, quality, discovery, dan portfolio review | Tidak menyetujui correctness domain tanpa domain owner |
| **Domain owner** | Akurasi, completeness, applicability, dan lifecycle isi domain | Tidak mengubah authority lintas domain tanpa review yang tepat |
| **Knowledge Steward** | Provenance, classification, curation, dan relasi Knowledge System | Knowledge tidak otomatis menjadi policy |
| **Repository maintainer** | Integritas file, link, tooling, version control, dan publication path | Commit/publish tidak sama dengan approval isi |
| **Author** | Menyusun, memverifikasi sumber, self-review, dan merespons review | Tidak self-approve perubahan yang memerlukan review independen |
| **Reviewer** | Memeriksa correctness, evidence, consistency, risk, dan usability | Tidak approve di luar kompetensi/delegasi |
| **Consumer** | Menggunakan versi/status yang benar dan melaporkan drift | Tidak menafsirkan draft sebagai approved |
| **AI Agent** | Drafting, update, cross-reference, validation, dan evidence sesuai Section 10 | Bukan Founder, approver, risk owner, atau sumber fakta tanpa evidence |

Setiap dokumen substantif wajib memiliki owner yang dapat bertanggung jawab atas akurasi dan pemeliharaan. Jika owner belum ditetapkan, status maksimal adalah `Draft` atau `In Review`, dan penggunaan operasional harus fail-closed sesuai risiko.

## 5. Jenis Dokumentasi

| Jenis | Tujuan | Kapan digunakan | Sumber/owner utama |
| --- | --- | --- | --- |
| **Architecture** | Menjelaskan struktur, boundary, dependency, interface, data/control flow, constraint, dan quality attributes | Ketika desain sistem/layer memengaruhi banyak komponen atau consumer | Architecture/domain owner |
| **Design Decision** | Mencatat keputusan desain lokal beserta konteks, opsi, trade-off, dan dampak | Untuk keputusan material yang perlu dilacak tetapi tidak memerlukan ADR formal | Design/domain owner |
| **ADR (Architecture Decision Record)** | Merekam keputusan arsitektural yang durable, alternatif, konsekuensi, dan supersession | Untuk keputusan architecture lintas komponen atau sulit dibatalkan | Architecture owner dan reviewer terdampak |
| **API** | Mendefinisikan contract endpoint/interface, auth, schema, error, example, version, dan compatibility | Untuk API yang dikonsumsi manusia atau sistem | API/service owner |
| **Product** | Menjelaskan tujuan, scope, user, requirement, behavior, metric, limitation, dan lifecycle produk | Untuk shared understanding produk; bukan pengganti keputusan Product owner | Product owner |
| **Knowledge** | Menyimpan fakta terkurasi, konsep, reference, learning, dan provenance | Saat informasi reusable perlu discovery dan review | Knowledge/domain owner |
| **Governance** | Menetapkan authority, ownership, approval, delegation, exception, escalation, dan audit | Untuk aturan pengambilan keputusan dan akuntabilitas | Governance authority |
| **Prompt** | Mendefinisikan kontrak system/user/task, dependency, input/output, safety, dan evaluation | Untuk prompt reusable atau material yang memengaruhi perilaku AI | Prompt owner dan reviewer safety/domain |
| **Playbook** | Memberi prosedur berurutan untuk kelas pekerjaan berulang dengan decision point | Ketika operator perlu menjalankan workflow adaptif yang approved | Process/domain owner |
| **Standard** | Menetapkan requirement konsisten yang dapat diverifikasi | Untuk aturan lintas artefak atau implementasi | Standard owner dan authority yang berlaku |
| **Policy** | Menetapkan apa yang wajib/dilarang, siapa berwenang, dan exception path | Untuk constraint organisasi, legal, security, atau operasional | Policy/Governance owner |
| **Runbook** | Memberi langkah operasional spesifik untuk menjalankan, memulihkan, atau menangani insiden | Untuk operasi yang time-sensitive dan harus dapat dieksekusi | Service/operations owner |
| **User Guide** | Membantu end user mencapai outcome melalui alur, example, dan troubleshooting | Ketika capability digunakan oleh pengguna non-implementor | Product/support owner |
| **Developer Guide** | Menjelaskan setup, architecture context, coding workflow, test, debugging, dan contribution | Untuk engineer/AI yang membangun atau memelihara sistem | Engineering/repository owner |
| **Changelog** | Menyediakan histori terkurasi perubahan penting menurut versi/waktu | Untuk consumer yang perlu memahami perubahan antarversi | Release/repository owner |
| **Release Notes** | Menjelaskan isi satu release, impact, migration, compatibility, known issue, dan rollback | Pada publication release tertentu | Release owner |

### 5.1 Pemilihan Jenis

1. Pilih berdasarkan kebutuhan consumer dan authority, bukan template yang tersedia.
2. Jangan menggunakan README sebagai tempat semua jenis konten; README adalah entry point dan index.
3. Gunakan ADR bila keputusan arsitektural perlu status serta supersession yang durable.
4. Gunakan runbook untuk tindakan operasional yang preskriptif; gunakan playbook untuk prosedur yang lebih adaptif.
5. Policy menetapkan kewajiban dan authority; standard menetapkan bentuk atau quality requirement; guide menjelaskan cara menggunakan.
6. Changelog bersifat lintas perubahan; release notes terikat pada satu release.
7. Satu dokumen boleh menggabungkan jenis hanya jika audience, owner, lifecycle, dan authority tetap jelas.

## 6. Lifecycle Dokumentasi

Lifecycle kanonik yang diminta SPOS-006 adalah:

```text
Draft → Review → Approved → Published → Updated → Archived
  ▲        │          │          │          │
  └────────┴──────────┴──────────┴──────────┘ revision loop
```

`In Review` adalah label status repository untuk tahap **Review**. `Superseded` dan `Deprecated` adalah state transisi khusus menuju update atau archive, bukan pengganti enam tahap utama.

### 6.1 Draft

Dokumen sedang disusun dan belum berlaku.

Syarat masuk:

- kebutuhan, audience, lokasi kanonik, owner awal, dan source diketahui;
- scope serta jenis dokumen dipilih;
- status `Draft` ditampilkan bila dapat disalahartikan.

Syarat keluar ke Review:

- struktur minimum proporsional tersedia;
- klaim material memiliki source atau label asumsi;
- self-review, terminology, link, security, dan completeness check selesai;
- reviewer serta approver yang berlaku ditentukan.

### 6.2 Review

Dokumen diperiksa untuk correctness, evidence, authority, consistency, risk, dan usability. Label repository: `In Review`.

Syarat transisi:

- reviewer memiliki kompetensi dan tidak memiliki conflict yang tidak dikelola;
- komentar material diselesaikan atau dicatat sebagai blocker;
- perubahan normatif mendapat review authority yang tepat;
- dokumen tidak boleh digunakan seolah approved hanya karena review dimulai.

Hasil Review:

- kembali ke Draft untuk revisi material;
- tetap In Review jika blocker terbuka;
- menuju Approved jika seluruh gate dan approval sah selesai;
- menuju Archived bila kebutuhan dibatalkan dengan alasan tercatat.

### 6.3 Approved

Authority yang tepat telah menyetujui isi untuk scope dan versi tertentu.

Approval record minimum:

- approver dan authority/delegation;
- keputusan serta tanggal;
- versi atau commit yang disetujui;
- scope efektif dan dependency;
- limitation, exception, atau expiry bila ada.

AI tidak boleh menetapkan status `Approved` tanpa evidence keputusan manusia yang sah.

### 6.4 Published

Dokumen approved tersedia melalui channel resmi dan dapat ditemukan oleh audience yang dituju.

Syarat publication:

- source kanonik dan versi benar;
- index, navigation, link, access control, dan consumer reference diperbarui;
- materi sensitif hanya tersedia bagi audience berwenang;
- publication tidak mengubah makna atau approval scope.

Dokumen dapat `Approved` tetapi belum `Published`. Publication draft hanya boleh dilakukan untuk review dengan label yang jelas dan bukan sebagai panduan operasional resmi.

### 6.5 Updated

Dokumen current mengalami perubahan setelah approval/publication. `Updated` adalah event lifecycle; status setelah update bergantung pada materialitas.

- Perubahan editorial dapat kembali ke Published setelah review maintainer sesuai delegation.
- Perubahan makna kembali ke Draft/Review dan approval lama tidak mencakup perubahan material tersebut.
- Perubahan breaking memerlukan impact analysis, migration, versioning, dan komunikasi consumer.
- Source drift atau perubahan upstream memicu review walaupun file belum diedit.

### 6.6 Archived

Dokumen tidak lagi menjadi sumber current dan dipertahankan untuk histori, audit, legal retention, atau evidence.

Syarat archive:

- owner/authority menyetujui sesuai jenis dokumen;
- alasan, tanggal, retention, dan pengganti bila ada dicatat;
- link aktif serta index diarahkan ke source current;
- dokumen archived read-only kecuali koreksi metadata/security;
- secret dan data pribadi tidak dipertahankan hanya karena alasan histori.

### 6.7 Deprecated dan Superseded

- **Deprecated:** masih dapat diakses selama transisi, tetapi tidak untuk penggunaan baru. Wajib mencantumkan deadline atau review trigger serta migration path.
- **Superseded:** telah diganti dokumen/version tertentu. Wajib memiliki link dua arah antara sumber lama dan pengganti.

### 6.8 Aturan Transisi Umum

- Tidak boleh melompati Review dan approval wajib untuk perubahan material.
- Commit, merge, tag, publish, atau traffic tidak sama dengan approval.
- Status tidak boleh dinaikkan oleh author/AI tanpa authority.
- Downgrade status diperbolehkan bila evidence invalid, source berubah, atau insiden ditemukan; alasan wajib dicatat.
- Dokumen dengan owner hilang, review lewat waktu, atau source tidak dapat diverifikasi ditandai untuk review; penggunaan berisiko dapat dihentikan.
- Penghapusan permanen hanya untuk alasan legal, privacy, security, atau retention yang sah dan tetap menjaga audit metadata secara aman bila diizinkan.

## 7. Standards Dokumentasi

### 7.1 Struktur Dokumen

Struktur minimum dipilih secara proporsional:

1. judul unik dan deskriptif;
2. metadata status/ownership;
3. tujuan dan audience;
4. scope serta non-scope;
5. prerequisite, dependency, atau source;
6. isi utama: keputusan, kontrak, prosedur, atau penjelasan;
7. example dan negative case bila membantu;
8. limitation, risk, exception, dan escalation;
9. validation atau review checklist;
10. referensi dan change history bila diperlukan.

Dokumen singkat tidak wajib memuat heading kosong. Dokumen normatif wajib menggunakan kata `wajib`, `dilarang`, `boleh`, dan `disarankan` secara konsisten agar level requirement jelas.

### 7.2 Penamaan File

- File kanonik substantif menggunakan `UPPER_SNAKE_CASE.md` sesuai repository saat ini.
- Index folder selalu `README.md`.
- ADR menggunakan ID stabil, misalnya `ADR-0001-short-title.md`, jika domain menetapkan registry ADR.
- Session report mengikuti `SESSION-NNN.md` atau `SPOS-NNN.md`.
- Jangan gunakan `final`, `latest`, `new`, `copy`, tanggal acak, nama author, atau suffix `v2` sebagai lifecycle.
- Nama stabil menggambarkan subject, bukan status sementara.
- Aturan umum mengikuti [`../../docs/standards/NAMING_CONVENTION.md`](../../docs/standards/NAMING_CONVENTION.md).

### 7.3 Metadata

Metadata minimum untuk dokumen substantif:

| Field | Requirement |
| --- | --- |
| **Status** | Wajib bila belum approved atau dapat disalahartikan |
| **Owner** | Wajib; pihak yang menjaga akurasi dan lifecycle |
| **Reviewer** | Wajib untuk dokumen material atau normatif |
| **Approver** | Wajib untuk Approved/policy/strategic material |
| **Version** | Wajib untuk kontrak versioned; selain itu histori Git cukup |
| **Established / Last reviewed** | Tanggal ISO 8601 yang relevan |
| **Effective / Expiry** | Wajib bila applicability berbatas waktu |
| **Review trigger / cadence** | Wajib untuk dokumen operasional atau berisiko tinggi |
| **Audience / Scope** | Wajib bila penggunaan dapat ambigu |
| **Sources / Dependencies** | Wajib untuk klaim material dan derived document |
| **Supersedes / Superseded by** | Wajib bila relasi lifecycle ada |
| **Classification** | Wajib bila akses atau sensitivity perlu dikendalikan |

Metadata tidak boleh berisi placeholder yang tampak seperti approval nyata. Field yang belum dapat diisi diberi label jelas dan owner tindak lanjut, atau dokumen tetap Draft.

### 7.4 Versioning

- Git adalah histori default untuk file repository.
- Versi independen hanya untuk contract/policy/API yang membutuhkan compatibility dan approval per versi.
- Gunakan Semantic Versioning bila perubahan memiliki compatibility contract: major untuk breaking, minor untuk penambahan kompatibel, patch untuk koreksi kompatibel.
- Editorial change tidak mengubah versi independen kecuali policy domain menentukan.
- Approval terikat pada content hash/version yang direview; perubahan material membuat approval sebelumnya stale.
- Nama file tetap stabil; jangan membuat salinan versi sebagai SSOT baru.
- Release/versioning repository mengikuti [`../../docs/standards/VERSIONING_CONVENTION.md`](../../docs/standards/VERSIONING_CONVENTION.md).

### 7.5 Cross-Reference

- Tautkan source kanonik, bukan salinan atau session report.
- Nyatakan relasi bila tidak jelas: `implements`, `derived from`, `governed by`, `supersedes`, `evidence for`, atau `related`.
- Sediakan link balik untuk supersession, dependency material, dan discovery kritis.
- Hindari circular authority: dua dokumen tidak boleh saling mengklaim sebagai sumber authority utama.
- Gunakan anchor hanya jika heading stabil; perubahan heading wajib memeriksa inbound link.

### 7.6 Internal Link

- Gunakan link Markdown relatif untuk file repository.
- Link label harus menjelaskan target.
- Verifikasi target dan anchor setelah create, rename, move, atau archive.
- README/index mengarah ke dokumen current, bukan archived.
- Jangan menggunakan local absolute path, credential-bearing URL, atau temporary branch URL.
- Broken link memblokir publication bila link dibutuhkan untuk penggunaan benar.

### 7.7 Ownership

Owner wajib:

- menjaga correctness, scope, dan source;
- memastikan review dan approval sesuai cadence/trigger;
- menilai impact update kepada consumer;
- mengelola deprecation, supersession, dan archive;
- menyediakan escalation path atau menunjuk successor.

Ownership adalah accountability, bukan izin unilateral untuk mengubah authority lebih tinggi. Perubahan owner material harus memiliki delegation record dan consumer notification.

### 7.8 Review Cadence

Gunakan trigger-based review sebagai default, ditambah cadence berbasis risiko:

| Kelas | Cadence maksimum yang disarankan | Contoh |
| --- | --- | --- |
| Critical/normative/operational | 3–6 bulan | Policy, security runbook, core engine |
| High-use technical contract | 6 bulan | API, architecture, developer guide |
| Stable reference | 12 bulan | Standard stabil, curated knowledge |
| Historical/evidential | Event-driven | ADR accepted, release note, report |

Owner dapat menetapkan cadence lebih ketat. Dokumen yang melewati due date tidak otomatis salah, tetapi status review overdue harus terlihat dan penggunaan berisiko dinilai.

Trigger review minimum:

- source atau dependency berubah;
- code/interface/workflow/ownership berubah;
- incident, support issue, atau user feedback menunjukkan gap;
- link, example, atau compatibility rusak;
- law, policy, security, atau platform berubah;
- reviewer menemukan konflik, duplikasi, atau ambiguity.

### 7.9 Change History

- Git menyimpan diff lengkap; changelog dokumen hanya ditambahkan bila consumer memerlukan ringkasan versi.
- Catat perubahan material, alasan, impact, migration, approver, dan version/commit.
- Jangan menyalin seluruh Git log ke dokumen.
- Changelog repository mencatat perubahan penting lintas consumer.
- Correction terhadap historical document harus menjaga provenance dan menjelaskan koreksi.

### 7.10 Bahasa dan Format

- Bahasa utama repository adalah Bahasa Indonesia profesional; istilah teknis Inggris digunakan bila lebih presisi.
- Gunakan satu H1, hierarki heading berurutan, kalimat langsung, dan newline akhir.
- Bedakan fakta, keputusan, asumsi, rekomendasi, example, dan status.
- Ikuti [`../../docs/standards/MARKDOWN_CONVENTION.md`](../../docs/standards/MARKDOWN_CONVENTION.md).
- Hindari jargon tanpa definisi, hiperbola, hidden context, dan generated filler.

### 7.11 Security, Privacy, dan Access

- Jangan menulis secret, token, private key, credential, exploit detail sensitif, atau personal data tanpa kebutuhan serta kontrol sah.
- Redact dengan cara yang tetap menjaga evidence berguna.
- Access classification dan publication channel mengikuti least privilege.
- Jika informasi sensitif terlanjur dipublikasikan, ikuti incident handling; menghapus teks saja tidak membatalkan exposure.
- AI tidak boleh memindahkan dokumen private ke channel publik tanpa approval.

## 8. Workflow Dokumentasi

### 8.1 Create

1. Konfirmasi kebutuhan, audience, owner, jenis, scope, dan source.
2. Cari dokumen yang sudah ada untuk mencegah duplikasi.
3. Pilih lokasi kanonik dan nama stabil.
4. Susun metadata serta struktur minimum.
5. Tulis berdasarkan evidence dan tandai unknown/asumsi.
6. Self-review lalu ajukan review sesuai risiko.
7. Setelah approval, publish melalui channel resmi dan perbarui index.

### 8.2 Update

1. Identifikasi trigger dan source of change.
2. Nilai materiality, affected consumer, compatibility, dan approval staleness.
3. Perbarui source kanonik dahulu.
4. Perbarui cross-reference, guide, index, changelog, migration, dan handoff yang terdampak.
5. Jalankan semantic, link, format, security, dan lifecycle review.
6. Kembalikan perubahan material ke Review; jangan mempertahankan label Approved secara otomatis.
7. Komunikasikan perubahan sesuai impact.

### 8.3 Deprecate, Supersede, atau Archive

1. Verifikasi alasan, owner, authority, consumer, dan retention.
2. Sediakan pengganti atau jelaskan gap.
3. Tambahkan status, tanggal, alasan, migration path, dan link dua arah.
4. Hapus dari rekomendasi/index current setelah transisi yang sah.
5. Pertahankan history/audit sesuai security, privacy, legal, dan retention policy.

### 8.4 Documentation Debt

Debt dicatat jika dokumen diketahui incomplete, stale, duplicated, ambiguous, unowned, atau tidak tervalidasi tetapi belum dapat diperbaiki dalam scope. Record minimum:

- lokasi dan masalah;
- dampak/consumer;
- risk level;
- owner atau authority yang dibutuhkan;
- mitigation sementara;
- review date atau exit criteria.

Debt tidak boleh digunakan untuk menutup session sebagai selesai bila dokumentasi tersebut adalah deliverable wajib atau diperlukan untuk penggunaan aman.

## 9. Hubungan Perubahan Kode dan Dokumentasi

Setiap perubahan code/config/schema/API/behavior wajib menjalankan documentation impact assessment.

| Perubahan | Dokumentasi minimum yang ditinjau |
| --- | --- |
| Public behavior atau user flow | Product docs, User Guide, release notes, changelog |
| API/interface/schema | API docs, example, compatibility, migration, changelog |
| Architecture/dependency | Architecture doc dan ADR/Design Decision |
| Setup/build/development | Developer Guide, README, runbook |
| Operations/incident path | Runbook, monitoring, rollback/recovery |
| Security/privacy/permission | Policy, threat/handling guidance, user/admin impact |
| Configuration/default | Reference, example, migration, release notes |
| Internal refactor tanpa behavior change | Verifikasi architecture/developer docs; update hanya bila benar-benar terdampak |
| Governance/workflow | Policy, Standard, Playbook, owner/approval map |
| Prompt/agent behavior | Prompt contract, evaluation, safety, dependency/version |

Aturan:

- dokumentasi yang diperlukan agar perubahan dapat digunakan atau dioperasikan dengan aman adalah bagian dari Definition of Done;
- code dan documentation update berada pada perubahan/release yang sama bila memungkinkan;
- jika publication harus terpisah, tracking item, owner, deadline, mitigation, dan release gate wajib tersedia;
- komentar code menjelaskan intent atau constraint lokal, bukan menggantikan guide atau architecture document;
- test membuktikan behavior, tetapi tidak menggantikan explanation bagi consumer.

## 10. AI Documentation Policy

### 10.1 Kapan AI Wajib Membuat Dokumentasi

AI wajib membuat dokumen baru jika:

- session secara eksplisit meminta artefak dokumentasi baru;
- capability, contract, architecture, policy, standard, decision, runbook, atau guide baru tidak memiliki lokasi kanonik;
- consumer tidak dapat menggunakan atau mengoperasikan perubahan secara aman tanpa dokumentasi;
- keputusan material memerlukan ADR/decision record;
- incident/recovery menghasilkan prosedur atau knowledge reusable yang telah diarahkan ke owner tepat;
- source yang ada tidak dapat diperluas tanpa mencampur authority atau audience yang berbeda.

Sebelum membuat, AI wajib mencari artefak yang sudah ada, menentukan owner/audience, dan memastikan file baru tidak menciptakan SSOT tandingan.

### 10.2 Kapan AI Wajib Memperbarui Dokumentasi

AI wajib memperbarui dokumentasi ketika perubahan dalam scope mengubah:

- behavior, interface, schema, workflow, architecture, dependency, setup, atau operation;
- policy, standard, ownership, approval, status, version, atau lifecycle;
- user/developer instruction, example, error handling, migration, atau compatibility;
- index, navigation, link, terminology, source, atau review metadata;
- technical debt, limitation, known issue, risk, atau recovery path yang perlu diketahui consumer.

AI juga wajib memperbaiki dokumentasi usang yang langsung disebabkan perubahan session. Drift yang ditemukan tetapi berada di luar scope dicatat dan dieskalasikan, bukan diperbaiki diam-diam jika berisiko memperluas objective.

### 10.3 Kapan AI Boleh Mengarsipkan

AI hanya boleh mengarsipkan jika:

- instruksi session atau policy yang sah mengizinkan;
- owner/authority serta retention path jelas;
- dokumen tidak lagi current dan consumer telah dipetakan;
- replacement/migration serta link update tersedia bila relevan;
- audit, legal, security, privacy, dan data retention telah ditinjau;
- operasi reversible atau recovery tersedia.

AI tidak boleh mengarsipkan untuk menyembunyikan konflik, menghapus evidence, menghindari review, atau menyatakan dokumen obsolete hanya berdasarkan asumsi.

### 10.4 Approval dan Batas AI

AI boleh:

- menyusun Draft;
- memperbarui isi sesuai source terverifikasi dan scope;
- melakukan self-review, link check, consistency check, dan cross-review;
- mengusulkan metadata, owner, reviewer, status, dan cadence;
- menyiapkan change summary, migration note, dan review evidence.

AI tidak boleh:

- menetapkan `Approved`, ratified, accepted risk, atau effective tanpa keputusan authority;
- mengarang source, citation, reviewer, approval, date, test result, atau user feedback;
- menyalin content normatif ke banyak lokasi untuk kenyamanan;
- mengubah fakta/keputusan agar konsisten dengan implementasi yang salah;
- mempublikasikan materi sensitif atau memperluas audience tanpa approval;
- meninggalkan placeholder tanpa owner/exit criteria pada deliverable selesai.

### 10.5 Larangan Perubahan Tanpa Dokumentasi

AI dilarang menyelesaikan atau melaporkan perubahan sebagai complete jika dokumentasi yang diperlukan:

- belum dibuat atau diperbarui;
- masih bertentangan dengan code/current state;
- memiliki link/status/source yang diketahui salah;
- diperlukan untuk migration, operation, security, rollback, atau penggunaan aman;
- merupakan deliverable atau acceptance criterion session.

Jika update dokumentasi terblokir, AI wajib menjaga state aman, mencatat blocker, consumer impact, mitigation, owner, dan next action. AI tidak boleh menyamarkan blocker sebagai technical debt ringan.

### 10.6 Workflow AI Minimum

1. Baca brief, source authority, file target, consumer, dan convention.
2. Klasifikasikan jenis dokumen, risiko, status, owner, audience, dan sensitivity.
3. Cari duplikasi serta source kanonik.
4. Susun perubahan terkecil berdasarkan evidence.
5. Cross-review upstream/downstream dan bedakan fakta/asumsi/keputusan.
6. Validasi heading, metadata, terminology, link, scope, security, dan readability.
7. Perbarui index, changelog, handoff, dan report sesuai dampak.
8. Ikuti Git Engine untuk diff, commit, push, dan evidence.
9. Laporkan status aktual tanpa self-approval.

### 10.7 Automatic Stop Conditions

AI menghentikan area dokumentasi terdampak jika:

- source of truth, authority, owner, atau intended audience tidak dapat dipastikan;
- dua source approved bertentangan dan precedence tidak menyelesaikan;
- content memerlukan keputusan strategis/domain yang belum tersedia;
- evidence kritis hilang atau citation tidak dapat diverifikasi;
- perubahan dapat mengekspos secret/data sensitif;
- archive/delete/publication berisiko irreversible atau melanggar retention;
- required review/approval gagal;
- perubahan dokumentasi akan menyesatkan consumer tentang behavior atau status aktual.

## 11. Review dan Quality Gates

### 11.1 Review Semantik

- objective, audience, scope, dan type sesuai;
- fakta, keputusan, asumsi, rekomendasi, dan example dibedakan;
- terminology serta definisi konsisten;
- isi mencerminkan current state dan source;
- instruction dapat dijalankan oleh audience tanpa hidden context;
- limitation, failure path, exception, dan escalation cukup jelas.

### 11.2 Review Authority dan Lifecycle

- status tidak melebihi evidence;
- owner, reviewer, approver, dependency, dan version tepat;
- perubahan material melalui approval path;
- publication channel sesuai classification;
- supersession/archive tidak menghapus audit trail.

### 11.3 Review Teknis

- satu H1 dan heading hierarchy valid;
- internal link relatif dan target tersedia;
- external source credible serta dapat ditelusuri;
- code/example/schema konsisten dengan implementasi;
- tidak ada placeholder rusak, secret, personal data, atau generated filler;
- diff dan staged diff bersih sesuai Git Engine.

### 11.4 Review Usability

- entry point dan navigation jelas;
- prerequisite serta expected outcome dinyatakan;
- example mewakili penggunaan nyata dan tidak menyesatkan;
- troubleshooting atau failure path tersedia bila dibutuhkan;
- bahasa ringkas, dapat dipindai, dan dapat dipahami manusia serta AI.

### 11.5 Gate Publication

Publication hanya lulus jika:

- source, status, version, owner, dan approval valid;
- review semantik, authority, teknis, usability, security, dan privacy lulus;
- index/navigation serta consumer reference diperbarui;
- migration/changelog/release note tersedia jika relevan;
- no known critical documentation drift tersisa.

## 12. Conflict, Failure, dan Recovery

| Kondisi | Tindakan |
| --- | --- |
| Dua SSOT tandingan | Hentikan propagasi, tentukan authority/owner, konsolidasikan melalui review, dan deprecate source lama |
| Dokumentasi tidak cocok dengan code | Jangan memilih salah satu secara asumtif; verifikasi intended behavior, perbaiki source yang salah, dan tambahkan regression evidence |
| Broken link/source hilang | Cari source kanonik; jika tidak ada, tandai gap dan owner, jangan mengarang replacement |
| Approval/status palsu | Turunkan ke status berdasarkan evidence, preservasi histori, beri tahu owner/consumer, dan review impact |
| Informasi sensitif terpublikasi | Batasi exposure, ikuti incident response, revoke/rotate secret bila ada, lalu lakukan remediation histori terotorisasi |
| Dokumen usang dipakai operasional | Hentikan penggunaan berisiko, identifikasi consumer, pulihkan panduan current, dan catat incident/lesson |
| Archive/delete salah | Pulihkan dari version control/backup jika sah, perbaiki index, dan review retention/authority |
| AI menghasilkan citation/claim palsu | Hapus atau koreksi klaim berdasarkan evidence, laporkan failure, dan lakukan review lebih luas pada output terkait |

Recovery mengikuti [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md): detect, stop propagation, preserve evidence, assess impact, stabilize, recover incrementally, revalidate, communicate, dan record learning.

## 13. Cross-System Alignment

| Sumber | Implementasi dalam Documentation Engine | Boundary |
| --- | --- | --- |
| [`CONSTITUTION.md`](CONSTITUTION.md) | Repository First, Documentation First, Truth over Assumption, human oversight, traceability, transparency, dan quality | Engine tidak meratifikasi Constitution atau menciptakan Founder decision |
| [`DEVELOPER_MODE_ENGINE.md`](DEVELOPER_MODE_ENGINE.md) | Documentation First, Read Before Write, Continuous Documentation, repository consistency, validation, dan reporting | Documentation Engine merinci standard tanpa memperluas otonomi AI |
| [`SESSION_ENGINE.md`](SESSION_ENGINE.md) | Documentation Update, continuity package, Session Report, handoff, closure, dan archive trigger | Session Engine mengorkestrasi kapan dokumentasi diperbarui; engine ini tetap sumber detail dokumentasi |
| [`EXECUTION_ENGINE.md`](EXECUTION_ENGINE.md) | Documentation task classification, Update Documentation, Documentation Check, evidence, failure/recovery, dan DoD | Execution Engine tetap sumber prosedur eksekusi; engine ini sumber detail dokumentasi |
| [`GIT_ENGINE.md`](GIT_ENGINE.md) | Versioned documentation, atomic diff, review, commit, audit, release, dan recovery | Git event tidak menjadi approval dokumentasi |
| [`QUALITY_ENGINE.md`](QUALITY_ENGINE.md) | Documentation Completeness, Documentation Review gate, DoD, metrics, audit, finding, CAPA, dan AI Quality Policy | Quality Engine menilai kualitas lintas artefak; Documentation Engine tetap sumber detail dokumentasi |
| [`../../01-foundation/FOUNDATION_ARCHITECTURE.md`](../../01-foundation/FOUNDATION_ARCHITECTURE.md) | SSOT, derived-not-duplicated, owner, lifecycle, evidence flow, dan feedback | Engine tidak mengambil ownership Foundation/domain |
| [`../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) | provenance, metadata, verification, knowledge lifecycle, deprecation, archive, dan cross-reference | Knowledge-specific confidence/verification tetap dimiliki Knowledge Governance |
| [`GOVERNANCE_ENGINE.md`](GOVERNANCE_ENGINE.md) | documentation ownership, delegation, approval, publication/archive authority, exception, escalation, lifecycle, dan audit | Documentation Engine tetap sumber detail dokumentasi |
| [`SPOS_ARCHITECTURE.md`](SPOS_ARCHITECTURE.md) | modular contract, traceability, lifecycle, bounded execution, report, dan feedback | Engine adalah kontrak dokumentasi, bukan runtime/CMS |
| [`../../docs/standards/DOCUMENTATION_CONVENTION.md`](../../docs/standards/DOCUMENTATION_CONVENTION.md) | Profil ringkas lifecycle dan bentuk dokumentasi repository | Convention tunduk pada engine dan tidak menjadi policy tandingan |
| [`../../docs/standards/MARKDOWN_CONVENTION.md`](../../docs/standards/MARKDOWN_CONVENTION.md) | Bentuk Markdown, link, bahasa, dan formatting | Markdown Convention mengatur syntax/style, bukan authority isi |

### 13.1 Resolusi Cross-Review SPOS-006

- Lifecycle brief `Draft → Review → Approved → Published → Updated → Archived` ditetapkan sebagai lifecycle kanonik; status repository `In Review`, `Deprecated`, dan `Superseded` dipetakan tanpa menghapus semantics yang sudah ada.
- Documentation Engine menjadi SSOT policy lintas ekosistem; `DOCUMENTATION_CONVENTION.md` tetap profil repository dan harus merujuk engine.
- Knowledge Governance tetap memiliki aturan khusus provenance, confidence, verification, dan curation Knowledge System; engine tidak menduplikasi authority domain tersebut.
- Execution Engine tetap memiliki tahap `Update Documentation` serta Documentation Check; detail standard didelegasikan ke Documentation Engine.
- Git Engine tetap memiliki version control dan audit history; commit/publication tidak diartikan sebagai approval.
- Governance Engine SPOS-008 menetapkan policy ownership/approval; sampai activation dan delegation aktual tersedia, ownership, approval, archive, dan publication yang ambigu tetap fail-closed.
- Handoff SPOS-005 merekomendasikan Governance Engine, tetapi brief SPOS-006 menetapkan Documentation Engine; deviasi historis dipertahankan, dan Governance Engine kemudian dibangun melalui SPOS-008.

## 14. Activation dan Change Control

Aktivasi sebagai standard binding memerlukan:

- Constitution dengan status operasional sah atau keputusan Founder yang secara eksplisit mengizinkan baseline sementara;
- Developer Mode, Execution Engine, dan Git Engine yang kompatibel;
- review Governance, Documentation owner, Knowledge Steward, repository maintainer, dan domain owner relevan;
- approval eksplisit, version, effective date, scope, dan audit trail;
- penyelarasan Documentation Convention serta consumer AI tanpa membuat salinan rule;
- mekanisme ownership, review trigger/cadence, dan publication yang dapat diverifikasi.

Activation record:

- Approver: `<authorized human>`
- Decision: `<approved / rejected / revision required>`
- Effective date: `<YYYY-MM-DD>`
- Version approved: `<version>`
- Constitution dependency: `<version and status>`
- Developer Mode dependency: `<version and status>`
- Execution Engine dependency: `<version and status>`
- Git Engine dependency: `<version and status>`
- Governance/Documentation decision: `<relative-link>`
- Consumer migration evidence: `<reference>`
- Commit hash: `<hash>`

AI tidak boleh mengisi field approval atas nama manusia. Perubahan material pada lifecycle, metadata, approval, archive, publication, AI authority, atau type definition memerlukan impact analysis, versioning, changelog, review, migration, dan approval sesuai authority.

## 15. Documentation Engine Review Checklist

- [x] Documentation First, SSOT, Living, Versioned, Traceable, Human/AI Readable, Consistency, Evidence, dan Explicitness terdokumentasi.
- [x] Architecture, Design Decision, ADR, API, Product, Knowledge, Governance, Prompt, Playbook, Standard, Policy, Runbook, User Guide, Developer Guide, Changelog, dan Release Notes didefinisikan.
- [x] Lifecycle Draft, Review, Approved, Published, Updated, dan Archived beserta aturan transisinya terdokumentasi.
- [x] Struktur, naming, metadata, versioning, cross-reference, internal link, ownership, review cadence, dan change history terdokumentasi.
- [x] AI create/update/archive policy, code-documentation relationship, approval boundary, stop condition, dan prohibition on undocumented change terdokumentasi.
- [x] Validation, publication gate, documentation debt, security/privacy, failure, dan recovery terdokumentasi.
- [x] Alignment dengan Constitution, Governance Engine, Developer Mode, Session Engine, Execution Engine, Git Engine, Quality Engine, Foundation, Knowledge System, SPOS Architecture, dan repository standards dipetakan.
- [x] Scope tidak membangun aplikasi, fitur produk, CMS, portal, deployment, atau automation runtime.
- [ ] Constitution diratifikasi atau baseline interim diizinkan secara eksplisit.
- [ ] Developer Mode, Session Engine, Execution Engine, Git Engine, dan Documentation Engine memperoleh approval operasional serta activation record.
- [ ] Governance Engine memperoleh approval/activation; Documentation Steward delegation, ownership registry, dan publication controls diterapkan serta diverifikasi.
- [ ] Consumer migration, review cadence operation, publication controls, dan conformance automation diterapkan serta diverifikasi.
