# VS Code -asetukset

Kun haet VS Coden asetuksista (`⌘,` / `Ctrl+,`) sanaa "Lunascape Docs", voit muuttaa seuraavia kohtia. Kaikki ovat käyttäjäkohtaisia asetuksia, eikä niitä tallenneta projektin dokumentteihin.

## Dokumenttijuuri

| Asetus | Arvot | Oletus | Toiminta |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` valitsee automaattisesti avattua Markdown-tiedostoa lähimpänä olevan dokumenttijuuren ja avaa tilapäisesti yläkansion, jos tiedosto ei kuulu mihinkään juureen. `fixed` avaa aina asetuksen `root` mukaisen dokumenttijuuren |
| `lunascapeDocEditor.rootDirectoryNames` | Merkkijonotaulukko | `["docs"]` | Kansionimet, jotka löydetään dokumenttijuuriksi `auto`-tilassa. Kansio, jossa on `lunascape-docs.json`, löydetään nimestä riippumatta. Jos säilön juuressa olevassa `lunascape-docs.json`-tiedostossa on `defaultFolder` tai `roots`, ne ovat etusijalla |
| `lunascapeDocEditor.root` | Polku | `docs` | Työtilaan nähden suhteellinen dokumenttijuuri `fixed`-tilassa ja komennolla avattaessa |
| `lunascapeDocEditor.startPage` | Polku | `README.md` | Aloitussivu dokumenttijuureen nähden suhteellisena |
| `lunascapeDocEditor.title` | Merkkijono | `Lunascape Docs` | Korvaa dokumenttivälilehden otsikon. Ei vaikuta dokumenttijuuren valintanimeen |
| `lunascapeDocEditor.ignoredDirectories` | Merkkijonotaulukko | `["99-archive"]` | Kansionimet, jotka jätetään pois INDEX-paneelista |

## Näyttö

| Asetus | Arvot | Oletus | Toiminta |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` käyttää valkoista taustaa, `auto` seuraa VS Coden väriteemaa |
| `lunascapeDocEditor.locale` | Kielitunnus | Ei mitään | Henkilökohtainen dokumentin kieli, jota käytetään ensisijaisesti silloin kun se on saatavilla. Ei muuta projektin alkuperäiskieltä |
| `lunascapeDocEditor.documentMetadata.compact` | Totuusarvo | `true` | Tiivistää H1-otsikon jälkeisen dokumentin hallintataulukon "Dokumentin tiedot" -riviksi |
| `lunascapeDocEditor.tree.showFileNames` | Totuusarvo | `false` | Näyttää INDEX-paneelissa tiedostonimet dokumenttien nimien sijaan |
| `lunascapeDocEditor.tree.showDocumentIcons` | Totuusarvo | `false` | Näyttää dokumenttikuvakkeet INDEX-paneelissa |
| `lunascapeDocEditor.tree.showFolderIcons` | Totuusarvo | `false` | Näyttää kansiokuvakkeet INDEX-paneelissa |
| `lunascapeDocEditor.tree.showItemCounts` | Totuusarvo | `false` | Näyttää INDEX-paneelissa kunkin kansion suorien kohteiden määrän |
| `lunascapeDocEditor.tree.showGuides` | Totuusarvo | `true` | Näyttää INDEX-paneelissa tasojen apuviivat |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX-paneelin riviväli |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Totuusarvo | `true` | Sulkee INDEX-paneelin ensimmäisellä kerralla, kun dokumentteja on vain yksi |

## Muokkaus

| Asetus | Arvot | Oletus | Toiminta |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Muokkausnäkymä ennen kuin vaihdat sitä. Viimeksi käytetty näkymä on etusijalla |
| `lunascapeDocEditor.editor.showEditButton` | Totuusarvo | `true` | Näyttää [Muokkaa]-painikkeen tekstin oikeassa alakulmassa |

## Kaaviot

| Asetus | Arvot | Oletus | Toiminta |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ-kaavioiden piirtoajoympäristö. `bundled` käyttää mukana toimitettavaa hyväksyttyä ajoympäristöä (ei sisälly nykyiseen jakeluversioon), `workspace` käyttää luotetun työtilan juuressa olevaa `node-tikzjax` 1.0.5 -pakettia (vain kehitykseen ja arviointiin), `disabled` ei piirrä mitään |

## Vanhentuneet asetukset

| Asetus | Käytä tämän sijaan |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json`-tiedoston `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json`-tiedoston `locales` |

Projektin kieliä ei voi ohittaa henkilökohtaisilla asetuksilla.

## Aiheeseen liittyvää

- [Näyttöasetusten muuttaminen](../02-reading/display-settings.md)
- [Projektin asetukset](../04-document-tools/project-configuration.md)
