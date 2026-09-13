# Čitanje na drugom jeziku

Dokument koji ima prijevode možete čitati na drugom jeziku tako da jezik promijenite u izborniku jezika (globus) na alatnoj traci.

## Promjena jezika

1. Pritisnite izbornik jezika na alatnoj traci.
   Prikazuju se jezik otvorene stranice i razlog za taj jezik (putanja prijevoda, automatsko prepoznavanje ili zadani jezik projekta).
2. Odaberite jezik na kojem želite čitati.
   Otvara se prijevod istog dokumenta. Odabrani jezik pamti se, pa se i sljedeći dokument koji otvorite prikazuje na tom jeziku ako prijevod postoji.

U popisu jezika prikazuje se ima li taj dokument prijevod.

| Prikaz | Značenje |
|---|---|
| Prevedeno | Prijevod postoji i može se otvoriti |
| Nije prevedeno | Projekt podržava taj jezik, ali prijevod ovog dokumenta još ne postoji |
| Zastarjelo | Prijevod postoji, ali je izvorni dokument promijenjen nakon prevođenja |

> **Napomena**
>
> - Odabir jezika samo otvara postojeći prijevod. Prijevod se pritom ne stvara niti se stvara datoteka. Za izradu prijevoda upotrijebite [Stvori i upravljaj prijevodima…] u istom izborniku.
> - Kad se utvrdi da se jezik prikazane stranice razlikuje od zadanog jezika projekta, prikazuje se upozorenje. Postavke se pritom ne mijenjaju.

## Jezik koji se prikazuje prvi

Kad otvorite dokument, jezik prvog prikaza određuje se ovim redoslijedom.

1. Jezik koji ste prije sami odabrali u ovom korijenu dokumentacije. Odabir se sprema (i odabir zadanog jezika sprema se kao odabir).
2. Jezik prikaza programa VS Code (u web-pregledniku postavke jezika preglednika). Automatski se odabire jezik koji odgovara podržanim jezicima. Jezik s oznakom regije (npr. `en-US`) odgovara i osnovnom jeziku (`en`).
3. Zamjenski jezik projekta (`fallbackLocale` u datoteci `lunascape-docs.json`).
4. Zadani jezik projekta.

> **Savjet**
>
> - Kad je jezik odabran automatski, uz trenutačni jezik u izborniku jezika prikazuje se oznaka „automatski odabrano”. Kad pokazivač zadržite na oznaci, prikazuje se razlog.
> - `fallbackLocale` je jezik koji se prikazuje čitateljima čiji jezik okruženja ne odgovara nijednom podržanom jeziku. Ako u projektu u kojem je izvornik na japanskom i postoji engleska verzija postavite `"en"`, čitatelju u, primjerice, španjolskom okruženju otvorit će se engleska verzija. Ako nije postavljen, upotrebljava se zadani jezik.

## Gdje se nalaze prijevodi

Dokumenti na zadanom jeziku ostaju na svojem mjestu, a prijevod se stavlja u **`i18n/<jezik>/` u istoj mapi**, pod istim nazivom datoteke.

```text
docs/
  README.md                  ← zadani jezik (primjerice japanski)
  i18n/en/README.md          ← njegova engleska verzija
  guide/
    setup.md
    i18n/en/setup.md         ← njegova engleska verzija
```

> **Napomena**
>
> - Struktura mapa ponovno izgrađena ispod mape `i18n/` (`i18n/en/guide/setup.md`) ne prepoznaje se. Mapa `i18n/` uvijek se nalazi u istoj mapi kao i dokument.
> - Prijevod se razrješava samo s tog jednog mjesta. Ako prijevod istog dokumenta stavite i u mapu `i18n/` nadređene mape, neće doći do sukoba oko toga što ima prednost: ta kopija postaje osamljena datoteka koja se ne pojavljuje ni u izborniku jezika ni u evidenciji (i ne briše se automatski). Nemojte isti prijevod držati na dva mjesta.

## Čitanje u web-pregledniku

I u web-pregledniku jezik možete promijeniti na isti način ako prijevod postoji. Kad želite čitati na jeziku za koji prijevod ne postoji, možete upotrijebiti prevođenje stranice u pregledniku. Kod, matematički izrazi i dijagrami izuzeti su iz prevođenja.

## Povezane teme

- [Predaja posla AI-ju](../05-ai/README.md)
- [Poslovi koje možete predati](../05-ai/tasks.md)
- [Promjena postavki prikaza](../02-reading/display-settings.md)
