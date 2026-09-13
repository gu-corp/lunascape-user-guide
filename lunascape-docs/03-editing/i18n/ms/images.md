# Melaraskan saiz imej

Imej yang dilekatkan pada dokumen akan muat secara automatik mengikut lebar teks dan tinggi skrin. Bagi imej yang ingin dipaparkan pada saiz tertentu, anda boleh menetapkan lebarnya.

## Cara pelarasan automatik berfungsi

- Imej Markdown biasa (`![keterangan](./images/screen.png)`) dikecilkan supaya muat dengan lebar teks. Imej tidak akan dibesarkan melebihi saiz asalnya.
- Tangkapan skrin yang tinggi dihadkan kepada 72% daripada tinggi skrin atau 720px, mana-mana yang lebih kecil.

## Menetapkan lebar dalam skrin penyuntingan

1. Tekan [Edit] dan pilih imej dalam paparan visual.
2. Pilih lebar daripada [Saiz imej] pada bar alat.
3. Tekan [Simpan].

| Pilihan | Lebar |
|---|---|
| [Automatik] | Tidak ditetapkan (pelarasan automatik) |
| [Kecil (360px)] | 360px |
| [Sederhana (560px)] | 560px |
| [Besar (760px)] | 760px |
| [Lebar teks (920px)] | 920px |
| [Tersuai…] | Sebarang integer dari 16 hingga 4096px |

## Menetapkan lebar dalam Markdown

Berikan nilai `width` berangka pada tag `img` HTML. Bentuk penulisan ini turut dipaparkan sama pada GitHub dan dalam MDX.

```html
<img src="./images/screen.png" alt="Skrin tetapan" width="360" />
```

> **Nota**
>
> - `width` menerima nombor sahaja. Jangan tambah `px` atau `%`. Nilai yang lebih besar daripada lebar teks tetap dipaparkan mengikut lebar teks.
> - Imej ditetapkan dengan laluan relatif daripada dokumen. Imej di luar akar dokumentasi tidak dipaparkan.

## Topik berkaitan

- [Menyunting dokumen](README.md)
- [Rajah, rumus matematik atau imej tidak dipaparkan](../07-troubleshooting/rendering.md)
