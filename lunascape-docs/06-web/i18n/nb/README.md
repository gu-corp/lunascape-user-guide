# Hva Web-visningen kan

Web-visningen av Lunascape Docs er tilgjengelig på <https://docs.lunascape.org/>. Uten å installere noe kan du lese dokumenter på GitHub som om de var et nettsted.

## Hva du kan gjøre

| Funksjon | Innhold |
|---|---|
| Vise offentlige repositorier | Åpner dokumentene i et offentlig GitHub-repositorium uten å logge på |
| Vise private repositorier | Når du logger på med GitHub, kan du åpne repositoriene du har lesetilgang til |
| Vise lokale mapper | Med [Åpne dokumenter] og deretter [Åpne dokumenter fra en lokal mappe] åpner du en mappe på enheten (kun i nettlesere som støtter det) |
| Visningsfunksjoner | INDEX, lenker, historikk, filtrering, sideinnhold, språkbytte og temabytte. Det samme som i VS Code-utvidelsen |
| Diagram og matematikk | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose og KaTeX-matematikk |
| Utkast | Rediger dokumenter og behold endringene som utkast på enheten. Ingenting skrives til repositoriet |
| Direktelenker til sider | En URL kan angi repositoriet og siden, slik at en bestemt side kan åpnes direkte |

## Forskjeller fra VS Code-utvidelsen

- Dokumentkontroll, oppretting fra maler, generering av oversettelsesforslag og organisering fra INDEX finnes ikke i Web-visningen.
- TikZ-diagrammer tegnes ikke.
- Redigeringer skrives ikke til repositoriet; de blir utkast på enheten. «Publiseringsforespørsel», som sender utkast som en pull request, er implementert, men er ikke aktivert i den offentlige visningen. For å oppdatere repositoriet må du redigere med VS Code-utvidelsen eller i en lokal klon.

## Relaterte emner

- [Åpne et GitHub-repositorium](open-repository.md)
- [Vise et privat repositorium](private-repository.md)
- [Lagre utkast](drafts.md)
