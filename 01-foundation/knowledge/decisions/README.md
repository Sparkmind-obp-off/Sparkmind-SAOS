# Knowledge Decision Context

> Status: Struktur aktif; indeks keputusan substantif belum dikurasi.

## Tujuan

Menyediakan discovery view atas keputusan yang memengaruhi pengetahuan, termasuk konteks, dependency, dan dampaknya, tanpa menjadi decision log tandingan.

## Informasi yang Disimpan

- indeks menuju decision record kanonik;
- decision-to-knowledge mapping;
- impact, dependency, supersession, dan review map;
- ringkasan konteks untuk discovery dengan link sumber.

## Aturan Pengelolaan

- Decision record Foundation tetap berada di [`../../decision-library/`](../../decision-library/README.md); ADR Engineering dan keputusan Products tetap berada di domainnya.
- Ringkasan tidak boleh mengubah decision, status, approval, atau rationale.
- Setiap entri mencantumkan sumber kanonik dan link pengganti bila superseded.
- Keputusan baru tidak boleh dibuat atau disahkan di folder ini.

## Hubungan

Decisions menghubungkan concepts, architecture, standards, best practices, learning, dan onboarding dengan keputusan kanonik. Perubahan keputusan memicu review artefak Knowledge yang bergantung padanya.
