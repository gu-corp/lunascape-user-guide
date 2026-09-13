# Lese et privat repositorium

Når du logger inn med GitHub, kan du lese dokumentene i private repositorier, begrenset til dem du har lesetilgang til. Lunascape Docs har aldri egne kontoer eller tillatelser.

## Logg inn og åpne

1. Åpne <https://docs.lunascape.org/>.
   Når du oppgir et privat dokument eller ennå ikke er logget inn, vises påloggingsskjermen.
2. Trykk på [Logg inn med GitHub].
   GitHubs autentiseringsskjerm åpnes i et sprettoppvindu.
3. Når du er logget inn, trykker du på [Åpne dokumenter] på verktøylinjen og velger repositoriet du vil åpne under [Velg blant repositorier du kan lese].

> **Tips**
>
> - Navnet på den påloggede kontoen vises på verktøylinjen. Du kan også [Logg ut] eller [Logg inn med en annen konto] herfra.
> - Listen viser repositoriene til de kontoene (organisasjoner eller enkeltpersoner) der GitHub-appen «Lunascape Docs» er installert, begrenset til dem du har lesetilgang til.

## Innstillinger som repositoriets eier gjør

Hvis det aktuelle repositoriet ikke vises i listen, må repositoriets eier eller organisasjonens administrator installere GitHub-appen «Lunascape Docs».

- Tillatelsene som kreves, er Contents (les og skriv) og Pull requests (les og skriv). Lesetilgang er for visning, skrivetilgang er for publiseringsforespørsler fra nettet (Pull Request). Lunascape Docs lagrer aldri innholdet i dokumentene.
- Installasjonsenheten er en konto (organisasjon eller enkeltperson). Du velger om målet skal være «All repositories» (som også automatisk omfatter repositorier som opprettes senere) eller bare utvalgte repositorier.

| Situasjon | Fremgangsmåte |
|---|---|
| Ta i bruk i en ny organisasjon eller personlig konto | Gjennomfør fra [installasjonssiden](https://github.com/apps/lunascape-docs/installations/new) |
| Legge til repositorier i en organisasjon som allerede har appen | Still inn under organisasjonens Settings → GitHub Apps → Lunascape Docs → Configure → Repository access |

Selv om appen installeres for hele organisasjonen, kan hvert medlem bare lese repositorier de selv har lesetilgang til. De kan bare sende publiseringsforespørsler til repositorier de selv har skrivetilgang til.

> **Tips**
> - Ved en ny installasjon vises tillatelsene som kreves i en liste på installasjonsskjermen, og når du trykker på «Install», har du godkjent dem. Ingen ytterligere handling er nødvendig.
> - En organisasjon som hadde installert appen før en tillatelse ble lagt til, får en bekreftelses-e-post til administratorene, og det vises en godkjenningsknapp øverst under organisasjonens Settings → GitHub Apps → Lunascape Docs → Configure. Inntil den er godkjent, kan organisasjonen bare lese, og hvis du sender en publiseringsforespørsel, vises meldingen «skrivetilgang må gis».
> - Hvilke tillatelser appen kjører med nå, kan du se på den samme Configure-skjermen. For en personlig konto er det Settings → Applications → Installed GitHub Apps.
> - Hvis du ved et uhell har fjernet det aktuelle repositoriet eller avinstallert appen, kan du gjenopprette den ved å installere på nytt fra [installasjonssiden](https://github.com/apps/lunascape-docs/installations/new). Avvisningsmeldingen for en publiseringsforespørsel har en lenke til skjermen der du retter det.
> - Hvis repositoriet ikke skal ta imot publiseringsforespørsler, skriver du `"publish": { "enabled": false }` i `lunascape-docs.json`. Lesing fungerer som før.

## Relaterte emner

- [Åpne et GitHub-repositorium](open-repository.md)
- [Kan ikke åpne eller logge inn i Web-versjonen](../07-troubleshooting/web.md)
