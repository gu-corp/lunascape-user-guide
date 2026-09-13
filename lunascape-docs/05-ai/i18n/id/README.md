# Menyerahkan pekerjaan kepada AI

Lunascape Docs tidak memanggil model bahasa. Produk ini menyiapkan **konteks, alat, dan pemeriksaan**, lalu menyerahkan pelaksanaan terjemahan, koreksi, dan penulisan kepada AI yang Anda gunakan.

## Cara berpikirnya

| Yang disediakan produk | Isi |
|---|---|
| Konteks | Konvensi dokumen (tempat versi terjemahan disimpan, front matter, standar dokumen, glosarium) dan letak dokumen sasaran |
| Alat kerja | Buku besar dokumen yang belum diterjemahkan dan yang perlu diperbarui, membaca dan menulis dokumen, pembuatan dari templat |
| Pemeriksaan setelahnya | Verifikasi dengan docs-lint, selisih cakupan dan kesegaran |

Teks instruksi tidak memuat isi dokumen. AI membaca berkasnya sendiri, menulisnya sendiri, dan memverifikasinya sendiri.

## Menyerahkan pekerjaan

1. Tekan [Alat Dokumen] pada bilah alat, lalu buka tab [AI].
2. Pilih pekerjaan yang ingin diserahkan dari [Tugas].
3. Isi bagian yang diperlukan (bahasa sasaran, pokok bahasan).
4. Tekan [Serahkan tugas ini].
   Terminal VS Code terbuka dan AI yang Anda pilih menerima instruksi lalu mulai bekerja.

> **Tips**
>
> Sesi Claude Code disertai alat kerja (server MCP `lunascape-docs`). Sesi tersebut dapat mengambil sendiri daftar dokumen yang belum diterjemahkan dan yang perlu diperbarui, menjalankan docs-lint, serta mencatat kesegaran setelah penerjemahan.

## Memeriksa hasilnya

| Bentuk penyedia | Tempat hasil mendarat |
|---|---|
| Tipe sesi (Claude Code, Codex) | Menulis langsung ke pohon kerja. **Periksa melalui perbedaan Git** |
| Tipe API (model bahasa VS Code, Anthropic, kompatibel OpenAI) | Mengembalikan usulan satu dokumen demi satu dokumen. Periksa dengan [Buka perbedaan], lalu tulis dengan [Simpan] |

### Memeriksa usulan dari tipe API

Bila dijalankan dengan tipe API, usulan akan sampai di tab [AI].

1. Tekan [Buka perbedaan] dan periksa bedanya dengan isi saat ini.
2. Jika sudah sesuai, tekan [Simpan]. Untuk terjemahan, kesegarannya juga dicatat. Bila ingin membatalkan, tekan [Buang].
   Untuk menghentikan pembuatan di tengah jalan, tekan [Hentikan].

> **Catatan**
>
> - Lunascape Docs tidak pernah melakukan staging atau commit pada Git. Selalu periksa perubahan melalui perbedaan.
> - Pada ruang kerja yang tidak tepercaya, dan pada tampilan folder sementara di luar root dokumentasi, pekerjaan tidak dapat diserahkan.

## Topik terkait

- [Pekerjaan yang dapat diserahkan](tasks.md)
- [Pengaturan AI](settings.md)
- [Buku besar dan catatannya](ledger.md)
