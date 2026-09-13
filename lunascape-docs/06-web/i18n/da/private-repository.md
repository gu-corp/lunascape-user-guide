# Læs et privat lager

Dokumenter i private lagre kan du læse, når du logger ind med GitHub, men kun de lagre, du har læseadgang til. Lunascape Docs har aldrig sine egne konti eller rettigheder.

## Log ind og åbn

1. Åbn <https://docs.lunascape.org/>.
   Hvis du har angivet et privat dokument, eller endnu ikke er logget ind, vises login-skærmen.
2. Tryk på [Log ind med GitHub].
   GitHubs godkendelsesskærm åbnes i et pop op-vindue.
3. Når du er logget ind, skal du trykke på [Åbn dokumenter] på værktøjslinjen og under [Vælg blandt lagre, du kan læse] vælge det lager, du vil åbne.

> **Tip**
>
> - Navnet på den konto, du er logget ind med, vises på værktøjslinjen. Herfra kan du også [Log ud] eller [Log ind med en anden konto].
> - Listen viser lagre fra de konti (organisationer eller enkeltpersoner), hvor GitHub App'en "Lunascape Docs" er installeret, begrænset til dem, du har læseadgang til.

## Indstillinger, som lagerets ejer foretager

Hvis det ønskede lager ikke vises på listen, skal lagerets ejer eller organisationens administrator installere GitHub App'en "Lunascape Docs".

- De rettigheder, der anmodes om, er Contents (læs og skriv) og Pull requests (læs og skriv). Læsning er til visning; skrivning er til anmodninger om udgivelse (Pull Request) fra web. Lunascape Docs gemmer aldrig dokumenternes indhold.
- Installationen sker pr. konto (organisation eller enkeltperson). Du vælger, om målet skal være "All repositories" (som også automatisk omfatter lagre, der oprettes senere), eller kun udvalgte lagre.

| Situation | Fremgangsmåde |
|---|---|
| Indfør på en ny organisations- eller personkonto | Gør det fra [installationssiden](https://github.com/apps/lunascape-docs/installations/new) |
| Tilføj lagre i en organisation, hvor det allerede er indført | Indstil under organisationens Settings → GitHub Apps → Lunascape Docs → Configure → Repository access |

Selv når App'en installeres for hele organisationen, kan hvert medlem kun læse de lagre, vedkommende selv har læseadgang til. Og du kan kun sende en anmodning om udgivelse til de lagre, du selv har skriveadgang til.

> **Tip**
> - Ved en ny installation vises de anmodede rettigheder i en liste på installationsskærmen, og når du trykker på "Install", har du godkendt dem. Der kræves ingen yderligere handling.
> - En organisation, der havde installeret App'en, før en rettighed blev tilføjet, får en bekræftelsesmail til sine administratorer, og en godkendelsesknap vises øverst under organisationens Settings → GitHub Apps → Lunascape Docs → Configure. Indtil den er godkendt, kan man i den organisation kun læse, og hvis man sender en anmodning om udgivelse, vises "Der kræves tildeling af skriveadgang".
> - Hvilke rettigheder du er inde med lige nu, kan du se på den samme Configure-skærm. For en personkonto er det Settings → Applications → Installed GitHub Apps.
> - Hvis du ved en fejl har fjernet det ønskede lager eller afinstalleret App'en, kan du sætte det tilbage ved at installere igen fra [installationssiden](https://github.com/apps/lunascape-docs/installations/new). Afvisningsbeskeden for en anmodning om udgivelse indeholder et link til den skærm, hvor det rettes.
> - Hvis lageret ikke skal modtage anmodninger om udgivelse, skriver du `"publish": { "enabled": false }` i `lunascape-docs.json`. Læsning fungerer uændret.

## Relaterede emner

- [Åbn et GitHub-lager](open-repository.md)
- [Web-versionen kan ikke åbnes, eller du kan ikke logge ind](../07-troubleshooting/web.md)
