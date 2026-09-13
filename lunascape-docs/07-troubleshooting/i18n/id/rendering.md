# Diagram, rumus, atau gambar tidak ditampilkan

## Gambar TikZ tampil sebagai sumber yang terlipat

- Ekstensi versi distribusi tidak menyertakan mesin penggambar TikZ. Tampilan ini normal.
- Untuk keperluan pengembangan dan evaluasi, pasang `node-tikzjax` 1.0.5 tepat di bawah ruang kerja tepercaya, lalu atur `lunascapeDocEditor.tikz.runtime` menjadi `workspace` agar gambar dapat digambar.
- Pada versi peramban Web, TikZ tidak digambar.

## Rumus ditampilkan sebagai teks biasa

- Periksa tanda pembatasnya. Untuk rumus sebaris gunakan `$...$` atau `\(...\)`, dan untuk rumus terpisah gunakan `$$...$$` atau `\[...\]`.
- Tanda `$` di dalam kode sebaris atau blok kode tidak menjadi rumus.
- Penulisan yang tampak seperti nominal uang, misalnya `$5 and $10`, tidak diperlakukan sebagai rumus.
- Rumus yang sangat besar atau yang banyak memerlukan perluasan makro tidak digambar jika melampaui batas (`maxSize: 50`, `maxExpand: 1000`). Pecah menjadi beberapa bagian.

## Diagram menjadi "tidak dapat digambar"

- Pesan galat dari Mermaid, Vega-Lite, WaveDrom, dan lainnya menunjukkan masalah sintaksisnya. Periksa sumbernya pada layar penyuntingan dengan [Markdown].
- Vega-Lite: sematkan data pada `data.values` atau `datasets`. Data dari URL eksternal dan tanda gambar tidak dapat digunakan.
- WaveDrom: tulis dalam JSON yang ketat. Bentuk JavaScript (misalnya kunci tanpa tanda kutip) tidak dapat digunakan.
- Penrose: gunakan hanya `@preset set-theory` di baris awal dan pernyataan yang diizinkan (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- "SVG yang dihasilkan memuat referensi yang tidak aman" / "SVG yang dihasilkan melampaui batas": diagram yang memuat referensi ke sumber daya eksternal, atau yang terlalu besar, tidak ditampilkan. Kurangi isinya atau hapus referensinya.

## Gambar tidak ditampilkan

- Tentukan jalur gambar sebagai jalur relatif dari dokumen. Gambar yang berada di luar root dokumentasi tidak ditampilkan.
- Atribut `width` pada `<img>` hanya menerima angka (`width="360"`).

## Diagram tidak tampil pada situs Web hasil ekspor

Pustaka penggambar untuk TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob, dan Penrose dimuat saat ditampilkan. Tempatkan juga folder `vendor/` bersama situs hasil ekspor.

## Topik terkait

- [Menulis rumus](../03-editing/math.md)
- [Menulis diagram dan grafik](../03-editing/diagrams.md)
- [Menyesuaikan ukuran gambar](../03-editing/images.md)
