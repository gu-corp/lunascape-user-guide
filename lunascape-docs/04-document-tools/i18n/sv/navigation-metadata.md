# Ange navigeringsinformation

Namnet och ordningen som visas i INDEX skrivs i varje dokuments YAML front matter. Dokument visas även utan detta, då används rubriken (H1) och ordningen efter filnamn.

## Dokumentets namn och ordning

Skriv följande överst i dokumentet.

```yaml
---
navigation:
  title: Komma igång
  order: 200
---
```

| Fält | Innebörd |
|---|---|
| `navigation.title` | Namnet som visas i INDEX. Om det utelämnas används H1, annars filnamnet |
| `navigation.order` | Ett heltal som bestämmer ordningen, i stigande följd. Om det utelämnas gäller en stabil standardordning (efter filnamn) |

> **Tips**
>
> - Ange `order` i steg om 100, till exempel 100, 200, 300, så att du senare kan skjuta in 150 däremellan.
> - Saknade, ogiltiga eller upprepade `order`-värden döljer aldrig ett dokument.
> - När du ändrar ordningen i INDEX skrivs `navigation.order` automatiskt. Du behöver inte skriva det för hand.

## Mappens namn och ordning

En mapps namn och ordning hör hemma i front matter i mappens `README.md` (eller `index.md` om README saknas). Startsidan behöver inget brödtext.

```yaml
---
navigation:
  title: Produktplanering
  order: 100
---
```

En mapp utan startsida visas med mappnamnet och standardordningen. Om en titeländring eller en omordning i INDEX kräver det skapas en `README.md` som bara innehåller front matter. Enbart läsning skapar aldrig någon fil.

## Hantering i översättningar

- Ordningen och mappens roll (startsida eller enbart inställningar) bestäms av dokumentet på standardspråket ensamt.
- En översättning kan endast åsidosätta `navigation.title`. När originaldokumentet har brödtext används även översättningens H1 som namn.
- En översättning på egen hand ger aldrig fler sidor.

## Ordning och hopfällning av underposter

`navigation.children.sort` och `navigation.children.defaultCollapsed` i en mapps startsida är definierade för att styra hur de direkta underposterna sorteras och om de börjar hopfällda. Läsning och redigering i VS Code planeras.

## Relaterade avsnitt

- [Ändra dokumentens ordning](../03-editing/reorder.md)
- [Dokumentrötter och filkonventioner](structure.md)
