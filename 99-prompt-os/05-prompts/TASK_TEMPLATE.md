# Task Prompt Template

> Status: Placeholder Draft SPOS-001 — bukan task prompt aktif atau approved.

## Tujuan

Mengubah objective session menjadi unit eksekusi terukur dengan input, langkah, validasi, output, dan stop condition yang eksplisit.

## Template

```text
TASK ID
<session-id/task-id>

OBJECTIVE
<one verifiable outcome>

INPUTS
- <input + source + status>

PRECONDITIONS
- <required capability, access, dependency, or approval>

STEPS
1. <bounded action>
2. <bounded action>
3. <review and validation action>

OUTPUTS
- <artifact or change at canonical path>
- <evidence or report>

VALIDATION
- <command, check, review, or acceptance criterion>

STOP CONDITIONS
- <authority conflict>
- <missing critical input or access>
- <scope, security, or irreversible-risk boundary>

FAILURE REPORT
State what succeeded, what failed, evidence, impact, and the exact recovery action required.
```

## Assembly Rules

- Satu task menghasilkan satu outcome logis yang dapat direview.
- Task tidak boleh memperluas scope session.
- Langkah validasi wajib menghasilkan evidence, bukan hanya klaim.
- Task berstatus gagal atau blocked tidak boleh dilaporkan sebagai completed.
- Perubahan yang ditemukan di luar scope dicatat sebagai rekomendasi, bukan dikerjakan diam-diam.
