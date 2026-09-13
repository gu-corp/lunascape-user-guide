# Kan ikke åbne eller logge ind i webversionen

## Logget ind, men lageret vises ikke på listen

GitHub App'en „Lunascape Docs" er ikke installeret på den konto, eller lageret er ikke inkluderet. Bed lagerets ejer eller en organisationsadministrator om at installere den efter fremgangsmåden i [Se et privat lager](../06-web/private-repository.md).

## Kan ikke komme videre fra login-skærmen

- Du har ikke læseadgang til lageret. Bed lagerets ejer om at give dig adgang.
- „GitHub-login er ikke konfigureret for dette websted": en fremviser, du selv har hostet, har ingen login-tjeneste konfigureret. En administrator skal opsætte en.

## Pop op-vinduet til login åbner ikke

Browseren blokerede pop op-vinduet. Tillad pop op-vinduer for dette websted, og prøv igen.

## „Dit login er udløbet" vises

Dit login er udløbet. Tryk på [Log ind med GitHub] igen.

## Et offentligt lager returnerer 404

- Kontrollér formen `owner/repo@ref/dir`.
- Grennavne, der indeholder `/`, kan ikke angives.

## Indlæsningen holder op med at virke efter et stykke tid

Når du ikke er logget ind, gælder GitHub API'ens forbrugsgrænse (60 gange i timen). Når „Grænsen for antallet af forespørgsler er nået" vises, skal du vente et stykke tid eller logge ind med [Log ind med GitHub].

## „Dette websted kan ikke vise dette lager" vises

For at åbne et lager fra en fremviser, du selv har hostet, skal webstedets URL tilføjes til `viewer.origins` i lagerets `lunascape-docs.json`.

## Der vises intet, når `index.html` åbnes

Det virker ikke, når den åbnes direkte via `file://`. Åbn den via en HTTP-server, eller brug VS Code-versionen.

## Et eksporteret websted viser „lunascape-docs-manifest.json blev ikke fundet"

Placér hele filsættet, der blev genereret af `npm run export:web` (inklusive manifestet), som det er.

## Kladder kan ikke gemmes

- „Kan ikke åbne IndexedDB" / „I brug af en anden fane": skyldes browserens private tilstand eller en anden fane, der viser det samme websted. Brug et normalt vindue, og luk de andre faner.
- Kladder gemmes pr. enhed og browser. De overføres ikke til en anden enhed.

## Relaterede emner

- [Åbne et GitHub-lager](../06-web/open-repository.md)
- [Gemme kladder](../06-web/drafts.md)
