# Dokumenttijuuren vaihtaminen

Dokumenttijuuri on yhden dokumenttijoukon ylin kansio. INDEX, suodatus, tarkistukset ja käännös toimivat kaikki dokumenttijuuri kerrallaan.

## Miten dokumenttijuuri löytyy

Lunascape Docs etenee avatusta Markdown-tiedostosta yläkansioita pitkin ylöspäin ja ottaa dokumenttijuureksi lähimmän kansion, joka täyttää jonkin seuraavista.

- Kansio, jossa on `lunascape-docs.json` (kansion nimellä ei ole väliä)
- Kansio nimeltä `docs` (asetuksella `lunascapeDocEditor.rootDirectoryNames` voit lisätä nimiä)

Kun suoritat komennon ”Lunascape Docs: Avaa määrittelykatselin”, avautuu asetuksen `lunascapeDocEditor.root` (oletus `docs`) mukainen dokumenttijuuri.

## Vaihda toiseen dokumenttijuureen

Kun työtilassa on useita dokumenttijuuria, työkalurivin vasemmassa reunassa oleva dokumenttijuuren nimi muuttuu pudotusvalikoksi.

1. Paina työkalurivin vasemmassa reunassa olevaa dokumenttijuuren nimeä.
2. Valitse dokumenttijuuri luettelosta.
   Valitun dokumenttijuuren aloitussivu tulee näkyviin ja INDEX vaihtuu.

> **Vihje**
>
> Luettelossa näkyvät nimet määräytyvät seuraavassa järjestyksessä. Ne eivät muutu, vaikka vaihtaisit näyttökieltä.
>
> 1. `lunascape-docs.json`-tiedoston `title`
> 2. Juuren `README.md`-tiedoston `navigation.title`, tai jos sitä ei ole, sen H1
> 3. Juuren `index.md`-tiedoston `navigation.title`, tai jos sitä ei ole, sen H1
> 4. Kansion nimi (tavallisessa `docs`-kansiossa sen yläkansion nimi)

## Avaa Markdown-tiedosto dokumenttijuuren ulkopuolelta

Kun avaat Markdown-tiedoston, joka ei kuulu mihinkään dokumenttijuureen, sen kansio näytetään tilapäisenä dokumenttijuurena. INDEX luettelee samassa kansiossa ja sen alla olevat Markdown-tiedostot.

- Kun painat työkalurivin [Ylempään kansioon], näkymä laajenee työtilan sisällä yläkansioon.
- Tässä näkymässä projektin kieliasetukset ja joukkokäännös eivät ole käytettävissä. Ne tulevat käyttöön, kun lisäät kansioon `lunascape-docs.json` ja teet siitä dokumenttijuuren.

## Avaa aina sama dokumenttijuuri

Kun asetat asetuksen `lunascapeDocEditor.rootMode` arvoksi `fixed`, avautuu aina asetuksen `lunascapeDocEditor.root` dokumenttijuuri riippumatta siitä, minkä Markdown-tiedoston avaat.

## Aiheeseen liittyvää

- [Dokumenttijuuret ja tiedostokäytännöt](../04-document-tools/structure.md)
- [Projektiasetukset](../04-document-tools/project-configuration.md)
- [VS Code -asetukset](../08-reference/settings.md)
