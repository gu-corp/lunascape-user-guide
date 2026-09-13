# Een GitHub-repository openen

In de webversie opent u documenten door een GitHub-repository op te geven. Voor openbare repository's is aanmelden niet nodig.

## Openen vanaf het scherm

1. Open <https://docs.lunascape.org/>.
2. Druk op [Documenten openen] (het mappictogram) in de werkbalk.
3. Voer de repository in bij [Repository rechtstreeks opgeven] en druk op [Openen].
   Wanneer u bij GitHub bent aangemeld, kunt u ook kiezen uit een lijst bij [Kiezen uit leesbare repository's].

> **Tip**
>
> - Het GitHub-pictogram ernaast opent het document dat u nu leest op github.com. Daarmee opent u dus geen documenten.

## Openen via een URL

Het adres zet de repository en de plaats van het document achter elkaar. Het pad is de plaats binnen de repository en heeft daarom dezelfde volgorde als de GitHub-URL.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Wat u opgeeft | Schrijfwijze |
|---|---|
| Alleen de repository (standaardbranch) | `/github/owner/repo` |
| Een document in de repository | `/github/owner/repo/docs/01-product/vision.md` |
| Een branch of tag opgeven | voeg `?ref=v1.2.0` toe aan het einde |

Als u naar een andere pagina gaat, verandert ook het adres. Druk op [Dit document delen] in de werkbalk om een koppeling naar de pagina die u nu leest door te geven. De knoppen [Terug] en [Vooruit] van de browser werken ook.

De oudere vorm met `?source=` opent nog altijd. Na het openen wordt die omgezet naar de nieuwe vorm.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Let op**
>
> - Als u niet bent aangemeld, geldt de gebruikslimiet van de GitHub API (60 aanvragen per uur). Meld u aan met [Aanmelden met GitHub] bij repository's met veel documenten of wanneer u herhaaldelijk leest.
> - Branchnamen met een `/` (zoals `feature/xxx`) kunt u opgeven met `?ref=` in de bovenstaande adresvorm. In de vorm met `?source=` kan dat niet.
> - Documenten worden geladen met de GitHub-rechten van de lezer. Wie geen leesrecht heeft, ziet ze niet.

## Documenten uit een lokale map openen

Druk op [Documenten openen] in de werkbalk en kies vervolgens onder aan de lijst [Documenten uit een lokale map openen] een map op uw apparaat. De bestanden worden binnen de browser verwerkt en worden nergens naartoe gestuurd. Dit werkt in browsers die mapselectie ondersteunen (Chrome, Edge en andere).

## Verwante onderwerpen

- [Een niet-openbare repository lezen](private-repository.md)
- [De webversie kan niet openen of aanmelden lukt niet](../07-troubleshooting/web.md)
