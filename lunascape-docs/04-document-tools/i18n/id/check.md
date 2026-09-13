# Memeriksa dokumen

Dengan docs-lint, Anda dapat memeriksa struktur judul, tautan rusak, dokumen atau bab wajib yang belum ada, ketidakseragaman istilah, kesesuaian ID persyaratan, dan lainnya. Pemeriksaan selalu mencakup seluruh root dokumentasi.

## Menjalankan pemeriksaan

1. Tekan [Alat Dokumen] pada bilah alat, lalu buka tab [Pemeriksaan].
2. Tekan [Periksa root dokumentasi].
   Anda juga dapat menjalankannya melalui "Lunascape Docs: Periksa root dokumentasi" pada Palet Perintah.
3. Periksa daftar hasilnya.

## Membaca hasil

- Gunakan [Dokumen ini] / [Semua] di atas daftar untuk mengganti cakupan yang ditampilkan. Cakupan pemeriksaannya sendiri selalu seluruh root dokumentasi.
- Temuan memiliki empat tingkat: "kesalahan", "peringatan", "informasi", dan "saran". [Alat Dokumen] pada bilah alat menampilkan jumlah kesalahan dan peringatan.
- Tekan sebuah temuan untuk membuka posisi sumber Markdown terkait di editor VS Code.
- Temuan yang menyangkut seluruh root dokumentasi (misalnya dokumen uji yang belum ada) ditampilkan sebagai butir "seluruh root dokumentasi" dan tidak memiliki posisi.
- Temuan yang sama juga ditampilkan pada panel "Masalah" VS Code.

## Hal yang diperiksa

Tekan [Tinjau dan ubah aturan] untuk menampilkan daftar pemeriksaan yang aktif beserta tujuan masing-masing. Butir utamanya adalah sebagai berikut.

| Butir | Isi |
|---|---|
| Struktur judul | Ada tepat satu H1 dan tingkat judul tidak melompat |
| Tautan internal | Dokumen tujuan tautan ada dan tidak keluar dari root dokumentasi |
| Bahasa blok kode | Blok kode mencantumkan nama bahasa |
| Folder dan dokumen yang diperlukan | Folder dan dokumen yang diminta profil Standard Pack sudah lengkap |
| Bab yang diperlukan pada dokumen | Setiap jenis dokumen memiliki bab yang diperlukan |
| Keseragaman istilah | Mendeteksi ungkapan yang dihindari dan mendorong penyeragaman ke istilah yang dianjurkan |
| Penamaan dan duplikasi ID persyaratan | ID persyaratan mengikuti aturan penamaan dan tidak didefinisikan dua kali |
| Kesesuaian rujukan ID persyaratan | ID persyaratan yang dirujuk desain, uji, tabel status, dan lainnya benar-benar ada |
| Kesesuaian persyaratan dan uji | ID persyaratan dirujuk dari dokumen uji |

Butir yang aktif ditentukan oleh Standard Pack dan profil yang dipilih pada `lunascape-docs.json`, serta oleh `docs-lint.config.json`.

> **Perhatian**
>
> - Jika Anda mengubah dokumen atau pengaturan, hasil sebelumnya menjadi "perlu diperiksa ulang". Tidak ada yang otomatis dianggap lulus. Tekan kembali [Periksa root dokumentasi].
> - Perubahan yang belum disimpan tidak tercakup dalam pemeriksaan. Simpan terlebih dahulu.
> - Pemeriksaan dijalankan secara deterministik di perangkat. Hasil penilaian atau terjemahan oleh AI tidak pernah tercampur ke dalam hasil pemeriksaan.

## Topik terkait

- [Mengubah aturan pemeriksaan](rules.md)
- [Pengaturan proyek](project-configuration.md)
- [Pemeriksaan, pembuatan, atau terjemahan tidak berhasil](../07-troubleshooting/tools.md)
