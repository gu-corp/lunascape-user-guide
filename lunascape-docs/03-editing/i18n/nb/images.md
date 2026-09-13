# Justere størrelsen på bilder

Bilder som er satt inn i et dokument, tilpasses automatisk tekstbredden og skjermhøyden. For et bilde du vil vise i en bestemt størrelse, kan du angi bredden.

## Slik fungerer automatisk tilpasning

- Et vanlig Markdown-bilde (`![beskrivelse](./images/screen.png)`) krympes slik at det får plass i tekstbredden. Det forstørres aldri utover sin opprinnelige størrelse.
- Et høyt skjermbilde begrenses til 72 % av skjermhøyden eller 720px, det som er minst.

## Angi bredden i redigeringsvisningen

1. Trykk [Rediger] og velg bildet i den visuelle visningen.
2. Velg en bredde under [Bildestørrelse] på verktøylinjen.
3. Trykk [Lagre].

| Alternativ | Bredde |
|---|---|
| [Automatisk] | Ikke angitt (automatisk tilpasning) |
| [Liten (360px)] | 360px |
| [Middels (560px)] | 560px |
| [Stor (760px)] | 760px |
| [Tekstbredde (920px)] | 920px |
| [Egendefinert …] | Et vilkårlig heltall fra 16 til 4096px |

## Angi bredden i Markdown

Gi HTML-taggen `img` en numerisk `width`. Denne skrivemåten vises også som et bilde på GitHub og i MDX.

```html
<img src="./images/screen.png" alt="Innstillingsskjerm" width="360" />
```

> **Merk**
>
> - `width` tar bare et tall, uten `px` eller `%`. En verdi som er større enn tekstbredden, tilpasses likevel tekstbredden ved visning.
> - Bildebaner angis relativt til dokumentet. Bilder som ligger utenfor dokumentroten, vises ikke.

## Se også

- [Redigere et dokument](README.md)
- [Diagrammer, matematikk eller bilder vises ikke](../07-troubleshooting/rendering.md)
