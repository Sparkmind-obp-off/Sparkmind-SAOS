# Contributing to SparkMind SAOS

## Tujuan

Pedoman ini memastikan setiap kontribusi terhadap SparkMind SAOS dapat dipahami, direview, ditelusuri, dan tetap selaras dengan repository sebagai Single Source of Truth (SSOT).

## Sebelum Berkontribusi

1. Baca [`README.md`](README.md), [`00-kernel/README.md`](00-kernel/README.md), dan [`01-foundation/README.md`](01-foundation/README.md).
2. Periksa dokumen terkait agar tidak membuat sumber kebenaran kedua.
3. Tentukan apakah perubahan bersifat rutin, operasional, strategis, atau sensitif.
4. Untuk perubahan Vision, Mission, Philosophy, Values, Ethics, Doctrine, Canon, atau identitas SparkMind, dapatkan persetujuan Founder sebelum menetapkan isi final.
5. Jangan memasukkan secret, credential, data pribadi, atau materi yang tidak memiliki hak penggunaan.

## Jenis Kontribusi

- Perbaikan typo, tata bahasa, link, atau format.
- Penyempurnaan dokumentasi tanpa mengubah makna normatif.
- Usulan standar repository.
- Klarifikasi definisi dan referensi silang.
- Proposal perubahan normatif yang disertai alasan, dampak, dan persetujuan yang tepat.

Kode aplikasi, fitur produk, deployment, database, CI/CD, dan pemilihan tech stack berada di luar ruang lingkup repository saat ini.

## Workflow Kontribusi

1. Sinkronkan branch utama lokal dengan remote.
2. Buat branch sesuai [`docs/standards/BRANCH_CONVENTION.md`](docs/standards/BRANCH_CONVENTION.md).
3. Buat perubahan sekecil dan sefokus mungkin.
4. Perbarui dokumen terkait, link, indeks, dan `CHANGELOG.md` bila relevan.
5. Lakukan self-review menggunakan checklist di bawah.
6. Commit sesuai [`docs/standards/COMMIT_CONVENTION.md`](docs/standards/COMMIT_CONVENTION.md).
7. Push branch tanpa force push.
8. Ajukan review dengan ringkasan tujuan, perubahan, risiko, dan keputusan yang diperlukan.

## Standar Perubahan

Setiap perubahan harus:

- memiliki tujuan yang jelas;
- menggunakan Bahasa Indonesia profesional, dengan istilah teknis Inggris bila lebih tepat;
- membedakan fakta, keputusan, asumsi, dan rekomendasi;
- mempertahankan status dokumen secara eksplisit;
- menggunakan link relatif untuk dokumen internal;
- mengikuti seluruh standar di [`docs/standards/README.md`](docs/standards/README.md);
- tidak mengubah makna normatif secara diam-diam.

## Review Checklist

- [ ] Perubahan berada dalam ruang lingkup yang disetujui.
- [ ] Tidak ada duplikasi sumber kebenaran.
- [ ] Istilah konsisten dengan `00-kernel/TERMINOLOGY.md` dan mapping di `01-foundation/terminology/`.
- [ ] Link internal valid.
- [ ] Tidak ada file kosong atau placeholder rusak.
- [ ] Tidak ada secret atau data sensitif.
- [ ] `CHANGELOG.md` diperbarui bila perubahan relevan bagi pengguna repository.
- [ ] Commit mengikuti Conventional Commits.
- [ ] Perubahan strategis telah mendapat persetujuan Founder.

## Pelaporan Security

Jangan membuka issue publik untuk kerentanan, credential, atau data sensitif. Ikuti [`SECURITY.md`](SECURITY.md).

## Perilaku

Seluruh kontributor wajib mengikuti [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).
