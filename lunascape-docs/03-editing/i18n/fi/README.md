# Dokumentin muokkaaminen

Dokumentteja voi muokata suoraan katseluohjelmassa. Muokkausnäkymässä on visuaalinen näkymä, jossa muokkaat sitä mitä näet, sekä Markdown-lähdenäkymä; yksi painike vaihtaa niiden välillä.

## Muokkauksen aloittaminen

Paina jotakin seuraavista. Ne kaikki avaavat saman muokkausnäkymän.

- [Muokkaa] tekstin oikeassa alakulmassa
- [⋯] (Lisää toimintoja) tekstin oikeassa yläkulmassa → [Muokkaa]
- INDEX-kohdan valikko → [Muokkaa]

## Muokkaaminen

1. Muokkaa tekstiä suoraan.
   Muokkausnäkymän yläreunan työkalurivillä ovat käytettävissä kappaleen muotoilu (leipäteksti, otsikot 1–4, lainaus, koodi), [Lihavointi], [Kursivointi], [Luettelomerkitty luettelo], [Numeroitu luettelo], [Linkki], [Lisää taulukko], [Kuvan leveys], [Kumoa] ja [Tee uudelleen].
2. Kun haluat muokata Markdown-lähdettä suoraan, paina [Markdown].
   Paina uudelleen palataksesi visuaaliseen näkymään. Viimeksi käyttämäsi näkymä muistetaan ja palautetaan, kun seuraavan kerran painat [Muokkaa].
3. Paina [Tallenna] (myös Ctrl+S / ⌘S tallentaa).
   Markdown-tiedostoon kirjoitetaan ja näkymä palaa lukutilaan. Kun haluat lopettaa muokkauksen ja palata viimeksi tallennettuun sisältöön, paina [Hylkää muokkaukset].

## Aloita aina muokkausnäkymästä (muokkaustila)

Kun painat työkalurivin [Muokkaustila] päälle, jokainen dokumentti avautuu muokkausnäkymään. Käytä tätä, kun kirjoitat jatkuvasti niin kuin muistilehtiöön.

- Kun se on päällä, [Tallenna] ei sulje muokkausnäkymää. [Hylkää muokkaukset] palauttaa viimeksi tallennettuun sisältöön ja pitää muokkausnäkymän auki.
- Paina uudelleen kytkeäksesi sen pois päältä ja palataksesi lukutilaan. Päällä/pois-valinta muistetaan käyttäjäkohtaisesti.
- Sitä ei näytetä dokumenttijuuressa, johon ei voi kirjoittaa (kuten vain luku -oikeuksinen GitHub-lähde).

## Tallentamattomat muokkaukset

Muokkaukset, joita et ole tallentanut, säilytetään tällä laitteella automaattisesti. Ne eivät katoa, vaikka siirryt toiseen dokumenttiin tai suljet välilehden tai ikkunan.

- Muokkausnäkymän [Tallentamaton] tarkoittaa, että teksti eroaa viimeksi tallennetusta sisällöstä.
- Kun seuraavan kerran avaat saman dokumentin, työ jatkuu säilytetyistä muokkauksista ja siitä ilmoitetaan. Jos alkuperäinen dokumentti on sen jälkeen päivittynyt, myös siitä ilmoitetaan. [Hylkää muokkaukset] palauttaa uusimpaan sisältöön.
- Säilytetyt muokkaukset poistuvat painikkeella [Tallenna] tai [Hylkää muokkaukset]. Koska mitään ei ole tallennettu, ne eivät näy Gitissä eivätkä luonnoksissa.

> **Huomautus**
>
> - Tallentaminen vain kirjoittaa tiedoston. Gitin lavausta ja committia ei tehdä koskaan automaattisesti.
> - Matematiikka ja kaaviot, kuten Mermaid, TikZ ja Vega-Lite, näytetään visuaalisessa näkymässä valmiiksi piirrettyinä. Vaihda [Markdown]-näkymään muuttaaksesi niiden sisältöä.
> - Dokumentit, jotka sisältävät MDX-kohtaista syntaksia (komponentteja, `import` ynnä muuta), muokataan vain Markdown-näkymässä, jotta syntaksi säilyy.
> - Front matter (alussa `---`-riveillä rajattu asetuslohko) säilyy, vaikka muokkaat visuaalisessa näkymässä.

> **Vinkki**
>
> - [VS Codeで開く] (Avaa VS Codessa) avaa tiedoston tavallisessa tekstieditorissa. Kun tallennat siellä, katseluohjelman näkymä päivittyy automaattisesti.
> - Kun et halua näyttää [Muokkaa]-painiketta, kytke [Muokkauspainike] pois päältä kohdassa [Näyttöasetukset]. Piilottaaksesi sen koko projektista aseta `editor.showEditButton` arvoon `false` tiedostossa `lunascape-docs.json`.
> - Ensimmäisenä avautuvan näkymän (visuaalinen / Markdown) oletusarvon voi muuttaa asetuksella `lunascapeDocEditor.editor.defaultMode` tai `editor.defaultMode` tiedostossa `lunascape-docs.json`.

## Katso myös

- [Dokumenttien ja kansioiden luominen ja järjestäminen](organize.md)
- [Kuvien koon säätäminen](images.md)
- [Matematiikan kirjoittaminen](math.md)
- [Kaavioiden ja graafien piirtäminen](diagrams.md)
