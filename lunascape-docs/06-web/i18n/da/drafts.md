# Gem en kladde

Når du redigerer et dokument i webudgaven, skrives ændringerne ikke til lageret, men gemmes som en "kladde" inde i browseren.

## Opret en kladde

1. Åbn et dokument, og tryk på [Rediger] nederst til højre.
2. Rediger, og tryk på [Gem].
   "Gemt som kladde" vises, og ændringen gemmes inde i browseren.

- Dokumenter med en kladde får et mærke i INDEX. Over teksten vises "Dette dokument er en kladde på enheden (ikke udgivet)".
- [Kladder] på værktøjslinjen viser antallet, og når du trykker på den, åbnes listen over kladder.

## Kassér en kladde

- For at kassere kladden for ét dokument skal du trykke på [Kassér kladden] over teksten.
- For at kassere alle skal du bruge listen over kladder.

## Anvend på lageret

Anmodning om udgivelse, der sender kladder som en Pull Request, er implementeret, men den er ikke aktiveret i den offentlige fremviser. For at anvende ændringerne på lageret skal du redigere i VS Code-udgaven eller i en lokal klon.

> **Bemærk**
>
> - Kladder gemmes i browseren (IndexedDB). De overføres ikke til en anden browser eller en anden enhed. Hvis du sletter browserens webstedsdata, slettes kladderne også.
> - Hvis dokumentet på lageret opdateres, efter du har oprettet en kladde, vises "Kilden er blevet opdateret". Kontrollér indholdet, og afgør derefter, om du vil kassere kladden eller bruge den som den er.
> - Hvis du åbner en lokal mappe via [Åbn dokumenter] og redigerer den, gemmes ændringerne direkte i filen, hvis browseren understøtter det. I browsere, der ikke understøtter det, bevares de kun i den pågældende session.

## Relaterede emner

- [Hvad du kan i webudgaven](README.md)
- [Rediger et dokument](../03-editing/README.md)
