# Penampil Web tidak boleh dibuka atau log masuk

## Sudah log masuk, tetapi repositori tiada dalam senarai

GitHub App "Lunascape Docs" tidak dipasang pada akaun tersebut, atau repositori itu tidak termasuk di dalamnya. Minta pemilik repositori atau pentadbir organisasi memasangnya mengikut langkah dalam [Membaca repositori persendirian](../06-web/private-repository.md).

## Tidak dapat meneruskan daripada skrin log masuk

- Anda tiada kebenaran membaca repositori tersebut. Minta pemilik repositori memberikan kebenaran itu.
- "Log masuk GitHub tidak ditetapkan untuk tapak ini": penampil yang anda sediakan sendiri tiada perkhidmatan log masuk yang ditetapkan. Pentadbir perlu menetapkan perkhidmatan log masuk.

## Tetingkap timbul untuk log masuk tidak terbuka

Pelayar menyekat tetingkap timbul. Benarkan tetingkap timbul bagi tapak ini, kemudian cuba sekali lagi.

## "Log masuk anda telah tamat tempoh" dipaparkan

Tempoh sah log masuk telah tamat. Tekan [Log masuk dengan GitHub] sekali lagi.

## Repositori awam memberikan 404

- Semak penulisan `owner/repo@ref/dir`.
- Nama cabang yang mengandungi `/` tidak boleh ditentukan.

## Selepas seketika, halaman tidak dapat dimuatkan

Tanpa log masuk, had penggunaan GitHub API (60 kali sejam) dikenakan. Apabila "Had bilangan telah dicapai" dipaparkan, tunggu seketika atau [Log masuk dengan GitHub].

## "Repositori ini tidak boleh dipaparkan daripada tapak ini" dipaparkan

Untuk membukanya daripada penampil yang anda sediakan sendiri, URL tapak tersebut perlu ditambah pada `viewer.origins` dalam `lunascape-docs.json` di pihak repositori.

## Tiada apa-apa dipaparkan apabila `index.html` dibuka

Ia tidak berfungsi apabila dibuka terus melalui `file://`. Bukanya melalui pelayan HTTP, atau gunakan versi VS Code.

## Tapak yang dieksport memaparkan "lunascape-docs-manifest.json tidak dijumpai"

Sediakan keseluruhan set fail yang dihasilkan oleh `npm run export:web` (termasuk manifes) sebagaimana adanya.

## Draf tidak dapat disimpan

- "IndexedDB tidak dapat dibuka" / "Sedang digunakan oleh tab lain": puncanya ialah mod persendirian pelayar, atau tab lain yang membuka tapak yang sama. Buka dalam tetingkap biasa dan tutup tab yang lain.
- Draf disimpan mengikut peranti dan pelayar. Ia tidak dibawa ke peranti lain.

## Topik berkaitan

- [Membuka repositori GitHub](../06-web/open-repository.md)
- [Menyimpan draf](../06-web/drafts.md)
