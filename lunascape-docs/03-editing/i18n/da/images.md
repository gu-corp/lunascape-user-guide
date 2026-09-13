# Justere billedstørrelsen

Billeder, du indsætter i et dokument, tilpasses automatisk til brødtekstens bredde og skærmens højde. For et billede, der skal vises i en bestemt størrelse, kan du angive bredden.

## Sådan fungerer den automatiske tilpasning

- Et almindeligt Markdown-billede (`![beskrivelse](./images/screen.png)`) forminskes, så det passer til brødtekstens bredde. Det forstørres aldrig ud over den oprindelige størrelse.
- Et højt skærmbillede begrænses til 72 % af skærmens højde eller 720px, alt efter hvad der er mindst.

## Angive bredden i redigeringsvisningen

1. Tryk på [Rediger], og vælg billedet i den visuelle visning.
2. Vælg en bredde under [Billedstørrelse] på værktøjslinjen.
3. Tryk på [Gem].

| Valgmulighed | Bredde |
|---|---|
| [Automatisk] | Ikke angivet (automatisk tilpasning) |
| [Lille (360px)] | 360px |
| [Mellem (560px)] | 560px |
| [Stor (760px)] | 760px |
| [Brødtekstbredde (920px)] | 920px |
| [Tilpasset …] | Et vilkårligt heltal fra 16 til 4096px |

## Angive bredden i Markdown

Giv HTML-tagget `img` en numerisk `width`. Denne skrivemåde vises på samme måde på GitHub og i MDX.

```html
<img src="./images/screen.png" alt="Indstillingsskærm" width="360" />
```

> **Bemærk**
>
> - `width` angives kun med et tal. Tilføj ikke `px` eller `%`. Selv hvis du angiver en værdi, der er større end brødtekstens bredde, vises billedet inden for brødtekstens bredde.
> - Billeder angives med en relativ sti fra dokumentet. Billeder uden for dokumentroden vises ikke.

## Relaterede emner

- [Redigere et dokument](README.md)
- [Diagrammer, matematik eller billeder vises ikke](../07-troubleshooting/rendering.md)
