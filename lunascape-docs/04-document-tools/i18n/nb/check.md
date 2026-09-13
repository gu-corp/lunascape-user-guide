# Kontrollere dokumenter

docs-lint lar deg kontrollere oppbyggingen av overskrifter, brutte lenker, manglende obligatoriske dokumenter og kapitler, uensartet terminologi, samsvar mellom krav-ID-er og mer. En kontroll gjelder alltid hele dokumentroten.

## Kjøre en kontroll

1. Trykk på [Dokumentverktøy] i verktøylinjen og åpne fanen [Kontroll].
2. Trykk på [Kontroller dokumentroten].
   Du kan også kjøre «Lunascape Docs: Kontroller dokumentroten» fra kommandopaletten.
3. Se gjennom listen med funn.

## Lese resultatene

- Med [Dette dokumentet] / [Alle] over listen bytter du hva som vises. Selve omfanget av kontrollen er alltid hele dokumentroten.
- Funn har fire nivåer: «feil», «advarsel», «informasjon» og «forslag». [Dokumentverktøy] i verktøylinjen viser antallet feil og advarsler.
- Trykk på et funn for å åpne det tilhørende stedet i Markdown-kilden i VS Code-editoren.
- Funn som gjelder hele dokumentroten (for eksempel et manglende testdokument) vises som oppføringer under «hele dokumentroten» og har ingen posisjon.
- De samme funnene vises også i «Problemer»-panelet i VS Code.

## Hva som kontrolleres

Trykk på [Se gjennom og endre reglene] for å vise listen over aktive kontroller og formålet med hver enkelt. De viktigste er som følger.

| Punkt | Innhold |
|---|---|
| Overskriftsoppbygging | Om det finnes én H1, og om overskriftsnivåene ikke hopper over underveis |
| Interne lenker | Om det lenkede dokumentet finnes, og om lenken ikke går ut av dokumentroten |
| Språk for kodeblokker | Om kodeblokker har et språknavn angitt |
| Nødvendige mapper og dokumenter | Om mappene og dokumentene som Standard Pack-profilen krever, er på plass |
| Nødvendige kapitler i dokumentet | Om det finnes nødvendige kapitler for hver dokumenttype |
| Enhetlig terminologi | Oppdager uttrykk som bør unngås, og oppfordrer til enhetlig bruk av anbefalte termer |
| Navngivning og duplikater av krav-ID-er | Om krav-ID-ene følger navnereglene og ikke er definert dobbelt |
| Referansesamsvar for krav-ID-er | Om krav-ID-ene som design, tester, statustabeller og lignende viser til, faktisk finnes |
| Samsvar mellom krav og tester | Om krav-ID-ene refereres fra testdokumenter |

Hvilke punkter som blir aktive, bestemmes av Standard Pack og profilen du har valgt i `lunascape-docs.json`, samt av `docs-lint.config.json`.

> **Merk**
>
> - Når du endrer et dokument eller en innstilling, blir det forrige resultatet «trenger ny kontroll». Ingenting regnes som bestått automatisk. Trykk på [Kontroller dokumentroten] på nytt.
> - Endringer som ikke er lagret, tas ikke med i kontrollen. Lagre først.
> - Kontrollen kjøres deterministisk på enheten. Resultater fra AI-vurderinger eller oversettelser blandes aldri inn i kontrollresultatene.

## Relaterte emner

- [Endre kontrollregler](rules.md)
- [Prosjektkonfigurasjon](project-configuration.md)
- [Kontroll, oppretting eller oversettelse fungerer ikke](../07-troubleshooting/tools.md)
