# Menyunting dokumen

Dokumen dapat disunting langsung di dalam viewer. Layar penyuntingan memiliki "tampilan visual", tempat Anda menyunting apa yang Anda lihat, dan "tampilan sumber Markdown"; satu tombol beralih di antara keduanya.

## Mulai menyunting

Tekan salah satu dari berikut. Semuanya membuka layar penyuntingan yang sama.

- [Edit] di kanan bawah dokumen
- [⋯] (tindakan lainnya) di kanan atas dokumen → [Edit]
- Menu item INDEX → [Edit]

## Menyunting

1. Sunting teks secara langsung.
   Pada bilah alat di bagian atas layar penyuntingan, Anda dapat menggunakan format paragraf (teks isi, judul 1–4, kutipan, kode), [Tebal], [Miring], [Daftar berbutir], [Daftar bernomor], [Tautan], [Sisipkan tabel], [Lebar gambar], [Urungkan], dan [Lakukan lagi].
2. Jika ingin menyunting sumber Markdown secara langsung, tekan [Markdown].
   Tekan sekali lagi untuk kembali ke tampilan visual. Tampilan yang terakhir Anda gunakan diingat dan dipulihkan saat berikutnya Anda menekan [Edit].
3. Tekan [Simpan] (juga dapat disimpan dengan Ctrl+S/⌘S).
   Berkas Markdown ditulis dan viewer kembali ke tampilan baca. Untuk berhenti menyunting dan kembali ke isi yang terakhir disimpan, tekan [Discard edits].

## Selalu mulai dari layar penyuntingan (mode edit)

Tekan [Edit mode] pada bilah alat untuk mengaktifkannya: setiap kali Anda membuka dokumen, Anda akan mulai dari layar penyuntingan. Gunakan ini ketika Anda ingin terus menulis seperti pada buku catatan.

- Selama aktif, menekan [Simpan] tidak menutup layar penyuntingan. [Discard edits] mengembalikan ke isi yang terakhir disimpan dan membiarkan layar penyuntingan tetap terbuka.
- Tekan sekali lagi untuk menonaktifkannya dan kembali ke tampilan baca. Status aktif/nonaktif diingat per pengguna.
- Tidak ditampilkan pada root dokumentasi yang tidak dapat ditulisi (seperti sumber GitHub yang hanya-baca).

## Suntingan yang belum disimpan

Suntingan yang belum disimpan otomatis dipertahankan di perangkat ini. Suntingan tidak hilang meskipun Anda berpindah ke dokumen lain, atau menutup tab atau jendela.

- [Unsaved] di layar penyuntingan menunjukkan bahwa ada perbedaan dengan isi yang terakhir disimpan.
- Saat berikutnya membuka dokumen yang sama, penyuntingan dilanjutkan dari suntingan yang dipertahankan, dan hal ini diberitahukan kepada Anda. Jika dokumen aslinya telah diperbarui sejak itu, hal itu juga diberitahukan. Anda dapat kembali ke isi terbaru dengan [Discard edits].
- Suntingan yang dipertahankan hilang dengan [Simpan] atau [Discard edits]. Karena belum disimpan, suntingan tidak muncul di Git maupun di draf.

> **Catatan**
>
> - Menyimpan hanya menulis ke berkas. Staging dan commit Git tidak dilakukan secara otomatis.
> - Diagram seperti rumus, Mermaid, TikZ, dan Vega-Lite ditampilkan sebagai hasil render pada tampilan visual. Untuk mengubah isinya, beralihlah ke [Markdown].
> - Dokumen yang memuat sintaks khas MDX (seperti komponen atau `import`) disunting hanya pada tampilan Markdown, untuk menjaga sintaks tersebut.
> - front matter (pengaturan yang diapit `---` di bagian awal) dipertahankan meskipun Anda menyuntingnya pada tampilan visual.

> **Tip**
>
> - Menekan [Buka di VS Code] membuka berkas di editor teks biasa. Ketika Anda menyimpan di editor teks, tampilan viewer juga diperbarui secara otomatis.
> - Jika tidak ingin menampilkan tombol [Edit], nonaktifkan [Tombol edit] di [Pengaturan tampilan]. Untuk menyembunyikannya di seluruh proyek, atur `editor.showEditButton` menjadi `false` di `lunascape-docs.json`.
> - Tampilan awal yang pertama kali terbuka (visual/Markdown) dapat diubah lewat pengaturan `lunascapeDocEditor.editor.defaultMode` atau `editor.defaultMode` di `lunascape-docs.json`.

## Lihat juga

- [Membuat dan menata dokumen serta folder](organize.md)
- [Menyesuaikan ukuran gambar](images.md)
- [Menulis rumus](math.md)
- [Menulis diagram dan grafik](diagrams.md)
