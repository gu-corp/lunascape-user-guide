# Justera bildstorlek

Bilder som du infogar i ett dokument anpassas automatiskt efter brödtextens bredd och skärmens höjd. För en bild som ska visas i en viss storlek kan du ange bredden.

## Så fungerar den automatiska anpassningen

- En vanlig Markdown-bild (`![beskrivning](./images/screen.png)`) förminskas så att den ryms inom brödtextens bredd. Den förstoras aldrig utöver sin ursprungliga storlek.
- En hög skärmbild begränsas till 72 % av skärmens höjd eller 720px, det som är minst.

## Ange bredden i redigeringsvyn

1. Tryck på [Redigera] och markera bilden i den visuella vyn.
2. Välj en bredd under [Bildstorlek] i verktygsfältet.
3. Tryck på [Spara].

| Alternativ | Bredd |
|---|---|
| [Automatisk] | Ingen angiven (automatisk anpassning) |
| [Liten (360px)] | 360px |
| [Mellan (560px)] | 560px |
| [Stor (760px)] | 760px |
| [Brödtextbredd (920px)] | 920px |
| [Anpassad …] | Valfritt heltal mellan 16 och 4096px |

## Ange bredden i Markdown

Ange ett numeriskt `width` i HTML-taggen `img`. Den här skrivningen visas på samma sätt på GitHub och i MDX.

```html
<img src="./images/screen.png" alt="Inställningsskärm" width="360" />
```

> **Obs!**
>
> - `width` tar bara ett tal. Lägg inte till `px` eller `%`. Även om du anger ett värde som är större än brödtextens bredd ryms visningen inom brödtextens bredd.
> - Bilder anges med en sökväg relativ till dokumentet. Bilder utanför dokumentroten visas inte.

## Relaterade avsnitt

- [Redigera ett dokument](README.md)
- [Diagram, matematik eller bilder visas inte](../07-troubleshooting/rendering.md)
