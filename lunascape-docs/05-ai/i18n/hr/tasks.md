# Dostupni zadaci

Odaberite ih pod [Zadatak] u kartici [AI]. Svaki zadatak mijenja upute koje se predaju i provjeru koja slijedi.

| Zadatak | Sadržaj | Potrebno | Vrsta API-ja |
|---|---|---|---|
| Prevedi ovu stranicu | Prevodi prikazani dokument na odabrani jezik | Otvoren dokument, ciljni jezik | ○ |
| Prevedi sve što nedostaje | Redom prevodi dokumente odabranog jezika koji su zastarjeli ili im nedostaje prijevod | Ciljni jezik | Samo sesijska vrsta |
| Lektoriraj ovu stranicu | Provjerava i ispravlja nazivlje, stil i poglavlja koja zahtijeva standard dokumenata | Otvoren dokument | ○ |
| Izradi novi dokument | Izrađuje novi dokument prema standardu dokumenata i predlošcima | Tema (neobavezno) | Samo sesijska vrsta |

## Što upute sadrže

| Br. | Sadržaj |
|---|---|
| 1 | Položaj korijena dokumentacije, uz uputu da se izvan njega ništa ne mijenja |
| 2 | Zadani jezik (izvornik) i mjesto gdje se nalaze prijevodi (mapa `i18n/<jezik>/` uz dokument) |
| 3 | Da `navigation.order` pripada samo izvorniku i da prijevod smije nadjačati jedino `navigation.title` |
| 4 | Da se ne smiju mijenjati ID-ovi zahtjeva, poveznice, kod, Mermaid, TeX ni struktura front mattera |
| 5 | Standard dokumenata i pojmovnik (`terminology` u datoteci `docs-lint.config.json`) |
| 6 | Da se po završetku pokrene provjera dokumenta, prijave izmijenjene datoteke i ne izvode nikakve Git radnje |

> **Savjet**
>
> Dokumenti za „Prevedi sve što nedostaje” uzimaju se iz evidencije, do 200 dokumenata po pokretanju. Ako ih je više, pokrenite zadatak više puta.

## Povezane teme

- [Predaja zadatka AI-ju](README.md)
- [Evidencija i zapisi](ledger.md)
