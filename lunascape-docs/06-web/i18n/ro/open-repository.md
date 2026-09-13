# Deschiderea unui depozit GitHub

În versiunea Web, deschideți documentele indicând un depozit GitHub. Pentru depozitele publice nu este necesară conectarea.

## Deschiderea din ecran

1. Deschideți <https://docs.lunascape.org/>.
2. Apăsați [Deschide documente] (pictograma folderului) din bara de instrumente.
3. Introduceți depozitul în [Indicați direct un depozit] și apăsați [Deschide].
   Când sunteți conectat la GitHub, puteți alege și din listă, prin [Alegeți dintre depozitele lizibile].

> **Sfat**
>
> - Pictograma GitHub de alături deschide pe github.com documentul pe care îl citiți. Nu este o operație de deschidere a documentelor.

## Deschiderea prin URL

Adresa așază depozitul și poziția documentului exact în această ordine. Calea este poziția din interiorul depozitului, deci ordinea este aceeași ca în URL-ul GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Ce indicați | Cum se scrie |
|---|---|
| Numai depozitul (ramura implicită) | `/github/owner/repo` |
| Un document din depozit | `/github/owner/repo/docs/01-product/vision.md` |
| O ramură sau o etichetă | adăugați la final `?ref=v1.2.0` |

Adresa se schimbă pe măsură ce navigați între pagini. Apăsați [Partajează acest document] din bara de instrumente pentru a transmite linkul paginii pe care o citiți. Funcționează și butoanele [Înapoi] și [Înainte] ale browserului.

Și forma anterioară, `?source=`, se deschide ca până acum. După deschidere, este rescrisă în forma nouă.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Notă**
>
> - Fără conectare, se aplică limita de utilizare a API-ului GitHub (60 de cereri pe oră). Pentru depozitele cu multe documente sau pentru citirea repetată, folosiți [Conectare cu GitHub].
> - Numele de ramuri care conțin `/` (de exemplu `feature/xxx`) pot fi indicate cu `?ref=` în forma de adresă de mai sus. În forma `?source=` nu pot fi scrise.
> - Documentele sunt încărcate cu drepturile GitHub ale cititorului. Persoanele fără drept de citire nu le văd.

## Deschiderea documentelor dintr-un folder local

Apăsați [Deschide documente] din bara de instrumente, apoi, sub listă, [Deschide documente dintr-un folder local] și alegeți un folder de pe dispozitiv. Fișierele sunt procesate în interiorul browserului și nu sunt trimise în exterior. Funcționează în browserele care acceptă selectarea folderelor (Chrome, Edge și altele).

## Subiecte conexe

- [Consultarea unui depozit privat](private-repository.md)
- [Versiunea Web nu se deschide sau nu permite conectarea](../07-troubleshooting/web.md)
