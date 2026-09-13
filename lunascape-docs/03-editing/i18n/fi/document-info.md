# Dokumentin tietojen näyttäminen

Dokumentin alkuun sijoitettu ”dokumentin hallintataulukko” (taulukko, jossa on dokumentin tunnus, versio, päivityspäivä, tila ja niin edelleen) näytetään lukutilassa pienenä ”dokumentin tiedot” -rivinä. Markdown itsessään pysyy tavallisena taulukkona, joten se on luettavissa sellaisenaan myös GitHubissa.

## Näyttämisen edellytykset

Sijoita otsikon (H1) välittömästi jälkeen seuraavanlainen kaksisarakkeinen taulukko.

```markdown
# Toiminnallinen määrittely

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Edellytyksenä on, että taulukossa on dokumentin tunnuksen rivi ja useita hallintakenttiä.
- Myös otsikon `## 文書管理` tai `## Document information` alla oleva taulukko tunnistetaan.
- Tekstin keskellä olevia taulukoita tai tavallisia ”kenttä/arvo”-taulukoita ei muunneta.

## Miten tiedot näytetään

- Lukutilassa näytetään pienellä vain tila ja päivityspäivä.
- Kun painat riviä, kaikki kentät tulevat näkyviin.
- Tulostettaessa näytetään kaikki kentät.
- Muokkausnäkymässä taulukko näkyy tavallisena taulukkona, ja sitä voi muokata sellaisenaan.

> **Vinkki**
>
> Jos haluat näyttää taulukon aina tiivistämättä sitä, poista käytöstä [Näyttöasetukset]-kohdan asetus [Tiivistä dokumentin tiedot].

## Aiheeseen liittyvää

- [Dokumentin muokkaaminen](README.md)
- [Näyttöasetusten muuttaminen](../02-reading/display-settings.md)
