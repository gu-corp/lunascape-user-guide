# Dokumentin luominen mallista

Dokumenttityökalujen [Luo]-välilehdellä voit valita mallin, esikatsella sisältöä ja luoda sitten uuden dokumentin.

1. Paina työkalurivin [Dokumenttityökalut]-painiketta ja avaa [Luo]-välilehti.
2. Paina [Luo mallista] ja valitse malli.
3. Täytä syöttökentät (otsikko, tiivistelmä ja niin edelleen). Pakollisissa kentissä lukee ”pakollinen”.
4. Kirjoita tallennuskohde polkuna suhteessa dokumenttijuureen (esimerkiksi `03-design/api.md`).
5. Paina [Esikatselu] ja tarkista luotava Markdown.
6. Paina [Luo tällä sisällöllä].
   Dokumentti luodaan ja näytetään katselimessa. Tämän jälkeen koko dokumenttijuuri tarkistetaan.

## Valittavat mallit

| Malli | Sisältö |
|---|---|
| Yhden sivun dokumentti | Lyhyt määrittely, muistiinpano tai erillinen selostus yhtenä tiedostona |
| Määrittely, käyttöopas, ohje | Yksi tiedosto, jossa on yleiskäyttöinen lukurakenne määrittelyä, käyttöopasta tai ohjetta varten |
| Standard Pack -mallit | Kun `lunascape-docs.json`-tiedostossa on valittu Standard Pack, mukaan tulevat sen profiilin sallimat dokumenttityypit (vaatimusmäärittely, suunnitteludokumentti ja niin edelleen) |

> **Huomautus**
>
> - Luominen edellyttää luotettua työtilaa.
> - Olemassa olevia tiedostoja ei korvata. Dokumenttia ei voi luoda, jos tallennuskohteessa on samanniminen dokumentti.
> - Tallennuskohteessa on oltava tarkenne `.md` tai `.mdx`. Kansion `i18n` alle (käännösten sijaintiin) ei voi luoda dokumentteja.
> - Kun muutat syötteitä, paina [Esikatselu] uudelleen ennen luomista.

> **Vihje**
>
> Jos projektissa ei vielä ole dokumenttikansiota, voit luoda ensimmäisen kokonaisuuden komentopaletin komennolla ”Lunascape Docs: Luo dokumentaatio mallista”. Katso [Ensimmäisten dokumenttien luominen](../01-introduction/first-documents.md).

## Aiheeseen liittyvää

- [Dokumenttityökalujen käyttö](README.md)
- [Tarkistussääntöjen muuttaminen](rules.md)
