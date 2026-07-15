# SparkMind Foundation (`01-foundation`)

> Status: Struktur aktif; konten domain akan dikembangkan dan direview secara bertahap.

## Tujuan

Foundation menerjemahkan arah normatif Kernel menjadi pengetahuan, tata kelola, pola, dan panduan yang dapat digunakan secara konsisten oleh SAOS, Engineering, dan Products tanpa menduplikasi sumber kanonik.

## Ruang Lingkup

Foundation mencakup:

- pengelolaan instrumen konstitusional dan governance;
- kurasi knowledge, wisdom, research, dan terminology;
- penerapan principles, values, dan ethics;
- pencatatan keputusan, pattern, dan anti-pattern;
- penyusunan playbook lintas domain.

Foundation tidak menetapkan ulang Vision, Mission, Philosophy, Values, Principles, Ethics, Doctrine, Canon, atau Terminology yang masih berada di Kernel. Foundation juga tidak memuat kode aplikasi, implementasi bisnis, database, deployment, CI/CD, atau infrastruktur cloud.

## Struktur

```text
01-foundation/
├── README.md
├── FOUNDATION_ARCHITECTURE.md
├── constitution/
├── governance/
├── knowledge/
│   ├── KNOWLEDGE_ARCHITECTURE.md
│   ├── KNOWLEDGE_GOVERNANCE.md
│   ├── concepts/
│   ├── glossary/
│   ├── architecture/
│   ├── standards/
│   ├── best-practices/
│   ├── decisions/
│   ├── references/
│   ├── learning/
│   └── onboarding/
├── wisdom/
├── principles/
├── values/
├── ethics/
├── decision-library/
├── pattern-library/
├── anti-pattern-library/
├── terminology/
├── research/
└── playbooks/
```

## Komponen

| Folder | Fungsi utama |
| --- | --- |
| [`constitution/`](constitution/README.md) | Instrumen konstitusional yang diratifikasi dan peta ke sumber Kernel. |
| [`governance/`](governance/README.md) | Otoritas, approval, lifecycle, dan mekanisme pengawasan. |
| [`knowledge/`](knowledge/README.md) | Knowledge System terverifikasi dan terkurasi, lengkap dengan arsitektur, governance, serta sembilan domain discovery dan transfer. |
| [`wisdom/`](wisdom/README.md) | Pembelajaran kontekstual dari pengalaman dan refleksi. |
| [`principles/`](principles/README.md) | Panduan penerapan prinsip Kernel dalam keputusan nyata. |
| [`values/`](values/README.md) | Panduan perilaku dan indikator penerapan nilai Kernel. |
| [`ethics/`](ethics/README.md) | Kerangka penerapan dan eskalasi isu etis. |
| [`decision-library/`](decision-library/README.md) | Catatan keputusan Foundation yang dapat ditelusuri. |
| [`pattern-library/`](pattern-library/README.md) | Pola yang telah terbukti dan konteks penggunaannya. |
| [`anti-pattern-library/`](anti-pattern-library/README.md) | Praktik yang perlu dihindari beserta mitigasinya. |
| [`terminology/`](terminology/README.md) | Ekstensi istilah domain yang tunduk pada Terminology Kernel. |
| [`research/`](research/README.md) | Bukti, sumber, hipotesis, dan hasil kajian. |
| [`playbooks/`](playbooks/README.md) | Prosedur operasional yang diturunkan dari Foundation. |

## Hubungan dengan Lapisan Lain

```text
Kernel → Foundation → SAOS / Engineering → Products
                     ↘ feedback & evidence ↗
```

- **Kernel** menetapkan sumber normatif paling stabil.
- **Foundation** mengorganisasi penerapan, pengetahuan, dan tata kelola.
- **SAOS** mengubah Foundation menjadi aturan dan workflow AI.
- **Engineering** menggunakan Foundation untuk standar dan keputusan teknis.
- **Products** menerapkan aturan tersebut dalam konteks produk serta mengirimkan evidence kembali.

Penjelasan dependency dan alur informasi tersedia di [`FOUNDATION_ARCHITECTURE.md`](FOUNDATION_ARCHITECTURE.md). Arsitektur dan aturan khusus Knowledge System tersedia di [`knowledge/KNOWLEDGE_ARCHITECTURE.md`](knowledge/KNOWLEDGE_ARCHITECTURE.md) dan [`knowledge/KNOWLEDGE_GOVERNANCE.md`](knowledge/KNOWLEDGE_GOVERNANCE.md). Ketika artefak Foundation digunakan sebagai context AI, hierarchy, dependency manifest, instruction/data separation, provenance, security, dan traceability mengikuti [`../99-prompt-os/00-core/MASTER_PROMPT_SYSTEM.md`](../99-prompt-os/00-core/MASTER_PROMPT_SYSTEM.md) tanpa memindahkan ownership Foundation.

## Aturan SSOT

1. Satu aturan, istilah, atau keputusan hanya memiliki satu sumber kanonik.
2. Folder dengan nama yang serupa dengan dokumen Kernel tidak menyalin isi Kernel; folder tersebut menyimpan panduan penerapan dan referensi silang.
3. Research memberi evidence, bukan otomatis menjadi kebijakan.
4. Laporan session mencatat pekerjaan, bukan menggantikan dokumen kanonik.
5. Perubahan strategis tetap memerlukan otoritas yang ditetapkan Kernel dan governance.
6. Pemuatan knowledge, research, pattern, playbook, report, atau tool output ke prompt tidak mengubah artefak tersebut menjadi instruction atau policy approved.

## Status dan Review

README setiap folder mendefinisikan tujuan, ruang lingkup, artefak, dan hubungan. Dokumen substantif baru harus menyatakan status, owner, sumber, serta reviewer sesuai standar repository.
