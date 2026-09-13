# Daftar status dan catatan

Daftar status di bagian atas tab [AI] menunjukkan keadaan terjemahan untuk setiap bahasa yang didukung. Tanpa menggunakan AI pun, Anda dapat memeriksa apa saja yang masih kurang.

| Tampilan | Arti |
|---|---|
| Belum diterjemahkan | Jumlah dokumen yang belum memiliki versi terjemahan |
| Perlu diperbarui | Jumlah dokumen yang versi terjemahannya ada, tetapi dokumen kanoniknya lebih baru daripada saat dicatat |
| Sudah diterjemahkan | Jumlah versi terjemahan yang mengikuti dokumen kanoniknya |

Daftar status dihitung dengan menelusuri root dokumentasi. AI maupun model bahasa tidak terlibat di dalamnya.

## Memperbarui catatan terjemahan

Untuk menentukan status "Perlu diperbarui", dokumen kanonik dan versi terjemahan pada saat penerjemahan harus dicatat terlebih dahulu. AI tipe sesi menulis berkas secara langsung, sehingga catatan tidak dibuat secara otomatis.

1. Setelah terjemahan selesai dan isinya Anda periksa, tekan [Perbarui catatan terjemahan].
2. Versi terjemahan yang belum memiliki catatan akan dicatat sebagai versi yang sesuai dengan dokumen kanonik saat ini.

Sesi Claude Code dan penyimpanan tipe API mencatatnya secara otomatis (sesi diinstruksikan untuk menggunakan alat MCP `record_translation_freshness`). Tombol ini diperlukan bila Anda menerjemahkan melalui Codex atau obrolan VS Code.

Setelah itu, jika dokumen kanonik diubah, versi terjemahannya akan ditampilkan sebagai "Perlu diperbarui".

> **Perhatian**
>
> - Versi terjemahan yang sudah memiliki catatan tidak ditimpa. Hal ini agar status "Perlu diperbarui" tidak terhapus.
> - Catatan disimpan di `.lunascape-docs/translation-freshness.json`. Yang disimpan hanya jalur relatif, bahasa, hash isi, dan tanggal waktu; isi dokumen tidak disertakan.

## Topik terkait

- [Pekerjaan yang dapat diserahkan](tasks.md)
- [Membaca dalam bahasa lain](../02-reading/languages.md)
