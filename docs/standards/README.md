# Repository Standards

## Tujuan

Folder ini menjadi sumber kanonik untuk standar pengelolaan repository SparkMind SAOS. Standar di sini mengatur bentuk dan workflow repository, bukan menetapkan Vision, Mission, nilai, arsitektur produk, atau implementasi teknis.

## Standar Aktif

| Dokumen | Cakupan |
| --- | --- |
| [`NAMING_CONVENTION.md`](NAMING_CONVENTION.md) | Penamaan file, folder, branch, tag, dan istilah |
| [`FOLDER_CONVENTION.md`](FOLDER_CONVENTION.md) | Struktur, fungsi, dan aturan penambahan folder |
| [`MARKDOWN_CONVENTION.md`](MARKDOWN_CONVENTION.md) | Format dan gaya Markdown |
| [`DOCUMENTATION_CONVENTION.md`](DOCUMENTATION_CONVENTION.md) | Lifecycle, status, ownership, dan review dokumen |
| [`COMMIT_CONVENTION.md`](COMMIT_CONVENTION.md) | Conventional Commits dan kualitas commit |
| [`BRANCH_CONVENTION.md`](BRANCH_CONVENTION.md) | Nama, lifecycle, proteksi, dan integrasi branch |
| [`VERSIONING_CONVENTION.md`](VERSIONING_CONVENTION.md) | Versi repository, dokumen, changelog, dan tag |

## Prioritas Aturan

Jika ditemukan konflik:

1. Hukum, kewajiban keselamatan, dan instruksi Founder yang terdokumentasi serta berlaku.
2. Constitution SPOS yang telah diratifikasi, untuk pekerjaan di dalam SPOS.
3. Dokumen Kernel approved sebagai source material fundamental sesuai kedudukan dan scope-nya.
4. Governance dan policy approved yang berlaku.
5. Kebijakan root seperti `SECURITY.md`, `LICENSE`, dan `CODE_OF_CONDUCT.md`.
6. Standar khusus pada folder ini.
7. Preferensi gaya lokal yang terdokumentasi.

Hanya artefak dengan status dan approval yang sah memiliki authority operasional. Konflik tidak boleh diselesaikan secara diam-diam; catat sumber, status, serta scope-nya dan eskalasikan bila memengaruhi makna normatif atau hak pihak lain.

## Cara Mengubah Standar

1. Jelaskan masalah dan tujuan perubahan.
2. Identifikasi dokumen serta kontributor yang terdampak.
3. Perbarui satu sumber kanonik dan semua referensi silang terkait.
4. Catat perubahan penting pada `CHANGELOG.md`.
5. Lakukan review konsistensi dan link.
6. Gunakan commit `docs(standards): ...` atau tipe lain yang paling akurat.

Perubahan standar repository tidak boleh digunakan untuk menyisipkan keputusan strategis yang seharusnya berada di Kernel atau memerlukan persetujuan Founder.
