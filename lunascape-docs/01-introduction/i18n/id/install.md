# Menginstal ekstensi

Ekstensi VS Code "Lunascape Docs Pro" didistribusikan sebagai berkas VSIX. Gratis; "Pro" menandai edisi yang menyerahkan pekerjaan kepada AI dan memperbarui dirinya sendiri.

## Persyaratan

- VS Code 1.90 atau yang lebih baru
- Fitur yang menulis berkas — membuat dokumen, menata INDEX, menyimpan pengaturan pemeriksaan, menerjemahkan — hanya berfungsi di ruang kerja yang telah Anda tandai sebagai tepercaya di VS Code.

## Menginstal

1. Dapatkan berkas VSIX. Tautan ini selalu menunjuk ke versi terkini.

   [Unduh lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Buka tampilan Extensions (`⇧⌘X` / `Ctrl+Shift+X`).
3. Pilih [Install from VSIX...] dari menu `…` di kanan atas, lalu tentukan berkas yang telah Anda unduh.

### Dari baris perintah

Cukup satu baris, jika Anda lebih suka tidak meninggalkan terminal. Perintah ini mengunduh dan menginstal sekaligus.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Catatan**
> Jika `code` tidak ditemukan, jalankan [Shell Command: Install 'code' command in PATH] dari Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).

## Memperbarui

Ketika versi yang lebih baru dipublikasikan, ekstensi mengambil dan menginstalnya sendiri. VS Code akan menawarkan untuk memuat ulang jendela, dan saat itulah versi baru mulai digunakan. Pengaturan dan dokumen Anda tetap seperti semula.

Pemeriksaan dilakukan sekali sehari. Untuk memeriksa sekarang juga, jalankan [Lunascape Docs: Periksa versi yang lebih baru] dari Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).

Perilakunya dapat diubah dengan pengaturan `lunascapeDocEditor.update.check`.

| Pengaturan | Yang terjadi |
|---|---|
| Instal versi yang lebih baru saat dipublikasikan | Bawaan |
| Beri tahu saya, dan biarkan saya memutuskan setiap kali | Sebuah pemberitahuan muncul, dan tidak ada yang berubah sampai Anda menekan [Perbarui] |
| Jangan pernah memeriksa | Tidak terjadi apa-apa |

### Ketika pembaruan gagal

"Pembaruan tidak dapat diambil: No Servers" berarti versi yang terpasang adalah 0.22.18 atau yang lebih lama. Alur pembaruannya selalu gagal pada langkah terakhir, sehingga tidak dapat memperbarui dirinya sendiri ke versi yang lebih baru. Instal sekali secara manual, seperti di atas; setelah itu ekstensi akan memperbarui dirinya sendiri.

## Memeriksa versi

Buka "Lunascape Docs Pro" di tampilan Extensions untuk melihat versi yang terpasang. Anda memerlukannya saat melaporkan masalah.

## Topik terkait

- [Membuat dokumen pertama Anda](first-documents.md)
- [Melaporkan masalah](../07-troubleshooting/report.md)
