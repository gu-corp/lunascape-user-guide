# Menyemak dokumen

Dengan docs-lint, anda boleh menyemak struktur tajuk, pautan rosak, dokumen atau bab wajib yang tiada, ketakseragaman istilah, keselarasan ID keperluan dan sebagainya. Semakan sentiasa dilakukan ke atas keseluruhan akar dokumentasi.

## Menjalankan semakan

1. Tekan [Alat Dokumen] pada bar alat, kemudian buka tab [Semakan].
2. Tekan [Semak akar dokumentasi].
   Anda juga boleh menjalankannya melalui "Lunascape Docs: Semak akar dokumentasi" dalam Palet Perintah.
3. Semak senarai penemuan.

## Membaca keputusan

- Gunakan [Dokumen ini] / [Semua] di atas senarai untuk menukar julat yang dipaparkan. Julat semakan itu sendiri sentiasa keseluruhan akar dokumentasi.
- Penemuan mempunyai empat tahap: "ralat", "amaran", "maklumat" dan "cadangan". [Alat Dokumen] pada bar alat memaparkan bilangan ralat dan amaran.
- Tekan sesuatu penemuan untuk membuka kedudukan berkenaan dalam sumber Markdown pada editor VS Code.
- Penemuan yang melibatkan keseluruhan akar dokumentasi (seperti dokumen ujian yang tiada) dipaparkan sebagai item "Seluruh akar dokumentasi" dan tidak mempunyai kedudukan.
- Penemuan yang sama turut dipaparkan dalam panel "Masalah" VS Code.

## Perkara yang disemak

Tekan [Semak dan ubah peraturan] untuk melihat senarai semakan yang aktif serta tujuan setiap satu. Perkara utamanya adalah seperti berikut.

| Perkara | Keterangan |
|---|---|
| Struktur tajuk | Terdapat satu H1 dan aras tajuk tidak melompat di pertengahan |
| Pautan dalaman | Dokumen yang dipaut wujud dan tidak keluar daripada akar dokumentasi |
| Bahasa blok kod | Blok kod menyatakan nama bahasa |
| Folder dan dokumen yang diperlukan | Folder dan dokumen yang dituntut oleh profil Standard Pack lengkap |
| Bab yang diperlukan dalam dokumen | Setiap jenis dokumen mempunyai bab yang diperlukan |
| Penyeragaman istilah | Mengesan ungkapan yang perlu dielakkan dan menyarankan istilah yang disyorkan |
| Penamaan dan pertindihan ID keperluan | ID keperluan menepati peraturan penamaan dan tidak ditakrifkan dua kali |
| Keselarasan rujukan ID keperluan | ID keperluan yang dirujuk oleh reka bentuk, ujian dan jadual status benar-benar wujud |
| Padanan keperluan dengan ujian | ID keperluan dirujuk daripada dokumen ujian |

Perkara yang aktif ditentukan oleh Standard Pack dan profil yang dipilih dalam `lunascape-docs.json`, serta oleh `docs-lint.config.json`.

> **Perhatian**
>
> - Apabila dokumen atau tetapan diubah, keputusan sebelumnya menjadi "perlu disemak semula". Ia tidak dianggap lulus secara automatik. Tekan [Semak akar dokumentasi] sekali lagi.
> - Perubahan yang belum disimpan tidak diambil kira dalam semakan. Simpan terlebih dahulu.
> - Semakan dijalankan secara deterministik dalam peranti. Hasil penilaian atau terjemahan oleh AI tidak sekali-kali bercampur dengan keputusan semakan.

## Topik berkaitan

- [Mengubah peraturan semakan](rules.md)
- [Tetapan projek](project-configuration.md)
- [Semakan, penciptaan atau terjemahan tidak berjaya](../07-troubleshooting/tools.md)
