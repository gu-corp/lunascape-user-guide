# Stvaranje prvih dokumenata

U projektu koji još nema mapu s dokumentacijom, početni skup dokumenata možete stvoriti iz palete naredbi.

1. Otvorite mapu projekta u VS Codeu i označite radni prostor kao pouzdan.
2. U paleti naredbi (`⇧⌘P` / `Ctrl+Shift+P`) pokrenite „Lunascape Docs: Stvori dokumentaciju iz predloška”.
   Ako radni prostor ima više mapa, odaberite onu u kojoj će se dokumenti stvoriti.
3. Odaberite strukturu koju želite stvoriti.
   - [Jednostranični dokument]: samo `README.md`. Prikladno za kratku specifikaciju, bilješke ili samostalan opis.
   - [Skup dokumenata]: početna stranica te ulazne stranice za `specification/` (specifikacija), `manual/` (priručnik) i `help/` (pomoć).
4. Unesite naslov dokumenta. Koristi se za README i za naslove pojedinih dokumenata.
5. Unesite mapu s dokumentacijom koju treba stvoriti, relativno u odnosu na radni prostor. Zadano je `docs`.
6. Pregledajte popis datoteka koje će se stvoriti i pritisnite [Stvori].
   Kada stvaranje završi, novi `README.md` otvara se u pregledniku.

> **Napomena**
>
> - Postojeće datoteke nikada se ne prepisuju. Ako već postoji makar jedna od datoteka koje treba stvoriti, ništa se ne stvara i postupak se prekida.
> - Stvaranje nije dostupno u radnom prostoru koji nije pouzdan.

> **Savjet**
>
> - Ako već imate mapu s dokumentacijom, preskočite ovaj postupak i prijeđite na [Osnovne radnje](../02-reading/README.md).
> - Kako dokumentacija raste, dokumente možete dodavati jedan po jedan iz predložaka na kartici [Stvori] u Alatima za dokumente.

## Povezane teme

- [Stvaranje dokumenta iz predloška](../04-document-tools/templates.md)
- [Korijeni dokumentacije i pravila za datoteke](../04-document-tools/structure.md)
