# Gebruik vanuit AI

De extensie registreert het alleen-lezen Language Model Tool `lunascape_getDocsSpecification` bij VS Code. Wanneer een compatibele agent van VS Code een vraag krijgt over functies, instellingen of documentconventies van Lunascape Docs, kan die met dit hulpmiddel de inhoud van deze Help (de algemene specificatie) ophalen.

## Gebruik

Stel uw vraag in de chat van VS Code met `#lunascapeDocs` erbij, of stel een vraag over de instellingen of de documentstructuur van Lunascape Docs.

```text
#lunascapeDocs Hoe schakel ik de Engelse vertaling in in lunascape-docs.json?
```

## Argumenten van het hulpmiddel

| Argument | Inhoud |
|---|---|
| `topic` | Het hoofdstuk dat wordt opgehaald: `all`, `usage` (basishandelingen), `structure` (documentatiehoofdmap en bestandsconventies), `editing` (een document bewerken), `configuration` (projectinstellingen), `security` (beveiliging en schrijfgrenzen), `ai` (gebruik vanuit AI) |
| `locale` | De taal van de Help (`ja`, `en` en andere taaltags van de meegeleverde Help). Laat u dit weg, dan wordt de weergavetaal van VS Code gebruikt, en anders de Japanse Help |

> **Opmerking**
>
> - Het hulpmiddel verzendt de inhoud van documenten niet naar buiten.
> - Het hulpmiddel geeft geen werkruimtenamen of lokale paden terug.
> - Het hulpmiddel wijzigt geen bestanden.
> - Ook zonder `AGENTS.md` is het bruikbaar vanuit compatibele agents van VS Code. Met andere AI-clients die de hulpmiddel-API van de extensie niet gebruiken, wordt het niet automatisch gedeeld.

## Verwante onderwerpen

- [Help weergeven](../02-reading/help.md)
- [Beveiliging en schrijfgrenzen](security.md)
