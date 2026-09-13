# Memaparkan maklumat dokumen

"Jadual kawalan dokumen" yang diletakkan di bahagian atas dokumen (ID dokumen, versi, tarikh kemas kini, status dan sebagainya) dihimpunkan menjadi satu baris "Maklumat dokumen" yang kecil semasa membaca. Markdown itu sendiri kekal sebagai jadual biasa, jadi ia tetap boleh dibaca seperti biasa di GitHub.

## Syarat untuk dipaparkan

Letakkan jadual dua lajur seperti berikut sejurus selepas tajuk (H1).

```markdown
# Spesifikasi keperluan fungsian

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Syaratnya ialah jadual itu mempunyai baris 文書ID dan beberapa item kawalan.
- Jadual yang diletakkan di bawah tajuk `## 文書管理` atau `## Document information` juga dikenali.
- Jadual yang berada di tengah-tengah teks dan jadual "item/kandungan" biasa tidak ditukar.

## Cara ia dipaparkan

- Semasa membaca, hanya status dan tarikh kemas kini dipaparkan dalam saiz kecil.
- Tekan baris itu untuk memaparkan semua item.
- Semasa mencetak, semua item dipaparkan.
- Dalam skrin penyuntingan, ia dipaparkan sebagai jadual biasa dan boleh disunting terus.

> **Petua**
>
> Jika anda mahu ia sentiasa dipaparkan sebagai jadual tanpa dikuncupkan, matikan [Kuncupkan maklumat dokumen] dalam [Tetapan paparan].

## Topik berkaitan

- [Menyunting dokumen](README.md)
- [Mengubah tetapan paparan](../02-reading/display-settings.md)
