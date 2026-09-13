# Promjena postavki prikaza

Putem [Postavke prikaza] (zupčanik) na alatnoj traci svaki korisnik može promijeniti izgled INDEX-a i prikaz gumba za uređivanje.

1. Pritisnite [Postavke prikaza] na alatnoj traci.
2. Uključite ili isključite stavke koje želite promijeniti. Promjene se primjenjuju odmah.
3. Ponovno pritisnite [Postavke prikaza] ili kliknite izvan ploče da biste je zatvorili.

## Stavke koje možete postaviti

| Skupina | Stavka | Funkcija |
|---|---|---|
| Jezik dokumenta | (trenutačno stanje) | Prikazuje zadani jezik projekta i jezik koji je trenutačno prikazan. [Postavi jezike projekta…] otvara jezične postavke projekta |
| Sadržaj | [Nazivi datoteka] | Prikazuje nazive datoteka umjesto naziva dokumenata |
| | [Ikone dokumenata] | Prikazuje ikonu uz stavke dokumenata |
| | [Ikone mapa] | Prikazuje ikonu uz stavke mapa |
| | [Broj stavki u mapi] | Prikazuje broj dokumenata u mapi |
| | [Vodilice razina] | Prikazuje crte koje označavaju razine |
| | [Sakrij kada postoji samo jedan dokument] | U korijenu dokumentacije sa samo jednim dokumentom automatski zatvara INDEX, ali samo prvi put |
| | [Sažmi podatke o dokumentu] | Sažima upravljačku tablicu na vrhu dokumenta u redak „Podaci o dokumentu”. Kada je isključeno, tablica se prikazuje u cijelosti |
| | [Gustoća prikaza] | Odabir razmaka između redaka INDEX-a: [Standardna] / [Zbijeno] |
| | [Gumb za uređivanje] | Prikazuje [Uredi] u donjem desnom kutu teksta |
| Radnje | [Vrati na zadano za projekt] | Briše sve korisnikove promjene i vraća postavke projekta |
| | [Otvori postavke proširenja] | Otvara postavke za Lunascape Docs u prozoru postavki VS Code-a |

> **Savjet**
>
> - Postavke prikaza spremaju se za svakog korisnika i za svaki korijen dokumentacije te se ne upisuju u datoteke kojima upravlja Git.
> - Postavke se primjenjuju ovim redoslijedom: „korisnikove postavke prikaza → postavke VS Code-a → `lunascape-docs.json` → zadane vrijednosti proizvoda”. Zajedničke zadane vrijednosti za tim određuju se u odjeljcima `tree` i `editor` u datoteci `lunascape-docs.json`.

## Promjena sheme boja

Pritiskom na prekidač teme (sunce/mjesec) na alatnoj traci prebacujete se između bijele pozadine i sheme boja VS Code-a. Shema boja pri otvaranju određena je postavkom `lunascapeDocEditor.appearance` (`light` ili `auto`).

## Povezane teme

- [Rad s INDEX-om](index-panel.md)
- [Postavke projekta](../04-document-tools/project-configuration.md)
- [Popis postavki VS Code-a](../08-reference/settings.md)
