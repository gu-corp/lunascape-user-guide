# Provjera, stvaranje ili prijevod ne uspijeva

## Provjera

### Prikazuje se poruka „docs-lint nije dostupan”

- Izvršno okruženje za docs-lint nije uključeno u proširenje ili postoji problem s postavkama. Ponovno instalirajte proširenje.
- „Da biste sigurno učitali lokalni Pack i postavke, označite ovaj radni prostor kao pouzdan u VS Codeu”: za upotrebu lokalnog Standard Packa potreban je pouzdani radni prostor.

### Rezultat ostaje na „potrebna je ponovna provjera”

Kada izmijenite dokument ili postavke, prethodni rezultat prestaje vrijediti. Ponovno pritisnite [Provjeri korijen dokumentacije]. Nespremljene izmjene neće biti uključene.

### Pritisak na nalaz ne otvara ništa

Stavke koje se odnose na „cijeli korijen dokumentacije” nisu vezane uz određeni dokument pa nemaju položaj. Provjerite odgovarajući dokument prema sadržaju nalaza.

### Pravilo se ne može spremiti

- Potreban je pouzdani radni prostor.
- „Postavke Linta promijenjene su drugom radnjom”: datoteka `docs-lint.config.json` promijenjena je izvana. Učitajte najnovije stanje pa pokušajte ponovno.
- Simbolične poveznice i datoteke postavki izvan korijena dokumentacije ne mogu se uređivati.

## Stvaranje iz predloška

- „Pregled predloška je istekao” / „Uneseni sadržaj je promijenjen”: ponovno pritisnite [Pregled] pa zatim stvorite dokument.
- „Dokument na odredištu već postoji”: postojeće datoteke ne prepisuju se. Navedite drugo odredište.
- Odredište mora biti relativna putanja od korijena dokumentacije s nastavkom `.md` ili `.mdx`. Unutar mape `i18n` ne može se stvarati.
- „Da biste stvarali dokumente, označite radni prostor kao pouzdan”: označite radni prostor kao pouzdan u VS Codeu.

<!-- ai-only:start -->
## Prijevod

### Gumbi za prijevod ne mogu se pritisnuti

- „AI prijevod nije omogućen za ovaj korijen dokumentacije”: postavite `translation.enabled` na `true` u datoteci `lunascape-docs.json`.
- „Zadani jezik projekta nije postavljen”: spremite zadani jezik prema uputama u [Promjena postavki prikaza](../02-reading/display-settings.md).
- „Dodajte odredišni jezik među podržane jezike”: dodajte jezik prijevoda u `locales`.
- „Nije pronađen izvornik za prijevod”: otvorena je prevedena stranica. Prijeđite na stranicu na zadanom jeziku.
- Skupni prijevod nije dostupan dok je mapa otvorena privremeno. Stavite datoteku `lunascape-docs.json` u tu mapu kako bi postala korijen dokumentacije.

### Prijedlog prijevoda je odbijen ili ga treba izraditi ponovno

- „Izvornik je promijenjen. Izradite prijedlog prijevoda ponovno”: izvornik ili odredište prijevoda promijenjeni su nakon izrade prijedloga. Prevedite ponovno.
- Ako u odgovoru jezičnog modela nedostaju zaštićeni identifikatori ili kôd, odgovor se ne prihvaća. Sadržaj odgovora možete provjeriti u izlaznoj ploči „Lunascape Docs prijevod”.
- „Skupni prijevod obuhvaća najviše 1000 dokumenata odjednom”: podijelite opseg po mapama ili izričitim odabirom.
<!-- ai-only:end -->

## Povezane teme

- [Provjera dokumenata](../04-document-tools/check.md)
- [Stvaranje dokumenta iz predloška](../04-document-tools/templates.md)
- [Predaja posla AI-ju](../05-ai/README.md)
