# SPOS Session Template

> Status: Draft baseline diselaraskan SPOS-012 — gunakan bersama Master Knowledge System, Master Prompt System, Session, Governance, Execution, Git, Documentation, Quality, dan Report Engine; salin sebagai session baru dan ganti seluruh token `<...>`.

## Metadata

| Field | Value |
| --- | --- |
| Session ID | `<SPOS-NNN atau SESSION-NNN>` |
| Title | `<judul singkat>` |
| Type | `Foundation / Architecture / Development / Documentation / Research / Governance / Quality / Refactor / Bug Fix / Release / Maintenance / Knowledge` |
| Secondary type | `<N/A atau type tambahan dengan alasan>` |
| State | `Pending / Running / Blocked / Waiting for Approval / Review / Completed / Archived / Cancelled` |
| Lifecycle phase | `<satu dari 13 tahap Session Engine>` |
| Owner | `<role atau nama>` |
| Executor | `<role atau nama>` |
| Reviewer | `<role atau nama>` |
| Approver | `<role atau nama jika diperlukan>` |
| Risk | `low / medium / high / critical` |
| Decision class | `D0 / D1 / D2 / D3 / Emergency` |
| Authority / delegation | `<source, scope, risk ceiling, effective/expiry>` |
| Created / updated | `<YYYY-MM-DD / YYYY-MM-DD>` |
| Target branch | `<branch>` |
| Baseline commit | `<full hash atau N/A>` |
| Source of truth | `<path atau repository>` |
| Predecessor / successor | `<session ID atau N/A>` |
| Related / blocked by | `<session ID dan relation atau N/A>` |

## 1. Objective

Nyatakan tepat satu outcome utama yang dapat diverifikasi.

`<objective>`

### Success Criteria

- [ ] `<hasil terukur>`

## 2. Context Manifest

Jelaskan keadaan awal, alasan session diperlukan, dan fakta yang telah diverifikasi.

| Context | Source / version | Status | Penggunaan / limitation |
| --- | --- | --- | --- |
| `<item>` | `<path, URL, decision, commit>` | `<fact / assumption / unknown>` | `<dampak>` |

Context percakapan atau memory AI tidak menjadi satu-satunya source of truth.

## 3. Upstream Dependencies

| Dependency | Path / reference | Version / status | Owner | Penggunaan / blocking behavior |
| --- | --- | --- | --- | --- |
| Constitution | `<path dan versi>` | `<status>` | `<owner>` | `<constraint>` |
| Foundation | `<path>` | `<status>` | `<owner>` | `<source, record, atau domain constraint>` |
| Governance Engine | `<path dan versi>` | `<status>` | `<owner>` | `<authority, role, ownership, decision class, approval, exception, escalation>` |
| Session Engine | `<path dan versi>` | `<status>` | `<owner>` | `<lifecycle, type, state, continuity, report, closure>` |
| Master Knowledge System / Knowledge / Decision | `<path dan version/status>` | `<status>` | `<owner>` | `<canonical source, claim/evidence, provenance, confidence, applicability, classification/rights, context, stale/conflict behavior>` |
| Developer Mode / Execution | `<path dan versi>` | `<status>` | `<owner>` | `<behavior, procedure, checkpoint, recovery, evidence, completion>` |
| Git Engine | `<path dan versi>` | `<status>` | `<owner>` | `<branch, review, commit, push, release, protection>` |
| Documentation Engine | `<path dan versi>` | `<status>` | `<owner>` | `<type, lifecycle, metadata, review, publication, archive>` |
| Quality Engine | `<path dan versi>` | `<status>` | `<owner>` | `<principles, gates, DoD, metrics, audit, CAPA>` |
| Report Engine | `<path dan versi>` | `<status>` | `<owner>` | `<taxonomy, lifecycle, structure, evidence/traceability, validation, publication, archive>` |
| Master Prompt System | `<path dan versi>` | `<status>` | `<owner>` | `<hierarchy, layer, assembly, dependency, context classification, security, traceability>` |
| Rule / playbook / session | `<path atau ID>` | `<status>` | `<owner>` | `<constraint, procedure, dependency relation>` |

Jangan memperlakukan dependency `Draft`, `In Review`, atau `Completed` session sebagai artefak `Approved` tanpa status/evidence terpisah.

## 4. Scope

### In Scope

- `<deliverable atau perubahan yang diizinkan>`

### Out of Scope

- `<pekerjaan yang dilarang atau ditunda>`

### Stop Conditions

- Konflik authority yang belum terselesaikan.
- Approval wajib, capability, akses, input, atau evidence kritis tidak tersedia.
- Perubahan akan melampaui scope/risk ceiling atau menjadi irreversible tanpa persetujuan.
- Actual state tidak dapat direkonstruksi atau unrelated work berisiko tertimpa.
- `<stop condition tambahan>`

## 5. Deliverables

| Deliverable | Lokasi kanonik | Acceptance criteria | Status / evidence |
| --- | --- | --- | --- |
| `<nama>` | `<path>` | `<hasil terukur>` | `<pending / done / blocked + reference>` |

## 6. Authority, Risk, dan Approval

- Authority source: `<reference>`
- Allowed actions: `<actions>`
- Prohibited actions: `<actions>`
- Risk ceiling / current risk: `<ceiling / current>`
- Required reviewer / independence: `<role dan separation>`
- Required approval / risk acceptance: `<role, artefact/version/scope>`
- Exception / escalation: `<reference atau N/A>`
- Capability / data / access boundary: `<boundary>`

## 7. Session Lifecycle Plan

Ikuti lifecycle kanonik [`../00-core/SESSION_ENGINE.md`](../00-core/SESSION_ENGINE.md). Detail execution mengikuti [`../00-core/EXECUTION_ENGINE.md`](../00-core/EXECUTION_ENGINE.md).

| # | Tahap | Planned action | Output / gate | Status / evidence |
| --- | --- | --- | --- | --- |
| 1 | Session Initialization | `<aksi>` | `<identity/intake>` | `<status>` |
| 2 | Context Loading | `<aksi>` | `<context manifest>` | `<status>` |
| 3 | Repository Analysis | `<aksi>` | `<baseline/file map>` | `<status>` |
| 4 | Objective Validation | `<aksi>` | `<validated contract>` | `<status>` |
| 5 | Planning | `<aksi>` | `<plan/checkpoint>` | `<status>` |
| 6 | Execution | `<aksi>` | `<increment/deliverable>` | `<status>` |
| 7 | Continuous Validation | `<aksi>` | `<check/finding>` | `<status>` |
| 8 | Documentation Update | `<aksi>` | `<documentation trace>` | `<status>` |
| 9 | Git Workflow | `<aksi>` | `<branch/commit/push>` | `<status>` |
| 10 | Quality Review | `<aksi>` | `<gate/DoD>` | `<status>` |
| 11 | Governance Check | `<aksi>` | `<authority/approval>` | `<status>` |
| 12 | Session Report | `<aksi>` | `<report>` | `<status>` |
| 13 | Session Closure | `<aksi>` | `<final state/handoff>` | `<status>` |

Turunkan tahap menjadi subtask atomik. Hanya satu subtask `in progress` bila task tracker tersedia. Tahap `Not Applicable` memerlukan alasan.

## 8. State History

| Timestamp | From | To | Phase | Actor / authority | Trigger / evidence | Next action |
| --- | --- | --- | --- | --- | --- | --- |
| `<ISO-8601>` | `<N/A>` | `Pending` | `Session Initialization` | `<actor>` | `<intake>` | `<action>` |

State history append-only secara semantik. Gunakan hanya transisi yang diizinkan Session Engine.

## 9. Continuity dan Recovery

- Last safe checkpoint: `<phase, commit, artefact, timestamp>`
- Current repository state: `<path, branch, commit, worktree, remote>`
- Completed work: `<ringkasan>`
- Remaining work: `<ringkasan>`
- Current blocker / approval: `<reference atau N/A>`
- Next atomic action: `<aksi tunggal>`
- Resume prerequisites: `<dependency, access, revalidation>`
- Rollback / recovery path: `<path>`
- Context intentionally excluded: `<security/privacy reason atau N/A>`
- Handoff recipient / acceptance: `<recipient dan evidence atau N/A>`

## 10. Quality Gates

Gunakan urutan [`../00-core/QUALITY_ENGINE.md`](../00-core/QUALITY_ENGINE.md): Objective, Requirement, Architecture, Implementation, Documentation, Git, Security & Privacy, Governance, dan Final Approval. Catat `Pass / Fail / Blocked / Not Applicable`, evidence, reviewer, waktu, serta alasan.

| Gate | Result | Evidence | Reviewer / independence | Finding / action |
| --- | --- | --- | --- | --- |
| Objective | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Requirement | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Architecture | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Implementation | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Documentation | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Git | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Security & Privacy | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Governance | `<result>` | `<reference>` | `<reviewer>` | `<action>` |
| Final Approval | `<result>` | `<reference>` | `<approver>` | `<action>` |

## 11. Cross-Review Matrix

| Area | Pertanyaan | Hasil / evidence |
| --- | --- | --- |
| Constitution | Apakah objective, tindakan, dan closure selaras dengan prinsip/authority tertinggi? | `<hasil>` |
| Developer Mode | Apakah perilaku AI, capability, autonomy, stop, dan reporting sesuai? | `<hasil>` |
| Session | Apakah identity, type, state, lifecycle, continuity, report, dan closure sesuai Session Engine? | `<hasil>` |
| Execution | Apakah procedure, checkpoint, failure/recovery, evidence, dan completion sesuai? | `<hasil>` |
| Governance | Apakah role, delegation, ownership, decision class, separation, approval, exception, dan escalation sesuai? | `<hasil>` |
| Git | Apakah branch, diff, commit, review, push, protection, dan remote evidence sesuai? | `<hasil>` |
| Documentation | Apakah source, jenis, status, metadata, owner, link, review, publication/archive, dan consumer sinkron? | `<hasil>` |
| Quality | Apakah objective/requirement traceable, gate, DoD, evidence, finding, metric, dan approval sesuai? | `<hasil>` |
| Report | Apakah taxonomy, lifecycle, struktur, claim-evidence trace, reproducibility, sensitive-data handling, correction, dan approval report sesuai? | `<hasil>` |
| Foundation / Knowledge | Apakah canonical ownership, claim/evidence, provenance/lineage, source assessment, taxonomy/relationship, status, confidence/applicability, classification/rights, retrieval/consumer use, dan learning flow sesuai Master Knowledge System? | `<hasil>` |
| Master Prompt | Apakah knowledge diperlakukan sebagai context/data dengan package manifest, instruction/data separation, least disclosure, dan prompt security yang benar? | `<hasil>` |
| SAOS / SPOS | Apakah komponen berada pada layer dan SSOT yang tepat? | `<hasil>` |
| Products | Apakah requirement atau logic produk dibuat di luar scope? | `<hasil>` |

## 12. Git Workflow

Ikuti [`../00-core/GIT_ENGINE.md`](../00-core/GIT_ENGINE.md).

- Branch / upstream: `<branch dan upstream>`
- Baseline / final commit: `<hash>`
- Protection / required workflow: `<direct low-risk / PR / reviewer / checks / blocked>`
- Commit subject: `<type>(<scope>): <description>`
- Reviewer / approver: `<role atau N/A dengan alasan>`
- Merge method: `<squash / merge commit / rebase / N/A>`
- Remote: `<remote>`
- Push policy / status: `<normal fast-forward / PR / blocked / N/A>`
- Verification evidence: `<local dan remote hash/check>`
- Tag / release: `<N/A atau version dan approval>`

Jangan mengklaim commit, push, merge, tag, release, protection, atau approval berhasil sebelum diverifikasi. Git event tidak otomatis mengubah state session.

## 13. Session Report

Ikuti [`../00-core/REPORT_ENGINE.md`](../00-core/REPORT_ENGINE.md). Catat metadata report, scope/objective, summary, deliverable, evidence manifest, validation result, decision, risk, debt, lesson, next action, approval, references, appendix, serta lifecycle/version/traceability yang berlaku.

Laporan penutupan minimum mencakup:

1. objective, type, scope, dan ringkasan;
2. lifecycle dan state history;
3. dependency/predecessor/successor penting;
4. dokumen/artefak baru serta diperbarui;
5. cross-review, quality/governance result, dan validation evidence;
6. branch, commit hash, remote, serta status push;
7. failure, rollback, recovery, decision, exception, dan approval;
8. temuan, technical debt, residual risk, dan blocker;
9. continuity/handoff, next atomic action, dan rekomendasi session berikutnya;
10. final state beserta alasan/evidence.

Report tidak menjadi sumber kanonik tandingan. Report final wajib memiliki claim-evidence trace, classification/least-disclosure review, dan current-version reference sesuai Report Engine.

## 14. Closure Checklist

Session hanya `Completed` jika:

- [ ] tepat satu objective tercapai;
- [ ] seluruh deliverable selesai pada lokasi kanonik;
- [ ] lifecycle wajib selesai atau N/A terjustifikasi;
- [ ] state history dan transition evidence lengkap;
- [ ] seluruh gate kritis lulus;
- [ ] required review/approval tersedia;
- [ ] dokumentasi selesai sesuai Documentation Engine;
- [ ] Git workflow selesai jika berlaku dan remote evidence akurat;
- [ ] tidak ada pekerjaan wajib parsial atau hidden blocker;
- [ ] report final tervalidasi sesuai Report Engine serta continuity/handoff mencerminkan keadaan aktual;
- [ ] debt, residual risk, successor, retention, dan archive trigger jelas;
- [ ] knowledge consumed/produced memiliki canonical target, provenance, claim status, confidence/applicability, classification/rights, consumer trace, dan revalidation path yang proporsional.

Jika tidak terpenuhi, gunakan `Blocked`, `Waiting for Approval`, atau `Cancelled` sesuai keadaan. Jangan mengubah session terminal kembali ke `Running`; buat successor.

## 15. Open Questions

- `<pertanyaan yang memerlukan keputusan atau approval>`
