# Knowledge Domain Architecture

> Status: Struktur aktif; arsitektur domain substantif belum ditambahkan.

## Tujuan

Menyimpan arsitektur informasi dan model dependency untuk domain pengetahuan tertentu. Arsitektur sistem secara keseluruhan tetap berada di [`../KNOWLEDGE_ARCHITECTURE.md`](../KNOWLEDGE_ARCHITECTURE.md).

## Informasi yang Disimpan

- domain map dan information model;
- dependency, upstream, downstream, dan data lineage konseptual;
- boundary, interface pengetahuan, serta ownership map;
- diagram dan rationale yang dapat ditelusuri.

## Aturan Pengelolaan

- Satu arsitektur memiliki scope dan owner yang jelas.
- Diagram harus disertai penjelasan tekstual agar dapat diakses manusia dan AI.
- Jangan menyimpan arsitektur runtime atau implementasi Engineering di sini.
- Perubahan boundary lintas domain wajib direview oleh seluruh owner terdampak dan dicatat pada decision record kanonik.

## Hubungan

Architecture diturunkan dari [`../concepts/`](../concepts/README.md), menggunakan glossary serta references, dan memberi konteks kepada standards, decisions, learning, SAOS, Engineering, dan Products.
