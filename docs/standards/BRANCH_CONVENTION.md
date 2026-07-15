# Branch Convention

## Tujuan

Menjaga perubahan terisolasi, mudah direview, dan aman untuk diintegrasikan tanpa merusak branch utama. Dokumen ini adalah profil bentuk branch repository; policy kanonik authority, Pull Request, review, merge, push, protection, dan AI automation berada di [`../../99-prompt-os/00-core/GIT_ENGINE.md`](../../99-prompt-os/00-core/GIT_ENGINE.md).

## Branch Utama

`main` adalah branch utama dan sumber keadaan repository yang paling mutakhir. Branch ini harus selalu berada dalam kondisi konsisten dan siap digunakan sebagai SSOT.

Jika proteksi branch tersedia, aktifkan review, larangan force push, dan pemeriksaan yang relevan. Konfigurasi proteksi platform berada di luar isi repository dan harus dikelola oleh owner GitHub.

## Format Nama

```text
<type>/<short-description>
```

Type yang disarankan:

- `feature/` — fitur atau capability baru;
- `fix/` — perbaikan defect atau inkonsistensi;
- `docs/` — dokumentasi;
- `refactor/` — restrukturisasi tanpa perubahan perilaku atau makna;
- `research/` — penelitian/eksperimen yang memang memerlukan branch;
- `chore/` — pemeliharaan repository atau tooling;
- `release/` — persiapan rilis;
- `hotfix/` — perbaikan mendesak yang telah diotorisasi.

`feat/` tetap diterima sebagai alias kompatibilitas untuk histori/repository yang sudah menggunakannya; branch baru menggunakan `feature/`. `develop` bersifat opsional dan hanya dibuat bila kebutuhan integration branch, owner, lifecycle, serta protection terdokumentasi.

Gunakan deskripsi `lowercase-kebab-case` yang singkat dan spesifik.

Contoh:

```text
docs/repository-foundation
fix/session-report-links
feature/bounded-agent-retry
research/release-signing-options
chore/normalize-document-status
```

## Lifecycle

1. Mulai dari `main` terbaru.
2. Buat satu branch untuk satu tujuan logis.
3. Commit secara atomic dan sesuai Conventional Commits.
4. Push branch tanpa force push.
5. Buat Pull Request bila diwajibkan dan selesaikan reviewer, check, approval, conversation, serta konflik.
6. Integrasikan dengan merge method sesuai Git Engine dan kebijakan repository.
7. Hapus branch setelah terintegrasi jika tidak lagi diperlukan.

## Perubahan Langsung pada `main`

Perubahan langsung hanya dapat dilakukan bila:

- owner repository mengizinkan workflow tersebut;
- perubahan berisiko rendah dan scope sudah jelas;
- tidak melewati review atau approval yang diwajibkan;
- branch tetap konsisten setelah commit.

Untuk perubahan strategis, security-sensitive, normatif, release, atau berisiko tinggi, gunakan branch terpisah, Pull Request, review independen, dan persetujuan yang sesuai. Commit/push langsung tidak boleh memintas protection atau approval wajib.

## Larangan

- Force push ke `main`.
- Branch berumur panjang tanpa owner atau tujuan aktif.
- Nama branch seperti `test`, `new`, `temp`, atau nama individu saja.
- Mencampurkan beberapa objective tidak terkait.
- Menghapus branch yang masih memuat perubahan unik dan belum direview.

## Konflik dan Sinkronisasi

- Jangan menyelesaikan konflik dengan memilih seluruh satu sisi tanpa memahami makna.
- Review kembali link, status, dan changelog setelah konflik dokumentasi.
- Rebase atau merge harus mengikuti kebijakan tim; jangan rewrite histori branch bersama tanpa koordinasi.

## Checklist

- [ ] Branch berasal dari `main` terbaru.
- [ ] Nama menjelaskan type dan tujuan.
- [ ] Scope tunggal dan owner jelas.
- [ ] Tidak ada force push yang tidak diotorisasi.
- [ ] Branch dihapus setelah aman dan terintegrasi.
