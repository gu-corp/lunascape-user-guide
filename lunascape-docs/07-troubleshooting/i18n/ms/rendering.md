# Rajah, rumus matematik atau imej tidak dipaparkan

## Rajah TikZ dipaparkan sebagai sumber yang dilipat

- Sambungan versi edaran tidak disertakan dengan enjin pemaparan TikZ. Paparan ini memang dijangka.
- Untuk tujuan pembangunan dan penilaian, pasang `node-tikzjax` 1.0.5 terus di bawah ruang kerja dipercayai, kemudian tetapkan `lunascapeDocEditor.tikz.runtime` kepada `workspace`, maka rajah akan dipaparkan.
- Versi pelayar web tidak memaparkan TikZ.

## Rumus matematik dipaparkan sebagai teks biasa

- Semak tanda pemisah. Untuk dalam baris gunakan `$...$` atau `\(...\)`, dan untuk rumus berasingan `$$...$$` atau `\[...\]`.
- Tanda `$` di dalam kod dalam baris atau di dalam blok kod tidak menjadi rumus matematik.
- Penulisan yang kelihatan seperti jumlah wang, seperti `$5 and $10`, tidak dijadikan rumus matematik.
- Rumus yang sangat besar atau yang banyak pengembangan makro tidak dipaparkan apabila melebihi had (`maxSize: 50`, `maxExpand: 1000`). Bahagikannya.

## Rajah memaparkan “tidak dapat dipaparkan”

- Mesej ralat daripada Mermaid, Vega-Lite, WaveDrom dan lain-lain menunjukkan masalah sintaksis. Semak sumbernya dengan [Markdown] pada skrin penyuntingan.
- Vega-Lite: benamkan data dalam `data.values` atau `datasets`. Data daripada URL luaran dan tanda imej tidak boleh digunakan.
- WaveDrom: tulis dalam JSON yang ketat. Bentuk JavaScript (kunci tanpa tanda petik dan seumpamanya) tidak boleh digunakan.
- Penrose: gunakan hanya `@preset set-theory` di bahagian atas serta pernyataan yang dibenarkan (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- “SVG yang dijana mengandungi rujukan yang tidak selamat” atau “SVG yang dijana melebihi had”: rajah yang mengandungi rujukan kepada sumber luaran, atau yang terlalu besar, tidak dipaparkan. Kurangkan kandungannya atau buang rujukan tersebut.

## Imej tidak dipaparkan

- Laluan imej ditentukan secara relatif daripada dokumen. Imej di luar akar dokumentasi tidak dipaparkan.
- `width` pada `<img>` menerima nombor sahaja (`width="360"`).

## Rajah tidak dipaparkan pada tapak web yang dieksport

Pustaka pemaparan untuk TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob dan Penrose dimuatkan semasa paparan. Letakkan folder `vendor/` bersama-sama tapak yang dieksport.

## Topik berkaitan

- [Menulis rumus matematik](../03-editing/math.md)
- [Menulis rajah dan carta](../03-editing/diagrams.md)
- [Melaraskan saiz imej](../03-editing/images.md)
