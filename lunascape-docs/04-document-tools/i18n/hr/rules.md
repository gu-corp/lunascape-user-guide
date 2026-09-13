# Promjena pravila provjere

Možete promijeniti razinu obavijesti (pogreška, upozorenje, informacija) za svaku stavku provjere ili je isključiti. Promjene se spremaju u datoteku `docs-lint.config.json` u korijenu dokumentacije i dijele se s timom.

## Promjena razine obavijesti

1. Na alatnoj traci pritisnite [Alati za dokumente] i otvorite karticu [Provjera].
2. Pritisnite [Pregledaj i promijeni pravila].
   Popis stavki provjere proširuje se unutar iste kartice. Uz svaku stavku prikazuju se njezina svrha i izvor trenutačne postavke (Project, Profile, Pack ili Default).
3. Odaberite razinu obavijesti za stavku koju želite promijeniti.
4. Pritisnite [Spremi i provjeri ponovno].
   Postavka se sprema, a cijeli korijen dokumentacije ponovno se provjerava s novim postavkama.

| Mogućnost | Značenje |
|---|---|
| [Standardna postavka (…)] | Uklanja izmjenu i vraća standardnu postavku koja se određuje redom iz profila, Standard Packa i zadane vrijednosti |
| [Isključeno] | Ova se stavka ne provjerava |
| [Informacija] / [Upozorenje] / [Pogreška] | Prijavljuje se na ovoj razini obavijesti |

> **Napomena**
>
> - Za spremanje je potreban pouzdani radni prostor.
> - Sprema se samo razina obavijesti svake stavke. Mogućnosti pojedinih stavki ostaju nepromijenjene. Standard Pack i sam profil ne mijenjaju se na ovom zaslonu.
> - Ako je datoteka `docs-lint.config.json` neposredno prije spremanja promijenjena izvana, spremanje se prekida. Učitajte najnovije stanje pa pokušajte ponovno.
> - Ako datoteka `docs-lint.config.json` ne postoji, stvara se pri spremanju.

## Izravno uređivanje datoteka s postavkama

- Pritiskom na [Otvori napredne postavke] datoteka `docs-lint.config.json` otvara se u VS Code.
- Otvorite [Izvor pravila i postavke dokumenta] i pritisnite [Uredi postavke dokumenta] da biste datoteku `lunascape-docs.json` otvorili u VS Code. Standard Pack i profil odabiru se ovdje.

Za obje datoteke dostupni su dovršavanje unosa i opisi na temelju JSON Schema priložene uz proširenje.

## Standard Pack i profili

Standard Pack je standard dokumentacije koji objedinjuje potrebne vrste dokumenata, strukturu poglavlja, nazivlje i predloške. Odabire se u datoteci `lunascape-docs.json` pomoću `documentStandards`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Priloženi Pack `builtin:gu-corp-software` sadrži profile `base`, `web-application`, `api-service`, `regulated-financial-product` i `smart-contract`.

## Povezane teme

- [Provjera dokumenata](check.md)
- [Postavke projekta](project-configuration.md)
