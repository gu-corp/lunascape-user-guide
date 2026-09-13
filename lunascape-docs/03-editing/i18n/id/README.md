# Menyunting dokumen

Dokumen dapat disunting langsung di dalam penampil. Layar penyuntingan memiliki "tampilan visual" yang menyunting apa adanya seperti yang terlihat dan "tampilan sumber Markdown"; keduanya dialihkan dengan satu tombol.

## Memulai penyuntingan

Tekan salah satu berikut. Semuanya membuka layar penyuntingan yang sama.

- [Edit] di kanan bawah isi dokumen
- [⋯] (tindakan lainnya) di kanan atas isi dokumen → [Edit]
- Menu butir INDEX → [Edit]

## Menyunting

1. Sunting isi dokumen secara langsung.
   Pada bilah alat di bagian atas layar penyuntingan, tersedia format paragraf (isi, judul 1–4, kutipan, kode), [Tebal], [Miring], [Daftar berbutir], [Daftar bernomor], [Tautan], [Sisipkan tabel], [Lebar gambar], [Urungkan], dan [Lakukan lagi].
2. Jika ingin menyunting sumber Markdown secara langsung, tekan [Markdown].
   Tekan sekali lagi untuk kembali ke tampilan visual. Tampilan yang terakhir digunakan akan diingat dan dipulihkan saat Anda menekan [Edit] berikutnya.
3. Tekan [Simpan].
   Berkas Markdown ditulis dan tampilan kembali ke mode baca. Jika ingin membatalkan, tekan [Batal].

> **Catatan**
>
> - Penyimpanan hanya menulis ke berkas. Penahapan (staging) dan komit Git tidak dilakukan secara otomatis.
> - Rumus serta diagram seperti Mermaid, TikZ, dan Vega-Lite ditampilkan sebagai hasil render pada tampilan visual. Untuk mengubah isinya, beralihlah ke [Markdown].
> - Dokumen yang memuat sintaksis khas MDX (komponen, `import`, dan sebagainya) hanya disunting pada tampilan Markdown agar sintaksisnya tetap terjaga.
> - Front matter (pengaturan yang diapit `---` di bagian awal) tetap dipertahankan meskipun disunting pada tampilan visual.

> **Tips**
>
> - Menekan [Buka di VS Code] akan membuka berkas di editor teks biasa. Jika disimpan di editor teks, tampilan penampil juga diperbarui secara otomatis.
> - Jika tidak ingin menampilkan tombol [Edit], matikan [Tombol edit] pada [Pengaturan tampilan]. Untuk menyembunyikannya di seluruh proyek, setel `editor.showEditButton` pada `lunascape-docs.json` menjadi `false`.
> - Tampilan bawaan yang pertama kali dibuka (visual atau Markdown) dapat diubah melalui pengaturan `lunascapeDocEditor.editor.defaultMode` atau `editor.defaultMode` pada `lunascape-docs.json`.

## Topik terkait

- [Membuat dan menata dokumen serta folder](organize.md)
- [Menyesuaikan ukuran gambar](images.md)
- [Menulis rumus](math.md)
- [Menulis diagram dan grafik](diagrams.md)
