# SPOS Session Template

> Status: Draft baseline SPOS-006 — gunakan bersama Execution Engine, Git Engine, dan Documentation Engine; salin sebagai session baru dan ganti seluruh token `<...>`.

## Metadata

| Field | Value |
| --- | --- |
| Session ID | `<SPOS-NNN atau SESSION-NNN>` |
| Title | `<judul singkat>` |
| Status | `Proposed / Draft / In Review / Approved / In Progress / Blocked / Completed` |
| Owner | `<role atau nama>` |
| Reviewer | `<role atau nama>` |
| Approver | `<role atau nama jika diperlukan>` |
| Risk | `low / medium / high / critical` |
| Created | `<YYYY-MM-DD>` |
| Target branch | `<branch>` |
| Source of truth | `<path atau repository>` |

## 1. Objective

Nyatakan satu outcome utama yang dapat diverifikasi.

`<objective>`

## 2. Context

Jelaskan keadaan awal, alasan session diperlukan, dan fakta yang sudah diverifikasi.

- `<context item>`

## 3. Upstream Dependencies

| Dependency | Path / reference | Status | Penggunaan |
| --- | --- | --- | --- |
| Kernel | `<path>` | `<status>` | `<constraint>` |
| Foundation / Governance | `<path>` | `<status>` | `<authority atau workflow>` |
| Knowledge / Decision | `<path>` | `<status>` | `<context>` |
| Developer Mode / Execution Engine | `<path dan versi>` | `<status>` | `<behavior, lifecycle, gates, dan completion contract>` |
| Git Engine | `<path dan versi>` | `<status>` | `<branch, review, commit, push, release, protection, dan automation contract>` |
| Documentation Engine | `<path dan versi>` | `<status>` | `<type, lifecycle, metadata, review, publication, archive, dan AI documentation contract>` |
| SPOS rule / playbook | `<path>` | `<status>` | `<constraint atau procedure>` |

Jangan memperlakukan dependency Draft sebagai aturan Approved.

## 4. Scope

### In Scope

- `<deliverable atau perubahan yang diizinkan>`

### Out of Scope

- `<pekerjaan yang dilarang atau ditunda>`

### Stop Conditions

- Konflik authority yang belum terselesaikan.
- Approval wajib, capability, akses, atau input kritis tidak tersedia.
- Perubahan akan melampaui scope atau menjadi irreversible tanpa persetujuan.
- `<stop condition tambahan>`

## 5. Deliverables

| Deliverable | Lokasi kanonik | Acceptance criteria |
| --- | --- | --- |
| `<nama>` | `<path>` | `<hasil terukur>` |

## 6. Execution Plan

Ikuti lifecycle kanonik [`../00-core/EXECUTION_ENGINE.md`](../00-core/EXECUTION_ENGINE.md):

1. Receive Objective.
2. Analyze Context.
3. Read Repository.
4. Identify Dependencies.
5. Plan Execution.
6. Execute Incrementally.
7. Validate Results.
8. Update Documentation.
9. Perform Git Workflow.
10. Generate Session Report.
11. Complete Session.

Turunkan tahap tersebut menjadi subtask atomik sesuai klasifikasi pekerjaan. Sesuaikan detail tanpa menghapus validation gate wajib.

## 7. Quality Gates

- [ ] Pre-Execution Check lulus dan dependency serta statusnya terverifikasi.
- [ ] Scope serta non-scope dipatuhi.
- [ ] Tidak ada duplikasi sumber kanonik.
- [ ] Naming, struktur, link, dan format valid.
- [ ] Security serta secret review selesai.
- [ ] During Execution Check dan Post-Execution Review lulus.
- [ ] Acceptance criteria setiap deliverable terpenuhi.
- [ ] Perubahan strategis memiliki approval yang tepat.
- [ ] Git Engine checklist yang berlaku, diff/staged diff, whitespace, dan secret review selesai.
- [ ] Required branch/PR/reviewer/check/approval/merge dipatuhi.
- [ ] Commit/push/remote hash atau alasan blocker diverifikasi.
- [ ] Documentation Engine impact assessment serta semantic/authority/lifecycle/link/security/usability check lulus.
- [ ] Repository Consistency Check dan Documentation Check lulus.
- [ ] Definition of Done Check lulus.
- [ ] Session Report selesai dan tidak menjadi sumber kanonik tandingan.

## 8. Cross-Review Matrix

| Area | Pertanyaan | Hasil / evidence |
| --- | --- | --- |
| Kernel | Apakah perubahan menduplikasi atau melemahkan sumber normatif? | `<hasil>` |
| Foundation | Apakah ownership atau SSOT Foundation diambil alih? | `<hasil>` |
| Knowledge | Apakah status dan provenance tetap benar? | `<hasil>` |
| Governance | Apakah authority, approval, dan escalation dipatuhi? | `<hasil>` |
| SAOS / SPOS | Apakah komponen berada pada layer yang tepat? | `<hasil>` |
| Documentation | Apakah source, jenis, status, metadata, owner, link, review, publication/archive, dan consumer sinkron? | `<hasil>` |
| Products | Apakah requirement atau logic produk dibuat di luar scope? | `<hasil>` |

## 9. Git Workflow

Ikuti [`../00-core/GIT_ENGINE.md`](../00-core/GIT_ENGINE.md).

- Branch / upstream: `<branch dan upstream>`
- Protection / required workflow: `<direct low-risk / pull request / reviewer / checks / blocked>`
- Commit subject: `<type>(<scope>): <description>`
- Reviewer / approver: `<role atau N/A dengan alasan>`
- Merge method: `<squash / merge commit / rebase / N/A>`
- Remote: `<remote>`
- Push policy: `<normal fast-forward push / pull request / blocked>`
- Verification command or evidence: `<local dan remote hash/check>`
- Tag / release: `<N/A atau version dan approval>`

Jangan mengklaim commit, push, merge, tag, release, protection, atau approval berhasil sebelum diverifikasi.

## 10. Session Report

Laporan penutupan minimum mencakup:

1. objective dan scope;
2. ringkasan pekerjaan;
3. struktur terbaru;
4. dokumen dibuat dan diperbarui;
5. cross-review serta validation evidence;
6. branch, commit hash, dan status push;
7. kendala dan unresolved issue;
8. technical debt dan risiko;
9. rekomendasi session berikutnya;
10. status `Completed` atau `Blocked` beserta alasannya.

## 11. Success Criteria

Session hanya `Completed` jika:

- [ ] seluruh deliverable selesai pada lokasi kanonik;
- [ ] seluruh quality gate wajib lulus;
- [ ] review dan dokumentasi selesai sesuai Documentation Engine;
- [ ] Git workflow selesai jika diwajibkan serta capability, authority, review, dan protection mengizinkan;
- [ ] jika Git terblokir, blocker dicatat jujur dan completion mengikuti Definition of Done/policy session;
- [ ] report final mencerminkan keadaan aktual.

## 12. Open Questions

- `<pertanyaan yang memerlukan keputusan atau approval>`
