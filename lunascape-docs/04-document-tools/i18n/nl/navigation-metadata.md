# Navigatiegegevens instellen

De naam en de volgorde die in de INDEX worden getoond, schrijft u in de YAML front matter van elk document. Ook zonder deze gegevens worden documenten getoond, met de kop (H1) en de volgorde van de bestandsnamen.

## Naam en volgorde van een document

Schrijf het volgende boven aan het document.

```yaml
---
navigation:
  title: Aan de slag
  order: 200
---
```

| Veld | Betekenis |
|---|---|
| `navigation.title` | De naam die in de INDEX wordt getoond. Wordt deze weggelaten, dan wordt de H1 gebruikt, en anders de bestandsnaam |
| `navigation.order` | Een geheel getal dat de volgorde bepaalt, oplopend. Wordt het weggelaten, dan geldt een vaste standaardvolgorde (op bestandsnaam) |

> **Tip**
>
> - Geef `order` waarden in stappen van 100, bijvoorbeeld 100, 200, 300, zodat u er later 150 tussen kunt schuiven.
> - Ontbrekende, ongeldige of dubbele `order`-waarden verbergen een document nooit.
> - Wanneer u de volgorde in de INDEX wijzigt, wordt `navigation.order` automatisch geschreven. U hoeft het niet met de hand te schrijven.

## Naam en volgorde van een map

De naam en de volgorde van een map staan in de front matter van de `README.md` van die map (of van `index.md` als er geen README is). De voorpagina hoeft geen tekst te bevatten.

```yaml
---
navigation:
  title: Productplanning
  order: 100
---
```

Een map zonder voorpagina wordt getoond met de mapnaam en de standaardvolgorde. Wanneer een titelwijziging of een wijziging van de volgorde in de INDEX dat vereist, wordt een `README.md` met alleen front matter aangemaakt. Alleen lezen maakt nooit een bestand aan.

## Vertalingen

- De volgorde en de rol van een map (voorpagina of alleen instellingen) worden uitsluitend door het document in de standaardtaal bepaald.
- Een vertaling kan alleen `navigation.title` overschrijven. Wanneer het brondocument tekst bevat, wordt de H1 van de vertaling ook als naam gebruikt.
- Een vertaling op zichzelf voegt nooit een pagina toe.

## Volgorde en inklappen van onderliggende items

`navigation.children.sort` en `navigation.children.defaultCollapsed` op de voorpagina van een map zijn gedefinieerd om te bepalen hoe de rechtstreeks onderliggende items worden gesorteerd en of ze ingeklapt beginnen. Het lezen en bewerken ervan in VS Code volgt later.

## Verwante onderwerpen

- [De volgorde van documenten wijzigen](../03-editing/reorder.md)
- [Documentatiehoofdmappen en bestandsconventies](structure.md)
