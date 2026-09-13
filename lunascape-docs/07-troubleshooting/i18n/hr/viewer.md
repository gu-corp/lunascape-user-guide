# Dokumenti se ne prikazuju

## Prikazuje se poruka „Nije pronađena nijedna Markdown datoteka ni mapa docs koju je moguće otvoriti”

- U radnom prostoru nema mape `docs` ili se koristi ime različito od `docs`.
  - Ako u tu mapu stavite `lunascape-docs.json`, ona se prepoznaje kao korijen dokumentacije bez obzira na ime.
  - Ili dodajte ime mape u postavku `lunascapeDocEditor.rootDirectoryNames`.
- Ako dokumenata još nema, izradite ih naredbom „Lunascape Docs: Izradi dokumentaciju iz predloška”.
- Moguće je i otvoriti Markdown datoteku u uređivaču pa pokrenuti naredbu „Lunascape Docs: Otvori u pregledniku specifikacija”.

## Dokument se ne prikazuje u INDEX-u

- Provjerite je li nastavak `.md`, `.markdown` ili `.mdx`.
- Sljedeće se mape ne prikazuju: mape koje počinju točkom `.`, `node_modules` i mape navedene u `ignoredDirectories` (zadano `99-archive`).
- Prijevodi koji se nalaze u mapi `i18n/` ne prikazuju se zasebno u INDEX-u. Na njih se prebacujete jezičnim izbornikom.
- Ako se datoteka koju ste upravo dodali ne prikazuje, pritisnite [Ponovno učitaj].
- Možda gledate drugi korijen dokumentacije. Provjerite ime korijena dokumentacije na lijevom kraju alatne trake.

## Pritisak na mapu ne prikazuje ništa

Datoteka `README.md` te mape „deskriptor je samo za postavke”: ima front matter, ali nema sadržaja. Otvorite mapu u INDEX-u i odaberite dokument u njoj.

## Otvara se korijen dokumentacije koji niste željeli

- Ako je postavka `lunascapeDocEditor.rootMode` postavljena na `fixed`, uvijek se otvara `lunascapeDocEditor.root`.
- Uz `auto` odabire se korijen dokumentacije najbliži otvorenoj Markdown datoteci. Možete ga promijeniti padajućim izbornikom na lijevom kraju alatne trake.

## Ime korijena dokumentacije razlikuje se od očekivanog

Ime se određuje ovim redoslijedom: `title` u `lunascape-docs.json` → `navigation.title` u korijenskoj datoteci `README.md` → njezin H1 → `index.md` → ime mape. Ako ga želite učvrstiti, postavite `title`.

## INDEX je nestao

- U korijenu dokumentacije koji ima samo jedan dokument INDEX se prvi put automatski zatvara. Možete ga otvoriti ikonom prikaza stupaca na alatnoj traci. To možete isključiti opcijom [Sakrij kada postoji samo jedan dokument] u [Postavke prikaza].
- Na uskom zaslonu otvorite ga pomoću [Otvori INDEX] (tri crte) lijevo od [Natrag].

## Poveznica se ne otvara

- „Odredište poveznice nije pronađeno”: ciljna datoteka ne postoji. Unutarnje poveznice možete provjeriti pomoću [Provjera] u Alatima za dokumente.
- „Nesigurna ili nepodržana poveznica nije otvorena”: poveznice izvan korijena dokumentacije i poveznice na sheme osim `https://` i `mailto:` ne otvaraju se.

## Prikazuje se jezik koji niste željeli

- U jezičnom izborniku provjerite jezik prikazane stranice i razlog zbog kojeg je odabran.
- Jezik prikaza koji ste zadnji put odabrali zapamćen je. U jezičnom izborniku ponovno odaberite zadani jezik.
- Ako je postavljena osobna postavka `lunascapeDocEditor.locale`, prednost ima prijevod na taj jezik.

## Povezane teme

- [Prebacivanje između korijena dokumentacije](../02-reading/roots.md)
- [Korijen dokumentacije i pravila za datoteke](../04-document-tools/structure.md)
