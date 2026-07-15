# SPOS Session Template

> Status: Draft baseline SPOS-001 — salin sebagai session baru dan ganti seluruh token `<...>`.

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
| SPOS engine / rule | `<path>` | `<status>` | `<execution contract>` |

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

1. Audit current state dan dependency.
2. Kunci scope serta risiko.
3. Terapkan perubahan atomik.
4. Jalankan validasi dan cross-review.
5. Perbarui indeks, changelog, dan dokumentasi terkait.
6. Commit serta push bila capability, akses, dan policy mengizinkan.
7. Verifikasi hasil dan finalisasi report.

Sesuaikan langkah tanpa menghapus quality gate wajib.

## 7. Quality Gates

- [ ] Dependency dan statusnya terverifikasi.
- [ ] Scope serta non-scope dipatuhi.
- [ ] Tidak ada duplikasi sumber kanonik.
- [ ] Naming, struktur, link, dan format valid.
- [ ] Security serta secret review selesai.
- [ ] Acceptance criteria setiap deliverable terpenuhi.
- [ ] Perubahan strategis memiliki approval yang tepat.
- [ ] Git diff direview dan whitespace check berhasil.
- [ ] Commit/push atau alasan blocker diverifikasi.
- [ ] Session Report selesai dan tidak menjadi sumber kanonik tandingan.

## 8. Cross-Review Matrix

| Area | Pertanyaan | Hasil / evidence |
| --- | --- | --- |
| Kernel | Apakah perubahan menduplikasi atau melemahkan sumber normatif? | `<hasil>` |
| Foundation | Apakah ownership atau SSOT Foundation diambil alih? | `<hasil>` |
| Knowledge | Apakah status dan provenance tetap benar? | `<hasil>` |
| Governance | Apakah authority, approval, dan escalation dipatuhi? | `<hasil>` |
| SAOS / SPOS | Apakah komponen berada pada layer yang tepat? | `<hasil>` |
| Products | Apakah requirement atau logic produk dibuat di luar scope? | `<hasil>` |

## 9. Git Workflow

- Branch: `<branch>`
- Commit subject: `<type>(<scope>): <description>`
- Remote: `<remote>`
- Push policy: `<normal push / pull request / blocked>`
- Verification command or evidence: `<evidence>`

Jangan mengklaim commit atau push berhasil sebelum diverifikasi terhadap remote.

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
- [ ] review dan dokumentasi selesai;
- [ ] commit dan push selesai jika diwajibkan serta capability tersedia;
- [ ] jika Git terblokir, session dinyatakan `Blocked`, bukan diklaim selesai;
- [ ] report final mencerminkan keadaan aktual.

## 12. Open Questions

- `<pertanyaan yang memerlukan keputusan atau approval>`
