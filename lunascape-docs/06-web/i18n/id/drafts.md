# Menyimpan draf

Saat Anda mengedit dokumen di penampil Web, perubahan tidak ditulis ke repositori, melainkan disimpan di dalam browser sebagai "draf".

## Membuat draf

1. Buka dokumen, lalu tekan [Edit] di kanan bawah.
2. Edit, lalu tekan [Simpan].
   "Disimpan sebagai draf" akan ditampilkan dan perubahan tersimpan di dalam browser.

- Dokumen yang memiliki draf diberi lencana di INDEX. Di atas isi teks ditampilkan "Dokumen ini adalah draf di perangkat ini (belum dipublikasikan)".
- [Draf] pada bilah alat menampilkan jumlahnya, dan menekannya akan membuka daftar draf.

## Membuang draf

- Untuk membuang draf satu dokumen, tekan [Buang draf] di atas isi teks.
- Untuk membuang semuanya, lakukan dari daftar draf.

## Menerapkan ke repositori

"Permintaan publikasi", yang mengirim draf sebagai Pull Request, sudah diterapkan tetapi belum diaktifkan pada penampil publik. Untuk menerapkan perubahan ke repositori, editlah dengan versi VS Code atau pada klona di komputer Anda.

> **Perhatian**
>
> - Draf disimpan di browser (IndexedDB). Draf tidak terbawa ke browser lain atau perangkat lain. Jika Anda menghapus data situs pada browser, draf pun ikut terhapus.
> - Jika dokumen di sisi repositori diperbarui setelah Anda membuat draf, akan ditampilkan "Sumber hulu telah diperbarui". Periksa isinya, lalu putuskan apakah akan membuang draf atau tetap menggunakannya.
> - Jika Anda membuka folder lokal dari [Buka dokumen] dan mengeditnya, perubahan disimpan langsung ke berkas apabila browser mendukungnya. Pada browser yang tidak mendukung, perubahan hanya bertahan selama sesi tersebut.

## Topik terkait

- [Yang dapat dilakukan versi Web](README.md)
- [Mengedit dokumen](../03-editing/README.md)
