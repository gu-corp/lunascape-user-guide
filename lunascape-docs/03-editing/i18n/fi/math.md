# Matematiikan kirjoittaminen

Matematiikka kirjoitetaan TeX-merkinnällä ja piirretään laitteessa KaTeX:lla. Verkkoa ei käytetä.

## Merkintätapa

| Laji | Erotinmerkit | Esimerkki |
|---|---|---|
| Rivinsisäinen matematiikka (lauseen sisällä) | `$...$` tai `\(...\)` | `Massan ja energian suhde on $E = mc^2$.` |
| Erillinen matematiikka (omalla rivillään) | `$$...$$` tai `\[...\]` | Katso alla |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Erotinmerkkien ympärille ei tarvita välilyöntejä. Matematiikka tunnistetaan myös silloin, kun se on kiinni japaninkielisessä tekstissä, esimerkiksi `値は$V=-H$である`.
- Rivinsisäisen koodin tai koodilohkon sisällä oleva `$` ei ole matematiikkaa, vaan se näytetään sellaisenaan.
- Rahasummalta näyttävää tekstiä, kuten `$5 and $10`, ei tulkita matematiikaksi.

## Muokkaaminen

Visuaalisessa näkymässä matematiikka näkyy piirrettynä. Kun haluat muuttaa sisältöä, paina muokkausnäkymässä [Markdown] ja muokkaa lähdettä. Kun tallennat visuaalisesta näkymästä, TeX-lähde ja alkuperäinen erotinmerkkien muoto (`$` vai `\(`) säilyvät ennallaan.

> **Huomautus**
>
> - Turvallisuuden vuoksi KaTeX toimii asetuksella `trust: false`, ja koolle (`maxSize: 50`) sekä makrojen laajennusten määrälle (`maxExpand: 1000`) on ylärajat. Nämä rajat ylittävää matematiikkaa ei piirretä.
> - Jos olemassa olevassa dokumentissa on kirjoitettu `tikzpicture` merkintöjen `$$...$$` tai `\[...\]` sisään, se tunnistetaan TikZ-kuvaksi eikä matematiikaksi.

## Aiheeseen liittyvää

- [Kaavioiden ja graafien kirjoittaminen](diagrams.md)
- [Kaaviot, matematiikka tai kuvat eivät näy](../07-troubleshooting/rendering.md)
