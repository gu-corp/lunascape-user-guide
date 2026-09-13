# Öppna en lagringsplats på GitHub

I webbversionen öppnar du dokument genom att ange en lagringsplats på GitHub. För öppna lagringsplatser behövs ingen inloggning.

## Öppna från skärmen

1. Öppna <https://docs.lunascape.org/>.
2. Tryck på [Öppna dokument] (mappikonen) i verktygsfältet.
3. Ange lagringsplatsen under [Ange en lagringsplats] och tryck på [Öppna].
   När du är inloggad på GitHub kan du också välja i listan under [Välj bland läsbara lagringsplatser].

> **Tips**
>
> - GitHub-ikonen bredvid öppnar det dokument du läser på github.com. Den öppnar inte dokument här.

## Öppna med en URL

Adressen anger lagringsplatsen och dokumentets plats i följd. Sökvägen är platsen inuti lagringsplatsen, så ordningen är densamma som i GitHub-adressen.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Vad du anger | Skrivsätt |
|---|---|
| Endast lagringsplatsen (standardgrenen) | `/github/owner/repo` |
| Ett dokument inuti lagringsplatsen | `/github/owner/repo/docs/01-product/vision.md` |
| En gren eller tagg | lägg till `?ref=v1.2.0` sist |

Adressen ändras när du går mellan sidor. Tryck på [Dela det här dokumentet] i verktygsfältet för att ge någon en länk till den sida du läser. Webbläsarens [Tillbaka] och [Framåt] fungerar också.

Den tidigare formen med `?source=` går fortfarande att öppna. När den har öppnats skrivs den om till den nya formen.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Obs!**
>
> - Utan inloggning gäller GitHub API:s användningsgräns (60 anrop per timme). Vid lagringsplatser med många dokument eller upprepad läsning, använd [Logga in med GitHub].
> - Grennamn som innehåller `/` (till exempel `feature/xxx`) kan anges med `?ref=` i adressformen ovan. Formen med `?source=` kan inte uttrycka dem.
> - Dokument läses in med läsarens egen behörighet på GitHub. Den som saknar läsbehörighet ser dem inte.

## Öppna dokument i en lokal mapp

Tryck på [Öppna dokument] i verktygsfältet och välj sedan [Öppna dokument från en lokal mapp] under listan, och välj en mapp på enheten. Filerna behandlas inuti webbläsaren och skickas inte någonstans. Detta fungerar i webbläsare som stöder mappval (Chrome, Edge med flera).

## Relaterade avsnitt

- [Läsa en privat lagringsplats](private-repository.md)
- [Webbversionen går inte att öppna eller logga in i](../07-troubleshooting/web.md)
