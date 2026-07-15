# Markdown Convention

## Tujuan

Menetapkan format Markdown yang konsisten, mudah dibaca sebagai teks, kompatibel dengan renderer umum, dan dapat dipelihara tanpa tool khusus.

## Struktur Dasar

- Gunakan tepat satu heading H1 (`#`) sebagai judul dokumen.
- Naikkan level heading secara berurutan tanpa melompati level.
- Mulai isi dengan tujuan atau konteks yang jelas.
- Gunakan heading deskriptif, bukan nomor yang mudah usang, kecuali urutan memang normatif.
- Akhiri file dengan satu newline.

## Gaya Teks

- Bahasa utama adalah Bahasa Indonesia profesional.
- Gunakan istilah teknis Inggris jika merupakan standar industri atau lebih presisi.
- Tulis akronim lengkap pada penggunaan pertama, misalnya Single Source of Truth (SSOT).
- Gunakan kalimat langsung, objektif, dan hindari hiperbola.
- Bedakan fakta, keputusan, asumsi, kandidat, dan rekomendasi secara eksplisit.

## Daftar

- Gunakan `-` untuk unordered list.
- Gunakan angka hanya jika urutan penting.
- Gunakan task list untuk checklist yang benar-benar dapat diverifikasi.
- Pertahankan bentuk gramatikal yang sejajar pada setiap item.

## Link

- Gunakan link relatif untuk file internal.
- Gunakan nama dokumen sebagai label link, bukan “klik di sini”.
- Link eksternal harus menggunakan HTTPS jika tersedia.
- Hindari link ke branch sementara atau URL yang memuat credential.
- Setelah rename atau pemindahan file, perbarui semua referensi.

## Code Fence dan Contoh

Code fence boleh digunakan untuk struktur teks, sintaks Git, atau contoh format, tetapi tidak untuk menyisipkan implementasi aplikasi pada session dokumentasi.

- Beri language identifier jika sesuai, misalnya `text`.
- Jangan gunakan indentation sebagai pengganti code fence untuk blok panjang.
- Contoh harus jelas berstatus contoh, bukan instruksi yang sudah dieksekusi.

## Tabel

Gunakan tabel untuk data komparatif yang ringkas. Hindari tabel untuk paragraf panjang atau konten yang membutuhkan hierarki kompleks.

## Metadata Status

Jika dokumen belum final, tampilkan status dekat bagian atas:

```text
> Status: Draft — menunggu review Founder.
```

Gunakan status sesuai `DOCUMENTATION_CONVENTION.md`; jangan menggunakan kata “final” pada nama file.

## Larangan

- HTML dekoratif tanpa kebutuhan aksesibilitas.
- Heading kosong.
- Link telanjang yang tidak menjelaskan tujuan, kecuali pada daftar URL teknis.
- Spasi trailing yang tidak disengaja.
- Placeholder seperti `TODO`, `TBD`, atau `lorem ipsum` tanpa owner dan tindak lanjut yang jelas.
- Emoji sebagai penanda status normatif.

## Checklist

- [ ] Satu H1 dan hierarki heading valid.
- [ ] Bahasa dan istilah konsisten.
- [ ] Link internal relatif dan valid.
- [ ] Tidak ada placeholder rusak.
- [ ] File memiliki newline akhir.
