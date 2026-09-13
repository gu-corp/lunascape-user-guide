# Dokumenttien järjestyksen muuttaminen

INDEX-paneelissa näkyvää järjestystä voi muuttaa vetämällä ja pudottamalla tai näppäimistöllä. Muutettu järjestys tallennetaan dokumentin front matter -osaan arvona `navigation.order`.

## Järjestäminen vetämällä ja pudottamalla

1. Vedä dokumenttia tai kansiota INDEX-paneelissa.
2. Pudota se samalla tasolla olevan kohteen eteen tai taakse tai kansion päälle.
   Saman tason sisällä järjestys muuttuu. Kun pudotat kohteen toiseen kansioon, se siirtyy kyseiseen kansioon.

## Järjestäminen näppäimistöllä tai valikosta

- Kohdista INDEX-paneelin kohteeseen ja paina `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Valitse kohteen valikosta [Siirrä ylemmäs] / [Siirrä alemmas].

## Mitä tallennetaan

- Kun järjestät kohteita saman tason sisällä, alkuperäisdokumentin front matter -osan `navigation.order` päivittyy. Kansion kohdalla arvo kirjoitetaan kansion tiedostoon `README.md`. Jos kansiossa ei ole `README.md`-tiedostoa, luodaan `README.md`, joka sisältää pelkän front matterin.
- Kun siirrät kohteen toiseen kansioon, alkuperäisdokumentti ja sitä vastaavat käännökset siirtyvät yhdessä. Ennen siirtoa näytetään vahvistus, koska siirto voi vaikuttaa suhteellisiin linkkeihin.
- Gitin vaiheistusta tai committeja ei tehdä.

> **Huomautus**
>
> - Järjestystä ei voi muuttaa suodatuksen aikana, dokumenttia muokattaessa eikä työtilassa, johon ei luoteta.
> - Ilmoitus ”INDEX on päivitetty” tarkoittaa, että jokin toinen muutos on juuri tullut voimaan. Tee toiminto uudelleen.
> - Aloitussivua ei voi siirtää toiseen kansioon.

> **Vihje**
>
> Kun annat `navigation.order`-arvot sadan välein, esimerkiksi 100, 200, 300, dokumentteja on myöhemmin helppo lisätä väliin. Lisätietoja on kohdassa [Navigointitietojen määrittäminen](../04-document-tools/navigation-metadata.md).

## Aiheeseen liittyvää

- [Dokumenttien ja kansioiden luominen ja järjestäminen](organize.md)
- [Navigointitietojen määrittäminen](../04-document-tools/navigation-metadata.md)
