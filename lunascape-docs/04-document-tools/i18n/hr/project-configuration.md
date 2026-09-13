# Postavke projekta

`lunascape-docs.json` neposredno u korijenu dokumentacije postavke su korijena dokumentacije koje dijeli cijeli tim. Njima se upravlja u Gitu.

## Stvaranje i uređivanje datoteke postavki

- Pritisnite [Alati za dokumente] na alatnoj traci → karticu [Provjera] → [Izvor pravila i postavke dokumenta] → [Uredi postavke dokumenta] i datoteka se otvara u VS Codeu. Ako datoteka ne postoji, u tom se trenutku stvara početna datoteka.
- Nazivu datoteke `lunascape-docs.json` automatski se pridružuje priloženi JSON Schema, pa dobivate dovršavanje unosa i opis svake stavke. Unos `$schema` nije potreban.

## Primjer postavki

```json
{
  "id": "product-docs",
  "title": "Dokumentacija proizvoda",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Opis stavki

| Stavka | Sadržaj | Zadano |
|---|---|---|
| `id` | Ključ pod kojim se spremaju postavke prikaza pojedinog korisnika. Dodijelite stalan ID kada želite zadržati postavke i nakon premještanja mape | Putanja mape |
| `title` | Naziv koji se prikazuje na krajnjem lijevom dijelu alatne trake i u popisu korijena dokumentacije. Ne mijenja se s promjenom jezika prikaza | Naslov iz README-a/indeksa u korijenu, inače naziv mape |
| `indexTitle` | Naslov INDEX-a | `INDEX` |
| `startPage` | Dokument koji se otvara prvi (putanja relativna prema korijenu dokumentacije) | `README.md` |
| `appearance` | Boje sučelja: `light` (uvijek svijetlo) ili `auto` (prati temu VS Codea) | `light` |
| `defaultLocale` | Zadani jezik (jezik izvornika). Navodi se oznakom jezika prema BCP 47 (`ja`, `en`, `zh-Hant` i slično). To je polazište prijevoda | Nije postavljeno (za prikaz se pretpostavlja iz teksta) |
| `fallbackLocale` | Jezik koji se prvi prikazuje čitateljima čije okruženje ne odgovara nijednom podržanom jeziku. Navedite jezik sadržan u `locales` | Nije postavljeno (koristi se `defaultLocale`) |
| `locales` | Popis podržanih jezika. Uključuje `defaultLocale`. Pojavljuju se u jezičnom izborniku i kao odredišta prijevoda | Samo `defaultLocale` |
| `ignoredDirectories` | Nazivi mapa isključenih iz INDEX-a, pretraživanja i provjera. Ako ga navedete, zamjenjuje zadano | `["99-archive"]` |
| `tree` | Zadane vrijednosti prikaza INDEX-a. Korisnik ih može nadjačati u postavkama prikaza | Kao u gornjem primjeru |
| `editor.defaultMode` | Prikaz uređivanja dok ga korisnik još nije promijenio: `visual` ili `source` | `visual` |
| `editor.showEditButton` | Prikazuje li se [Uredi] u donjem desnom kutu teksta | `true` |
| `documentStandards.pack` | Standard Pack koji se koristi za provjeru dokumenata i predloške: `builtin:<naziv>` ili putanja relativna prema korijenu dokumentacije | Nema |
| `documentStandards.profile` | Naziv profila koji definira Pack | Nema |
| `translation.enabled` | Omogućuje izradu prijedloga prijevoda i skupni prijevod | `true` |
| `translation.contextFiles` | Markdown datoteke izvornika (putanje relativne prema korijenu dokumentacije) koje se pri prijevodu predaju kao uzor za nazivlje i stil | `[]` |
| `translation.maxContextCharacters` | Gornja granica ukupnog broja znakova referentnih dokumenata (najviše 1048576) | `49152` |
| `description` | Opis skupa dokumenata u jednom retku. Prikazuje se na kartici na početnoj stranici repozitorija. Kao i `title`, može se napisati kao niz znakova ili kao objekt po jezicima | Nema |

## Kako reći gdje su dokumenti u repozitoriju

U `lunascape-docs.json` smještenom neposredno u korijenu repozitorija možete napisati **kartu repozitorija** umjesto postavki te mape. Ako napišete bilo koju od sljedeće tri stavke, datoteka postaje karta, a sama ta mapa tada nije korijen dokumentacije.

| Stavka | Sadržaj | Zadano |
|---|---|---|
| `defaultFolder` | U kojoj se mapi nalaze dokumenti (putanja relativna prema ovoj mapi). Mapi na koju upućuje nije potrebna vlastita datoteka postavki | Nema (koristi se `docs`) |
| `roots` | Popis skupova dokumenata kada ih ima više (putanje relativne prema ovoj mapi, redoslijedom prikaza). U tom slučaju ova mapa postaje početna stranica | Nema |
| `excludes` | Mape isključene iz pronalaženja korijena dokumentacije (putanje relativne prema ovoj mapi). Pribrajaju se zadanim iznimkama kao što je `node_modules` | `[]` |
| `home.cards` | Prikazuju li se kartice skupova dokumenata ispod README-a početne stranice. Postavite na `false` ako poveznice pišete sami u README-u | `true` |

Korijen dokumentacije određuje se sljedećim redoslijedom. Koristi se prvi pronađeni, odozgo prema dolje.

1. Mapa navedena u postavkama ili u naredbi, ako je navedena
2. Mapa na koju upućuje `defaultFolder` ili `roots` u `lunascape-docs.json` u korijenu repozitorija
3. Mapa u kojoj postoji `lunascape-docs.json` (ako ih pod zajedničkim nadređenim ima dvije ili više, taj nadređeni postaje početna stranica)
4. Mapa `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Sam korijen repozitorija

> **Savjet**
>
> Ako ništa ne napišete, vrijedi 4. točka, pa se uobičajeni repozitorij s jednim `docs/` ponaša kao i dosad. `defaultFolder` pišete samo kada mapu želite nazvati drukčije, primjerice `manual`.

### Primjer karte

```json
{
  "title": "Lunascape pomoć",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Redoslijed prvenstva postavki

Stavke koje se odnose na prikaz primjenjuju se sljedećim redoslijedom.

1. Korisnikove postavke prikaza (ploča [Postavke prikaza])
2. Postavke VS Codea (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Zadane vrijednosti proizvoda

Jedina su iznimka jezici (`defaultLocale`, `fallbackLocale`, `locales`): za njih je mjerodavan `lunascape-docs.json`. Osobnim postavkama VS Codea ne mogu se nadjačati jezici projekta.

> **Napomena**
>
> Standard Pack može se navesti i kao `standard` u `docs-lint.config.json`. Ako postoji u oba, prednost ima `docs-lint.config.json`.

## Povezane teme

- [Promjena pravila provjere](rules.md)
- [Promjena postavki prikaza](../02-reading/display-settings.md)
- [Popis postavki VS Codea](../08-reference/settings.md)
