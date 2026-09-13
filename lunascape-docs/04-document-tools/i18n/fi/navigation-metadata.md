# Navigointitietojen määrittäminen

INDEX-luettelossa näkyvä nimi ja järjestys kirjoitetaan kunkin dokumentin YAML front matter -osaan. Dokumentit näkyvät ilmankin, jolloin käytetään otsikkoa (H1) ja tiedostonimen mukaista järjestystä.

## Dokumentin nimi ja järjestys

Kirjoita dokumentin alkuun seuraavasti.

```yaml
---
navigation:
  title: Aloitus
  order: 200
---
```

| Kenttä | Merkitys |
|---|---|
| `navigation.title` | INDEX-luettelossa näkyvä nimi. Jos jätetään pois, käytetään H1-otsikkoa ja sen puuttuessa tiedostonimeä |
| `navigation.order` | Kokonaisluku, joka määrää järjestyksen nousevasti. Jos jätetään pois, käytetään vakaata oletusjärjestystä (tiedostonimen mukaan) |

> **Vihje**
>
> - Anna `order`-arvot sadan välein, esimerkiksi 100, 200, 300, niin voit myöhemmin lisätä väliin arvon 150.
> - Puuttuvat, virheelliset tai samat `order`-arvot eivät koskaan piilota dokumenttia.
> - Kun järjestät kohteita uudelleen INDEX-luettelossa, `navigation.order` kirjoitetaan puolestasi. Sitä ei tarvitse kirjoittaa käsin.

## Kansion nimi ja järjestys

Kansion nimi ja järjestys ovat sen `README.md`-tiedoston front matter -osassa (tai `index.md`-tiedoston, jos README puuttuu). Aloitussivulla ei tarvitse olla leipätekstiä.

```yaml
---
navigation:
  title: Tuotesuunnittelu
  order: 100
---
```

Kansio, jolla ei ole aloitussivua, näkyy kansion nimellä ja oletusjärjestyksessä. Jos nimen muuttaminen tai uudelleenjärjestäminen INDEX-luettelossa sitä vaatii, luodaan `README.md`, jossa on pelkkä front matter. Pelkkä lukeminen ei koskaan luo tiedostoa.

## Käännökset

- Järjestyksen ja kansion roolin (aloitussivu vai pelkkä asetustiedosto) määrää yksin oletuskielinen dokumentti.
- Käännös voi korvata vain kentän `navigation.title`. Kun alkuperäisdokumentissa on leipätekstiä, myös käännöksen H1-otsikkoa käytetään nimenä.
- Pelkkä käännös ei koskaan lisää sivua.

## Alikohteiden järjestys ja tiivistäminen

Kansion aloitussivun kentät `navigation.children.sort` ja `navigation.children.defaultCollapsed` on määritelty ohjaamaan, miten sen suorat alikohteet järjestetään ja ovatko ne aluksi tiivistettyinä. Niiden lukeminen ja muokkaaminen VS Codessa on suunnitteilla.

## Liittyvät aiheet

- [Dokumenttien järjestyksen muuttaminen](../03-editing/reorder.md)
- [Dokumenttijuuret ja tiedostokäytännöt](structure.md)
