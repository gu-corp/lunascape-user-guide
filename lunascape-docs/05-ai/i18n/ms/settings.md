# Tetapan AI

Pilih AI dan model yang akan menerima kerja anda. Skrin ini menggunakan menu juntai bawahnya sendiri, bukan pemilih pantas VS Code.

1. Tekan [Alat Dokumen] → tab [AI] → [Tetapan AI…].
2. Pilih [Pembekal].
   Pembekal yang tidak boleh digunakan pada persekitaran ini dipaparkan dalam keadaan tidak boleh dipilih, berserta sebabnya.
3. Pilih [Model]. Pilihan berubah mengikut pembekal.
4. Tutup skrin. Pilihan disimpan bagi setiap pengguna dan digunakan semula pada kali berikutnya.

## Pembekal

| Pembekal | Bentuk | Cara pengesanan |
|---|---|---|
| Claude Code | Jenis sesi | Kewujudan perintah `claude` |
| Codex | Jenis sesi | Kewujudan perintah `codex` |
| Model bahasa VS Code | Jenis API | Model yang didaftarkan pada VS Code Language Model API |
| Anthropic API | Jenis API | Pendaftaran kunci API |
| API serasi OpenAI | Jenis API | Pendaftaran kunci API dan titik akhir |

**Jenis sesi** membaca dan menulis fail sendiri, serta menjalankan semakan dokumen sendiri. Hasilnya ditulis terus ke dalam pokok kerja dan disemak melalui beza Git.

**Jenis API** memulangkan Markdown bagi satu dokumen, dan sambungan menunjukkan bezanya sebelum menyimpan.

## Mendaftarkan kunci API

Anthropic API dan API serasi OpenAI boleh digunakan setelah kunci API didaftarkan.

1. Pilih destinasi pendaftaran pada [Pembekal]. Medan kunci API dipaparkan.
2. Masukkan [Kunci API]. Bagi API serasi OpenAI, masukkan juga [Titik akhir] (contohnya `https://api.openai.com/v1`).
3. Tekan [Simpan]. "Kunci telah didaftarkan" dipaparkan.

> **Perhatian**
>
> - Kunci disimpan dalam SecretStorage VS Code dan tidak dipaparkan semula. Kunci juga tidak sekali-kali ditulis ke dalam `settings.json` atau mana-mana dokumen. Ia boleh dipadamkan dengan [Padam kunci].
> - Senarai model diambil daripada setiap perkhidmatan menggunakan kunci yang didaftarkan. Selagi senarai itu belum diperoleh, senarai yang sedia diketahui dipaparkan.
> - Kerja yang boleh dijalankan dengan jenis API hanyalah "Terjemah halaman ini" dan "Baca pruf halaman ini". Untuk menyusuri beberapa dokumen dan mencipta dokumen, gunakan jenis sesi.

> **Petua**
>
> Jika tiada pembekal ditemui, pasang Claude Code atau Codex, atau daftarkan kunci API. Buka semula [Tetapan AI…] dan ia akan dikesan.

## Topik berkaitan

- [Menyerahkan kerja kepada AI](README.md)
- [Senarai tetapan VS Code](../08-reference/settings.md)
