# SparkMind Knowledge System

> Status: Master Knowledge System baseline SPOS-012 tersedia sebagai `In Review`; struktur dan governance aktif, sedangkan konten pengetahuan substantif serta activation manusia belum tersedia.

## Tujuan

Knowledge System adalah pusat pengetahuan terverifikasi, terkurasi, dapat ditelusuri, dan dapat digunakan ulang oleh AI Agents, Engineering, Documentation, Governance, Products, serta tim masa depan. Sistem ini menjadi **Single Source of Truth (SSOT) pengetahuan**, tetapi tidak mengambil alih otoritas normatif Kernel atau sumber kanonik domain lain.

## Ruang Lingkup

Knowledge System mencakup model konsep, navigasi istilah, arsitektur pengetahuan domain, indeks standar, best practice berbasis evidence, konteks keputusan, referensi, materi pembelajaran, dan onboarding.

Knowledge System tidak menyimpan transcript mentah, opini tanpa status, duplikasi dokumen kanonik, kode aplikasi, implementasi bisnis, database, deployment, CI/CD, atau infrastruktur cloud.

## Struktur

```text
01-foundation/knowledge/
├── README.md
├── MASTER_KNOWLEDGE_SYSTEM.md
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

- [`MASTER_KNOWLEDGE_SYSTEM.md`](MASTER_KNOWLEDGE_SYSTEM.md) — kontrak integratif model knowledge, claim/evidence, provenance, taxonomy/relationship, source assessment, curation, retrieval/consumption, traceability, security/rights, quality, learning, AI policy, dan activation.
- [`KNOWLEDGE_ARCHITECTURE.md`](KNOWLEDGE_ARCHITECTURE.md) — sumber kanonik alur, lifecycle dasar, dependency, peran, dan hubungan antarlapisan.
- [`KNOWLEDGE_GOVERNANCE.md`](KNOWLEDGE_GOVERNANCE.md) — sumber kanonik naming, metadata, versioning, review, approval, deprecation, archiving, serta referensi silang domain.

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
7. Claim, evidence, synthesis, recommendation, decision, dan prompt instruction wajib dibedakan; knowledge tidak memperoleh authority hanya karena ditemukan, diringkas, atau sering digunakan.
8. Discovery, retrieval, dan learning view mempertahankan canonical source, version, status, confidence, applicability, classification, serta limitation.

## Kontrak Minimum Artefak

Artefak substantif harus menyatakan, bila relevan: status, owner, reviewer, tanggal review, sumber, tingkat keyakinan, asumsi, batas berlaku, dependency, dan trigger review ulang. Struktur lengkap mengikuti [`KNOWLEDGE_GOVERNANCE.md`](KNOWLEDGE_GOVERNANCE.md).

## Cara Menggunakan

1. Mulai dari indeks ini dan baca Master Knowledge System untuk kontrak integratif.
2. Verifikasi status, version, provenance, confidence, applicability, classification, dan review state artefak sebelum menggunakannya.
3. Ikuti link menuju sumber kanonik untuk keputusan, definisi, claim, atau evidence penting.
4. Perlakukan retrieval dan AI synthesis sebagai context/data sampai verification serta authority yang benar tersedia.
5. Ajukan pembaruan melalui lifecycle yang ditetapkan Knowledge Architecture dan Governance.
6. Laporkan conflict, stale source, rights/access issue, harmful gap, dan outcome ke owner atau Knowledge Steward.
