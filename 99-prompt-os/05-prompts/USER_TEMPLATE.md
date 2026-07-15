# User Prompt Template

> Status: Placeholder Draft SPOS-001 — bukan user prompt aktif atau approved.

## Tujuan

Menangkap intent, konteks, preferensi, dan acceptance criteria pengguna tanpa mengubah authority system atau scope session secara implisit.

## Template

```text
REQUEST
<what outcome is requested>

CONTEXT
<verified current state and relevant background>

SOURCE OF TRUTH
- Repository/path: <location>
- Upstream references: <canonical paths>

SCOPE
In scope:
- <item>

Out of scope:
- <item>

DELIVERABLES
- <deliverable and canonical destination>

ACCEPTANCE CRITERIA
- <measurable criterion>

PREFERENCES
- <language, format, or reversible implementation preference>

APPROVAL / RISK NOTES
- <approval already granted, required approval, or explicit risk boundary>
```

## Assembly Rules

- Pisahkan fakta terverifikasi, asumsi, dan preferensi.
- Permintaan pengguna tidak boleh diam-diam mengubah dependency atau status dokumen.
- Jika intent ambigu pada keputusan berisiko tinggi atau irreversible, tandai sebagai clarification atau blocker sesuai governance.
- Objective teknis rinci ditempatkan pada Task Prompt.
