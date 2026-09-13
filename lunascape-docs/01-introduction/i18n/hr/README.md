# Što je Lunascape Docs

Lunascape Docs alat je koji Markdown dokumente smještene u Git repozitoriju obrađuje takve kakvi jesu, kao „stranicu specifikacija”. Nije potrebna prethodna izgradnja, poslužitelj dokumentacije ni namjenska baza podataka.

## Što možete raditi

| Svrha | Glavne značajke |
|---|---|
| Čitanje | INDEX (sadržaj), poveznice u tekstu, navigacijski trag, natrag i naprijed, pregled sadržaja stranice, pretraživanje s filtrom |
| Prikaz | Tablice, blokovi koda, automatsko prilagođavanje slika, KaTeX matematički izrazi, dijagrami Mermaid, Vega-Lite, Markmap, WaveDrom i Svgbob, sažeti prikaz tablica za upravljanje dokumentima |
| Pisanje | Prebacivanje između vizualnog uređivanja i uređivanja izvornog Markdowna; stvaranje, dupliciranje, preimenovanje i promjena redoslijeda iz INDEX-a |
| Provjera | Provjera dokumenata alatom docs-lint, provjera obveznih dokumenata, poglavlja i pojmova prema paketu Standard Pack, stvaranje iz predložaka |
| Prevođenje | Izrada prijedloga prijevoda za jednu stranicu ili skupno. Spremanje nakon pregleda <!-- ai-only --> |
| Upotreba iz umjetne inteligencije | Alat za specifikacije samo za čitanje koji agenti u VS Codeu mogu koristiti <!-- ai-only --> |

## Dostupna okruženja

| Okruženje | Namjena |
|---|---|
| Proširenje za VS Code | Pregledavanje, uređivanje, provjera i prevođenje repozitorija na vašem računalu. Ova je pomoć usredotočena na njega |
| Web-preglednik | Pregledavanje dokumenata na GitHubu (javnih i privatnih), nacrti na uređaju, pregledavanje lokalne mape |
| Proširenje za Chromium | Otvara web-verziju u kartici preglednika |
| Preglednik Lunascape | Planirana je ugradnja istog modela dokumenata |

## Osnovna načela

- **Markdown je izvornik.** Dokumenti ostaju Markdown datoteke kojima upravlja Git. Lunascape Docs ih ne pretvara u drugi format niti ga čuva.
- **Spremanje obavlja korisnik.** Uređeni se sadržaj upisuje u datoteku tek kad pritisnete [Spremi]. Pripremanje i urezivanje u Git ne obavljaju se automatski.
- **Dokumenti se obrađuju na uređaju.** Radi pregledavanja ili uređivanja dokumenti se ne šalju izvan uređaja. Samo se pri prevođenju unaprijed prikazuju odredište i sadržaj, a slanje slijedi nakon vašeg odobrenja.
- **Prijevodi se smještaju u `i18n/<jezik>/`.** Dokumenti na zadanom jeziku ostaju na svom mjestu, a prijevodi se s istom relativnom putanjom smještaju u `i18n/en/` i slično.
- **Umjetna inteligencija samo predlaže.** Prijedlozi prijevoda spremaju se nakon pregleda razlika. Dokumenti se nikada ne mijenjaju bez vašeg znanja. <!-- ai-only -->

## Povezane teme

- [Nazivi i uloge dijelova zaslona](screen.md)
- [Instalacija proširenja](install.md)
- [Osnovne radnje](../02-reading/README.md)
