# Angiv navigationsoplysninger

Navnet og rækkefølgen, der vises i INDEX, skrives i hvert dokuments YAML front matter. Dokumenter vises også uden den, hvor overskriften (H1) og filnavnsrækkefølgen bruges.

## Dokumentets navn og rækkefølge

Skriv følgende øverst i dokumentet.

```yaml
---
navigation:
  title: Kom godt i gang
  order: 200
---
```

| Felt | Betydning |
|---|---|
| `navigation.title` | Navnet, der vises i INDEX. Når det udelades, bruges H1, ellers filnavnet |
| `navigation.order` | Et heltal, der bestemmer rækkefølgen, i stigende orden. Når det udelades, gælder en stabil standardrækkefølge (efter filnavn) |

> **Tip**
>
> - Angiv `order`-værdier i spring på 100, f.eks. 100, 200, 300, så du senere kan indsætte 150 imellem dem.
> - Manglende, ugyldige eller dublerede `order`-værdier skjuler aldrig et dokument.
> - Når du ændrer rækkefølgen i INDEX, skrives `navigation.order` for dig; du behøver ikke skrive den i hånden.

## Mappens navn og rækkefølge

En mappes navn og rækkefølge hører til i front matter i dens `README.md` (eller `index.md`, når der ikke findes en README). Forsiden behøver ikke at have brødtekst.

```yaml
---
navigation:
  title: Produktplanlægning
  order: 100
---
```

En mappe uden forside bruger sit mappenavn og standardrækkefølgen. Når en titeländring eller en ændret rækkefølge i INDEX kræver det, oprettes en `README.md`, der kun indeholder front matter. Blot at læse opretter aldrig en fil.

## Håndtering i oversættelser

- Rækkefølgen og mappens rolle (forside eller kun konfiguration) bestemmes alene af dokumentet på standardsproget.
- En oversættelse kan kun tilsidesætte `navigation.title`. Når originaldokumentet har brødtekst, bruges oversættelsens H1 også som navn.
- En oversættelse alene tilføjer aldrig en side.

## Sortering og sammenfoldning af underelementer

`navigation.children.sort` og `navigation.children.defaultCollapsed` i en mappes forside er defineret til at styre, hvordan dens direkte underelementer sorteres, og om de starter sammenfoldede. Læsning og redigering af dem i VS Code er planlagt.

## Relaterede emner

- [Ændr dokumenternes rækkefølge](../03-editing/reorder.md)
- [Dokumentrødder og filkonventioner](structure.md)
