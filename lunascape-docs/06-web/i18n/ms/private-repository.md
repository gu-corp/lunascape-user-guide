# Membaca repositori peribadi

Selepas log masuk dengan GitHub, anda boleh membaca dokumen repositori peribadi, terhad kepada repositori yang anda mempunyai kebenaran membaca. Lunascape Docs tidak pernah memiliki akaun atau kebenaran tersendiri.

## Log masuk dan buka

1. Buka <https://docs.lunascape.org/>.
   Apabila anda menyatakan dokumen peribadi atau belum log masuk, skrin log masuk akan dipaparkan.
2. Tekan [Log masuk dengan GitHub].
   Skrin pengesahan GitHub akan terbuka dalam tetingkap timbul.
3. Selepas log masuk, tekan [Buka dokumen] pada bar alat, dan pilih repositori yang hendak dibuka melalui [Pilih daripada repositori yang boleh dibaca].

> **Petua**
>
> - Nama akaun yang sedang log masuk dipaparkan pada bar alat. [Log keluar] atau [Log masuk dengan akaun lain] juga boleh dilakukan dari sini.
> - Senarai memaparkan repositori bagi akaun (organisasi atau individu) yang mempunyai GitHub App "Lunascape Docs" dipasang, terhad kepada repositori yang anda mempunyai kebenaran membaca.

## Tetapan yang dilakukan oleh pemilik repositori

Jika repositori sasaran tidak muncul dalam senarai, pemilik repositori atau pentadbir organisasi perlu memasang GitHub App "Lunascape Docs".

- Kebenaran yang diminta ialah Contents (baca dan tulis) dan Pull requests (baca dan tulis). Baca adalah untuk membaca; tulis adalah untuk permintaan penerbitan (Pull Request) dari Web. Lunascape Docs tidak pernah menyimpan kandungan dokumen.
- Unit pemasangan ialah akaun (organisasi atau individu). Tetapkan sama ada sasaran "All repositories" (termasuk juga repositori yang dicipta kemudian secara automatik) atau hanya repositori yang dipilih.

| Situasi | Langkah |
|---|---|
| Memasang buat kali pertama pada organisasi atau akaun individu | Lakukan melalui [halaman pemasangan](https://github.com/apps/lunascape-docs/installations/new) |
| Menambah repositori sasaran pada organisasi yang sudah memasang | Tetapkan melalui Settings organisasi → GitHub Apps → Lunascape Docs → Configure → Repository access |

Walaupun dipasang untuk seluruh organisasi, setiap ahli hanya boleh membaca repositori yang mereka sendiri mempunyai kebenaran membaca. Permintaan penerbitan juga hanya boleh dihantar ke repositori yang mereka sendiri mempunyai kebenaran menulis.

> **Petua**
> - Untuk pemasangan baharu, kebenaran yang diminta dipaparkan sebagai senarai pada skrin pemasangan, dan menekan "Install" bermakna anda telah meluluskannya. Tiada operasi tambahan diperlukan.
> - Organisasi yang telah memasang sebelum kebenaran ditambah akan menerima e-mel pengesahan kepada pentadbirnya, dan butang kelulusan akan dipaparkan di bahagian atas Settings organisasi → GitHub Apps → Lunascape Docs → Configure. Sehingga diluluskan, organisasi itu hanya boleh membaca, dan apabila permintaan penerbitan dihantar, ia akan memaparkan "kebenaran menulis perlu diberikan".
> - Kebenaran yang sedang berkuat kuasa boleh disemak pada skrin Configure yang sama. Bagi akaun individu, ia ialah Settings → Applications → Installed GitHub Apps.
> - Jika repositori sasaran tersilap dikeluarkan atau dinyahpasang, ia boleh dikembalikan dengan memasangnya semula daripada [halaman pemasangan](https://github.com/apps/lunascape-docs/installations/new). Mesej penolakan permintaan penerbitan disertakan pautan ke skrin pembaikan.
> - Jika di pihak repositori anda tidak mahu menerima permintaan penerbitan, tulis `"publish": { "enabled": false }` dalam `lunascape-docs.json`. Bacaan tetap boleh digunakan seperti biasa.

## Topik berkaitan

- [Membuka repositori GitHub](open-repository.md)
- [Tidak dapat membuka atau log masuk pada versi Web](../07-troubleshooting/web.md)
