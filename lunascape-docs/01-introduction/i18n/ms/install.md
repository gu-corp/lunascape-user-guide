# Memasang sambungan

Sambungan VS Code "Lunascape Docs Pro" diedarkan sebagai fail VSIX. Ia percuma; "Pro" menandakan edisi yang menyerahkan kerja kepada AI dan mengemas kini dirinya sendiri.

## Keperluan

- VS Code 1.90 atau lebih baharu
- Ciri yang menulis fail — mencipta dokumen, menyusun INDEX, menyimpan tetapan semakan, menterjemah — hanya berfungsi dalam ruang kerja yang telah anda tandakan sebagai dipercayai dalam VS Code.

## Memasang

1. Dapatkan fail VSIX. Pautan ini sentiasa menuju ke versi semasa.

   [Muat turun lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Buka paparan Sambungan (`⇧⌘X` / `Ctrl+Shift+X`).
3. Pilih [Pasang daripada VSIX...] daripada menu `…` di bahagian kanan atas, dan pilih fail yang telah anda muat turun.

### Daripada baris arahan

Satu baris, jika anda tidak mahu meninggalkan terminal. Ia memuat turun dan memasang.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Perhatian**
> Jika `code` tidak dijumpai, jalankan [Perintah Shell: Pasang perintah 'code' dalam PATH] daripada Palet Perintah (`⇧⌘P` / `Ctrl+Shift+P`).

## Mengemas kini

Apabila versi lebih baharu diterbitkan, sambungan itu mengambil dan memasangnya. VS Code menawarkan untuk memuat semula tetingkap, dan pada waktu itulah anda mula menggunakannya. Tetapan dan dokumen anda dibiarkan seadanya.

Ia menyemak sekali sehari. Untuk menyemak sekarang, jalankan [Lunascape Docs: Semak versi lebih baharu] daripada Palet Perintah (`⇧⌘P` / `Ctrl+Shift+P`).

`lunascapeDocEditor.update.check` mengubah apa yang berlaku.

| Tetapan | Apa yang berlaku |
|---|---|
| Pasang versi lebih baharu apabila satu diterbitkan | Lalai |
| Beritahu saya, dan biar saya tentukan setiap kali | Satu notis muncul, dan tiada apa yang berubah sehingga anda menekan [Kemas kini] |
| Jangan sekali-kali semak | Tiada apa yang berlaku |

### Apabila ia tidak dapat mengemas kini

"The update could not be fetched: No Servers" bermaksud versi yang dipasang ialah 0.22.18 atau lebih awal. Laluan kemas kininya gagal pada langkah terakhir setiap kali, jadi ia tidak dapat membawa dirinya ke versi lebih baharu. Pasang sekali secara manual, seperti di atas; selepas itu ia mengemas kini dirinya sendiri.

## Menyemak versi

Buka "Lunascape Docs Pro" dalam paparan Sambungan untuk melihat versi yang dipasang. Anda memerlukannya semasa melaporkan masalah.

## Topik berkaitan

- [Mencipta dokumen pertama anda](first-documents.md)
- [Melaporkan masalah](../07-troubleshooting/report.md)
