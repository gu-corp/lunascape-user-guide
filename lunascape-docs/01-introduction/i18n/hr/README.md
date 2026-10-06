# Što je Lunascape Docs

Lunascape Docs alat je koji omogućuje da se Markdown dokumenti smješteni u Git repozitorij, onakvi kakvi jesu, koriste kao „web-mjesto specifikacija”. Nisu potrebni ni prethodni build, ni poslužitelj za dokumente, ni namjenska baza podataka.

## Što možete učiniti

| Cilj | Glavne značajke |
|---|---|
| Čitanje | INDEX (sadržaj), poveznice u tekstu, navigacijski trag, natrag i naprijed, pregled stranice, pretraživanje s filtriranjem |
| Prikaz | Tablice, blokovi koda, automatsko prilagođavanje slika, matematički izrazi KaTeX, dijagrami Mermaid, Vega-Lite, Markmap, WaveDrom i Svgbob, sažeti prikaz tablica kontrole dokumenta |
| Pisanje | Prebacivanje između vizualnog uređivanja i uređivanja Markdown izvornog koda, stvaranje, dupliciranje, preimenovanje i promjena redoslijeda iz ploče INDEX |
| Provjera | Provjera dokumenata alatom docs-lint, provjera obaveznih dokumenata, poglavlja i pojmova prema paketu Standard Pack, stvaranje iz predloška |
| Prevođenje | Izrada prijedloga prijevoda za pojedinu stranicu ili skupno. Spremanje nakon pregleda <!-- ai-only --> |
| Korištenje putem AI-ja | Specifikacijski alat samo za čitanje koji mogu koristiti agenti u programu VS Code <!-- ai-only --> |

## Dostupna okruženja

| Okruženje | Namjena |
|---|---|
| Proširenje za VS Code | Pregledavanje, uređivanje, provjera i prevođenje lokalnog repozitorija. Ova je pomoć usmjerena uglavnom na njega |
| Verzija za web-preglednik | Pregledavanje dokumenata na GitHubu (javnih i privatnih), nacrti na uređaju, pregledavanje lokalne mape |
| Proširenje za Chromium | Otvara verziju za web-preglednik u kartici preglednika |

## Osnovna načela

- **Markdown je izvornik.** Dokumenti ostaju Markdown datoteke kojima se upravlja u Gitu. Lunascape Docs ih ne pretvara u drugi oblik niti ih tako pohranjuje.
- **Spremanje obavlja korisnik.** Uređeni sadržaj zapisuje se u datoteku samo kada pritisnete [Spremi]. Staging i commit u Gitu ne izvode se automatski.
- **Dokumenti se obrađuju na vašem uređaju.** Za pregledavanje i uređivanje dokumenti se nikamo ne šalju. Samo se pri prevođenju unaprijed prikazuju odredište i sadržaj slanja, a slanje se obavlja tek nakon vašeg odobrenja.
- **Prijevodi se smještaju u `i18n/<jezik>/`.** Dokumenti na zadanom jeziku ostaju na svom mjestu, a prijevodi se smještaju pod istom relativnom putanjom u `i18n/en/` i slično.
- **AI samo predlaže.** Prijedlozi prijevoda spremaju se nakon što pregledate razlike. Dokumenti se nikada ne mijenjaju bez vašeg znanja. <!-- ai-only -->

## Povezane teme

- [Nazivi i funkcije dijelova zaslona](screen.md)
- [Instaliranje proširenja](install.md)
- [Osnovne radnje](../02-reading/README.md)
