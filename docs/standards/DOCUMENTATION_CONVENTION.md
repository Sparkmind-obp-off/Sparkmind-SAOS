# Documentation Convention

> Status: Repository profile SPOS-006 — policy lintas ekosistem berada di Documentation Engine `In Review`.

## Tujuan

Menetapkan bentuk ringkas dokumentasi pada repository SparkMind SAOS agar setiap dokumen memiliki fungsi, status, sumber, owner, dan jalur review yang dapat ditelusuri. Policy kanonik jenis, lifecycle, metadata, publication, archive, code-documentation relationship, dan AI Documentation Policy berada di [`../../99-prompt-os/00-core/DOCUMENTATION_ENGINE.md`](../../99-prompt-os/00-core/DOCUMENTATION_ENGINE.md).

Convention ini mengatur profile repository dan tidak boleh melemahkan authority atau gate Documentation Engine. Untuk artefak Knowledge System, gunakan juga [`../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md).

## Prinsip

- **Documentation First:** pahami dan dokumentasikan intent, constraint, keputusan, serta impact secara proporsional.
- **Single Source of Truth:** satu aturan atau definisi memiliki satu sumber kanonik.
- **Living and Versioned:** dokumentasi dipelihara bersama subject-nya dan histori disimpan melalui Git.
- **Traceable:** klaim serta keputusan penting memiliki source, owner, review, dan histori.
- **Human and AI Readable:** struktur, metadata, status, dan istilah eksplisit.
- **Evidence Before Assumption:** fakta diverifikasi; asumsi diberi label.
- **Consistency:** convention repository mengalahkan preferensi personal.
- **Human Oversight:** AI dapat menyusun dan meninjau, tetapi tidak mengesahkan keputusan strategis.
- **Proportionality:** kedalaman dokumen sebanding dengan risiko, longevity, dan kebutuhan consumer.

## Jenis Dokumen

Gunakan taxonomy pada Documentation Engine:

- Architecture, Design Decision, dan Architecture Decision Record (ADR);
- API dan Product;
- Knowledge dan Governance;
- Prompt, Playbook, Standard, dan Policy;
- Runbook, User Guide, dan Developer Guide;
- Changelog dan Release Notes.

README adalah entry point/index, bukan tempat menumpuk seluruh jenis konten. Pilih jenis berdasarkan audience, outcome, authority, dan lifecycle.

## Lifecycle

Lifecycle kanonik:

```text
Draft → Review → Approved → Published → Updated → Archived
```

Mapping status repository:

- **Draft:** sedang disusun; belum berlaku.
- **In Review:** tahap Review; siap diperiksa reviewer yang berwenang.
- **Approved:** disetujui authority untuk scope dan versi tertentu.
- **Published:** approved dan tersedia melalui channel resmi.
- **Updated:** event perubahan; perubahan material kembali ke Draft/Review.
- **Deprecated:** masih tersedia untuk transisi, bukan penggunaan baru.
- **Superseded:** digantikan dokumen/version kanonik lain.
- **Archived:** dipertahankan hanya untuk histori, audit, atau retention.

Commit, merge, publication, atau penggunaan berulang tidak sama dengan approval. Status ditulis dekat judul bila belum approved atau jika pembaca dapat salah menganggapnya berlaku. Detail transition gate mengikuti Documentation Engine.

## Struktur Minimum

Dokumen baru, bila relevan, memuat:

1. judul;
2. metadata status dan ownership;
3. tujuan serta audience;
4. scope dan non-scope;
5. source/dependency;
6. isi utama atau keputusan;
7. limitation, risk, exception, atau escalation;
8. referensi;
9. review/validation checklist.

Tidak semua bagian wajib jika tidak menambah nilai. Jangan mengisi heading dengan filler hanya untuk memenuhi template.

## Metadata

Dokumen substantif mencantumkan secara proporsional:

- status;
- owner;
- reviewer dan approver bila berlaku;
- version bila memiliki contract independen;
- established/last-reviewed/effective/expiry date;
- review trigger atau cadence;
- audience, scope, source/dependency, dan classification;
- supersedes/superseded-by bila ada.

Field approval tidak boleh diisi AI atas nama manusia. Placeholder hanya diperbolehkan pada draft jika owner dan exit criteria jelas.

## Sumber dan Keputusan

- Kutipan atau keputusan Founder dibedakan dari interpretasi AI.
- Klaim eksternal memiliki source yang dapat diverifikasi.
- Fakta, keputusan, asumsi, rekomendasi, dan example dibedakan.
- Perubahan normatif menjelaskan alasan, impact, reviewer, dan approval.
- Laporan session tidak menjadi sumber kanonik; hasil penting diterapkan ke dokumen yang tepat.
- Gunakan source kanonik, bukan salinan ringkasan yang dapat drift.

## Ownership dan Review

Sebelum publication, tentukan:

- owner dokumen;
- reviewer/approver sesuai jenis dan risiko;
- consumer serta pihak terdampak;
- cadence dan trigger review;
- lifecycle serta escalation path.

Dokumen Kernel yang belum memiliki owner formal menunggu persetujuan Founder. Artefak Foundation merujuk sumber Kernel dan tidak mengubah statusnya melalui interpretasi downstream. Knowledge mengikuti Knowledge Governance untuk provenance, confidence, verification, curation, dan lifecycle domain.

Cadence berbasis risiko mengikuti Documentation Engine: 3–6 bulan untuk critical/normative/operational, 6 bulan untuk high-use technical contract, 12 bulan untuk stable reference, dan event-driven untuk historical/evidential artefact, kecuali owner menetapkan cadence lebih ketat.

## Cross-Reference dan Link

- Gunakan link Markdown relatif untuk file repository.
- Tautkan sumber kanonik dan jelaskan relasi jika tidak jelas.
- Sediakan link dua arah untuk supersession dan dependency material.
- Perbarui inbound/outbound link setelah rename, move, deprecation, atau archive.
- README/index mengarah ke source current, bukan archived.
- Broken link yang dibutuhkan untuk penggunaan benar memblokir publication.

## Versioning dan Change History

- Git adalah histori default; jangan membuat file `final-v2` atau backup manual.
- Versi independen hanya untuk contract formal dengan compatibility serta approval path.
- Status lifecycle tidak sama dengan versi.
- Perubahan makna material dicatat pada commit dan `CHANGELOG.md` bila berdampak lintas consumer.
- Changelog dokumen ditambahkan hanya jika consumer memerlukan ringkasan versi; jangan menyalin seluruh Git log.

## Hubungan Code dan Dokumentasi

Setiap perubahan code, config, schema, API, behavior, architecture, setup, operations, security, atau prompt menjalankan documentation impact assessment. Dokumentasi yang dibutuhkan untuk penggunaan, migration, operasi, security, dan rollback aman merupakan bagian Definition of Done.

Perbarui source kanonik dan consumer dalam perubahan/release yang sama bila memungkinkan. Jika publication terpisah, sediakan tracking item, owner, deadline, mitigation, dan release gate.

## AI Documentation Policy Ringkas

AI wajib:

- mencari sebelum membuat dan memilih lokasi kanonik;
- membuat/memperbarui dokumentasi ketika deliverable atau perubahan consumer memerlukannya;
- membedakan source, fakta, asumsi, keputusan, dan approval;
- memperbarui index, link, changelog, handoff, dan report sesuai impact;
- menghentikan perubahan jika authority, source, sensitivity, archive, atau publication path kritis ambigu.

AI hanya boleh mengarsipkan jika authority, retention, migration, access, dan recovery jelas. AI tidak boleh self-approve, mengarang citation/evidence, membuka materi sensitif, atau menyatakan perubahan complete sementara dokumentasi wajib belum sinkron.

## Pemeliharaan

Perbarui dokumentasi ketika:

- behavior, structure, interface, workflow, atau policy berubah;
- source, ownership, status, version, atau dependency berubah;
- link, example, atau reference usang;
- konflik atau duplikasi ditemukan;
- dokumen dideprecate, superseded, atau archived;
- incident atau feedback menunjukkan guidance tidak memadai.

Gunakan Git untuk histori. Archive mengikuti authority, retention, security/privacy, dan consumer migration; archive tidak digunakan untuk menyembunyikan konflik atau menghapus evidence.

## Checklist

- [ ] Tujuan, audience, scope, dan jenis jelas.
- [ ] Status sesuai evidence serta lifecycle.
- [ ] Source dan keputusan dapat ditelusuri.
- [ ] Owner, reviewer, approver, serta cadence dapat diidentifikasi.
- [ ] Tidak menduplikasi sumber kanonik.
- [ ] Fakta, asumsi, keputusan, dan rekomendasi dibedakan.
- [ ] Link internal relatif dan valid.
- [ ] Perubahan code/consumer dan dokumentasi sinkron.
- [ ] Tidak ada secret, data sensitif, atau placeholder rusak.
- [ ] Publication/archive mengikuti authority dan retention.
