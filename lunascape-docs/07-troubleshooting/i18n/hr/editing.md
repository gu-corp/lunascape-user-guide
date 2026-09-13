# Nije moguće uređivati, spremiti ni promijeniti redoslijed

## Nema gumba [Uredi]

- [Gumb za uređivanje] u [Postavke prikaza] je isključen. Uključite ga ili upotrijebite [⋯] → [Uredi] u gornjem desnom kutu teksta odnosno [Uredi] u izborniku stavke u INDEX-u.
- Isto vrijedi i kada je `editor.showEditButton` u datoteci `lunascape-docs.json` postavljen na `false`.
- Dok je prikazana pomoć, uređivanje nije moguće. Zatvorite pomoć.

## Nije moguće prijeći na vizualni prikaz

„Ovaj dokument sadrži MDX sintaksu pa se ne može otvoriti u uobičajenom prikazu za uređivanje”: dokumenti koji sadrže sintaksu svojstvenu MDX-u (komponente, `import` i slično) uređuju se samo u prikazu Markdowna kako bi se ta sintaksa očuvala.

## Nije moguće izravno urediti matematičke izraze ni dijagrame

Vizualni prikaz prikazuje rezultat iscrtavanja. U prikazu za uređivanje pritisnite [Markdown] i uredite izvorni kôd.

## Nije moguće promijeniti redoslijed ni povlačiti stavke

- Redoslijed se ne može mijenjati tijekom filtriranja, tijekom uređivanja dokumenta ni dok je u tijeku druga radnja u INDEX-u.
- Ako radni prostor nije pouzdan, radnje stvaranja, sređivanja i brisanja nisu dostupne. Označite radni prostor kao pouzdan u VS Code.
- „INDEX je ažuriran. Povucite ponovno”: upravo je primijenjena druga promjena. Ponovite radnju.
- Početna stranica (korijenska datoteka `README.md`) ne može se premjestiti.

## Prikazuje se poruka „Postoje nespremljene promjene”

Odabrana datoteka trenutačno se uređuje u uređivaču VS Code. Najprije spremite ili odbacite promjene pa pokušajte ponovno.

## Nije moguće promijeniti naziv

Sljedeći se nazivi ne mogu upotrijebiti.

- Nazivi koji počinju s `.`, naziv `i18n` te nazivi rezervirani u sustavu Windows (`CON` i slično)
- Nazivi koji završavaju točkom ili razmakom te nazivi koji sadrže upravljačke znakove ili znakove nedopuštene u nazivima datoteka
- Nazivi koji već postoje u istoj mapi (uključujući nazive koji se razlikuju samo po velikim i malim slovima)
- Nazivi dokumenata bez nastavka za Markdown

## Spremio sam promjene, ali se ne pojavljuju u Gitu ili nisu potvrđene

Lunascape Docs samo zapisuje u datoteku; ne obavlja pripremu ni potvrđivanje promjena u Gitu. Provjerite prikaz kontrole izvornog kôda u VS Code i po potrebi potvrdite promjene.

## Povezane teme

- [Uređivanje dokumenta](../03-editing/README.md)
- [Stvaranje i sređivanje dokumenata i mapa](../03-editing/organize.md)
- [Promjena redoslijeda dokumenata](../03-editing/reorder.md)
