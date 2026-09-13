# Luonnosten tallentaminen

Kun muokkaat dokumenttia Web-versiossa, muutoksia ei kirjoiteta säilöön, vaan ne tallennetaan selaimeen luonnoksena.

## Luonnoksen luominen

1. Avaa dokumentti ja paina oikeassa alakulmassa [Muokkaa].
2. Muokkaa dokumenttia ja paina [Tallenna].
   Näyttöön tulee ”Tallennettu luonnoksena”, ja muutos tallentuu selaimeen.

- Dokumentit, joilla on luonnos, saavat merkin INDEX-luettelossa. Tekstin yläpuolella lukee ”Tämä dokumentti on laitteessa oleva luonnos (julkaisematon)”.
- Työkalurivin [Luonnokset] näyttää luonnosten määrän, ja sitä painamalla avautuu luonnosten luettelo.

## Luonnoksen hylkääminen

- Yhden dokumentin luonnos hylätään painamalla tekstin yläpuolella [Hylkää luonnos].
- Kaikki luonnokset hylätään luonnosten luettelosta.

## Muutosten vieminen säilöön

Julkaisupyyntö, joka lähettää luonnokset pull requestina, on toteutettu, mutta se ei ole käytössä julkisessa katselimessa. Jos haluat viedä muutokset säilöön, muokkaa dokumenttia VS Code -versiossa tai paikallisessa kloonissa.

> **Huomautus**
>
> - Luonnokset tallennetaan selaimeen (IndexedDB). Ne eivät siirry toiseen selaimeen eivätkä toiseen laitteeseen. Jos poistat selaimen sivustotiedot, myös luonnokset poistuvat.
> - Jos säilössä oleva dokumentti päivittyy luonnoksen tekemisen jälkeen, näyttöön tulee ”Ylävirta on päivittynyt”. Tarkista sisältö ja päätä sitten, hylkäätkö luonnoksen vai käytätkö sitä sellaisenaan.
> - Jos avaat paikallisen kansion toiminnolla [Avaa dokumentteja] ja muokkaat sitä, muutokset tallentuvat suoraan tiedostoon, mikäli selain tukee sitä. Selaimissa, jotka eivät tue tätä, muutokset säilyvät vain istunnon ajan.

## Liittyvät aiheet

- [Mitä Web-versiossa voi tehdä](README.md)
- [Dokumentin muokkaaminen](../03-editing/README.md)
