# SparkMind Knowledge System

> Status: Baseline aktif untuk struktur dan governance; konten pengetahuan substantif belum dikurasi.

## Tujuan

Knowledge System adalah pusat pengetahuan terverifikasi, terkurasi, dapat ditelusuri, dan dapat digunakan ulang oleh AI Agents, Engineering, Documentation, Governance, Products, serta tim masa depan. Sistem ini menjadi **Single Source of Truth (SSOT) pengetahuan**, tetapi tidak mengambil alih otoritas normatif Kernel atau sumber kanonik domain lain.

## Ruang Lingkup

Knowledge System mencakup model konsep, navigasi istilah, arsitektur pengetahuan domain, indeks standar, best practice berbasis evidence, konteks keputusan, referensi, materi pembelajaran, dan onboarding.

Knowledge System tidak menyimpan transcript mentah, opini tanpa status, duplikasi dokumen kanonik, kode aplikasi, implementasi bisnis, database, deployment, CI/CD, atau infrastruktur cloud.

## Struktur

```text
01-foundation/knowledge/
├── README.md
├── KNOWLEDGE_ARCHITECTURE.md
├── KNOWLEDGE_GOVERNANCE.md
├── concepts/
├── glossary/
├── architecture/
├── standards/
├── best-practices/
├── decisions/
├── references/
├── learning/
└── onboarding/
```

| Folder | Fungsi utama |
| --- | --- |
| [`concepts/`](concepts/README.md) | Model konsep dan hubungan antarkonsep. |
| [`glossary/`](glossary/README.md) | Indeks navigasi istilah tanpa menduplikasi definisi kanonik. |
| [`architecture/`](architecture/README.md) | Arsitektur pengetahuan per domain dan dependency map. |
| [`standards/`](standards/README.md) | Indeks dan penjelasan standar yang telah ditetapkan sumber kanonik. |
| [`best-practices/`](best-practices/README.md) | Rekomendasi terkurasi berbasis evidence dan konteks. |
| [`decisions/`](decisions/README.md) | Indeks konteks pengetahuan dari keputusan kanonik. |
| [`references/`](references/README.md) | Registry sumber dan bibliografi terkurasi. |
| [`learning/`](learning/README.md) | Jalur belajar dan materi transfer pengetahuan. |
| [`onboarding/`](onboarding/README.md) | Panduan orientasi berbasis peran. |

## Dokumen Sistem

- [`KNOWLEDGE_ARCHITECTURE.md`](KNOWLEDGE_ARCHITECTURE.md) — alur, lifecycle, dependency, peran, dan hubungan antarlapisan.
- [`KNOWLEDGE_GOVERNANCE.md`](KNOWLEDGE_GOVERNANCE.md) — naming, versioning, review, approval, deprecation, archiving, serta referensi silang.

## Hubungan dengan Domain Foundation Lain

- [`../research/`](../research/README.md) menghasilkan evidence dan temuan yang dapat dikurasi menjadi knowledge.
- [`../terminology/`](../terminology/README.md) dan [`../../00-kernel/TERMINOLOGY.md`](../../00-kernel/TERMINOLOGY.md) tetap menjadi sumber definisi kanonik.
- [`../decision-library/`](../decision-library/README.md) tetap menjadi sumber decision record Foundation.
- [`../pattern-library/`](../pattern-library/README.md) dan [`../anti-pattern-library/`](../anti-pattern-library/README.md) menyimpan pola yang telah dinilai.
- [`../wisdom/`](../wisdom/README.md) menyimpan pembelajaran kontekstual jangka panjang.
- [`../governance/`](../governance/README.md) menentukan otoritas dan eskalasi Foundation.
- [`../playbooks/`](../playbooks/README.md) mengoperasionalkan pengetahuan approved.

## Aturan SSOT

1. Setiap klaim memiliki sumber, status verifikasi, owner, dan batas berlaku.
2. Dokumen kanonik eksternal direferensikan, bukan disalin.
3. Ringkasan tidak boleh mengubah makna sumber; konflik diselesaikan dengan sumber kanonik sebagai acuan.
4. Research belum menjadi knowledge approved sebelum kurasi dan review.
5. Knowledge memberi konteks bagi keputusan, tetapi tidak menjadi keputusan hanya karena terdokumentasi.
6. AI boleh mengusulkan dan memelihara draft; approval strategis tetap berada pada manusia berwenang.

## Kontrak Minimum Artefak

Artefak substantif harus menyatakan, bila relevan: status, owner, reviewer, tanggal review, sumber, tingkat keyakinan, asumsi, batas berlaku, dependency, dan trigger review ulang. Struktur lengkap mengikuti [`KNOWLEDGE_GOVERNANCE.md`](KNOWLEDGE_GOVERNANCE.md).

## Cara Menggunakan

1. Mulai dari indeks ini dan pilih domain yang sesuai.
2. Verifikasi status artefak sebelum menggunakannya.
3. Ikuti link menuju sumber kanonik untuk keputusan atau definisi penting.
4. Ajukan pembaruan melalui lifecycle yang ditetapkan governance.
5. Laporkan konflik, sumber usang, dan gap ke owner atau Knowledge Steward.
