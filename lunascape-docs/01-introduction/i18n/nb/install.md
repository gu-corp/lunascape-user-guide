# Installere utvidelsen

VS Code-utvidelsen «Lunascape Docs Pro» distribueres som en VSIX-fil. Den er gratis; «Pro» angir utgaven som gir arbeid videre til en AI og oppdaterer seg selv.

## Systemkrav

- VS Code 1.90 eller nyere
- Funksjoner som skriver til filer – opprette dokumenter, organisere INDEX, lagre kontrollinnstillinger, oversette – fungerer bare i et arbeidsområde du har merket som klarert i VS Code.

## Installere

1. Hent VSIX-filen. Denne lenken peker alltid til den nyeste versjonen.

   [Last ned lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Åpne utvidelsesvisningen (`⇧⌘X` / `Ctrl+Shift+X`).
3. Velg [Installer fra VSIX...] fra `…`-menyen øverst til høyre, og pek ut filen du lastet ned.

### Fra kommandolinjen

Én linje, hvis du heller vil bli i terminalen. Den henter og installerer.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Merk**
> Hvis `code` ikke blir funnet, kjør [Shell-kommando: Installer 'code'-kommandoen i PATH] fra kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).

## Oppdatere

Når en nyere versjon publiseres, henter og installerer utvidelsen den selv. VS Code ber om å laste inn vinduet på nytt, og det er da du tar den i bruk. Innstillingene og dokumentene dine blir liggende som de er.

Den ser etter én gang om dagen. For å se etter med det samme, kjør [Lunascape Docs: Se etter en nyere versjon] fra kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).

`lunascapeDocEditor.update.check` endrer hva som skjer.

| Innstilling | Hva som skjer |
|---|---|
| Installer en nyere versjon når en publiseres | Standard |
| Gi beskjed, og la meg bestemme hver gang | Et varsel dukker opp, og ingenting endres før du trykker [Oppdater] |
| Se aldri etter | Ingenting skjer |

### Når den ikke kan oppdatere

«Kunne ikke hente oppdateringen: No Servers» betyr at den installerte versjonen er 0.22.18 eller eldre. Oppdateringsforløpet dens svikter alltid i det siste steget, så den kan ikke få seg selv over på en nyere versjon. Installer én gang for hånd, som ovenfor; fra da av oppdaterer den seg selv.

## Sjekke versjonen

Åpne «Lunascape Docs Pro» i utvidelsesvisningen for å se den installerte versjonen. Du trenger den når du rapporterer et problem.

## Relaterte emner

- [Opprette de første dokumentene dine](first-documents.md)
- [Rapportere et problem](../07-troubleshooting/report.md)
