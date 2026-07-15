# Naming Convention

## Tujuan

Menjaga nama artefak repository konsisten, mudah dicari, dapat dipahami manusia dan AI, serta tidak bergantung pada satu vendor atau sistem operasi.

## Prinsip Umum

- Gunakan nama yang menjelaskan fungsi, bukan nama sementara seperti `misc`, `new`, `final-final`, atau `temp`.
- Pilih satu istilah kanonik dan gunakan secara konsisten.
- Hindari singkatan yang belum didefinisikan.
- Gunakan karakter ASCII untuk path, branch, dan tag agar kompatibel lintas platform.
- Jangan memasukkan credential, data pribadi, tanggal kedaluwarsa yang menyesatkan, atau nama vendor tanpa kebutuhan.

## Folder

- Gunakan `lowercase-kebab-case`.
- Prefix numerik dua digit hanya digunakan untuk urutan layer kanonik, misalnya `00-kernel`.
- Nama berbentuk kata benda atau domain, misalnya `docs`, `standards`, dan `reports`.
- Jangan gunakan spasi, underscore, atau trailing dot.

Contoh benar:

```text
00-kernel/
docs/standards/
reports/sessions/
```

## File Dokumentasi

- Dokumen standar atau kanonik menggunakan `UPPER_SNAKE_CASE.md`.
- File indeks folder selalu bernama `README.md`.
- Dokumen kebijakan root mengikuti nama komunitas yang umum, misalnya `SECURITY.md` dan `CONTRIBUTING.md`.
- Laporan session menggunakan `SESSION-NNN.md`, dengan tiga digit dan zero-padding.
- Nama file harus stabil; perubahan judul tidak otomatis mengharuskan rename.

## Branch

Gunakan format `<type>/<short-description>` dengan deskripsi `lowercase-kebab-case`. Detail tersedia di `BRANCH_CONVENTION.md`.

```text
docs/repository-foundation
fix/broken-kernel-links
chore/normalize-metadata
```

## Commit Scope

Gunakan kata benda singkat dalam lowercase, misalnya `kernel`, `repository`, `standards`, atau `session`. Jangan membuat scope baru jika scope yang ada sudah akurat.

## Version dan Tag

Gunakan SemVer dan prefix `v` untuk tag repository:

```text
v0.1.0
v1.0.0
```

## Istilah

Definisi istilah inti berada di `00-kernel/TERMINOLOGY.md`. Jika istilah belum disahkan:

- tandai sebagai kandidat atau draft;
- jangan memperlakukannya sebagai definisi final;
- hindari membuat sinonim baru tanpa alasan;
- catat sumber keputusan saat definisi disahkan.

## Checklist

- [ ] Nama menjelaskan fungsi artefak.
- [ ] Format sesuai jenis artefak.
- [ ] Tidak ada istilah ambigu atau duplikatif.
- [ ] Link dan referensi diperbarui setelah rename.
- [ ] Rename yang memengaruhi makna telah direview.
