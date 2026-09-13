# Lejar dan rekodnya

Lejar di bahagian atas tab [AI] ialah keadaan terjemahan bagi setiap bahasa yang disokong. Ia berguna tanpa AI: ia menunjukkan apa yang masih kurang.

| Paparan | Maksud |
|---|---|
| Belum diterjemah | Bilangan dokumen yang belum mempunyai versi terjemahan |
| Perlu dikemas kini | Bilangan dokumen yang mempunyai versi terjemahan, tetapi dokumen kanoniknya lebih baharu daripada rekod |
| Sudah diterjemah | Bilangan versi terjemahan yang mengikut dokumen kanoniknya |

Lejar dikira dengan mengimbas akar dokumentasi. Tiada AI dan tiada model bahasa terlibat.

## Mengemas kini rekod terjemahan

Untuk menentukan "Perlu dikemas kini", rekod dokumen kanonik dan versi terjemahan pada waktu ia diterjemahkan perlu disimpan. AI jenis sesi menulis fail secara terus, jadi rekod tidak dibuat secara automatik.

1. Setelah terjemahan selesai dan kandungannya disemak, tekan [Kemas kini rekod terjemahan].
2. Versi terjemahan yang tiada rekod akan direkodkan sebagai sepadan dengan dokumen kanonik semasa.

Sesi Claude Code dan simpanan penyedia jenis API merekodkannya secara automatik (sesi diarahkan menggunakan alat MCP `record_translation_freshness`). Butang ini diperlukan apabila anda menterjemah dengan Codex atau sembang VS Code.

Selepas itu, apabila dokumen kanonik diubah, versi terjemahannya akan dipaparkan sebagai "Perlu dikemas kini".

> **Perhatian**
>
> - Versi terjemahan yang sudah mempunyai rekod tidak ditulis ganti. Ini supaya keadaan "Perlu dikemas kini" tidak terpadam.
> - Rekod disimpan dalam `.lunascape-docs/translation-freshness.json`. Yang disimpan hanyalah laluan relatif, bahasa, cincangan kandungan dan tarikh masa — teks dokumen tidak disertakan.

## Topik berkaitan

- [Kerja yang boleh diserahkan](tasks.md)
- [Membaca dalam bahasa lain](../02-reading/languages.md)
