# Deschiderea unui depozit GitHub

În versiunea web puteți deschide și citi direct un depozit GitHub, fără să-l clonați. Pentru depozitele publice nu este necesară conectarea.

## Deschiderea din ecran

1. Apăsați [Deschide documente] (pictograma folder) din bara de instrumente. Se deschide ecranul „Deschide documente”.
2. În coloana din stânga, alegeți locul din care deschideți.

   | Loc | Ce conține |
   |---|---|
   | Toate | Tot ce este mai jos. Elementele deschise recent apar primele |
   | Deschise recent | Depozitele și folderele pe care le-ați deschis până acum |
   | Recomandate | Manualele prezentate de site |
   | Depozite GitHub | Când sunteți conectat cu GitHub, depozitele pe care le puteți citi |
   | Acest computer | Folderele de pe acest dispozitiv |

3. Apăsați [Deschide] pe rândul dorit. Pentru a restrânge rândurile, introduceți text în [Filtrare după numele documentului sau al depozitului] din partea de sus.

Pentru un depozit care nu apare în listă, folosiți [Introdu owner/repo și deschide] din coloana din stânga.

> **Sfat**
>
> - Depozitele GitHub din listă sunt cele pe care este instalată aplicația GitHub App „Lunascape Docs” și pentru care aveți drept de citire. Dacă nu găsiți un depozit, cereți proprietarului acestuia să adauge aplicația.

## Verificarea locației documentului

Pictograma mică din partea stângă a barei de instrumente (indicatorul de locație) arată unde se află documentul pe care îl citiți.

| Pictogramă | Locație |
|---|---|
| Sigla GitHub | Documentul este citit de pe GitHub. Nu este salvat pe acest dispozitiv |
| Folder | Un folder de pe acest dispozitiv |

Apăsați pictograma pentru a vedea locația, starea și operațiile disponibile de acolo ([Vizualizează pe GitHub], [Copiază linkul] etc.).

## Deschiderea prin URL

Adresa conține depozitul și poziția documentului, în ordinea în care apar. Calea este poziția din depozit, deci are aceeași ordine ca URL-ul GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Ce specificați | Formă |
|---|---|
| Doar depozitul (ramura implicită) | `/github/owner/repo` |
| Un document din depozit | `/github/owner/repo/docs/01-product/vision.md` |
| O ramură sau o etichetă | Adăugați `?ref=v1.2.0` la sfârșit |

Când treceți la altă pagină, se schimbă și adresa. Apăsați [Partajează acest document] din bara de instrumente pentru a transmite linkul paginii pe care o citiți. Puteți folosi și butoanele [Înapoi] și [Înainte] ale browserului.

Forma mai veche `?source=` se deschide în continuare. După deschidere, adresa este rescrisă în forma nouă.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Atenție**
>
> - Fără conectare se aplică limita de utilizare a API-ului GitHub (60 de solicitări pe oră). Pentru depozitele cu multe documente sau pentru citiri repetate, folosiți [Conectare cu GitHub].
> - Numele de ramuri care conțin `/` (de exemplu, `feature/xxx`) pot fi specificate cu `?ref=` în forma de adresă de mai sus. Ele nu pot fi scrise în forma `?source=`.
> - Documentele se încarcă cu permisiunile GitHub ale cititorului. Persoanele fără drept de citire nu le văd.

## Deschiderea documentelor dintr-un folder local

Apăsați [Deschide documente] din bara de instrumente, apoi alegeți un folder de pe dispozitiv cu [Deschide documente dintr-un folder local] din coloana din stânga. Fișierele sunt procesate în browser și nu sunt trimise în exterior. Funcția este disponibilă în browserele care permit selectarea folderelor (Chrome, Edge etc.).

## Subiecte conexe

- [Citirea unui depozit privat](private-repository.md)
- [Versiunea web nu se deschide sau conectarea nu reușește](../07-troubleshooting/web.md)
