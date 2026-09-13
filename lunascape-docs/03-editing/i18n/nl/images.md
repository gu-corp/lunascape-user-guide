# Afbeeldingsgrootte aanpassen

Afbeeldingen in een document passen zich automatisch aan de breedte van de tekst en de hoogte van het scherm aan. Voor een afbeelding die op een bepaalde grootte getoond moet worden, kunt u de breedte instellen.

## Hoe de automatische aanpassing werkt

- Een gewone Markdown-afbeelding (`![beschrijving](./images/screen.png)`) wordt verkleind zodat ze binnen de tekstbreedte past. Ze wordt nooit groter gemaakt dan het origineel.
- Een hoge schermafbeelding wordt beperkt tot 72% van de schermhoogte of tot 720px, afhankelijk van wat het kleinst is.

## De breedte instellen in het bewerkingsscherm

1. Druk op [Bewerken] en selecteer de afbeelding in de visuele weergave.
2. Kies een breedte bij [Afbeeldingsbreedte] op de werkbalk.
3. Druk op [Opslaan].

| Optie | Breedte |
|---|---|
| [Automatisch] | Niet opgegeven (automatische aanpassing) |
| [Klein (360px)] | 360px |
| [Middel (560px)] | 560px |
| [Groot (760px)] | 760px |
| [Tekstbreedte (920px)] | 920px |
| [Aangepast…] | Een willekeurig geheel getal van 16 tot 4096px |

## De breedte instellen in Markdown

Geef de HTML-tag `img` een numerieke `width`. Deze schrijfwijze wordt ook op GitHub en in MDX op dezelfde manier weergegeven.

```html
<img src="./images/screen.png" alt="Instellingenscherm" width="360" />
```

> **Let op**
>
> - Geef bij `width` alleen een getal op, zonder `px` of `%`. Ook bij een waarde die groter is dan de tekstbreedte blijft de weergave binnen de tekstbreedte.
> - Afbeeldingspaden zijn relatief ten opzichte van het document. Afbeeldingen buiten de documentatiehoofdmap worden niet getoond.

## Verwante onderwerpen

- [Een document bewerken](README.md)
- [Diagrammen, formules of afbeeldingen worden niet weergegeven](../07-troubleshooting/rendering.md)
