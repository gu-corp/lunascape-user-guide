# Pengaturan AI

Pilih AI dan model yang menerima pekerjaan Anda. Layar ini memakai menu turun miliknya sendiri, bukan quick pick VS Code.

1. Tekan [Alat Dokumen] → tab [AI] → [Pengaturan AI…].
2. Pilih [Penyedia].
   Penyedia yang tidak dapat dipakai di lingkungan ini muncul dalam keadaan tidak dapat dipilih, disertai alasannya.
3. Pilih [Model]. Pilihannya berbeda untuk setiap penyedia.
4. Tutup layar. Pilihan disimpan per pengguna dan dipakai lagi berikutnya.

## Penyedia

| Penyedia | Bentuk | Cara deteksi |
|---|---|---|
| Claude Code | Sesi | Ada tidaknya perintah `claude` |
| Codex | Sesi | Ada tidaknya perintah `codex` |
| Model bahasa VS Code | API | Model yang terdaftar pada VS Code Language Model API |
| Anthropic API | API | Kunci API yang terdaftar |
| API yang kompatibel dengan OpenAI | API | Kunci API dan endpoint yang terdaftar |

Penyedia **sesi** membaca dan menulis berkas sendiri, serta menjalankan pemeriksaan dokumen sendiri. Hasilnya ditulis langsung ke pohon kerja dan diperiksa lewat diff Git.

Penyedia **API** mengembalikan Markdown untuk satu dokumen, lalu ekstensi menampilkan diff sebelum menyimpannya.

## Mendaftarkan kunci API

Anthropic API dan API yang kompatibel dengan OpenAI dapat dipakai setelah kunci API didaftarkan.

1. Pilih tujuan pendaftaran pada [Penyedia]. Kolom isian kunci API akan muncul.
2. Masukkan [Kunci API]. Untuk API yang kompatibel dengan OpenAI, masukkan juga [Endpoint] (misalnya `https://api.openai.com/v1`).
3. Tekan [Simpan]. Akan tampil "Kunci terdaftar".

> **Catatan**
>
> - Kunci disimpan di SecretStorage milik VS Code dan tidak ditampilkan kembali. Kunci juga tidak pernah ditulis ke `settings.json` atau ke dokumen mana pun. Kunci dapat dihapus dengan [Hapus kunci].
> - Daftar model diambil dari setiap layanan memakai kunci yang telah didaftarkan. Selama daftar itu belum diperoleh, daftar yang sudah dikenal ditampilkan.
> - Pekerjaan yang dapat dijalankan penyedia API hanya "Terjemahkan halaman ini" dan "Koreksi halaman ini". Penelusuran beberapa dokumen dan pembuatan dokumen harus dijalankan dengan penyedia sesi.

> **Tips**
>
> Bila tidak ada satu pun penyedia yang ditemukan, pasang Claude Code atau Codex, atau daftarkan kunci API. Buka kembali [Pengaturan AI…] dan penyedia akan terdeteksi.

## Topik terkait

- [Menyerahkan pekerjaan kepada AI](README.md)
- [Daftar pengaturan VS Code](../08-reference/settings.md)
