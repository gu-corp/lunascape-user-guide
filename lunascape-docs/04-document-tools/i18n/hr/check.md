# Provjera dokumenata

Pomoću docs-lint možete provjeriti strukturu naslova, neispravne poveznice, nedostatak obaveznih dokumenata ili poglavlja, nedosljednost pojmova, usklađenost ID-eva zahtjeva i drugo. Provjera se uvijek provodi nad cijelim korijenom dokumentacije.

## Pokretanje provjere

1. Na alatnoj traci pritisnite [Alati za dokumente] i otvorite karticu [Provjera].
2. Pritisnite [Provjeri korijen dokumentacije].
   Provjeru možete pokrenuti i naredbom „Lunascape Docs: Provjeri korijen dokumentacije” iz palete naredbi.
3. Pregledajte popis nalaza.

## Čitanje rezultata

- Pomoću [Ovaj dokument] / [Sve] iznad popisa mijenjate opseg prikaza. Sama provjera uvijek obuhvaća cijeli korijen dokumentacije.
- Nalazi imaju četiri razine: „pogreška”, „upozorenje”, „informacija” i „prijedlog”. [Alati za dokumente] na alatnoj traci prikazuje broj pogrešaka i upozorenja.
- Pritisnite nalaz da se odgovarajuće mjesto u Markdown izvoru otvori u uređivaču VS Code.
- Nalazi koji se odnose na cijeli korijen dokumentacije (primjerice nedostatak dokumenta o testovima) prikazuju se kao stavke „Cijeli korijen dokumentacije” i nemaju položaj.
- Isti se nalazi prikazuju i na ploči „Problemi” u VS Code.

## Što se provjerava

Pritisnite [Pregledaj i promijeni pravila] za popis aktivnih provjera i svrhu svake od njih. Glavne su stavke sljedeće.

| Stavka | Sadržaj |
|---|---|
| Struktura naslova | Postoji li točno jedan H1 i preskaču li se razine naslova |
| Interne poveznice | Postoji li odredišni dokument i ostaje li unutar korijena dokumentacije |
| Jezik blokova koda | Je li za blok koda naveden naziv jezika |
| Potrebne mape i dokumenti | Postoje li sve mape i dokumenti koje traži profil paketa Standard Pack |
| Poglavlja potrebna u dokumentu | Ima li svaka vrsta dokumenta potrebna poglavlja |
| Ujednačenost pojmova | Otkriva izraze koje treba izbjegavati i potiče na preporučene pojmove |
| Imenovanje i udvostručenje ID-eva zahtjeva | Slijede li ID-evi zahtjeva pravilo imenovanja i jesu li definirani dvaput |
| Usklađenost referenci na ID-eve zahtjeva | Postoje li ID-evi zahtjeva na koje se pozivaju dizajn, testovi i tablice stanja |
| Podudaranje zahtjeva i testova | Pozivaju li se dokumenti o testovima na ID-eve zahtjeva |

Koje su stavke aktivne ovisi o paketu Standard Pack i profilu odabranima u `lunascape-docs.json` te o `docs-lint.config.json`.

> **Napomena**
>
> - Kada promijenite dokument ili postavku, prethodni rezultat dobiva oznaku „potrebna ponovna provjera”. Ništa se ne ocjenjuje uspješnim automatski. Ponovno pritisnite [Provjeri korijen dokumentacije].
> - Nespremljene promjene ne ulaze u provjeru. Najprije spremite.
> - Provjera se izvodi lokalno na uređaju i deterministički. Rezultati AI ocjena i prijevoda nikada se ne miješaju s rezultatima provjere.

## Povezane teme

- [Promjena pravila provjere](rules.md)
- [Postavke projekta](project-configuration.md)
- [Provjera, izrada ili prijevod ne uspijeva](../07-troubleshooting/tools.md)
