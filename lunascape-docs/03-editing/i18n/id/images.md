# Menyesuaikan ukuran gambar

Gambar yang ditempatkan dalam dokumen otomatis menyesuaikan dengan lebar isi dan tinggi layar. Untuk gambar yang ingin ditampilkan dengan ukuran tertentu, Anda dapat menentukan lebarnya.

## Cara kerja penyesuaian otomatis

- Gambar Markdown biasa (`![keterangan](./images/screen.png)`) diperkecil agar muat dalam lebar isi. Gambar tidak pernah diperbesar melebihi ukuran aslinya.
- Tangkapan layar yang tinggi dibatasi hingga 72% dari tinggi layar atau 720px, mana yang lebih kecil.

## Menentukan lebar di layar edit

1. Tekan [Edit], lalu pilih gambar pada tampilan visual.
2. Pilih lebar dari [Lebar gambar] pada bilah alat.
3. Tekan [Simpan].

| Pilihan | Lebar |
|---|---|
| [Otomatis] | Tidak ditentukan (penyesuaian otomatis) |
| [Kecil (360px)] | 360px |
| [Sedang (560px)] | 560px |
| [Besar (760px)] | 760px |
| [Lebar isi (920px)] | 920px |
| [Khusus…] | Bilangan bulat mana pun dari 16 hingga 4096px |

## Menentukan lebar di Markdown

Berikan nilai numerik `width` pada tag `img` HTML. Penulisan ini juga ditampilkan dengan cara yang sama di GitHub maupun MDX.

```html
<img src="./images/screen.png" alt="Layar pengaturan" width="360" />
```

> **Catatan**
>
> - `width` hanya menerima angka. Jangan menambahkan `px` atau `%`. Nilai yang lebih besar dari lebar isi pun tetap ditampilkan sesuai lebar isi.
> - Gambar ditentukan dengan jalur relatif terhadap dokumen. Gambar di luar root dokumentasi tidak ditampilkan.

## Topik terkait

- [Mengedit dokumen](README.md)
- [Diagram, rumus, atau gambar tidak ditampilkan](../07-troubleshooting/rendering.md)
