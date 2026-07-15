# Security Policy

## Tujuan

Kebijakan ini menjelaskan cara melaporkan kerentanan, credential yang terekspos, data sensitif, atau risiko keamanan pada repository SparkMind SAOS.

## Cakupan

Kebijakan berlaku untuk:

- isi dan riwayat repository;
- konfigurasi repository dan akses kolaborator;
- link, automation, atau integrasi yang terhubung ke repository;
- kebocoran secret, data pribadi, informasi proprietary, atau materi pihak ketiga;
- dokumentasi yang dapat mendorong praktik tidak aman.

Repository Foundation belum berisi aplikasi produksi. Klaim keamanan untuk produk, API, atau deployment belum berlaku.

## Versi yang Didukung

| Versi | Status |
| --- | --- |
| Branch `main` terbaru | Didukung |
| Commit, branch, atau salinan lama | Tidak dijamin |

## Cara Melaporkan

1. Jangan membuka issue atau pull request publik.
2. Hubungi maintainer atau Founder melalui kanal privat yang telah diotorisasi.
3. Sertakan deskripsi, lokasi terdampak, langkah reproduksi yang aman, dampak, dan bukti minimum.
4. Hindari mengakses, menyalin, atau menyebarkan data lebih dari yang diperlukan untuk pelaporan.
5. Beri waktu yang wajar untuk triase dan mitigasi sebelum melakukan pengungkapan lebih lanjut.

Repository belum menetapkan alamat email security publik. Sampai kanal resmi ditetapkan, gunakan kanal privat pemilik repository GitHub. Ketiadaan email publik tidak mengizinkan pengungkapan di issue publik.

## Ekspektasi Penanganan

Maintainer akan berupaya:

- mengonfirmasi penerimaan laporan;
- membatasi akses berdasarkan need-to-know;
- menilai tingkat risiko dan ruang lingkup;
- mencatat keputusan tanpa mengekspos detail sensitif;
- menghapus atau merotasi credential bila relevan;
- memberi pembaruan status kepada pelapor secara wajar.

Waktu respons formal belum ditetapkan karena struktur maintainer masih dalam Foundation. Hal ini dicatat sebagai technical debt, bukan jaminan SLA.

## Safe Harbor Beritikad Baik

Riset harus beritikad baik, meminimalkan dampak, menghormati privasi, dan tidak mengganggu layanan. Kebijakan ini bukan izin untuk mengakses data tanpa kewenangan atau melanggar hukum yang berlaku.

## Larangan Repository

- Jangan commit secret, token, key, password, atau credential.
- Jangan commit data pribadi atau informasi rahasia tanpa dasar dan perlindungan yang sah.
- Jangan memasukkan exploit aktif ke kanal publik.
- Jangan menghapus histori untuk menyembunyikan insiden; lakukan containment dan remediation yang dapat diaudit.
