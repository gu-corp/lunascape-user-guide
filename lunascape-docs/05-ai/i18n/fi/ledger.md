# Luettelo ja merkinnät

[AI]-välilehden yläosassa oleva luettelo kertoo käännöstilanteen jokaisella tuetulla kielellä. Näet siitä, mitä puuttuu, vaikka et käyttäisi tekoälyä.

| Näyttö | Merkitys |
|---|---|
| Kääntämättä | Niiden dokumenttien määrä, joista ei vielä ole käännöstä |
| Päivitettävä | Niiden dokumenttien määrä, joiden käännös on olemassa, mutta joiden alkuperäisdokumentti on merkintää uudempi |
| Käännetty | Alkuperäisdokumenttiaan seuraavien käännösten määrä |

Luettelo lasketaan käymällä dokumenttijuuri läpi. Tekoäly tai kielimalli ei osallistu siihen.

## Päivitä käännösmerkinnät

Tilan ”Päivitettävä” päätteleminen edellyttää merkintää siitä, millaisia alkuperäisdokumentti ja käännös olivat käännöshetkellä. Istuntopohjainen tekoäly kirjoittaa tiedostot suoraan, joten merkintä ei synny automaattisesti.

1. Kun käännös on valmis ja olet tarkistanut sen sisällön, paina [Päivitä käännösmerkinnät].
2. Käännökset, joilla ei ole merkintää, merkitään nykyistä alkuperäisdokumenttia vastaaviksi.

Claude Code -istunnot ja API-tyyppisen palvelun tallennukset tekevät merkinnän automaattisesti (istuntoa ohjeistetaan käyttämään MCP-työkalua `record_translation_freshness`). Painiketta tarvitaan silloin, kun käännös on tehty Codexilla tai VS Coden chatissa.

Tämän jälkeen alkuperäisdokumentin muuttaminen näyttää sen käännöksen tilassa ”Päivitettävä”.

> **Huomautus**
>
> - Käännöksiä, joilla jo on merkintä, ei korvata. Näin olemassa oleva ”Päivitettävä”-tila ei katoa.
> - Merkinnät tallennetaan tiedostoon `.lunascape-docs/translation-freshness.json`. Siihen tallentuvat vain suhteellinen polku, kieli, sisällön tiiviste ja ajankohta – ei dokumentin tekstiä.

## Aiheeseen liittyvää

- [Annettavat työt](tasks.md)
- [Lukeminen toisella kielellä](../02-reading/languages.md)
