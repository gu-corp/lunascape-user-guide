# Menulis rumus

Rumus ditulis dengan notasi TeX dan digambarkan di dalam perangkat menggunakan KaTeX. Jaringan tidak digunakan.

## Cara penulisan

| Jenis | Notasi | Contoh |
|---|---|---|
| Rumus sebaris (di dalam kalimat) | `$...$` atau `\(...\)` | `Hubungan massa dan energi dinyatakan dengan $E = mc^2$.` |
| Rumus tampilan (pada baris tersendiri) | `$$...$$` atau `\[...\]` | Lihat di bawah |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Spasi di sekitar tanda pembatas tidak diperlukan. Rumus yang langsung berdampingan dengan teks Jepang, seperti `値は$V=-H$である`, tetap dikenali.
- Tanda `$` di dalam kode sebaris atau blok kode tidak diperlakukan sebagai rumus dan ditampilkan apa adanya.
- Penulisan yang menyerupai nominal uang seperti `$5 and $10` tidak dijadikan rumus.

## Menyunting

Pada tampilan visual, rumus ditampilkan sebagai hasil penggambarannya. Untuk mengubah isinya, tekan [Markdown] pada layar penyuntingan lalu sunting sumbernya. Menyimpan dari tampilan visual tetap mempertahankan sumber TeX dan bentuk tanda pembatas aslinya (`$` atau `\(`).

> **Perhatian**
>
> - Demi keamanan, KaTeX berjalan dengan `trust: false` serta memiliki batas ukuran (`maxSize: 50`) dan jumlah pengembangan makro (`maxExpand: 1000`). Rumus yang melampaui batas ini tidak digambarkan.
> - Pada dokumen yang sudah ada, `tikzpicture` yang ditulis di dalam `$$...$$` atau `\[...\]` dikenali sebagai diagram TikZ, bukan sebagai rumus.

## Topik terkait

- [Menulis diagram dan grafik](diagrams.md)
- [Diagram, rumus, atau gambar tidak tampil](../07-troubleshooting/rendering.md)
