# Menulis rumus matematik

Rumus matematik ditulis dengan tatatanda TeX dan dipaparkan pada peranti anda menggunakan KaTeX. Rangkaian tidak digunakan.

## Cara penulisan

| Jenis | Tatatanda | Contoh |
|---|---|---|
| Rumus dalam baris (dalam ayat) | `$...$` atau `\(...\)` | `Hubungan antara jisim dan tenaga ialah $E = mc^2$.` |
| Rumus paparan (pada baris tersendiri) | `$$...$$` atau `\[...\]` | Lihat di bawah |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Ruang kosong tidak diperlukan sebelum atau selepas pembatas. Rumus yang bersebelahan terus dengan teks Jepun, seperti `値は$V=-H$である`, tetap dikenali.
- Tanda `$` di dalam kod dalam baris atau blok kod tidak dianggap sebagai rumus dan dipaparkan sebagaimana adanya.
- Penulisan yang menyerupai mata wang seperti `$5 and $10` tidak dianggap sebagai rumus.

## Menyunting

Dalam paparan visual, rumus dipaparkan sebagai hasil yang telah dilukis. Untuk mengubah kandungannya, tekan [Markdown] pada skrin penyuntingan dan sunting sumbernya. Menyimpan daripada paparan visual mengekalkan sumber TeX dan bentuk pembatas asal (`$` atau `\(`) tanpa perubahan.

> **Perhatian**
>
> - Demi keselamatan, KaTeX berjalan dengan `trust: false` serta mempunyai had saiz (`maxSize: 50`) dan had bilangan pengembangan makro (`maxExpand: 1000`). Rumus yang melebihi had ini tidak dipaparkan.
> - `tikzpicture` yang ditulis di dalam `$$...$$` atau `\[...\]` pada dokumen sedia ada dikenali sebagai rajah TikZ, bukan sebagai rumus matematik.

## Topik berkaitan

- [Menulis rajah dan carta](diagrams.md)
- [Rajah, rumus matematik atau imej tidak dipaparkan](../07-troubleshooting/rendering.md)
