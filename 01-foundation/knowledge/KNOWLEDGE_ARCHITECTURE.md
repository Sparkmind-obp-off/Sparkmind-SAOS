# Knowledge Architecture

> Status: Baseline arsitektur Session 004.

## Tujuan

Mendefinisikan bagaimana pengetahuan SparkMind diperoleh, dikurasi, disahkan, ditemukan, digunakan, dan diperbarui tanpa memecah SSOT atau melampaui otoritas setiap layer.

## Prinsip

1. **Traceable:** klaim dapat ditelusuri ke evidence atau sumber kanonik.
2. **Derived, not duplicated:** Knowledge System menghubungkan sumber, bukan membuat salinan bayangan.
3. **Status-aware:** draft, verified, approved, deprecated, dan archived tidak diperlakukan sama.
4. **Human-governed:** AI membantu akuisisi, sintesis, dan pemeriksaan; manusia berwenang mengesahkan perubahan berdampak.
5. **Reusable and bounded:** pengetahuan dapat dipakai ulang hanya dalam konteks dan batas yang dinyatakan.
6. **Feedback-driven:** penggunaan, outcome, insiden, dan perubahan konteks memicu review.

## Posisi dalam SparkMind

```text
00-kernel (authority & constraints)
           │
           ▼
01-foundation (governance & interpretation)
           │
           ├── research ──► knowledge ──► decision-library / playbooks
           │                  │
           │                  ├──► SAOS / AI Agents
           │                  ├──► Engineering / Documentation
           │                  └──► Products / Future Teams
           │
           └◄──── evidence, outcomes, incidents, feedback ────────────┘
```

- **Kernel** menetapkan arah, istilah fundamental, nilai, prinsip, ethics, doctrine, dan canon.
- **Foundation** mengatur interpretasi, governance, evidence, dan penerapan lintas domain.
- **Knowledge System** mengkurasi pengetahuan yang dapat ditemukan dan digunakan ulang.
- **SAOS** menggunakan knowledge sebagai konteks untuk aturan dan workflow AI tanpa menjadikannya prompt vendor-specific.
- **Engineering** menggunakan knowledge sebagai konteks; standar teknis kanonik tetap dimiliki domain Engineering saat tersedia.
- **Products** menggunakan pengetahuan approved sesuai konteks dan mengirimkan feedback, outcome, serta gap.

## Alur Pengetahuan

```text
Need / Question
      ▼
Source Discovery ──► Research & Evidence
      ▼
Triage ──► reject / request clarification / accept for curation
      ▼
Draft & Synthesis
      ▼
Verification ──► source, scope, terminology, conflict, confidence
      ▼
Review & Approval
      ▼
Publication & Indexing
      ▼
Consumption
      ▼
Feedback / Outcome / Change Signal
      └──────────────────────► Review Queue
```

### Input

Input dapat berasal dari Kernel, Foundation, keputusan, research, pengalaman terverifikasi, standar, insiden, feedback produk, atau sumber eksternal. Transcript mentah dan opini tidak langsung dipublikasikan sebagai knowledge.

### Transformasi

- `references/` mencatat sumber.
- `concepts/` dan `architecture/` menyusun model serta relationship.
- `glossary/` mengarahkan pembaca ke definisi kanonik.
- `standards/` dan `decisions/` menyediakan discovery view menuju artefak sumber.
- `best-practices/` menyintesis rekomendasi dengan konteks dan evidence.
- `learning/` dan `onboarding/` mengemas knowledge approved untuk transfer.

### Output

Output berupa knowledge artifact terkurasi, relationship map, indeks, learning path, dan onboarding guide. Output bukan otomatis kebijakan, keputusan, pattern, atau playbook.

## Siklus Pembaruan

```text
Proposed → Draft → In Review → Verified → Approved
                                      │          │
                                      └──────────┴─► Deprecated → Archived
                                                      │
                                                      └─► Superseded by ...
```

- **Proposed:** kebutuhan atau kandidat dicatat.
- **Draft:** isi sedang disusun dan belum boleh dianggap benar.
- **In Review:** siap diperiksa sumber, konteks, dan konsistensinya.
- **Verified:** evidence dan referensi telah diverifikasi, tetapi approval kebijakan belum tersirat.
- **Approved:** layak menjadi referensi operasional dalam batas yang dinyatakan.
- **Deprecated:** masih tersedia untuk transisi, tetapi tidak untuk penggunaan baru.
- **Archived:** hanya untuk audit atau histori.

Review ulang dipicu oleh perubahan upstream, sumber usang, konflik, insiden, feedback material, review date, atau perubahan konteks penggunaan.

## Peran dan Hak Perubahan

| Peran | Hak utama |
| --- | --- |
| Contributor manusia | Mengusulkan, menyusun, memberi evidence, dan merespons review. |
| AI Agent | Menyusun draft, mengklasifikasi, memeriksa link/konsistensi, dan memberi rekomendasi; tidak mengesahkan keputusan strategis. |
| Domain Owner | Memastikan akurasi domain, scope, dan dampak downstream. |
| Knowledge Steward | Menjaga struktur, metadata, discovery, lifecycle, dan konsistensi SSOT. |
| Reviewer | Memeriksa sumber, logika, terminology, risiko, dan konflik kepentingan. |
| Approver | Memberi approval sesuai authority; Founder wajib untuk perubahan strategis atau normatif. |
| Consumer | Menggunakan sesuai status dan melaporkan gap, konflik, atau outcome. |

Perubahan editorial berisiko rendah dapat disetujui maintainer. Perubahan makna domain memerlukan Domain Owner. Perubahan lintas domain, strategis, etis, atau normatif mengikuti Governance Foundation dan approval Founder bila relevan.

## Dependency dan Batas

- Konflik dengan Kernel: Kernel menjadi acuan sementara dan konflik dieskalasikan.
- Konflik dengan dokumen kanonik Foundation: sumber kanonik domain menang; knowledge diperbaiki.
- Standar atau keputusan downstream: knowledge hanya mengindeks dan menjelaskan, tidak mengambil ownership.
- Satu artefak boleh memiliki banyak consumer, tetapi hanya satu lokasi kanonik.
- Materi learning dan onboarding harus diturunkan dari knowledge yang statusnya jelas.

## Quality Gates

Sebelum published atau approved, pastikan:

- sumber dan provenance dapat ditelusuri;
- status, owner, reviewer, dan review trigger tersedia;
- terminology konsisten;
- tidak ada duplikasi sumber kanonik;
- scope, confidence, asumsi, serta keterbatasan dinyatakan;
- link silang valid dan dua arah bila dibutuhkan;
- dampak kepada SAOS, Engineering, Documentation, Governance, serta Products telah dinilai.
