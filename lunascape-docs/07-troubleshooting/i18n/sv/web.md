# Det går inte att öppna eller logga in i webbversionen

## Jag loggar in men lagringsplatsen visas inte i listan

GitHub App:en ”Lunascape Docs” är inte installerad på det kontot, eller så ingår inte lagringsplatsen. Be lagringsplatsens ägare eller organisationens administratör att installera den enligt stegen i [Läsa en privat lagringsplats](../06-web/private-repository.md).

## Det går inte att komma vidare från inloggningsskärmen

- Du har inte läsbehörighet till lagringsplatsen. Be lagringsplatsens ägare att ge dig behörighet.
- ”GitHub-inloggning är inte konfigurerad för den här webbplatsen”: ett visningsprogram som du själv har placerat saknar inloggningstjänst. En administratör måste konfigurera en inloggningstjänst.

## Popupfönstret för inloggning öppnas inte

Webbläsaren blockerar popupfönster. Tillåt popupfönster för den här webbplatsen och försök igen.

## ”Din inloggning har upphört att gälla” visas

Inloggningen har upphört att gälla. Tryck på [Logga in med GitHub] igen.

## En offentlig lagringsplats ger 404

- Kontrollera skrivsättet `owner/repo@ref/dir`.
- Grennamn som innehåller `/` kan inte anges.

## Inläsningen slutar fungera efter en stund

När du inte är inloggad gäller GitHub API:s användningsgräns (60 anrop per timme). Om ”Gränsen för antal anrop har nåtts” visas väntar du en stund eller loggar in med [Logga in med GitHub].

## ”Den här webbplatsen kan inte visa den här lagringsplatsen” visas

För att öppna lagringsplatsen från ett visningsprogram som du själv har placerat måste webbplatsens URL läggas till i `viewer.origins` i lagringsplatsens `lunascape-docs.json`.

## Ingenting visas när `index.html` öppnas

Det fungerar inte om filen öppnas direkt via `file://`. Öppna den via en HTTP-server eller använd VS Code-versionen.

## Den exporterade webbplatsen visar ”lunascape-docs-manifest.json hittades inte”

Placera hela filuppsättningen som `npm run export:web` skapar, inklusive manifestet, som den är.

## Utkast kan inte sparas

- ”Det går inte att öppna IndexedDB” eller ”Används i en annan flik”: orsaken är webbläsarens privata läge eller en annan flik som visar samma webbplats. Öppna i ett vanligt fönster och stäng de andra flikarna.
- Utkast sparas per enhet och webbläsare. De följer inte med till en annan enhet.

## Relaterade avsnitt

- [Öppna en GitHub-lagringsplats](../06-web/open-repository.md)
- [Spara utkast](../06-web/drafts.md)
