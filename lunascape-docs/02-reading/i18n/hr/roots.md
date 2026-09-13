# Prebacivanje korijena dokumentacije

Korijen dokumentacije je najviša mapa jednog skupa dokumenata. INDEX, filtriranje, provjere i prijevod rade po korijenu dokumentacije.

## Kako se pronalazi korijen dokumentacije

Lunascape Docs kreće od otvorene Markdown datoteke prema nadređenim mapama i za korijen dokumentacije uzima najbližu mapu koja odgovara jednome od sljedećega.

- Mapa koja sadrži `lunascape-docs.json` (naziv mape nije važan)
- Mapa naziva `docs` (dodatne nazive možete dodati postavkom `lunascapeDocEditor.rootDirectoryNames`)

Kada pokrenete naredbu „Lunascape Docs: Otvori preglednik specifikacija”, otvara se korijen dokumentacije iz postavke `lunascapeDocEditor.root` (zadano `docs`).

## Prebacivanje na drugi korijen dokumentacije

Kada radni prostor ima više korijena dokumentacije, naziv korijena na lijevom kraju alatne trake postaje padajući izbornik.

1. Pritisnite naziv korijena dokumentacije na lijevom kraju alatne trake.
2. Na popisu odaberite korijen dokumentacije.
   Prikazuje se početna stranica odabranog korijena dokumentacije, a INDEX se mijenja.

> **Savjet**
>
> Nazivi na popisu određuju se ovim redoslijedom. Ne mijenjaju se ni kada promijenite jezik prikaza.
>
> 1. `title` u datoteci `lunascape-docs.json`
> 2. `navigation.title` datoteke `README.md` u korijenu, a ako ga nema, njezin H1
> 3. `navigation.title` datoteke `index.md` u korijenu, a ako ga nema, njezin H1
> 4. Naziv mape (kod standardne mape `docs` naziv njezine nadređene mape)

## Otvaranje Markdown datoteke izvan korijena dokumentacije

Kada otvorite Markdown datoteku koja nije u korijenu dokumentacije, mapa u kojoj se ona nalazi privremeno se prikazuje kao korijen dokumentacije. U INDEX-u su navedene Markdown datoteke iz te mape i iz mapa ispod nje.

- Pritisnite [Na mapu iznad] na alatnoj traci da biste opseg prikaza proširili na nadređenu mapu unutar radnog prostora.
- U ovom prikazu nisu dostupne jezične postavke projekta ni skupni prijevod. Postat će dostupne ako u tu mapu stavite `lunascape-docs.json` i tako je učinite korijenom dokumentacije.

## Otvaranje uvijek istoga korijena dokumentacije

Ako postavku `lunascapeDocEditor.rootMode` postavite na `fixed`, uvijek se otvara korijen dokumentacije iz `lunascapeDocEditor.root`, koju god Markdown datoteku otvorili.

## Povezane teme

- [Korijen dokumentacije i pravila za datoteke](../04-document-tools/structure.md)
- [Postavke projekta](../04-document-tools/project-configuration.md)
- [Popis postavki VS Code](../08-reference/settings.md)
