# Commit Convention

## Tujuan

Menjaga histori Git mudah dibaca, dicari, direview, dan digunakan untuk memahami evolusi SparkMind SAOS. Dokumen ini adalah profil format commit repository; policy kanonik branch, review, push, release, protection, audit, dan AI automation berada di [`../../99-prompt-os/00-core/GIT_ENGINE.md`](../../99-prompt-os/00-core/GIT_ENGINE.md).

## Format

Gunakan Conventional Commits:

```text
<type>(<scope>): <description>

[optional body]

[optional footer]
```

Scope bersifat opsional tetapi disarankan jika membantu menjelaskan area perubahan.

## Type yang Diizinkan

| Type | Penggunaan |
| --- | --- |
| `docs` | Menambah atau mengubah dokumentasi |
| `fix` | Memperbaiki kesalahan atau inkonsistensi |
| `chore` | Pemeliharaan repository tanpa perubahan makna utama |
| `refactor` | Menata ulang tanpa mengubah perilaku atau makna |
| `test` | Menambah atau memperbaiki validasi/test |
| `build` | Perubahan sistem build pada layer mendatang |
| `ci` | Perubahan CI pada layer mendatang |
| `feat` | Fitur pengguna pada layer produk mendatang |
| `revert` | Membatalkan commit sebelumnya |

Pada Foundation, type yang paling umum adalah `docs`, `fix`, dan `chore`.

## Description

- Gunakan bahasa Inggris singkat agar konsisten dengan Conventional Commits.
- Gunakan imperative mood dan lowercase setelah titik dua.
- Maksimum yang disarankan 72 karakter untuk subject.
- Jangan akhiri subject dengan titik.
- Jelaskan hasil, bukan aktivitas umum seperti “update files”.

Contoh:

```text
docs(repository): establish SparkMind repository foundation
fix(kernel): correct broken terminology links
docs(spos): establish Git Engine
refactor(knowledge): simplify index hierarchy
chore(repository): add editor defaults
test(engine): cover blocked execution state
ci(repository): add markdown link check
```

## Body dan Footer

Gunakan body untuk menjelaskan alasan, konteks, risiko, atau trade-off yang tidak terlihat dari diff. Gunakan footer untuk referensi issue, approval, atau breaking change.

```text
BREAKING CHANGE: repository navigation now uses canonical layer paths
```

Breaking change atau perubahan strategis memerlukan review dan persetujuan yang sesuai sebelum integrasi.

## Atomic Commit

Setiap commit harus:

- fokus pada satu tujuan logis;
- berada dalam kondisi dapat direview;
- tidak mengandung secret atau file lokal;
- menyertakan dokumentasi terkait;
- tidak mencampurkan formatting massal dengan perubahan makna tanpa alasan.

## Larangan

- Pesan seperti `update`, `fix`, `wip`, atau `final` tanpa konteks.
- Force push ke branch utama.
- Mengubah author atau histori untuk menyembunyikan asal perubahan.
- Commit langsung ke `main` jika aturan proteksi atau workflow kolaborasi melarangnya.

## Checklist Sebelum Commit

- [ ] Diff sudah direview.
- [ ] Scope perubahan jelas.
- [ ] Validasi relevan berhasil.
- [ ] Dokumentasi dan changelog sinkron.
- [ ] Tidak ada secret atau file lokal.
- [ ] Subject mengikuti format Conventional Commits.
- [ ] Staged diff telah direview dan hanya memuat satu tujuan logis.
- [ ] Commit tidak digunakan untuk mengklaim approval, ratifikasi, atau risk acceptance.
