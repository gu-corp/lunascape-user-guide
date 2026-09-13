# Läsa en privat lagringsplats

Dokument i privata lagringsplatser kan du läsa när du loggar in med GitHub, begränsat till de lagringsplatser du har läsbehörighet till. Lunascape Docs har aldrig egna konton eller behörigheter.

## Logga in och öppna

1. Öppna <https://docs.lunascape.org/>.
   Om du anger ett privat dokument eller ännu inte har loggat in visas inloggningsskärmen.
2. Tryck på [Logga in med GitHub].
   GitHubs autentiseringsskärm öppnas i ett popup-fönster.
3. När inloggningen är klar trycker du på [Öppna dokument] i verktygsfältet och väljer den lagringsplats du vill öppna under [Välj bland läsbara lagringsplatser].

> **Tips**
>
> - Namnet på det inloggade kontot visas i verktygsfältet. Härifrån kan du också [Logga ut] eller [Logga in med ett annat konto].
> - I listan visas de lagringsplatser du har läsbehörighet till, bland lagringsplatserna för de konton (organisationer eller personliga) där GitHub-appen ”Lunascape Docs” är installerad.

## Inställningar som lagringsplatsens ägare gör

Om den önskade lagringsplatsen inte visas i listan måste lagringsplatsens ägare eller organisationens administratör installera GitHub-appen ”Lunascape Docs”.

- De behörigheter som begärs är Contents (läs och skriv) och Pull requests (läs och skriv). Läsbehörigheten är för att visa, skrivbehörigheten är för publiceringsbegäran från webben (Pull Request). Lunascape Docs sparar aldrig dokumentens innehåll.
- Appen installeras per konto (organisation eller personligt). Du väljer om den ska omfatta ”All repositories” (som automatiskt även inkluderar lagringsplatser som skapas senare) eller endast utvalda lagringsplatser.

| Situation | Steg |
|---|---|
| Införa på en ny organisation eller ett personligt konto | Utför det från [installationssidan](https://github.com/apps/lunascape-docs/installations/new) |
| Lägga till lagringsplatser i en organisation där den redan är införd | Ställ in under organisationens Settings → GitHub Apps → Lunascape Docs → Configure → Repository access |

Även om appen installeras för hela organisationen kan varje medlem endast läsa de lagringsplatser hen själv har läsbehörighet till. Publiceringsbegäran kan endast skickas till de lagringsplatser hen själv har skrivbehörighet till.

> **Tips**
> - Vid en ny installation visas de behörigheter som begärs i en lista på installationsskärmen, och de godkänns i och med att du trycker på ”Install”. Ingen ytterligare åtgärd behövs.
> - En organisation som var installerad redan innan en behörighet lades till får ett bekräftelsemail till sina administratörer, och en godkännandeknapp visas överst under organisationens Settings → GitHub Apps → Lunascape Docs → Configure. Tills den godkänns kan den organisationen endast läsa, och en publiceringsbegäran svarar då ”skrivbehörighet måste beviljas”.
> - Vilka behörigheter appen körs med just nu kan du kontrollera på samma Configure-skärm. För ett personligt konto är det Settings → Applications → Installed GitHub Apps.
> - Om du av misstag tog bort en lagringsplats eller avinstallerade appen kan du återställa det genom att installera om från [installationssidan](https://github.com/apps/lunascape-docs/installations/new). Meddelandet om en avvisad publiceringsbegäran innehåller en länk till skärmen där det åtgärdas.
> - Om en lagringsplats inte vill ta emot publiceringsbegäranden skriver du `"publish": { "enabled": false }` i `lunascape-docs.json`. Läsningen fungerar som vanligt.

## Relaterade ämnen

- [Öppna en GitHub-lagringsplats](open-repository.md)
- [Går inte att öppna eller logga in i webbversionen](../07-troubleshooting/web.md)
