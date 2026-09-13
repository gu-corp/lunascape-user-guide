# Kuvien koon säätäminen

Dokumenttiin lisätyt kuvat sovitetaan automaattisesti leipätekstin leveyteen ja näytön korkeuteen. Kuvalle, joka halutaan näyttää tietyn kokoisena, voi määrittää leveyden.

## Automaattisen sovituksen toiminta

- Tavallinen Markdown-kuva (`![kuvaus](./images/screen.png)`) pienennetään mahtumaan leipätekstin leveyteen. Sitä ei koskaan suurenneta alkuperäistä kokoa suuremmaksi.
- Korkea kuvakaappaus mahtuu enintään 72 %:iin näytön korkeudesta tai 720 pikseliin sen mukaan, kumpi on pienempi.

## Leveyden määrittäminen muokkausnäkymässä

1. Paina [Muokkaa] ja valitse kuva visuaalisessa näkymässä.
2. Valitse leveys työkalurivin kohdasta [Kuvan leveys].
3. Paina [Tallenna].

| Vaihtoehto | Leveys |
|---|---|
| [Automaattinen] | Ei määritetty (automaattinen sovitus) |
| [Pieni (360 px)] | 360 px |
| [Keskikokoinen (560 px)] | 560 px |
| [Suuri (760 px)] | 760 px |
| [Leipätekstin leveys (920 px)] | 920 px |
| [Mukautettu…] | Mikä tahansa kokonaisluku väliltä 16–4096 px |

## Leveyden määrittäminen Markdownissa

Anna HTML:n `img`-tunnisteelle numeerinen `width`. Tämä kirjoitustapa näkyy samalla tavalla myös GitHubissa ja MDX:ssä.

```html
<img src="./images/screen.png" alt="Asetusnäkymä" width="360" />
```

> **Huomautus**
>
> - `width`-määritteeseen annetaan vain luku. Älä lisää `px`- tai `%`-merkintää. Vaikka arvo olisi leipätekstin leveyttä suurempi, kuva näytetään leipätekstin levyisenä.
> - Kuvat määritetään dokumenttiin nähden suhteellisella polulla. Dokumenttijuuren ulkopuolella olevia kuvia ei näytetä.

## Aiheeseen liittyvää

- [Dokumentin muokkaaminen](README.md)
- [Kaaviot, matematiikka tai kuvat eivät näy](../07-troubleshooting/rendering.md)
