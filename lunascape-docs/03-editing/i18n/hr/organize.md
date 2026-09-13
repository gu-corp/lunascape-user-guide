# Stvaranje i organiziranje dokumenata i mapa

Iz izbornika stavke u INDEX-u možete stvarati, duplicirati, preimenovati i brisati dokumente i mape. Unos se obavlja u malom dijaloškom okviru unutar preglednika, bez prekidanja čitanja.

> **Napomena**
>
> Ove su radnje dostupne samo kada je radni prostor označen kao pouzdan u VS Code. Ne mogu se izvesti dok se dokument uređuje, dok je druga radnja u tijeku ili kada odabrana stavka ima nespremljene promjene.

## Stvaranje dokumenta ili mape

1. Otvorite izbornik stavke ([⋯] ili desni klik) mape u kojoj želite stvoriti stavku.
   Za stvaranje izravno u korijenu dokumentacije upotrijebite [⋯] na desnom kraju naslova INDEX ili desnom tipkom miša kliknite prazan dio INDEX-a.
2. Odaberite [Novi dokument] ili [Nova mapa].
3. Unesite naziv i pritisnite [Stvori].
   Naziv dokumenta mora imati Markdown nastavak (`.md`, `.markdown`, `.mdx` i slično).

Novi dokumenti stvaraju se kao dokumenti na zadanom jeziku (izvornici).

## Dupliciranje dokumenta

1. Otvorite izbornik stavke dokumenta i odaberite [Dupliciraj].
2. Unesite novi naziv i pritisnite [Stvori].

Duplicira se samo izvornik. Prijevodi se ne dupliciraju.

## Promjena naslova

Mijenja naslov dokumenta (H1). Naziv datoteke ostaje isti.

1. Otvorite izbornik stavke dokumenta ili mape i odaberite [Promijeni naslov].
2. Unesite novi naslov u jednom retku i pritisnite [Promijeni].

Kod mape mijenja se naslov njezine datoteke `README.md`. Kada je prikazan prijevod, mijenja se naslov dokumenta na tom jeziku.

## Promjena naziva dokumentacije

Mijenja naziv dokumentacije prikazan na alatnoj traci (naziv korijena dokumentacije).

1. Desnom tipkom miša kliknite naziv dokumentacije na alatnoj traci. Isti izbornik otvara i [⋯] na desnom kraju naslova INDEX.
2. Odaberite [Promijeni naziv dokumenta] i unesite novi naziv.

Dok ništa nije postavljeno, prikazuje se naziv mape takav kakav jest.

Naziv koji postavite zapisuje se na **ono mjesto s kojeg se naziv dokumentacije trenutačno uzima**, tako da naslov koji vidite nikada ne ostane zanemaren.

| Trenutačno stanje | Zapisuje se u |
|---|---|
| `lunascape-docs.json` sadrži naziv | Ažurira se `lunascape-docs.json` |
| Naziva nema, ali korijen dokumentacije ima README | Prepisuje se naslov (H1) u README-u |
| Nema ni jedno ni drugo | Stvara se `lunascape-docs.json` i naziv se sprema u njega |

U poruci nakon promjene navedeno je gdje je naziv zapisan.

> **Savjet**
>
> Naziv dokumentacije određuje se ovim redoslijedom: naziv u datoteci `lunascape-docs.json`, zatim naslov README-a u korijenu dokumentacije, pa naziv mape.

## Promjena naziva datoteke ili mape

1. Otvorite izbornik stavke i odaberite [Promijeni naziv datoteke] ili [Promijeni naziv mape].
2. Unesite novi naziv i pritisnite [Promijeni].

Odgovarajući prijevodi (ista putanja u `i18n/<jezik>/`) preimenuju se zajedno s njom.

## Brisanje

1. Otvorite izbornik stavke i odaberite [Premjesti u smeće].
2. Provjerite sadržaj poruke potvrde i odobrite premještanje.

Stavka se premješta u koš za smeće operacijskog sustava pa se po potrebi može vratiti. Prijevodi se ne brišu i ostaju na svojem mjestu.

## Nazivi koji se ne mogu upotrijebiti

- Nazivi koji počinju s `.` (ne bi se prikazali u INDEX-u)
- `i18n` (rezervirano za datoteke prijevoda)
- Nazivi rezervirani u sustavu Windows (`CON`, `PRN` i slično)
- Nazivi koji završavaju točkom ili razmakom
- Nazivi s upravljačkim znakovima ili znakovima koji nisu dopušteni u nazivima datoteka
- Nazivi koji već postoje u istoj mapi (uključujući nazive koji se razlikuju samo po veličini slova)

> **Napomena**
>
> Početna stranica (obično `README.md` u korijenu) ne može se preimenovati ni premjestiti. Najprije promijenite `startPage` u datoteci `lunascape-docs.json`.

## Povezane teme

- [Promjena redoslijeda dokumenata](reorder.md)
- [Upotreba INDEX-a](../02-reading/index-panel.md)
