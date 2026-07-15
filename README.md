# SparkMind SAOS

SparkMind AI Operating System (SAOS) adalah repository dokumentasi yang menjadi Single Source of Truth (SSOT) untuk fondasi, identitas, standar, dan pengetahuan operasional SparkMind.

> Status repository: Foundation Architecture aktif. Kernel Session 001 masih berupa kerangka terstruktur yang menunggu review dan persetujuan Founder.

## Tujuan

Repository ini dirancang untuk:

- menjaga satu sumber kebenaran bagi keputusan dan dokumen SparkMind;
- memisahkan prinsip fundamental dari aturan operasional dan implementasi produk;
- memastikan perubahan dapat direview, dilacak, dan dipelihara;
- menyediakan fondasi vendor-agnostic bagi manusia dan AI yang bekerja untuk SparkMind.

## Ruang Lingkup Saat Ini

### Selesai

- Kernel awal dengan 10 dokumen terstruktur.
- Dokumentasi root repository.
- Standar penamaan, folder, Markdown, dokumentasi, commit, branch, dan versioning.
- Pedoman kontribusi, keamanan, dukungan, dan perilaku komunitas.
- Struktur lengkap `01-foundation/` dengan 13 domain terdokumentasi.
- Foundation Architecture, dependency, alur informasi, dan boundary antarlapisan.

### Belum Diimplementasikan

- Isi final dokumen Kernel dan persetujuan Founder.
- Isi substantif serta approval artefak pada setiap domain Foundation.
- Operating rules, engine, prompt, dan layer SAOS berikutnya.
- Spesifikasi atau implementasi produk, termasuk Hifz AI.
- Kode aplikasi, database, deployment, dan CI/CD.

## Struktur Repository

```text
sparkmind-saos/
├── 00-kernel/             # Dokumen fundamental dan normatif
├── 01-foundation/         # Pengetahuan, governance, library, dan playbook
├── docs/
│   └── standards/         # Standar pengelolaan repository
├── reports/
│   └── sessions/          # Laporan hasil setiap session
├── README.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── CHANGELOG.md
├── LICENSE
├── SECURITY.md
└── SUPPORT.md
```

Direktori baru hanya ditambahkan ketika memiliki tujuan, owner, dan dokumen indeks yang jelas. Konvensi lengkap tersedia di [`docs/standards/FOLDER_CONVENTION.md`](docs/standards/FOLDER_CONVENTION.md).

## Indeks Dokumentasi

### Kernel

- [`00-kernel/README.md`](00-kernel/README.md) — kedudukan dan indeks Kernel.
- [`00-kernel/VISION.md`](00-kernel/VISION.md) — arah jangka panjang.
- [`00-kernel/MISSION.md`](00-kernel/MISSION.md) — mandat utama.
- [`00-kernel/PHILOSOPHY.md`](00-kernel/PHILOSOPHY.md) — pandangan dasar.
- [`00-kernel/PRINCIPLES.md`](00-kernel/PRINCIPLES.md) — prinsip pengarah.
- [`00-kernel/VALUES.md`](00-kernel/VALUES.md) — nilai inti.
- [`00-kernel/ETHICS.md`](00-kernel/ETHICS.md) — batas etis.
- [`00-kernel/DOCTRINE.md`](00-kernel/DOCTRINE.md) — cara berpikir stabil.
- [`00-kernel/CANON.md`](00-kernel/CANON.md) — hierarki sumber normatif.
- [`00-kernel/TERMINOLOGY.md`](00-kernel/TERMINOLOGY.md) — kosakata terkontrol.

### Foundation

- [`01-foundation/README.md`](01-foundation/README.md) — indeks 13 domain Foundation.
- [`01-foundation/FOUNDATION_ARCHITECTURE.md`](01-foundation/FOUNDATION_ARCHITECTURE.md) — peran, dependency, alur informasi, dan boundary.

### Repository

- [`CONTRIBUTING.md`](CONTRIBUTING.md) — alur kontribusi dan review.
- [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) — standar perilaku.
- [`CHANGELOG.md`](CHANGELOG.md) — riwayat perubahan terkurasi.
- [`SECURITY.md`](SECURITY.md) — pelaporan kerentanan dan informasi sensitif.
- [`SUPPORT.md`](SUPPORT.md) — jalur bantuan dan pertanyaan.
- [`docs/standards/README.md`](docs/standards/README.md) — indeks standar repository.
- [`reports/sessions/README.md`](reports/sessions/README.md) — indeks laporan session.

## Panduan Penggunaan

1. Mulai dari dokumen ini untuk memahami ruang lingkup repository.
2. Baca [`00-kernel/README.md`](00-kernel/README.md) sebelum mengusulkan perubahan fundamental.
3. Baca [`01-foundation/README.md`](01-foundation/README.md) dan arsitekturnya sebelum menambah pengetahuan atau playbook.
4. Ikuti [`CONTRIBUTING.md`](CONTRIBUTING.md) dan seluruh standar di `docs/standards/`.
5. Bedakan isi berstatus draft, approved, deprecated, atau superseded.
6. Gunakan issue atau jalur privat yang sesuai sebelum mengirim perubahan sensitif.

## Data dan Teknologi

Repository ini hanya berisi Kernel, Foundation, dan dokumentasi tata kelola repository. Tidak ada data model aplikasi, database, layanan penyimpanan, API, runtime, atau tech stack yang dipilih pada tahap ini.

## URL dan Status

- **Repository remote:** <https://github.com/Sparkmind-obp-off/Sparkmind-SAOS>
- **Production:** Belum tersedia; deployment berada di luar ruang lingkup Foundation.
- **Platform target:** Belum ditetapkan.
- **Status:** Foundation aktif, belum berupa aplikasi.
- **Terakhir diperbarui:** 2026-07-15.

## Lisensi

Repository ini bersifat proprietary. Tidak ada hak penggunaan, penyalinan, modifikasi, atau distribusi yang diberikan tanpa izin tertulis. Lihat [`LICENSE`](LICENSE).
