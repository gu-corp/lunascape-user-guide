# Tidak bisa mengedit, menyimpan, atau mengubah urutan

## Tombol [Edit] tidak ada

- [Tombol edit] pada [Pengaturan tampilan] dalam keadaan nonaktif. Aktifkan tombol tersebut, atau gunakan [⋯] → [Edit] di kanan atas isi dokumen, atau menu item INDEX → [Edit].
- Hal yang sama berlaku bila `editor.showEditButton` pada `lunascape-docs.json` bernilai `false`.
- Pengeditan tidak dapat dilakukan selama Bantuan ditampilkan. Tutup Bantuan terlebih dahulu.

## Tidak bisa beralih ke tampilan visual

"Dokumen ini berisi sintaks MDX sehingga tidak dapat dialihkan ke layar edit biasa": dokumen yang berisi sintaks khusus MDX (komponen, `import`, dan sebagainya) hanya diedit dalam tampilan Markdown agar sintaksnya tetap terjaga.

## Tidak bisa mengedit rumus atau diagram secara langsung

Tampilan visual menampilkan hasil penggambaran. Tekan [Markdown] pada layar edit, lalu edit sumbernya.

## Tidak bisa mengubah urutan atau menyeret

- Urutan tidak dapat diubah selama penyaringan, selama dokumen sedang diedit, dan selama operasi INDEX lain sedang diproses.
- Bila ruang kerja tidak dipercaya, operasi pembuatan, penataan, dan penghapusan tidak dapat digunakan. Jadikan ruang kerja tersebut tepercaya di VS Code.
- "INDEX telah diperbarui. Seret sekali lagi": perubahan lain baru saja diterapkan. Ulangi operasinya.
- Halaman awal (`README.md` di root) tidak dapat dipindahkan.

## Muncul pesan "Ada perubahan yang belum disimpan"

Berkas yang dimaksud sedang diedit di editor VS Code. Simpan terlebih dahulu, atau buang perubahannya, lalu coba lagi.

## Tidak bisa mengubah nama

Nama berikut tidak dapat digunakan.

- Nama yang diawali `.`, `i18n`, dan nama yang dicadangkan Windows (seperti `CON`)
- Nama yang diakhiri titik atau spasi, serta nama yang mengandung karakter kontrol atau karakter yang tidak dapat dipakai pada nama berkas
- Nama yang sudah ada di folder yang sama (termasuk nama yang hanya berbeda huruf besar-kecilnya)
- Nama dokumen tanpa ekstensi Markdown

## Sudah disimpan, tetapi perubahan tidak muncul di Git atau tidak terkomit

Lunascape Docs hanya menulis ke berkas, dan tidak melakukan staging maupun komit di Git. Periksa pada tampilan Source Control di VS Code, lalu komit bila perlu.

## Topik terkait

- [Mengedit dokumen](../03-editing/README.md)
- [Membuat dan menata dokumen dan folder](../03-editing/organize.md)
- [Mengubah urutan dokumen](../03-editing/reorder.md)
