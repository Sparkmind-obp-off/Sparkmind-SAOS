# Foundation Architecture

> Status: Baseline arsitektur informasi Session 003; prompt-system diselaraskan SPOS-011, Master Knowledge System SPOS-012, Master Integration System SPOS-013, dan Master Workflow System SPOS-014 `In Review`.

## Tujuan

Mendefinisikan posisi, tanggung jawab, dependency, dan alur informasi `01-foundation/` agar menjadi pusat pengetahuan dan tata kelola yang konsisten tanpa mengambil alih otoritas Kernel atau implementasi layer berikutnya.

## Prinsip Arsitektur

1. **Constitutional boundary:** Constitution yang diratifikasi menjadi authority tertinggi di dalam SPOS; `00-kernel/` mempertahankan source material fundamental dan historinya.
2. **Single Source of Truth:** tidak ada dua artefak yang menetapkan aturan atau definisi yang sama.
3. **Derived, not duplicated:** Foundation merujuk dan menerapkan Kernel, bukan menyalinnya.
4. **Evidence before adoption:** research dan knowledge harus dapat ditelusuri sebelum memengaruhi keputusan.
5. **Human oversight:** AI dapat menyusun dan menganalisis; keputusan strategis memerlukan otoritas manusia yang tepat.
6. **Bidirectional learning:** arahan mengalir ke bawah, sedangkan evidence dan feedback mengalir kembali untuk review.

## Posisi dalam Arsitektur SparkMind

```text
┌──────────────────────────────────────┐
│ Founder + 00-kernel                  │
│ Authority + fundamental source       │
└──────────────────┬───────────────────┘
                   ▼
┌──────────────────────────────────────┐
│ SPOS Constitution                    │
│ Highest SPOS authority when ratified │
└──────────────────┬───────────────────┘
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
| Constitution | Mengelola source map, ratification record, dan amendment record | Constitution SPOS, Canon, dan dokumen Kernel | Peta sumber, status, serta jejak ratifikasi/amendment |
| Governance | Menetapkan proses approval, ownership, review, dan eskalasi | Constitution, risiko, feedback | Kebijakan governance dan matriks otoritas |
| Knowledge | Mengelola Master Knowledge System: claim/evidence, source/provenance, kurasi, taxonomy/relationship, discovery/retrieval, lifecycle, quality, protection, learning, dan onboarding | Research, keputusan, sumber internal/eksternal, report, outcome, insiden, feedback | Knowledge artifact/package, indeks, relationship map, learning path, onboarding guide, dan review signal |
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
Founder authority + 00-kernel source material
  └─ 99-prompt-os/00-core/CONSTITUTION.md
      └─ Foundation constitution records / source map
          └─ Governance
              ├─ Principles / Values / Ethics application
              └─ approval rules for all Foundation artifacts
```

Constitution menjadi authority tertinggi di dalam SPOS setelah ratifikasi Founder. Foundation tidak menyimpan Constitution tandingan; domain `constitution/` mencatat source map, ratifikasi, dan amendment.

### Dependency pengetahuan

```text
Research → Knowledge System → Decision Library → Patterns / Anti-patterns → Playbooks
             ├── concepts / architecture / references
             ├── glossary / standards / decisions (discovery views)
             ├── best-practices
             └── learning / onboarding
                         └────────► Wisdom ──────────────┘
```

### Dependency istilah

Semua komponen menggunakan `00-kernel/TERMINOLOGY.md` sebagai kosakata fundamental. `terminology/` hanya mengelola istilah domain turunan dan proposal perubahan; konflik harus dieskalasikan ke owner Terminology Kernel.

## Alur Informasi

1. **Arah:** Founder Authority, Constitution yang berlaku, dan source material Kernel memberikan batas normatif kepada Foundation sesuai kedudukan masing-masing.
2. **Akuisisi:** Research mengumpulkan sumber, evidence, asumsi, dan tingkat keyakinan.
3. **Kurasi:** Knowledge System memisahkan claim/evidence, memverifikasi source/provenance, menghubungkan context/relationship, serta menjaga confidence/applicability melalui kontrak integratif [`knowledge/MASTER_KNOWLEDGE_SYSTEM.md`](knowledge/MASTER_KNOWLEDGE_SYSTEM.md), lifecycle dasar [`knowledge/KNOWLEDGE_ARCHITECTURE.md`](knowledge/KNOWLEDGE_ARCHITECTURE.md), dan governance domain [`knowledge/KNOWLEDGE_GOVERNANCE.md`](knowledge/KNOWLEDGE_GOVERNANCE.md).
4. **Penilaian:** Principles, Values, dan Ethics memberi lensa evaluasi tanpa mengubah sumber Kernel.
5. **Keputusan:** Decision Library mencatat pilihan, alasan, trade-off, owner, dan approval.
6. **Pembelajaran:** Outcomes diklasifikasikan menjadi wisdom, pattern, atau anti-pattern.
7. **Operasionalisasi:** Playbooks menyusun prosedur berdasarkan artefak approved.
8. **Konsumsi:** SAOS, Engineering, dan Products menggunakan output Foundation.
9. **Feedback:** Hasil, insiden, quality finding, metric signal, prompt evaluation/drift, dan perubahan konteks kembali ke Research, Knowledge, serta Governance untuk review; audit/CAPA mengikuti [`../99-prompt-os/00-core/QUALITY_ENGINE.md`](../99-prompt-os/00-core/QUALITY_ENGINE.md), taxonomy/lifecycle/struktur/evidence laporan mengikuti [`../99-prompt-os/00-core/REPORT_ENGINE.md`](../99-prompt-os/00-core/REPORT_ENGINE.md), assembly/dependency/security/traceability prompt mengikuti [`../99-prompt-os/00-core/MASTER_PROMPT_SYSTEM.md`](../99-prompt-os/00-core/MASTER_PROMPT_SYSTEM.md), relationship/authority/interface/compatibility/change propagation lintas sistem mengikuti [`../99-prompt-os/00-core/MASTER_INTEGRATION_SYSTEM.md`](../99-prompt-os/00-core/MASTER_INTEGRATION_SYSTEM.md), dan komposisi stage/gate/handoff/validation/decision/escalation/feedback mengikuti [`../99-prompt-os/00-core/MASTER_WORKFLOW_SYSTEM.md`](../99-prompt-os/00-core/MASTER_WORKFLOW_SYSTEM.md) tanpa mengubah policy secara otomatis.

## Aturan Dependency

- Artefak Foundation wajib menyebutkan sumber upstream yang relevan, termasuk versi Constitution bila berlaku.
- Artefak downstream tidak boleh melemahkan Constitution atau batas upstream.
- Research note tidak boleh diperlakukan sebagai keputusan approved.
- Pattern tidak otomatis menjadi playbook sebelum review konteks dan risiko.
- Playbook tidak boleh menetapkan Vision, Values, Principles, atau Ethics baru.
- Knowledge, research, pattern, playbook, retrieved content, dan tool output yang dimuat ke prompt tetap mempertahankan canonical source, version, claim status, provenance, confidence, applicability, classification, rights, contradiction, serta limitation dan diperlakukan sebagai context/data; pemuatan tidak mengubahnya menjadi instruction atau policy approved.
- Konflik dengan Constitution yang telah diratifikasi diselesaikan dengan Constitution sebagai authority internal SPOS; konflik Constitution dengan source material Kernel atau authority Founder dihentikan dan dieskalasikan untuk resolusi konstitusional.

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
| Quality finding tidak ditindaklanjuti | Catat severity, owner, CAPA, due date, verification, escalation sesuai Quality Engine, dan report trace sesuai Report Engine. |
| Context pengetahuan diperlakukan sebagai instruksi prompt | Pertahankan provenance/status/confidence/applicability/classification, klasifikasikan sebagai data, gunakan instruction/data separation, dan eskalasikan authority conflict sesuai Master Prompt System. |
| Retrieval/ranking dianggap truth atau approval | Tampilkan canonical source, search scope, claim/evidence, contradiction, limitation, dan authority aktual sesuai Master Knowledge System. |
| Integration map mengambil ownership domain | Gunakan Master Integration System hanya sebagai relationship/dependency/interface view; source kanonik dan owner semantik tetap berlaku. |
| Workflow map menggantikan lifecycle atau owner domain | Gunakan Master Workflow System hanya untuk komposisi stage/gate/handoff/flow; lifecycle dan semantics tetap pada Session, Execution, Documentation, Knowledge, Prompt, Report, Git, Quality, dan Governance. |
| Source poisoning, stale knowledge, atau rights breach | Stop propagation, preservasi evidence, koreksi/retract/supersede, beri tahu consumer, dan revalidate sebelum reuse. |
| Istilah bercabang | Terminology Kernel tetap acuan fundamental; usulan perubahan dieskalasikan. |

## Review Checklist

- [x] Seluruh komponen Foundation memiliki peran tunggal.
- [x] Dependency terhadap Constitution dan Kernel eksplisit.
- [x] Posisi terhadap SAOS, Engineering, dan Products jelas.
- [x] Alur arah, evidence, keputusan, operasionalisasi, dan feedback terdokumentasi.
- [x] Dependency Master Prompt System menjaga knowledge sebagai context/data dengan provenance, bukan authority/instruction otomatis.
- [x] Master Knowledge System mengintegrasikan claim/evidence, provenance/lineage, taxonomy/relationship, source assessment, curation, retrieval/consumption, protection, quality, learning, dan AI policy tanpa SSOT tandingan.
- [x] Master Integration System memetakan relationship/dependency/authority/interface/flow lintas Foundation dan SPOS tanpa memindahkan ownership Foundation atau membuat mega-policy.
- [x] Master Workflow System mengomposisikan stage/gate/handoff/validation/decision/feedback tanpa mengambil semantics Foundation, knowledge, decision, pattern, atau playbook.
- [x] Batas Session 003 tidak dilanggar; penyelarasan SPOS-012 tidak membangun database, retrieval service, RAG, aplikasi, atau runtime dan tidak mengambil ownership Foundation.
