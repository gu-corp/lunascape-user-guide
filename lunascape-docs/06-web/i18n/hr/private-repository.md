# Pregledavanje privatnog repozitorija

Dokumente privatnih repozitorija možete pregledati nakon prijave putem GitHuba, ograničeno na one za koje imate pravo čitanja. Lunascape Docs nikada nema vlastite račune ni ovlasti.

## Prijava i otvaranje

1. Otvorite <https://docs.lunascape.org/>.
   Kada zatražite privatni dokument ili se još niste prijavili, prikazuje se zaslon za prijavu.
2. Pritisnite [Prijava putem GitHuba].
   GitHubov zaslon za autorizaciju otvara se u skočnom prozoru.
3. Nakon prijave pritisnite [Otvori dokumente] na alatnoj traci i pod [Odaberi među repozitorijima koje možete čitati] odaberite repozitorij koji želite otvoriti.

> **Savjet**
>
> - Ime prijavljenog računa prikazano je na alatnoj traci. Odavde možete i [Odjava] te [Prijava drugim računom].
> - Na popisu se prikazuju repozitoriji računa (organizacija ili osoba) na kojima je instaliran GitHub App „Lunascape Docs”, i to samo oni za koje imate pravo čitanja.

## Postavke koje obavlja vlasnik repozitorija

Ako se ciljani repozitorij ne prikazuje na popisu, vlasnik repozitorija ili administrator organizacije mora instalirati GitHub App „Lunascape Docs”.

- Tražene su ovlasti Contents (čitanje i pisanje) te Pull requests (čitanje i pisanje). Čitanje služi za pregledavanje, a pisanje za zahtjev za objavu s weba (Pull Request). Lunascape Docs nikada ne pohranjuje sadržaj dokumenata.
- Instalacija se obavlja po računu (organizaciji ili osobi). Postavlja se hoće li se odnositi na „All repositories” (što automatski uključuje i naknadno stvorene repozitorije) ili samo na odabrane repozitorije.

| Situacija | Postupak |
|---|---|
| Prvo uvođenje u organizaciju ili osobni račun | Provedite putem [stranice za instalaciju](https://github.com/apps/lunascape-docs/installations/new) |
| Dodavanje ciljanih repozitorija u organizaciji koja ga već ima | Postavite u Settings → GitHub Apps → Lunascape Docs → Configure → Repository access organizacije |

Čak i kada je instaliran za cijelu organizaciju, svaki član može pregledavati samo repozitorije za koje ima pravo čitanja. Zahtjev za objavu također može poslati samo za repozitorije za koje ima pravo pisanja.

> **Savjet**
> - Kod nove instalacije tražene ovlasti prikazane su popisom na zaslonu za instalaciju, a pritiskom na „Install” smatra se da ste ih odobrili. Dodatne radnje nema.
> - Organizacija koja je bila instalirala aplikaciju prije nego što je ovlast dodana dobiva potvrdni e-mail administratorima, a na vrhu zaslona Settings → GitHub Apps → Lunascape Docs → Configure organizacije prikazuje se gumb za odobrenje. Dok se ne odobri, u toj organizaciji moguće je samo pregledavanje, a slanje zahtjeva za objavu prikazuje poruku „potrebno je dodijeliti pravo pisanja”.
> - S kojim ste ovlastima trenutačno uključeni možete provjeriti na istom zaslonu Configure. Za osobni račun to je Settings → Applications → Installed GitHub Apps.
> - Ako ste greškom isključili ciljani repozitorij ili deinstalirali aplikaciju, ponovnom instalacijom sa [stranice za instalaciju](https://github.com/apps/lunascape-docs/installations/new) sve se vraća u prijašnje stanje. Poruka o odbijenom zahtjevu za objavu sadrži poveznicu na zaslon za ispravak.
> - Ako na strani repozitorija ne želite primati zahtjeve za objavu, u `lunascape-docs.json` upišite `"publish": { "enabled": false }`. Pregledavanje i dalje ostaje dostupno.

## Povezane teme

- [Otvaranje GitHub repozitorija](open-repository.md)
- [Web-verzija se ne može otvoriti ili prijaviti](../07-troubleshooting/web.md)
