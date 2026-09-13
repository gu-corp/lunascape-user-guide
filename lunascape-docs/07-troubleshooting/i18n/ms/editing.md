# Tidak boleh mengedit, menyimpan atau menyusun semula

## Butang [Edit] tiada

- [Butang edit] dalam [Tetapan paparan] dimatikan. Hidupkannya, atau gunakan [⋯] → [Edit] di bahagian kanan atas teks, atau menu item INDEX → [Edit].
- Perkara yang sama berlaku apabila `editor.showEditButton` dalam `lunascape-docs.json` ialah `false`.
- Pengeditan tidak boleh dilakukan semasa bantuan dipaparkan. Tutup bantuan.

## Tidak boleh bertukar kepada paparan visual

"Dokumen ini mengandungi sintaks MDX, jadi tidak boleh bertukar kepada skrin pengeditan biasa": dokumen yang mengandungi sintaks khusus MDX (komponen, `import` dan sebagainya) diedit dalam paparan Markdown sahaja, untuk mengekalkan sintaks tersebut.

## Rumus matematik atau rajah tidak boleh diedit secara terus

Paparan visual menunjukkan hasil paparan. Tekan [Markdown] pada skrin pengeditan dan edit sumbernya.

## Tidak boleh menyusun semula atau menyeret

- Penyusunan semula tidak boleh dilakukan semasa penapisan, semasa dokumen sedang diedit, dan semasa operasi INDEX yang lain sedang diproses.
- Apabila ruang kerja tidak dipercayai, operasi mencipta, menyusun dan memadam tidak boleh digunakan. Percayai ruang kerja itu dalam VS Code.
- "INDEX telah dikemas kini. Sila seret sekali lagi": satu perubahan lain baru sahaja diterapkan. Ulang operasi itu.
- Halaman permulaan (`README.md` pada akar) tidak boleh dialihkan.

## "Terdapat perubahan yang belum disimpan" dipaparkan

Fail berkenaan sedang diedit dalam editor VS Code. Simpan dahulu atau buang perubahan itu, kemudian cuba lagi.

## Tidak boleh menukar nama

Nama berikut tidak boleh digunakan.

- Nama yang bermula dengan `.`, `i18n`, dan nama simpanan Windows (`CON` dan sebagainya)
- Nama yang berakhir dengan noktah atau ruang kosong, dan nama yang mengandungi aksara kawalan atau aksara yang tidak boleh digunakan dalam nama fail
- Nama yang sudah wujud dalam folder yang sama (termasuk nama yang berbeza pada huruf besar dan huruf kecil sahaja)
- Nama dokumen tanpa sambungan fail Markdown

## Sudah disimpan tetapi perubahan tidak muncul dalam Git atau tidak dikomit

Lunascape Docs hanya menulis ke dalam fail, dan tidak melakukan pementasan atau komit dalam Git. Semak dalam paparan kawalan sumber VS Code dan komit apabila perlu.

## Perkara berkaitan

- [Mengedit dokumen](../03-editing/README.md)
- [Mencipta dan menyusun dokumen dan folder](../03-editing/organize.md)
- [Menukar susunan dokumen](../03-editing/reorder.md)
