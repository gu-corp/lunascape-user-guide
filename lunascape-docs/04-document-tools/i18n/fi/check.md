# Dokumenttien tarkistaminen

docs-lint tarkistaa otsikkorakenteen, rikkinäiset linkit, puuttuvat pakolliset dokumentit ja luvut, termien epäjohdonmukaisuudet, vaatimustunnusten eheyden ja muuta. Tarkistus kohdistuu aina koko dokumenttijuureen.

## Tarkistuksen suorittaminen

1. Paina työkalurivin [Dokumenttityökalut]-painiketta ja avaa [Tarkistus]-välilehti.
2. Paina [Tarkista dokumenttijuuri].
   Voit suorittaa tarkistuksen myös komentopaletin komennolla ”Lunascape Docs: Tarkista dokumenttijuuri”.
3. Käy havaintoluettelo läpi.

## Tulosten lukeminen

- Luettelon yläpuolella olevilla valinnoilla [Tämä dokumentti] / [Kaikki] vaihdat näytettävän alueen. Itse tarkistus kohdistuu aina koko dokumenttijuureen.
- Havainnoilla on neljä tasoa: virhe, varoitus, tieto ja ehdotus. Työkalurivin [Dokumenttityökalut] näyttää virheiden ja varoitusten määrän.
- Kun painat havaintoa, vastaava kohta Markdown-lähteessä avautuu VS Coden editoriin.
- Koko dokumenttijuurta koskevat havainnot (kuten puuttuva testidokumentti) näkyvät kohtana ”Koko dokumenttijuuri”, eikä niillä ole sijaintia.
- Samat havainnot näkyvät myös VS Coden Ongelmat-paneelissa.

## Tarkistettavat kohdat

Kun painat [Tarkastele ja muuta sääntöjä], näet luettelon käytössä olevista tarkistuksista ja kunkin tarkoituksen. Tärkeimmät kohdat ovat seuraavat.

| Kohta | Sisältö |
|---|---|
| Otsikkorakenne | Onko H1-otsikoita täsmälleen yksi eivätkä otsikkotasot hyppää välistä |
| Sisäiset linkit | Ovatko linkitetyt dokumentit olemassa eivätkä johda dokumenttijuuren ulkopuolelle |
| Koodilohkon kieli | Onko koodilohkoille määritetty kielen nimi |
| Vaaditut kansiot ja dokumentit | Ovatko Standard Pack -profiilin vaatimat kansiot ja dokumentit olemassa |
| Dokumentin vaaditut luvut | Onko kullakin dokumenttityypillä sen vaatimat luvut |
| Termien yhtenäisyys | Havaitsee vältettävät ilmaisut ja ehdottaa suositeltuja termejä |
| Vaatimustunnusten nimeäminen ja kaksoiskappaleet | Noudattavatko vaatimustunnukset nimeämissääntöä eikä niitä ole määritelty kahdesti |
| Vaatimustunnusten viite-eheys | Ovatko suunnittelun, testien ja tilannetaulukoiden viittaamat vaatimustunnukset olemassa |
| Vaatimusten ja testien vastaavuus | Viitataanko vaatimustunnuksiin testidokumenteista |

Käyttöön tulevat kohdat määräytyvät tiedostossa `lunascape-docs.json` valitun Standard Packin ja profiilin sekä tiedoston `docs-lint.config.json` mukaan.

> **Huomautus**
>
> - Kun muutat dokumenttia tai asetusta, edellinen tulos merkitään uudelleentarkistusta vaativaksi. Mikään ei mene automaattisesti läpi. Paina [Tarkista dokumenttijuuri] uudelleen.
> - Tallentamattomat muutokset eivät sisälly tarkistukseen. Tallenna ensin.
> - Tarkistukset suoritetaan laitteessa deterministisesti. Tekoälyn arviot tai käännösten tulokset eivät sekoitu tarkistuksen tuloksiin.

## Aiheeseen liittyvää

- [Tarkistussääntöjen muuttaminen](rules.md)
- [Projektin asetukset](project-configuration.md)
- [Tarkistus, luonti tai käännös ei onnistu](../07-troubleshooting/tools.md)
