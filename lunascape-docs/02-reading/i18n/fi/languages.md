# Lukeminen toisella kielellä

Jos dokumentista on käännös, voit vaihtaa kieltä työkalurivin kielivalikosta (maapallo).

## Kielen vaihtaminen

1. Paina työkalurivin kielivalikkoa.
   Näkyviin tulevat avoinna olevan sivun kieli ja sen peruste (käännöksen polku, automaattinen tunnistus tai projektin oletuskieli).
2. Valitse kieli, jolla haluat lukea.
   Saman dokumentin käännös avautuu. Valittu kieli jää muistiin, ja seuraavaksi avaamasi dokumentti näytetään samalla kielellä, jos siitä on käännös.

Kieliluettelossa näkyy, onko dokumentista käännös kullakin kielellä.

| Merkintä | Merkitys |
|---|---|
| Käännetty | Käännös on olemassa ja sen voi avata |
| Kääntämättä | Kieli kuuluu projektin tuettuihin kieliin, mutta tästä dokumentista ei ole vielä käännöstä |
| Päivitettävä | Käännös on olemassa, mutta alkuperäisdokumenttia on muutettu kääntämisen jälkeen |

> **Huomautus**
>
> - Kielen valitseminen vain avaa olemassa olevan käännöksen. Se ei luo käännöstä eikä tiedostoa. Käännöksen tekemiseen käytetään saman valikon kohtaa [Luo ja hallitse käännöksiä…].
> - Jos avoinna olevan sivun kielen todetaan poikkeavan projektin oletuskielestä, näkyviin tulee varoitus. Asetuksia ei kirjoiteta uudelleen.

## Ensin näytettävä kieli

Kun avaat dokumentin, ensimmäinen näyttökieli määräytyy seuraavassa järjestyksessä.

1. Kieli, jonka olet aiemmin itse valinnut tässä dokumenttijuuressa. Valinta tallennetaan (myös oletuskielen valitseminen tallentuu valintana).
2. VS Coden näyttökieli (selainversiossa selaimen kieliasetus). Tuetuista kielistä valitaan automaattisesti vastaava. Aluetunnuksellinen kieli (esimerkiksi `en-US`) vastaa myös peruskieltä (`en`).
3. Projektin varakieli (`lunascape-docs.json`-tiedoston `fallbackLocale`).
4. Projektin oletuskieli.

> **Vihje**
>
> - Kun kieli on valittu automaattisesti, kielivalikon nykyisen kielen kohdalla lukee Automaattinen valinta. Kun viet osoittimen merkinnän päälle, näet perusteen.
> - `fallbackLocale` on kieli, joka näytetään lukijalle, jonka ympäristön kieli ei vastaa mitään tuetuista kielistä. Jos projektin alkuperäisdokumentit ovat japaniksi ja niistä on englanninkielinen käännös, asetus `"en"` avaa englanninkielisen version esimerkiksi espanjankielisessä ympäristössä. Jos asetusta ei ole, käytetään oletuskieltä.

## Käännösten sijainti

Oletuskieliset dokumentit pysyvät paikallaan, ja käännökset tallennetaan **saman kansion `i18n/<kieli>/`-kansioon** samalla tiedostonimellä.

```text
docs/
  README.md                  ← oletuskieli (esimerkiksi japani)
  i18n/en/README.md          ← sen englanninkielinen käännös
  guide/
    setup.md
    i18n/en/setup.md         ← sen englanninkielinen käännös
```

> **Huomautus**
>
> - Kansiorakenteen rakentamista uudelleen `i18n/`-kansion alle (`i18n/en/guide/setup.md`) ei tunnisteta. `i18n/`-kansio sijoitetaan aina samaan kansioon kääntämänsä dokumentin kanssa.
> - Käännös haetaan vain tästä yhdestä paikasta. Jos sijoitat saman dokumentin käännöksen myös yläkansion `i18n/`-kansioon, siitä ei synny kiistaa etusijasta: yläkansion tiedostosta tulee irrallinen tiedosto, joka ei näy kielivalikossa eikä luettelossa (eikä sitä poisteta automaattisesti). Älä pidä samaa käännöstä kahdessa paikassa.

## Lukeminen selainversiossa

Myös selainversiossa kieltä voi vaihtaa samalla tavalla, jos käännös on olemassa. Jos haluat lukea kielellä, josta ei ole käännöstä, voit käyttää selaimen sivunkäännöstoimintoa. Koodi, matematiikka ja kaaviot on rajattu kääntämisen ulkopuolelle.

## Aiheeseen liittyvää

- [Työn antaminen tekoälylle](../05-ai/README.md)
- [Annettavat työt](../05-ai/tasks.md)
- [Näyttöasetusten muuttaminen](../02-reading/display-settings.md)
