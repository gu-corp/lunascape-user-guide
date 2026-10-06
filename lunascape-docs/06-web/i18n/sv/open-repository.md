# Öppna en lagringsplats på GitHub

I webbversionen kan du öppna och läsa en lagringsplats på GitHub direkt, utan att klona den. Publika lagringsplatser kräver ingen inloggning.

## Öppna från skärmen

1. Tryck på [Öppna dokument] (mappikonen) i verktygsfältet. Skärmen ”Öppna dokument” öppnas.
2. Välj en plats att öppna från i den vänstra kolumnen.

   | Plats | Det som visas |
   |---|---|
   | Alla | Allt nedan. Det du har öppnat senast visas först |
   | Senast öppnade | Lagringsplatser och mappar som du har öppnat tidigare |
   | Rekommenderade | Handböcker som webbplatsen tipsar om |
   | Lagringsplatser på GitHub | Lagringsplatser som du kan läsa, när du är inloggad med GitHub |
   | Den här datorn | Mappar på den här enheten |

3. Tryck på [Öppna] på raden som du vill öppna. Skriv i [Filtrera på dokument- eller lagringsplatsnamn] högst upp om du vill begränsa antalet rader.

En lagringsplats som inte finns i listan anger du via [Ange owner/repo och öppna] i den vänstra kolumnen.

> **Tips**
>
> - De lagringsplatser på GitHub som visas i listan är de där GitHub-appen ”Lunascape Docs” är installerad och som du har läsbehörighet till. Om du inte hittar en lagringsplats ber du dess ägare att lägga till appen.

## Se var dokumentet finns

Den lilla ikonen till vänster i verktygsfältet (platsetiketten) visar var dokumentet som du läser just nu finns.

| Ikon | Plats |
|---|---|
| GitHub-märket | Dokumentet läses från GitHub. Det är inte sparat på den här enheten |
| Mapp | En mapp på den här enheten |

Tryck på ikonen så visas platsen, dess status och vad du kan göra därifrån (till exempel [Visa på GitHub] och [Kopiera länk]).

## Öppna via URL

Adressen består av lagringsplatsen och dokumentets plats, i den ordningen. Sökvägen anger platsen i lagringsplatsen, så den följer samma ordning som GitHub-URL:en.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Vad som anges | Skrivsätt |
|---|---|
| Endast lagringsplatsen (standardgren) | `/github/owner/repo` |
| Ett dokument i lagringsplatsen | `/github/owner/repo/docs/01-product/vision.md` |
| En gren eller tagg | Lägg till `?ref=v1.2.0` sist |

Adressen ändras när du går till en annan sida. Tryck på [Dela det här dokumentet] i verktygsfältet för att dela en länk till sidan som du läser. Webbläsarens [Tillbaka] och [Framåt] fungerar också.

Det äldre formatet `?source=` går fortfarande att öppna som tidigare. När sidan har öppnats skrivs adressen om till det nya formatet.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Observera**
>
> - Utan inloggning gäller användningsgränsen för GitHub API (60 anrop per timme). För lagringsplatser med många dokument eller vid upprepad läsning bör du välja [Logga in med GitHub].
> - Grennamn som innehåller `/` (till exempel `feature/xxx`) kan anges med `?ref=` i adressformatet ovan. De kan inte skrivas i formatet `?source=`.
> - Dokumenten läses in med läsarens egna GitHub-behörigheter. De visas inte för personer som saknar läsbehörighet.

## Öppna dokument från en lokal mapp

Tryck på [Öppna dokument] i verktygsfältet och välj en mapp på enheten via [Öppna dokument från en lokal mapp] i den vänstra kolumnen. Filerna behandlas i webbläsaren och skickas aldrig vidare. Funktionen kan användas i webbläsare som har stöd för val av mapp (Chrome, Edge med flera).

## Relaterade avsnitt

- [Läsa en privat lagringsplats](private-repository.md)
- [Det går inte att öppna eller logga in i webbversionen](../07-troubleshooting/web.md)
