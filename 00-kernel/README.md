# SparkMind Kernel (`00-kernel`)

> Status: Kerangka awal — belum menjadi isi final.

## Tujuan

Menjadi indeks dan pintu masuk untuk dokumen paling fundamental SparkMind. Folder ini menampung arah, nilai, prinsip, etika, doktrin, kanon, dan istilah yang menjadi acuan seluruh lapisan SparkMind berikutnya.

## Ruang Lingkup

Folder ini mencakup dokumen Kernel berikut:

- `VISION.md` — arah jangka panjang.
- `MISSION.md` — mandat dan kontribusi utama.
- `PHILOSOPHY.md` — pandangan dasar tentang manusia, AI, dan teknologi.
- `PRINCIPLES.md` — prinsip pengarah keputusan dan tindakan.
- `VALUES.md` — nilai inti dan perilaku yang diharapkan.
- `ETHICS.md` — batas moral dan kerangka pertimbangan etis.
- `DOCTRINE.md` — cara berpikir ketika menghadapi situasi baru.
- `CANON.md` — aturan tentang sumber normatif dan hierarkinya.
- `TERMINOLOGY.md` — kosakata resmi dan definisi terkontrol.

Folder ini tidak mencakup implementasi produk, kode, tech stack, infrastruktur, database, deployment, CI/CD, maupun spesifikasi Hifz AI.

## Kedudukan Kernel

Kernel dirancang sebagai lapisan paling stabil dan menjadi rujukan bagi Foundation, SAOS, playbook, prompt, engineering, serta produk SparkMind. Baseline hubungan antarlapisan didokumentasikan pada [`../01-foundation/FOUNDATION_ARCHITECTURE.md`](../01-foundation/FOUNDATION_ARCHITECTURE.md); perubahan hierarki strategis tetap memerlukan keputusan Founder.

## Struktur Awal

```text
00-kernel/
├── README.md
├── VISION.md
├── MISSION.md
├── PHILOSOPHY.md
├── PRINCIPLES.md
├── VALUES.md
├── ETHICS.md
├── DOCTRINE.md
├── CANON.md
└── TERMINOLOGY.md
```

## Status Dokumen

Seluruh dokumen pada Session 001 hanya berupa placeholder terstruktur. Pernyataan dari materi Founder Discovery merupakan sumber kandidat, bukan keputusan final, sampai ditinjau dan disetujui Founder pada session berikutnya.

## Aturan Pengembangan

1. Satu dokumen diselesaikan melalui satu session yang terarah.
2. Isi normatif tidak boleh ditetapkan oleh AI tanpa persetujuan Founder.
3. Fakta, pernyataan Founder, interpretasi, dan rekomendasi harus dapat dibedakan.
4. Duplikasi aturan antardokumen harus dihindari melalui referensi silang.
5. Perubahan Kernel harus memiliki alasan, review, dan jejak Git.

## Urutan Review yang Diusulkan

1. Vision
2. Mission
3. Philosophy
4. Values
5. Principles
6. Ethics
7. Doctrine
8. Canon
9. Terminology

## Kriteria Kelengkapan Kernel

- [ ] Setiap dokumen memiliki owner dan status yang jelas.
- [ ] Seluruh isi telah ditinjau Founder.
- [ ] Tidak ada istilah inti yang ambigu.
- [ ] Tidak ada aturan normatif yang saling bertentangan.
- [ ] Hubungan antardokumen terdokumentasi.
- [ ] Riwayat keputusan dapat ditelusuri.
