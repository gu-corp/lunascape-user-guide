# Angi navigasjonsinformasjon

Navnet og rekkefølgen som vises i INDEX, skrives i YAML front matter i hvert dokument. Dokumenter vises også uten dette, og da brukes overskriften (H1) og rekkefølgen etter filnavn.

## Dokumentets navn og rekkefølge

Skriv følgende øverst i dokumentet.

```yaml
---
navigation:
  title: Kom i gang
  order: 200
---
```

| Felt | Innhold |
|---|---|
| `navigation.title` | Navnet som vises i INDEX. Utelates det, brukes H1, og ellers filnavnet |
| `navigation.order` | Et heltall som bestemmer rekkefølgen. Sorteres stigende. Utelates det, brukes en stabil standardrekkefølge (etter filnavn) |

> **Tips**
>
> - Angi `order` i trinn på 100, som 100, 200, 300, slik at du senere kan skyte inn 150 mellom dem.
> - Manglende, ugyldig eller duplisert `order` skjuler aldri et dokument.
> - Når du endrer rekkefølge i INDEX, skrives `navigation.order` inn automatisk. Du trenger ikke skrive det for hånd.

## Mappens navn og rekkefølge

Navnet og rekkefølgen til en mappe ligger i front matter i mappens `README.md` (eller `index.md` hvis README mangler). Forsiden trenger ikke ha brødtekst.

```yaml
---
navigation:
  title: Produktplanlegging
  order: 100
---
```

En mappe uten forside vises med mappenavnet og standardrekkefølgen. Når en tittelendring eller en omorganisering i INDEX krever det, opprettes en `README.md` som bare inneholder front matter. Bare det å lese oppretter aldri en fil.

## Behandling i oversettelser

- Rekkefølgen og mappens rolle (forside eller kun konfigurasjon) bestemmes utelukkende av dokumentet på standardspråket.
- En oversettelse kan bare overstyre `navigation.title`. Når originaldokumentet har brødtekst, brukes også oversettelsens H1 som navn.
- En oversettelse alene gir aldri flere sider.

## Sortering og sammenslåing av underelementer

På en mappes forside er `navigation.children.sort` og `navigation.children.defaultCollapsed` definert for å angi hvordan de direkte underelementene sorteres og om de starter sammenslått. Lesing og redigering i VS Code er planlagt.

## Relaterte emner

- [Endre rekkefølgen på dokumenter](../03-editing/reorder.md)
- [Dokumentrot og filkonvensjoner](structure.md)
