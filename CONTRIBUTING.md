# Contributing to SparkMind SAOS

## Tujuan

Pedoman ini memastikan setiap kontribusi terhadap SparkMind SAOS dapat dipahami, direview, ditelusuri, dan tetap selaras dengan repository sebagai Single Source of Truth (SSOT).

## Sebelum Berkontribusi

1. Baca [`README.md`](README.md), [`00-kernel/README.md`](00-kernel/README.md), [`01-foundation/README.md`](01-foundation/README.md), dan [`99-prompt-os/00-core/GIT_ENGINE.md`](99-prompt-os/00-core/GIT_ENGINE.md).
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

1. Verifikasi repository, remote, default branch, protection, authority, dan working tree.
2. Sinkronkan branch utama lokal dengan remote tanpa menimpa pekerjaan pihak lain.
3. Buat branch sesuai [`docs/standards/BRANCH_CONVENTION.md`](docs/standards/BRANCH_CONVENTION.md); `develop` hanya digunakan bila policy repository mengaktifkannya.
4. Buat perubahan sekecil dan sefokus mungkin.
5. Perbarui dokumen terkait, link, indeks, dan `CHANGELOG.md` bila relevan.
6. Lakukan self-review menggunakan checklist di bawah.
7. Commit sesuai [`docs/standards/COMMIT_CONVENTION.md`](docs/standards/COMMIT_CONVENTION.md).
8. Push normal tanpa force push atau protection bypass.
9. Ajukan Pull Request/review sesuai risiko dengan ringkasan tujuan, perubahan, validasi, rollback, risiko, dan keputusan yang diperlukan.
10. Integrasikan dan verifikasi remote mengikuti [`99-prompt-os/00-core/GIT_ENGINE.md`](99-prompt-os/00-core/GIT_ENGINE.md).

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
- [ ] Branch, Pull Request, reviewer, check, approval, merge, dan push mengikuti Git Engine.
- [ ] Perubahan strategis telah mendapat persetujuan Founder.

## Pelaporan Security

Jangan membuka issue publik untuk kerentanan, credential, atau data sensitif. Ikuti [`SECURITY.md`](SECURITY.md).

## Perilaku

Seluruh kontributor wajib mengikuti [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).
