# Korijen dokumentacije i pravila za datoteke

Pravila po kojima Lunascape Docs pronalazi dokumente i sastavlja INDEX. Sam datotečni sustav je izvornik, pa nisu potrebni ni popis ni postavke za izgradnju.

## Korijen dokumentacije

- Najbliža mapa `docs` ili mapa u kojoj se nalazi `lunascape-docs.json` postaje korijen dokumentacije.
- Ako postavite `lunascape-docs.json`, mapa se ne mora zvati `docs`.
- Kada otvorite Markdown koji ne pripada nijednom korijenu dokumentacije, njegova se mapa prikazuje kao privremeni korijen dokumentacije.

## Datoteke koje se prikazuju u INDEX-u

- Prikazuju se datoteke `.md`, `.markdown` i `.mdx`. Nove se datoteke uvijek prikazuju, i bez front mattera ili navigacijskih podataka.
- Mape koje počinju s `.`, `node_modules` te mape navedene u `ignoredDirectories` (zadano `99-archive`) ne prikazuju se.
- Sve ispod `i18n/` smatra se prijevodima i ne prikazuje se zasebno u INDEX-u.

## Naslovnica mape

- `README.md` s tekstom (ili `index.md` ako READMEa nema) naslovnica je svoje mape. Pritiskom na naziv mape u INDEX-u otvara se naslovnica.
- `README.md` koji sadrži samo front matter, bez teksta, smatra se „deskriptorom samo za postavke” i ne prikazuje se kao stranica. Upotrijebite ga kada mapi treba dati samo naslov ili redoslijed.
- Kada postoje i `README.md` i `index.md`, prednost ima `README.md`.

## Zadani jezik i prijevodi

- Dokumenti na zadanom jeziku (izvornici) ostaju na svojem mjestu.
- Prijevod se sprema u mapu `i18n/<jezik>/` uz izvornik, pod istim nazivom datoteke. Ponovna izgradnja strukture mapa ispod `i18n/` ne prepoznaje se.
- To je jedino mjesto s kojeg se prijevod razrješava. Ista datoteka smještena bilo gdje drugdje ostaje osamljena i nijedan je dokument ne preuzima kao svoj prijevod.

```text
docs/
  lunascape-docs.json
  README.md                  ← naslovnica korijena dokumentacije (početna stranica)
  i18n/en/README.md          ← njezina engleska verzija
  01-product/
    README.md                ← naslovnica mape
    requirements.md
    i18n/en/README.md        ← engleske verzije dvaju dokumenata iznad
    i18n/en/requirements.md
  99-archive/                ← zadano isključeno iz INDEX-a
```

## O datoteci `_meta.json`

Nextrin `_meta.json` ne upotrebljava se za navigaciju. Postojeće se datoteke niti mijenjaju niti brišu. Ubuduće će se njima baviti samo izričita značajka uvoza i izvoza.

## Povezane teme

- [Postavljanje navigacijskih podataka](navigation-metadata.md)
- [Postavke projekta](project-configuration.md)
- [Promjena korijena dokumentacije](../02-reading/roots.md)
