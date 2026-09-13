# Dokumentin muokkaaminen

Dokumentteja voi muokata suoraan katseluohjelmassa. Muokkausnäkymässä on visuaalinen näkymä, jossa muokkaat sitä mitä näet, sekä Markdown-lähdenäkymä; yksi painike vaihtaa näkymästä toiseen.

## Muokkauksen aloittaminen

Paina jotakin seuraavista. Kaikki avaavat saman muokkausnäkymän.

- Dokumentin oikeassa alakulmassa [Muokkaa]
- Dokumentin oikeassa yläkulmassa [⋯] (muut toiminnot) → [Muokkaa]
- INDEX-kohdan valikko → [Muokkaa]

## Muokkaaminen

1. Muokkaa tekstiä suoraan.
   Muokkausnäkymän yläreunan työkalurivillä ovat kappalemuotoilu (leipäteksti, otsikot 1–4, lainaus, koodi), [Lihavointi], [Kursivointi], [Luettelomerkitty luettelo], [Numeroitu luettelo], [Linkki], [Lisää taulukko], [Kuvan leveys], [Kumoa] ja [Tee uudelleen].
2. Kun haluat muokata Markdown-lähdettä suoraan, paina [Markdown].
   Painamalla uudelleen palaat visuaaliseen näkymään. Viimeksi käytetty näkymä muistetaan ja palautetaan, kun seuraavan kerran painat [Muokkaa].
3. Paina [Tallenna].
   Muutokset kirjoitetaan Markdown-tiedostoon ja näkymä palaa lukutilaan. Jos haluat keskeyttää, paina [Peruuta].

> **Huomautus**
>
> - Tallennus vain kirjoittaa tiedoston. Git-vaiheistusta tai committia ei tehdä automaattisesti.
> - Matematiikka ja kaaviot, kuten Mermaid, TikZ ja Vega-Lite, näkyvät visuaalisessa näkymässä piirrettyinä. Vaihda [Markdown]-näkymään, kun haluat muuttaa niiden sisältöä.
> - Dokumentteja, joissa on MDX:n omaa syntaksia (komponentteja, `import` ja vastaavia), muokataan vain Markdown-näkymässä, jotta syntaksi säilyy.
> - Front matter (alussa `---`-rivien väliin rajattu asetuslohko) säilyy, vaikka muokkaat visuaalisessa näkymässä.

> **Vihje**
>
> - Painikkeella [Avaa VS Codessa] tiedoston voi avata tavallisessa tekstieditorissa. Kun tallennat tekstieditorissa, katseluohjelman näkymä päivittyy automaattisesti.
> - Kun et halua näyttää [Muokkaa]-painiketta, poista käytöstä [Muokkauspainike] kohdassa [Näyttöasetukset]. Jos haluat piilottaa sen koko projektista, aseta `lunascape-docs.json`-tiedostossa `editor.showEditButton` arvoon `false`.
> - Aluksi avautuvan näkymän (visuaalinen tai Markdown) oletuksen voi vaihtaa asetuksella `lunascapeDocEditor.editor.defaultMode` tai `lunascape-docs.json`-tiedoston asetuksella `editor.defaultMode`.

## Aiheeseen liittyvää

- [Dokumenttien ja kansioiden luominen ja järjestäminen](organize.md)
- [Kuvien koon säätäminen](images.md)
- [Matematiikan kirjoittaminen](math.md)
- [Kaavioiden ja graafien piirtäminen](diagrams.md)
