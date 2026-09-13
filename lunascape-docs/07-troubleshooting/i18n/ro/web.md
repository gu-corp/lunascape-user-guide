# Vizualizatorul Web nu se deschide sau conectarea eșuează

## M-am conectat, dar depozitul nu apare în listă

Aplicația GitHub „Lunascape Docs” nu este instalată pe acel cont sau depozitul nu este inclus. Cereți proprietarului depozitului sau unui administrator al organizației să o instaleze urmând pașii din [Consultarea unui depozit privat](../06-web/private-repository.md).

## Nu pot trece de ecranul de conectare

- Nu aveți drept de citire asupra depozitului. Cereți proprietarului depozitului să vă acorde acces.
- „Conectarea cu GitHub nu este configurată pentru acest site”: un vizualizator găzduit pe cont propriu nu are niciun serviciu de conectare configurat. Un administrator trebuie să configureze unul.

## Fereastra pop-up de conectare nu se deschide

Browserul blochează ferestrele pop-up. Permiteți ferestrele pop-up pentru acest site și încercați din nou.

## Apare mesajul „Conectarea a expirat”

Sesiunea de conectare a expirat. Apăsați din nou [Conectare cu GitHub].

## Un depozit public întoarce eroarea 404

- Verificați forma `owner/repo@ref/dir`.
- Numele de ramuri care conțin `/` nu pot fi indicate.

## După un timp, încărcarea nu mai funcționează

Fără conectare se aplică limita de utilizare a API-ului GitHub (60 de cereri pe oră). Când apare mesajul „S-a atins limita de cereri”, așteptați puțin sau folosiți [Conectare cu GitHub].

## Apare mesajul „Acest site nu poate afișa acest depozit”

Pentru a deschide depozitul dintr-un vizualizator găzduit pe cont propriu, URL-ul site-ului trebuie adăugat în `viewer.origins` din fișierul `lunascape-docs.json` al depozitului.

## Deschid `index.html`, dar nu se afișează nimic

Nu funcționează dacă este deschis direct prin `file://`. Deschideți-l printr-un server HTTP sau folosiți versiunea pentru VS Code.

## Site-ul exportat afișează „lunascape-docs-manifest.json nu a fost găsit”

Publicați ca atare întregul set de fișiere generat de `npm run export:web`, inclusiv manifestul.

## Ciornele nu pot fi salvate

- „IndexedDB nu poate fi deschis” / „Este folosit în altă filă”: cauza este modul privat al browserului sau o altă filă care afișează același site. Deschideți site-ul într-o fereastră obișnuită și închideți celelalte file.
- Ciornele se salvează pentru fiecare dispozitiv și browser în parte. Ele nu se transferă pe alt dispozitiv.

## Subiecte conexe

- [Deschiderea unui depozit GitHub](../06-web/open-repository.md)
- [Salvarea ciornelor](../06-web/drafts.md)
