# Foundation Architecture

> Status: Baseline arsitektur informasi Session 003.

## Tujuan

Mendefinisikan posisi, tanggung jawab, dependency, dan alur informasi `01-foundation/` agar menjadi pusat pengetahuan dan tata kelola yang konsisten tanpa mengambil alih otoritas Kernel atau implementasi layer berikutnya.

## Prinsip Arsitektur

1. **Kernel authority:** sumber normatif fundamental tetap berada di `00-kernel/`.
2. **Single Source of Truth:** tidak ada dua artefak yang menetapkan aturan atau definisi yang sama.
3. **Derived, not duplicated:** Foundation merujuk dan menerapkan Kernel, bukan menyalinnya.
4. **Evidence before adoption:** research dan knowledge harus dapat ditelusuri sebelum memengaruhi keputusan.
5. **Human oversight:** AI dapat menyusun dan menganalisis; keputusan strategis memerlukan otoritas manusia yang tepat.
6. **Bidirectional learning:** arahan mengalir ke bawah, sedangkan evidence dan feedback mengalir kembali untuk review.

## Posisi dalam Arsitektur SparkMind

```text
┌──────────────────────────────────────┐
│ 00-kernel                            │
│ Arah dan sumber normatif fundamental │
└──────────────────┬───────────────────┘
                   │ constraints & authority
                   ▼
┌──────────────────────────────────────┐
│ 01-foundation                        │
│ Knowledge, governance, application   │
└──────────┬───────────────┬───────────┘
           │               │
           ▼               ▼
       SAOS rules      Engineering standards
           └──────────┬────┘
                      ▼
                   Products
                      │
                      └── evidence, incidents, feedback ──► Foundation
```

Foundation tidak bergantung pada detail implementasi SAOS, Engineering, atau Products. Layer-layer tersebut bergantung pada Foundation untuk konteks, batas, dan pengetahuan bersama.

## Tanggung Jawab Komponen

| Komponen | Tanggung jawab | Input utama | Output utama |
| --- | --- | --- | --- |
| Constitution | Mengelola instrumen konstitusional terakit dan jejak ratifikasi | Canon dan dokumen Kernel approved | Instrumen dan peta otoritas |
| Governance | Menetapkan proses approval, ownership, review, dan eskalasi | Constitution, risiko, feedback | Kebijakan governance dan matriks otoritas |
| Knowledge | Mengkurasi pengetahuan yang telah diverifikasi | Research, keputusan, sumber internal | Knowledge note dan referensi terkurasi |
| Wisdom | Menangkap pembelajaran kontekstual jangka panjang | Retrospective, insiden, outcomes | Lesson dan heuristic berstatus jelas |
| Principles | Menjelaskan penerapan prinsip Kernel | `00-kernel/PRINCIPLES.md` | Guidance, contoh, dan trade-off |
| Values | Menjelaskan perilaku yang mencerminkan nilai Kernel | `00-kernel/VALUES.md` | Behavioral guidance dan indikator |
| Ethics | Mengoperasionalkan batas etis dan eskalasi | `00-kernel/ETHICS.md`, kasus, research | Assessment dan panduan eskalasi |
| Decision Library | Menyimpan keputusan Foundation dan rasionalenya | Proposal, evidence, approval | Decision record yang traceable |
| Pattern Library | Menyimpan solusi berulang yang terbukti | Outcomes dan review | Pattern dengan konteks dan batas |
| Anti-pattern Library | Menyimpan kegagalan berulang dan mitigasi | Insiden dan retrospective | Anti-pattern dan recovery guidance |
| Terminology | Mengelola istilah domain turunan | Terminology Kernel dan kebutuhan domain | Definisi domain dan usulan promosi |
| Research | Mengelola evidence dan ketidakpastian | Sumber, pertanyaan, eksperimen | Research note dan rekomendasi |
| Playbooks | Mengubah pengetahuan approved menjadi prosedur | Governance, decisions, patterns | Langkah operasional dan checklist |

## Dependency

### Dependency normatif

```text
00-kernel/CANON.md
  └─ Constitution
      └─ Governance
          ├─ Principles / Values / Ethics application
          └─ approval rules for all Foundation artifacts
```

### Dependency pengetahuan

```text
Research → Knowledge → Decision Library → Patterns / Anti-patterns → Playbooks
                  └──────────────► Wisdom ──────────────┘
```

### Dependency istilah

Semua komponen menggunakan `00-kernel/TERMINOLOGY.md` sebagai kosakata fundamental. `terminology/` hanya mengelola istilah domain turunan dan proposal perubahan; konflik harus dieskalasikan ke owner Terminology Kernel.

## Alur Informasi

1. **Arah:** Kernel memberikan batas normatif kepada Foundation.
2. **Akuisisi:** Research mengumpulkan sumber, evidence, asumsi, dan tingkat keyakinan.
3. **Kurasi:** Knowledge memverifikasi serta menghubungkan evidence dengan konteks.
4. **Penilaian:** Principles, Values, dan Ethics memberi lensa evaluasi tanpa mengubah sumber Kernel.
5. **Keputusan:** Decision Library mencatat pilihan, alasan, trade-off, owner, dan approval.
6. **Pembelajaran:** Outcomes diklasifikasikan menjadi wisdom, pattern, atau anti-pattern.
7. **Operasionalisasi:** Playbooks menyusun prosedur berdasarkan artefak approved.
8. **Konsumsi:** SAOS, Engineering, dan Products menggunakan output Foundation.
9. **Feedback:** Hasil, insiden, dan perubahan konteks kembali ke Research dan Governance untuk review.

## Aturan Dependency

- Artefak Foundation wajib menyebutkan sumber upstream yang relevan.
- Artefak downstream tidak boleh melemahkan batas upstream.
- Research note tidak boleh diperlakukan sebagai keputusan approved.
- Pattern tidak otomatis menjadi playbook sebelum review konteks dan risiko.
- Playbook tidak boleh menetapkan Vision, Values, Principles, atau Ethics baru.
- Konflik antara Foundation dan Kernel diselesaikan dengan Kernel sebagai acuan sementara, lalu dieskalasikan melalui governance.

## Lifecycle Artefak

```text
Proposed → Draft → In Review → Approved → Superseded / Archived
```

Status `Approved` hanya diberikan oleh otoritas yang sesuai. Perubahan makna strategis memerlukan approval Founder. Histori perubahan dipertahankan melalui Git dan referensi keputusan.

## Boundary

### Foundation memiliki

- arsitektur informasi Foundation;
- proses kurasi pengetahuan;
- governance penerapan;
- library lintas domain;
- playbook lintas domain.

### Foundation tidak memiliki

- keputusan fundamental yang masih menjadi otoritas Kernel;
- runtime, prompt vendor, atau workflow executable SAOS;
- standar implementasi teknis spesifik Engineering;
- kebutuhan atau logika bisnis Products;
- kode, database, deployment, CI/CD, dan cloud infrastructure.

## Risiko dan Mitigasi

| Risiko | Mitigasi |
| --- | --- |
| Duplikasi Kernel | Gunakan referensi silang dan aturan derived-not-duplicated. |
| Research dianggap kebijakan | Status eksplisit dan approval melalui Decision Library/Governance. |
| Library menjadi tempat sampah | Wajibkan owner, konteks, status, dan trigger review. |
| Playbook usang | Cantumkan dependency, owner, dan kondisi review ulang. |
| Istilah bercabang | Terminology Kernel tetap acuan fundamental; usulan perubahan dieskalasikan. |

## Review Checklist

- [x] Seluruh komponen Foundation memiliki peran tunggal.
- [x] Dependency terhadap Kernel eksplisit.
- [x] Posisi terhadap SAOS, Engineering, dan Products jelas.
- [x] Alur arah, evidence, keputusan, operasionalisasi, dan feedback terdokumentasi.
- [x] Batas Session 003 tidak dilanggar.
