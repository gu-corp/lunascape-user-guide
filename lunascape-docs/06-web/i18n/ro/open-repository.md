# Deschiderea unui depozit GitHub

În versiunea web și în Lunascape puteți deschide și citi direct un depozit GitHub, fără să-l clonați. Pentru depozitele publice nu este nevoie de conectare.

## Deschiderea din ecran

1. Apăsați [Deschide documente] (pictograma folder) din bara de instrumente. Se deschide ecranul „Deschide documente”.
2. În coloana din stânga, alegeți locul din care deschideți.

   | Loc | Ce se afișează |
   |---|---|
   | Toate | Tot ce este mai jos. Elementele deschise recent apar primele |
   | Deschise recent | Depozitele și folderele pe care le-ați deschis până acum |
   | Recomandate | Manualele prezentate de site |
   | Depozite GitHub | Când sunteți conectat la GitHub, depozitele pe care le puteți citi |
   | Acest computer | Folderele de pe acest dispozitiv. În Lunascape, aici apar și depozitele clonate |

3. Apăsați [Deschide] pe rândul dorit. Dacă scrieți în [Filtrare după numele documentului sau al depozitului] din partea de sus, puteți restrânge rândurile.

Pentru un depozit care nu apare în listă, folosiți [Introdu owner/repo și deschide] din coloana din stânga.

> **Sfat**
>
> - Depozitele GitHub din listă sunt cele pe care este instalată aplicația GitHub „Lunascape Docs” și pentru care aveți drept de citire. Dacă nu găsiți un depozit, rugați proprietarul acestuia să adauge aplicația.

## Verificarea locului unui document

Pictograma mică din partea stângă a barei de instrumente (indicatorul de locație) arată unde se află documentul pe care îl citiți.

| Pictogramă | Loc |
|---|---|
| Sigla GitHub | Citiți de pe GitHub. Documentul nu este salvat pe acest dispozitiv |
| Computer | Un folder de pe acest dispozitiv, gestionat de Lunascape. Se afișează și numele ramurii Git și numărul de fișiere modificate |
| Folder | Un folder de pe acest dispozitiv |

Apăsați pictograma pentru a vedea locul, starea și operațiunile disponibile de acolo ([Vizualizează pe GitHub], [Copiază linkul] etc.).

## Clonarea unui depozit în Lunascape

În Lunascape puteți clona un depozit GitHub pe acest dispozitiv, apoi puteți edita și face commit cu Git.

- În ecranul „Deschide documente”, apăsați [Duplică] pe rândul depozitului.
- Când citiți un depozit deschis de pe GitHub, apăsați indicatorul de locație, apoi [Duplică pe acest computer]. După ce clonarea se termină, același document se deschide din copia de pe acest dispozitiv.

Un depozit clonat este marcat în listă cu „Pe acest computer”, iar [Deschide pe acest computer] apare primul.

## Deschiderea prin URL

Adresa conține depozitul și poziția documentului, în ordinea în care apar. Calea este poziția din interiorul depozitului, deci ordinea este aceeași ca în URL-ul GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Ce indicați | Formă |
|---|---|
| Doar depozitul (ramura implicită) | `/github/owner/repo` |
| Un document din depozit | `/github/owner/repo/docs/01-product/vision.md` |
| O ramură sau o etichetă | Adăugați la sfârșit `?ref=v1.2.0` |

Când treceți la altă pagină, se schimbă și adresa. Apăsați [Partajează acest document] din bara de instrumente pentru a trimite cuiva linkul paginii pe care o citiți. Puteți folosi și butoanele [Înapoi] și [Înainte] ale browserului.

Vechea formă `?source=` se deschide în continuare. După deschidere, adresa este rescrisă în noua formă.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Notă**
>
> - Fără conectare, se aplică limita de utilizare a API-ului GitHub (60 de solicitări pe oră). Pentru depozite cu multe documente sau pentru citire repetată, folosiți [Conectare cu GitHub].
> - Numele de ramuri care conțin `/` (de exemplu, `feature/xxx`) se pot indica cu `?ref=` în forma de adresă de mai sus. Forma `?source=` nu le poate exprima.
> - Documentele se încarcă cu permisiunile GitHub ale cititorului. Persoanele fără drept de citire nu le văd.

## Deschiderea documentelor dintr-un folder local

Apăsați [Deschide documente] din bara de instrumente, apoi alegeți un folder de pe dispozitiv din [Deschide documente dintr-un folder local], în coloana din stânga. Fișierele sunt procesate în browser și nu sunt trimise nicăieri. Funcția este disponibilă în browserele care permit selectarea folderelor (Chrome, Edge etc.).

## Subiecte conexe

- [Vizualizarea unui depozit privat](private-repository.md)
- [Versiunea web nu se deschide sau conectarea nu reușește](../07-troubleshooting/web.md)
