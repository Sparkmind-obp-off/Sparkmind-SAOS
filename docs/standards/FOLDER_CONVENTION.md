# Folder Convention

## Tujuan

Menjaga struktur repository mudah dipahami, tidak prematur, dan mampu berkembang tanpa menjadikan folder sebagai tempat penampungan artefak yang tidak jelas.

## Struktur Foundation Aktif

```text
sparkmind-saos/
├── 00-kernel/
├── 01-foundation/
├── docs/
│   └── standards/
├── reports/
│   └── sessions/
└── [root governance documents]
```

### `00-kernel/`

Menyimpan dokumen fundamental dan normatif paling stabil. Perubahan makna strategis memerlukan persetujuan Founder. Folder ini tidak menampung SOP, implementasi produk, atau konfigurasi teknis.

### `01-foundation/`

Menyimpan governance, pengetahuan, panduan penerapan, library, research, dan playbook lintas domain. Setiap subfolder memiliki `README.md`. Folder dengan nama yang sama seperti dokumen Kernel hanya menyimpan penerapan dan referensi silang, bukan salinan sumber normatif.

#### `01-foundation/knowledge/`

Menyimpan Knowledge System terkurasi dalam domain concepts, glossary, architecture, standards, best practices, decisions, references, learning, dan onboarding. Folder glossary, standards, dan decisions berfungsi sebagai discovery view dan wajib merujuk sumber kanonik agar tidak menduplikasi Terminology, repository standards, atau Decision Library.

### `docs/standards/`

Menyimpan standar repository dan dokumentasi yang dapat diterapkan lintas layer. Satu topik hanya memiliki satu dokumen kanonik.

### `reports/sessions/`

Menyimpan laporan pekerjaan per session untuk ketertelusuran. Laporan mencatat hasil dan status, bukan menggantikan dokumen kanonik.

## Aturan Penambahan Folder

Folder baru hanya boleh dibuat jika:

1. terdapat sekurangnya satu artefak yang sah, termasuk README kontrak yang diwajibkan oleh scope arsitektur aktif, bukan hanya rencana abstrak;
2. tujuan dan batasnya berbeda dari folder yang ada;
3. memiliki `README.md` ketika fungsi folder tidak langsung jelas;
4. owner atau otoritas review dapat ditentukan;
5. tidak melanggar scope session aktif;
6. penambahannya memperkuat, bukan memecah, SSOT.

Folder kosong tidak digunakan sebagai placeholder. Rencana struktur masa depan cukup didokumentasikan sampai artefaknya benar-benar diperlukan.

## Kedalaman dan Organisasi

- Pertahankan kedalaman path seminimal mungkin.
- Kelompokkan berdasarkan domain atau fungsi, bukan berdasarkan nama orang atau tool.
- Jangan mencampur sumber kanonik, laporan, draft sementara, dan hasil generate dalam satu folder.
- Jangan menduplikasi dokumen untuk kemudahan akses; gunakan link relatif.
- Artefak deprecated tetap dapat disimpan bila dibutuhkan untuk audit, tetapi harus diberi status dan pengganti yang jelas.

## Folder yang Belum Aktif

Folder aplikasi, package, infrastructure, deployment, database, CI/CD, produk, dan Hifz AI belum dibuat. Penambahannya harus menunggu scope dan keputusan session berikutnya.

## Perubahan Struktur

Perubahan struktur wajib:

- menjelaskan alasan dan dampak;
- memperbarui seluruh link dan indeks;
- mempertahankan histori melalui `git mv` bila tersedia;
- dicatat di changelog jika memengaruhi navigasi pengguna;
- direview sebagai perubahan arsitektur informasi.

## Checklist

- [ ] Setiap folder memiliki fungsi tunggal yang jelas.
- [ ] Tidak ada folder kosong atau duplikatif.
- [ ] Indeks dan link sesuai dengan struktur aktual.
- [ ] Struktur masa depan tidak dibuat prematur.
- [ ] Perubahan dapat ditelusuri melalui Git.
