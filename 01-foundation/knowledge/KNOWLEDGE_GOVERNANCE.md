# Knowledge Governance

> Status: Baseline governance Session 004; otoritas formal menunggu penetapan Governance Foundation dan Founder.

## Tujuan

Menetapkan aturan pengelolaan Knowledge System agar artefak konsisten, dapat direview, memiliki provenance, dan tidak berubah menjadi sumber kebenaran yang saling bersaing.

## Naming

- Folder menggunakan `lowercase-kebab-case`.
- File kanonik menggunakan `UPPER_SNAKE_CASE.md`; indeks folder selalu `README.md`.
- Nama harus menggambarkan topik stabil, bukan status sementara seperti `final`, `latest`, atau `v2`.
- Gunakan istilah yang telah didefinisikan. Istilah kandidat diberi label draft dan dirujuk ke owner Terminology.
- Indeks berurutan, bila benar-benar diperlukan, menggunakan ID stabil yang didefinisikan owner domain; nomor tidak boleh menyiratkan approval.

Aturan umum mengikuti [`../../docs/standards/NAMING_CONVENTION.md`](../../docs/standards/NAMING_CONVENTION.md).

## Metadata Minimum

Artefak substantif mencantumkan metadata berikut dekat judul atau dalam bagian khusus:

| Field | Keterangan |
| --- | --- |
| Status | Proposed, Draft, In Review, Verified, Approved, Deprecated, Superseded, atau Archived. |
| Owner | Pihak yang bertanggung jawab atas akurasi dan pemeliharaan. |
| Reviewer | Pihak yang memeriksa evidence, consistency, dan risiko. |
| Approver | Wajib bila status Approved atau dampaknya strategis. |
| Last reviewed | Tanggal ISO 8601 review terakhir. |
| Review trigger | Tanggal, perubahan upstream, insiden, atau kondisi lain. |
| Sources | Link ke evidence atau sumber kanonik. |
| Scope / confidence | Batas berlaku dan tingkat keyakinan bila relevan. |
| Supersedes / superseded by | Relasi lifecycle jika ada. |

README indeks dapat menggunakan metadata ringkas selama status koleksinya tidak ambigu.

## Versioning

- Histori utama disimpan melalui Git; jangan membuat file `final-v2` atau salinan backup.
- Dokumen mengikuti versi repository secara default.
- Versi independen hanya digunakan untuk kontrak formal yang memiliki owner dan proses approval.
- Perubahan editorial tidak menaikkan versi dokumen independen kecuali kontraknya menentukan lain.
- Perubahan makna wajib dicatat di commit dan, bila material, di `CHANGELOG.md`.
- Status lifecycle bukan nomor versi dan tidak berubah otomatis karena commit atau tag.

Aturan lengkap mengikuti [`../../docs/standards/VERSIONING_CONVENTION.md`](../../docs/standards/VERSIONING_CONVENTION.md).

## Review

Setiap review menilai:

1. kecukupan dan kredibilitas sumber;
2. pemisahan fakta, interpretasi, asumsi, dan rekomendasi;
3. consistency dengan Kernel dan Foundation;
4. terminology dan referensi silang;
5. scope, confidence, limitation, risiko, dan bias;
6. dampak kepada consumer serta kebutuhan migrasi;
7. tanggal atau kondisi review ulang.

AI boleh melakukan pre-review dan cross-check, tetapi reviewer manusia bertanggung jawab untuk artefak yang akan digunakan secara operasional atau strategis.

## Approval

| Jenis perubahan | Approval minimum |
| --- | --- |
| Typo, link, format tanpa perubahan makna | Maintainer atau Knowledge Steward. |
| Isi pengetahuan satu domain | Domain Owner setelah review. |
| Perubahan lintas domain | Knowledge Steward dan seluruh Domain Owner terdampak. |
| Kebijakan, etika, terminology fundamental, atau arah strategis | Otoritas Foundation dan Founder. |
| Perubahan yang berkonflik dengan Kernel | Tidak boleh approved sebelum eskalasi diselesaikan. |

`Verified` berarti sumber telah diperiksa; `Approved` berarti artefak boleh menjadi referensi operasional dalam scope yang dinyatakan. Keduanya tidak boleh disamakan.

## Deprecation dan Supersession

Artefak dideprecate ketika sumber usang, konteks tidak lagi berlaku, ada pengganti, atau risiko penggunaan baru terlalu tinggi.

Dokumen deprecated wajib:

- mempertahankan histori;
- menyatakan alasan dan tanggal;
- mengarahkan ke pengganti atau menjelaskan ketiadaannya;
- mencatat dampak dan masa transisi bila relevan;
- tidak lagi muncul sebagai rekomendasi default pada learning atau onboarding.

Artefak superseded tetap dapat diakses untuk audit dan harus memiliki link dua arah dengan penggantinya.

## Archiving

- Archive digunakan untuk histori, audit, atau kewajiban retensi; bukan untuk menyembunyikan konflik yang belum selesai.
- Lokasi archive ditetapkan saat kebutuhan nyata muncul; Session 004 tidak membuat folder placeholder.
- Artefak archived bersifat read-only kecuali koreksi metadata atau keamanan.
- Link aktif harus mengarah ke artefak current, bukan archived.
- Secret, data pribadi, dan materi berlisensi tidak dipertahankan hanya karena alasan histori.

## Referensi Silang

1. Gunakan link Markdown relatif untuk artefak repository.
2. Tautkan ke sumber kanonik, bukan ke salinan atau laporan session.
3. Jelaskan jenis relasi bila tidak jelas: `derived from`, `implements`, `supersedes`, `evidence for`, atau `related`.
4. Sediakan link balik bila relasi memengaruhi discovery atau lifecycle.
5. Link eksternal mencantumkan judul, publisher/author, tanggal publikasi bila tersedia, serta tanggal akses bila relevan.
6. Broken link dan source drift memicu review.
7. Ringkasan kutipan tidak boleh menggantikan konteks sumber.

## Lifecycle Perubahan

1. **Propose:** catat kebutuhan, owner awal, dan sumber.
2. **Draft:** susun pada folder yang tepat dengan status eksplisit.
3. **Review:** jalankan quality gate dan minta reviewer berwenang.
4. **Resolve:** tangani komentar, konflik, dan perubahan downstream.
5. **Approve/Verify:** tetapkan status sesuai bukti dan authority sebenarnya.
6. **Publish:** perbarui indeks, link silang, changelog, dan consumer terkait.
7. **Monitor:** kumpulkan feedback, outcome, serta sinyal perubahan.
8. **Deprecate/Archive:** pertahankan traceability dan arahkan consumer ke sumber current.

## Larangan

- Menggunakan laporan session sebagai sumber kanonik.
- Mengubah status menjadi Approved hanya karena AI atau satu contributor menyatakan selesai.
- Menyalin definisi Kernel, decision record, standard, atau pattern untuk kemudahan akses.
- Menghapus histori yang masih dibutuhkan untuk audit tanpa alasan dan approval.
- Menyimpan secret, credential, transcript mentah, atau data pribadi yang tidak diperlukan.
