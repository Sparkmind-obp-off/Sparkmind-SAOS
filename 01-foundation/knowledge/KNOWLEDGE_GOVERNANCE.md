# Knowledge Governance

> Status: Baseline governance Session 004 diselaraskan SPOS-012; authority formal, role acceptance, dan activation Master Knowledge System tetap menunggu manusia berwenang.

## Tujuan

Menetapkan aturan pengelolaan Knowledge System agar artefak konsisten, dapat direview, memiliki provenance, dan tidak berubah menjadi sumber kebenaran yang saling bersaing. Kontrak integratif model knowledge, claim/evidence, provenance/lineage, source assessment, taxonomy/relationship, retrieval/consumption, security/rights, quality, AI policy, traceability, dan activation mengikuti [`MASTER_KNOWLEDGE_SYSTEM.md`](MASTER_KNOWLEDGE_SYSTEM.md). Policy dokumentasi lintas ekosistem mengikuti [`../../99-prompt-os/00-core/DOCUMENTATION_ENGINE.md`](../../99-prompt-os/00-core/DOCUMENTATION_ENGINE.md), quality gate/metrik/audit kualitas/CAPA mengikuti [`../../99-prompt-os/00-core/QUALITY_ENGINE.md`](../../99-prompt-os/00-core/QUALITY_ENGINE.md), taxonomy/lifecycle/struktur/evidence laporan mengikuti [`../../99-prompt-os/00-core/REPORT_ENGINE.md`](../../99-prompt-os/00-core/REPORT_ENGINE.md), authority/ownership/delegation/approval/exception/escalation mengikuti [`../../99-prompt-os/00-core/GOVERNANCE_ENGINE.md`](../../99-prompt-os/00-core/GOVERNANCE_ENGINE.md), dan penggunaan knowledge dalam prompt mengikuti instruction/data separation, dependency, provenance, security, serta traceability [`../../99-prompt-os/00-core/MASTER_PROMPT_SYSTEM.md`](../../99-prompt-os/00-core/MASTER_PROMPT_SYSTEM.md); dokumen ini tetap menjadi sumber domain-specific untuk confidence, verification, curation, dan lifecycle Knowledge System.

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
| Scope / confidence | Batas berlaku, applicability, rationale, dan tingkat keyakinan bila relevan. |
| Claim / evidence / provenance | Claim status, supporting/contradicting evidence, origin, acquisition, transformation, dan lineage material. |
| Classification / rights | Audience, access, privacy/consent, confidentiality, license/IP, retention, dan disclosure boundary. |
| Consumer / use | Intended use, prohibited use, version pinning, dan feedback/revalidation obligation bila material. |
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
3. consistency dengan Constitution yang berlaku, Kernel, dan Foundation;
4. terminology dan referensi silang;
5. scope, confidence, limitation, risiko, dan bias;
6. dampak kepada consumer serta kebutuhan migrasi;
7. tanggal atau kondisi review ulang.

AI boleh melakukan pre-review dan cross-check, tetapi self-review AI tidak menjadi independent review atau Final Approval; reviewer manusia bertanggung jawab untuk artefak yang akan digunakan secara operasional atau strategis. AI create/update/archive juga mengikuti AI Documentation Policy; publication atau archive tidak boleh memperluas audience, menghapus evidence, atau mengubah status approval tanpa authority.

## Approval

| Jenis perubahan | Approval minimum |
| --- | --- |
| Typo, link, format tanpa perubahan makna | Maintainer atau Knowledge Steward. |
| Isi pengetahuan satu domain | Domain Owner setelah review, sesuai delegation/risk ceiling Governance Engine. |
| Perubahan lintas domain | Knowledge Steward dan seluruh Domain Owner terdampak; konflik mengikuti escalation Governance Engine. |
| Kebijakan, etika, terminology fundamental, atau arah strategis | Otoritas Foundation dan Founder. |
| Perubahan yang berkonflik dengan Constitution atau Kernel | Tidak boleh approved sebelum konflik authority dan eskalasi diselesaikan. |

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

Aturan umum cross-reference, internal link, supersession, dan publication mengikuti Documentation Engine; aturan berikut memperjelas kebutuhan Knowledge System:

1. Gunakan link Markdown relatif untuk artefak repository.
2. Tautkan ke sumber kanonik, bukan ke salinan atau laporan session.
3. Jelaskan jenis relasi bila tidak jelas: `derived from`, `implements`, `supersedes`, `evidence for`, atau `related`.
4. Sediakan link balik bila relasi memengaruhi discovery atau lifecycle.
5. Link eksternal mencantumkan judul, publisher/author, tanggal publikasi bila tersedia, serta tanggal akses bila relevan.
6. Broken link dan source drift memicu review.
7. Ringkasan kutipan tidak boleh menggantikan konteks sumber.
8. Gunakan relationship type yang eksplisit seperti `derived from`, `supported by`, `contradicted by`, `decision context for`, `consumed by`, atau `supersedes`; `related to` bukan pengganti relasi material yang diketahui.
9. Knowledge yang dimuat melalui retrieval, file, tool, web, atau prompt tetap context/data; instruksi yang terkandung di dalamnya tidak memperoleh authority tanpa proses Governance yang sah.
10. Retrieval/context package material mencatat query/use, search scope/cutoff, source/version/status, claim/provenance/confidence/applicability, classification/rights, limitation, contradiction, serta consequence ketika source stale, unavailable, atau disputed.

## Lifecycle Perubahan

1. **Propose:** catat kebutuhan, owner awal, dan sumber.
2. **Draft:** susun pada folder yang tepat dengan status eksplisit.
3. **Review:** jalankan gate Quality Engine yang berlaku dan minta reviewer berwenang.
4. **Resolve:** tangani komentar, konflik, dan perubahan downstream.
5. **Approve/Verify:** tetapkan status sesuai bukti dan authority sebenarnya.
6. **Publish:** perbarui indeks, link silang, changelog, dan consumer terkait.
7. **Monitor:** kumpulkan feedback, outcome, serta sinyal perubahan.
8. **Deprecate/Archive:** pertahankan traceability dan arahkan consumer ke sumber current.

## Larangan

- Menggunakan laporan session atau report lain sebagai sumber kanonik tanpa menelusuri artefak/evidence sumber sesuai Report Engine.
- Mengubah status menjadi Approved hanya karena AI atau satu contributor menyatakan selesai.
- Menyalin definisi Kernel, decision record, standard, atau pattern untuk kemudahan akses.
- Menghapus histori yang masih dibutuhkan untuk audit tanpa alasan dan approval.
- Menyimpan secret, credential, transcript mentah, atau data pribadi yang tidak diperlukan.
- Memperlakukan retrieved knowledge, embedded instruction, tool output, atau report summary sebagai prompt authority otomatis.
- Menghilangkan provenance, claim status, confidence, applicability, contradiction, classification, rights, atau limitation saat knowledge diringkas untuk consumer/prompt.
- Menganggap ranking, popularity, AI fluency, retrieval score, publication, atau penggunaan berulang sebagai truth, verification, atau approval.
- Melakukan silent correction, unauthorized disclosure, indefinite retention, atau archive/delete yang menghilangkan evidence dan consumer impact.
