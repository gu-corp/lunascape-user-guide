# Web preglednik se ne može otvoriti ili prijaviti

## Prijavljeni ste, ali repozitorij nije na popisu

GitHub App „Lunascape Docs” nije instaliran na tom računu ili repozitorij nije obuhvaćen. Zatražite od vlasnika repozitorija ili administratora organizacije da ga instalira prema postupku u [Čitanje privatnog repozitorija](../06-web/private-repository.md).

## Ne može se proći dalje od zaslona za prijavu

- Nemate dopuštenje za čitanje tog repozitorija. Zatražite od vlasnika repozitorija da vam dodijeli dopuštenje.
- „Za ovu stranicu nije postavljena prijava putem GitHuba”: na pregledniku koji ste sami postavili nije konfigurirana usluga prijave. Administrator mora postaviti uslugu prijave.

## Skočni prozor za prijavu se ne otvara

Preglednik blokira skočne prozore. Dopustite skočne prozore za ovu stranicu i pokušajte ponovno.

## Prikazuje se „Prijava je istekla”

Prijava je istekla. Ponovno pritisnite [Prijava putem GitHuba].

## Otvaranje javnog repozitorija vraća 404

- Provjerite zapis `owner/repo@ref/dir`.
- Nazivi grana koji sadrže `/` ne mogu se navesti.

## Nakon nekog vremena učitavanje prestaje raditi

Bez prijave vrijedi ograničenje korištenja GitHub API-ja (60 zahtjeva na sat). Kad se prikaže „Dosegnuto je ograničenje broja zahtjeva”, pričekajte neko vrijeme ili se prijavite putem [Prijava putem GitHuba].

## Prikazuje se „S ove stranice nije moguće prikazati ovaj repozitorij”

Da biste repozitorij otvorili s preglednika koji ste sami postavili, URL te stranice treba dodati u `viewer.origins` u datoteci `lunascape-docs.json` u repozitoriju.

## Otvaranje datoteke `index.html` ne prikazuje ništa

Ne radi ako je otvorite izravno preko `file://`. Otvorite je putem HTTP poslužitelja ili upotrijebite VS Code verziju.

## Na izvezenoj stranici piše „lunascape-docs-manifest.json nije pronađen”

Postavite cjelokupan skup datoteka koje je ispisala naredba `npm run export:web` (uključujući manifest) onakvim kakav jest.

## Nacrt se ne može spremiti

- „Nije moguće otvoriti IndexedDB” / „Koristi se u drugoj kartici”: uzrok je privatni način rada preglednika ili druga kartica s istom stranicom. Otvorite je u običnom prozoru i zatvorite ostale kartice.
- Nacrti se spremaju po uređaju i pregledniku. Ne prenose se na drugi uređaj.

## Povezane teme

- [Otvaranje GitHub repozitorija](../06-web/open-repository.md)
- [Spremanje nacrta](../06-web/drafts.md)
