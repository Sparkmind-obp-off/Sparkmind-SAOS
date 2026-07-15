# Documentation Convention

## Tujuan

Menetapkan lifecycle dokumentasi agar setiap dokumen memiliki fungsi, status, sumber keputusan, dan jalur review yang dapat ditelusuri.

## Prinsip

- Documentation First: pahami dan dokumentasikan sebelum implementasi.
- Single Source of Truth: satu aturan atau definisi memiliki satu sumber kanonik.
- Traceability: keputusan penting memiliki alasan, reviewer, dan histori Git.
- Human Oversight: AI dapat menyusun dan meninjau, tetapi tidak mengesahkan keputusan strategis.
- Proportionality: kedalaman dokumen sebanding dengan risiko dan dampak.

## Kategori Dokumen

| Kategori | Contoh | Otoritas |
| --- | --- | --- |
| Kernel/normatif | Vision, Ethics, Canon | Founder atau otoritas yang ditetapkan |
| Foundation | Governance, knowledge, patterns, playbooks | Owner domain; Founder bila strategis |
| Kebijakan repository | Security, Contributing | Maintainer; Founder bila strategis |
| Standar | Naming, Markdown, Commit | Maintainer dengan review |
| Laporan | Session report | Penulis dan reviewer session |
| Referensi | Indeks dan panduan | Owner domain terkait |

## Status Dokumen

- **Draft:** sedang disusun; belum menjadi aturan final.
- **In Review:** siap diperiksa oleh reviewer yang berwenang.
- **Approved:** telah disetujui oleh otoritas yang tepat dan berlaku.
- **Superseded:** digantikan dokumen atau versi lain; pengganti wajib disebutkan.
- **Deprecated:** masih tersedia untuk transisi, tetapi tidak disarankan untuk penggunaan baru.
- **Archived:** dipertahankan hanya untuk histori atau audit.

Status harus ditulis dekat judul jika dokumen belum approved atau jika pembaca dapat salah menganggapnya berlaku.

## Struktur Minimum

Dokumen baru, bila relevan, memuat:

1. judul;
2. status;
3. tujuan;
4. ruang lingkup dan non-scope;
5. isi utama atau keputusan;
6. risiko, batas, atau pertanyaan terbuka;
7. referensi;
8. review checklist.

Tidak semua bagian wajib jika tidak menambah nilai. Jangan mengisi bagian dengan teks generik hanya untuk memenuhi template.

## Sumber dan Keputusan

- Kutipan atau keputusan Founder harus dibedakan dari interpretasi AI.
- Klaim eksternal harus memiliki sumber yang dapat diverifikasi.
- Asumsi diberi label dan tidak boleh berubah menjadi fakta hanya karena diulang.
- Perubahan normatif harus menjelaskan alasan dan dampak.
- Laporan tidak boleh menjadi sumber kanonik baru; hasil penting harus diterapkan ke dokumen yang sesuai.

## Ownership dan Review

Sebelum approved, tentukan:

- owner dokumen;
- reviewer atau otoritas persetujuan;
- pihak yang terdampak;
- kondisi yang memicu review ulang.

Dokumen Kernel yang belum memiliki owner formal tetap menunggu persetujuan Founder dan tidak dianggap final. Artefak Foundation wajib merujuk sumber Kernel terkait dan tidak boleh mengubah statusnya melalui interpretasi downstream. Artefak Knowledge System juga mengikuti [`../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md`](../../01-foundation/knowledge/KNOWLEDGE_GOVERNANCE.md) untuk metadata, verification, approval, deprecation, archiving, dan referensi silang.

## Pemeliharaan

Perbarui dokumentasi ketika:

- makna, struktur, workflow, atau kebijakan berubah;
- link atau referensi menjadi usang;
- ditemukan konflik atau duplikasi;
- status berubah;
- dokumen pengganti diterbitkan.

Perubahan penting dicatat di `CHANGELOG.md`. Gunakan Git untuk histori; jangan membuat salinan `final-v2` atau backup manual di repository.

## Checklist

- [ ] Tujuan dan non-scope jelas.
- [ ] Status sesuai kenyataan.
- [ ] Sumber keputusan dapat ditelusuri.
- [ ] Owner dan reviewer dapat diidentifikasi.
- [ ] Tidak menduplikasi dokumen kanonik.
- [ ] Perubahan terkait telah disinkronkan.
