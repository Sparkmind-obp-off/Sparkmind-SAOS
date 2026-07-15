# Versioning Convention

## Tujuan

Menetapkan cara memberi versi pada repository dan dokumen tanpa menciptakan klaim stabilitas atau persetujuan yang menyesatkan.

## Versioning Repository

Gunakan Semantic Versioning (SemVer):

```text
MAJOR.MINOR.PATCH
```

- **MAJOR:** perubahan tidak kompatibel pada struktur, kontrak, atau sumber normatif yang telah approved.
- **MINOR:** penambahan layer, kapabilitas, atau dokumen kanonik yang kompatibel.
- **PATCH:** koreksi, klarifikasi, atau perbaikan yang tidak mengubah kontrak utama.

Selama Foundation dan dokumen inti belum approved, gunakan versi `0.y.z`. Versi `1.0.0` hanya dapat ditetapkan setelah baseline yang jelas disetujui oleh otoritas yang tepat.

## Tag Git

- Gunakan annotated tag dengan prefix `v`, misalnya `v0.1.0`.
- Tag hanya dibuat pada commit yang telah direview dan konsisten.
- Tag yang sudah dipublikasikan tidak dipindahkan atau ditimpa.
- Kesalahan pada rilis ditangani dengan versi baru, bukan rewrite histori.

## Versioning Dokumen

Secara default, dokumen mengikuti versi repository dan histori Git. Jangan menambahkan nomor versi pada nama file.

Metadata versi per dokumen hanya digunakan jika dokumen:

- memiliki lifecycle rilis independen;
- dirujuk sebagai kontrak atau kebijakan formal;
- memiliki owner dan proses approval yang jelas.

Jika digunakan, metadata minimum mencakup status, versi, tanggal berlaku, owner, approver, dan dokumen yang digantikan.

## Status Bukan Versi

`Draft`, `In Review`, `Approved`, `Deprecated`, dan `Superseded` adalah status lifecycle, bukan nomor versi. Peningkatan versi tidak otomatis mengubah status menjadi approved.

## Changelog

- Catat perubahan penting pada `CHANGELOG.md` di bagian `Unreleased`.
- Pindahkan entri ke versi bertanggal saat rilis benar-benar dibuat.
- Gunakan tanggal ISO 8601 `YYYY-MM-DD`.
- Kelompokkan entri dengan kategori yang jelas seperti Added, Changed, Fixed, Deprecated, Removed, atau Security.
- Jangan mencatat setiap typo jika tidak berdampak pada pengguna repository.

## Versi Foundation Saat Ini

Baseline Kernel Session 001 didokumentasikan sebagai `0.1.0` pada changelog. Pencatatan tersebut tidak dengan sendirinya berarti tag atau release GitHub telah diterbitkan. Status rilis harus diverifikasi terhadap Git sebelum diumumkan.

## Persetujuan

Perubahan MAJOR atau versi `1.0.0` memerlukan:

- baseline dan scope yang terdokumentasi;
- review konsistensi seluruh sumber kanonik;
- persetujuan Founder untuk materi strategis;
- changelog dan release note yang akurat.

## Checklist

- [ ] Nomor versi sesuai dampak perubahan.
- [ ] Status dokumen tidak disamakan dengan versi.
- [ ] Changelog sesuai dengan commit yang dirilis.
- [ ] Tag menunjuk commit yang benar dan tidak dipindahkan.
- [ ] Approval strategis tersedia bila diperlukan.
