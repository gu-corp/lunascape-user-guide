# Menyunting dokumen

Dokumen boleh disunting terus di dalam pemapar. Skrin penyuntingan mempunyai "paparan visual" yang menyunting apa yang anda lihat, dan "paparan sumber Markdown"; satu butang bertukar antara kedua-duanya.

## Mula menyunting

Tekan mana-mana yang berikut. Kesemuanya membuka skrin penyuntingan yang sama.

- [Edit] di bahagian bawah kanan dokumen
- [⋯] (Tindakan lain) di bahagian atas kanan dokumen → [Edit]
- Menu item INDEX → [Edit]

## Menyunting

1. Sunting teks secara terus.
   Bar alat di bahagian atas skrin penyuntingan menyediakan format perenggan (badan, tajuk 1–4, petikan, kod), [Tebal], [Condong], [Senarai berbulet], [Senarai bernombor], [Pautan], [Sisip jadual], [Saiz imej], [Buat asal] dan [Buat semula].
2. Apabila anda mahu menyunting sumber Markdown secara terus, tekan [Markdown].
   Tekan sekali lagi untuk kembali ke paparan visual. Paparan yang terakhir digunakan diingati dan dipulihkan pada kali seterusnya anda menekan [Edit].
3. Tekan [Simpan] (boleh juga simpan dengan Ctrl+S／⌘S).
   Fail Markdown ditulis dan pemapar kembali ke paparan bacaan. Untuk berhenti menyunting dan kembali ke kandungan yang terakhir disimpan, tekan [Discard edits].

## Sentiasa mula dari skrin penyuntingan (mod edit)

Tekan [Mod edit] pada bar alat untuk menghidupkannya: setiap kali dokumen dibuka, ia bermula dari skrin penyuntingan. Gunakannya apabila anda menulis berterusan seperti buku nota.

- Semasa ia dihidupkan, menekan [Simpan] tidak menutup skrin penyuntingan. [Discard edits] mengembalikan kandungan yang terakhir disimpan dan mengekalkan skrin penyuntingan.
- Tekan sekali lagi untuk mematikannya dan kembali ke paparan bacaan. Pilihan hidup／mati diingati bagi setiap pengguna.
- Ia tidak dipaparkan pada akar dokumentasi yang tidak boleh ditulis, seperti sumber GitHub baca sahaja.

## Suntingan yang belum disimpan

Suntingan yang belum anda simpan dikekalkan secara automatik pada peranti ini. Berpindah ke dokumen lain, atau menutup tab atau tetingkap, tidak menghilangkannya.

- [Unsaved] dalam skrin penyuntingan menunjukkan terdapat perbezaan dengan kandungan yang terakhir disimpan.
- Kali seterusnya anda membuka dokumen yang sama, ia disambung semula daripada suntingan yang dikekalkan dan memberitahu anda tentang hal itu. Jika dokumen asal telah dikemas kini selepas itu, ia turut memberitahu anda. [Discard edits] boleh mengembalikan kandungan terkini.
- Suntingan yang dikekalkan hilang dengan [Simpan] atau [Discard edits]. Oleh sebab ia belum disimpan, ia tidak muncul dalam Git atau dalam draf.

> **Nota**
>
> - Menyimpan hanya menulis ke fail. Pemetakan (staging) dan komit Git tidak dilakukan secara automatik.
> - Rumus matematik dan rajah seperti Mermaid, TikZ dan Vega-Lite dipaparkan sebagai hasil lukisan dalam paparan visual. Untuk menukar kandungannya, beralih ke [Markdown].
> - Dokumen yang mengandungi sintaks khusus MDX (komponen, `import` dan seumpamanya) disunting dalam paparan Markdown sahaja, untuk mengekalkan sintaks tersebut.
> - Front matter (tetapan yang dikelilingi oleh `---` di bahagian atas) dikekalkan walaupun disunting dalam paparan visual.

> **Petua**
>
> - [Buka dalam VS Code] membuka fail dalam editor teks biasa. Menyimpan dalam editor teks turut mengemas kini paparan pemapar secara automatik.
> - Apabila anda tidak mahu memaparkan butang [Edit], matikan [Butang edit] dalam [Tetapan paparan]. Untuk menyembunyikannya bagi keseluruhan projek, tetapkan `editor.showEditButton` kepada `false` dalam `lunascape-docs.json`.
> - Paparan yang mula-mula dibuka (visual／Markdown) secara lalai boleh diubah dengan tetapan `lunascapeDocEditor.editor.defaultMode` atau `editor.defaultMode` dalam `lunascape-docs.json`.

## Lihat juga

- [Mencipta dan menyusun dokumen dan folder](organize.md)
- [Melaraskan saiz imej](images.md)
- [Menulis rumus matematik](math.md)
- [Menulis rajah dan graf](diagrams.md)
