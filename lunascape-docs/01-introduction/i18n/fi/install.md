# Laajennuksen asentaminen

VS Code -laajennus "Lunascape Docs Pro" jaetaan VSIX-tiedostona. Se on maksuton; "Pro" tarkoittaa versiota, joka antaa työn tekoälölle ja päivittää itsensä.

## Käyttöympäristö

- VS Code 1.90 tai uudempi
- Kirjoittamista edellyttävät toiminnot — dokumenttien luominen, INDEX-panelin järjestäminen, tarkistusasetusten tallentaminen, kääntäminen — toimivat vain työtilassa, jonka olet merkinnyt VS Codessa luotetuksi.

## Asentaminen

1. Hanki VSIX-tiedosto. Tämä linkki osoittaa aina uusimpaan versioon.

   [Lataa lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Avaa laajennusnäkymä (`⇧⌘X` / `Ctrl+Shift+X`).
3. Valitse oikean yläkulman `…`-valikosta [Asenna VSIX-tiedostosta...] ja osoita lataamasi tiedosto.

### Komennolla asentaminen

Voit hoitaa asian yhdellä rivillä poistumatta päätteestä. Lataus ja asennus tapahtuvat peräkkäin.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Huomautus**
> Jos `code` ei löydy, suorita komentopaletista (`⇧⌘P` / `Ctrl+Shift+P`) komento [Shell-komento: Asenna 'code'-komento PATHiin].

## Päivittäminen

Kun uudempi versio julkaistaan, laajennus hakee ja asentaa sen itse. VS Code kehottaa lataamaan ikkunan uudelleen, ja siinä vaiheessa uusi versio otetaan käyttöön. Asetuksesi ja dokumenttisi säilyvät ennallaan.

Tarkistus tehdään kerran päivässä. Jos haluat tarkistaa heti, suorita komentopaletista (`⇧⌘P` / `Ctrl+Shift+P`) komento [Lunascape Docs: Tarkista päivitykset].

Toimintaa voi muuttaa asetuksella `lunascapeDocEditor.update.check`.

| Asetus | Toiminta |
|---|---|
| Asenna uudempi versio, kun sellainen julkaistaan | Oletus |
| Ilmoita, ja anna minun päättää joka kerta | Näkyviin tulee ilmoitus, ja vaihto tapahtuu vasta kun painat [Päivitä] |
| Älä tarkista | Ei tee mitään |

### Kun päivitys ei onnistu

Jos näkyviin tulee "Päivitystä ei voitu hakea: No Servers", asennettu versio on 0.22.18 tai vanhempi. Sen version päivitystoiminto epäonnistuu haun jälkeisessä viimeisessä vaiheessa aina, joten se ei voi päivittää itseään uudempaan. Asenna se tällöin kerran käsin yllä olevien ohjeiden mukaan. Sen jälkeen se päivittyy itse.

## Version tarkistaminen

Kun avaat "Lunascape Docs Pro" -laajennuksen laajennusnäkymässä, näet asennetun version. Tarvitset sen, kun ilmoitat viasta.

## Katso myös

- [Ensimmäisten dokumenttien luominen](first-documents.md)
- [Vian ilmoittaminen](../07-troubleshooting/report.md)
