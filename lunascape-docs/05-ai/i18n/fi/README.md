# Työn antaminen tekoälylle

Lunascape Docs ei kutsu kielimallia. Se valmistelee **asiayhteyden, työkalut ja tarkistukset** ja jättää kääntämisen, oikoluvun ja kirjoittamisen käyttämällesi tekoälylle.

## Ajatus

| Mitä tuote tarjoaa | Sisältö |
|---|---|
| Asiayhteys | Dokumenttien käytännöt (käännösten sijainti, front matter, dokumenttistandardi, sanasto) ja kohdedokumentin sijainti |
| Työkalut | Kääntämättä olevien ja päivitettävien käännösten luettelo, dokumenttien luku ja kirjoitus, luonti mallista |
| Jälkitarkistus | docs-lint-tarkistus sekä kattavuuden ja tuoreuden erot |

Ohje ei sisällä dokumentin tekstiä. Tekoäly lukee tiedostot itse, kirjoittaa ne itse ja tarkistaa ne itse.

## Työn antaminen

1. Paina työkalurivin [Dokumenttityökalut]-painiketta ja avaa [AI]-välilehti.
2. Valitse annettava työ kohdasta [Työ].
3. Täytä tarvittavat tiedot (kohdekieli, aihe).
4. Paina [Anna tämä työ].
   VS Code -pääte avautuu, ja valitsemasi tekoäly vastaanottaa ohjeen ja aloittaa työn.

> **Vihje**
>
> Claude Code -istunnon mukana kulkevat työkalut (MCP-palvelin `lunascape-docs`). Istunto voi itse hakea kääntämättä olevien ja päivitettävien luettelon, suorittaa docs-lint-tarkistuksen ja kirjata käännöksen tuoreuden.

## Tuloksen tarkistaminen

| Palveluntarjoajan tyyppi | Mihin tulos päätyy |
|---|---|
| Istuntotyyppinen (Claude Code, Codex) | Kirjoittaa suoraan työpuuhun. **Tarkista tulos Gitin erotuksesta** |
| API-tyyppinen (VS Coden kielimallit, Anthropic, OpenAI-yhteensopivat) | Palauttaa ehdotuksen dokumentti kerrallaan. Tarkista se painikkeella [Avaa erotus] ja kirjoita painikkeella [Tallenna] |

### API-tyyppisen ehdotuksen tarkistaminen

Kun työ suoritetaan API-tyyppisellä palveluntarjoajalla, ehdotus saapuu [AI]-välilehdelle.

1. Paina [Avaa erotus] ja vertaa ehdotusta nykyiseen sisältöön.
2. Jos ehdotus kelpaa, paina [Tallenna]. Käännöksen yhteydessä myös tuoreus kirjataan. Jos haluat luopua ehdotuksesta, paina [Hylkää].
   Voit keskeyttää luonnin kesken painamalla [Keskeytä].

> **Huomautus**
>
> - Lunascape Docs ei koskaan lisää muutoksia Gitin hakemistoon eikä tee kommitteja. Tarkista muutokset aina erotuksesta.
> - Työtä ei voi antaa työtilassa, johon ei luoteta, eikä silloin, kun selaat dokumenttijuuren ulkopuolista väliaikaista kansiota.

## Aiheeseen liittyvää

- [Annettavat työt](tasks.md)
- [AI-asetukset](settings.md)
- [Luettelo ja kirjaukset](ledger.md)
