# Brug fra AI-agenter

Udvidelsen registrerer det skrivebeskyttede Language Model Tool `lunascape_getDocsSpecification` i VS Code. Når en kompatibel VS Code-agent bliver spurgt om funktioner, indstillinger eller dokumentkonventioner i Lunascape Docs, kan den hente indholdet af denne hjælp (den generelle specifikation) via værktøjet.

## Sådan bruger du det

Spørg i VS Code-chatten med `#lunascapeDocs`, eller spørg blot om indstillinger eller dokumentstruktur i Lunascape Docs.

```text
#lunascapeDocs Hvordan aktiverer jeg engelske oversættelser i lunascape-docs.json?
```

## Værktøjets argumenter

| Argument | Betydning |
|---|---|
| `topic` | Det afsnit, der skal hentes: `all`, `usage` (Grundlæggende betjening), `structure` (Dokumentrødder og filkonventioner), `editing` (Redigering af et dokument), `configuration` (Projektkonfiguration), `security` (Sikkerhed og skrivegrænser) eller `ai` (Brug fra AI-agenter) |
| `locale` | Hjælpens sprog (et sprogtag for en medfølgende hjælp, såsom `ja` eller `en`). Udelades det, bruges VS Codes visningssprog, med den japanske hjælp som reserve |

> **Bemærk**
>
> - Værktøjet sender aldrig dokumentindhold nogen steder hen.
> - Værktøjet returnerer aldrig arbejdsområdenavne eller lokale stier.
> - Værktøjet ændrer aldrig filer.
> - Det fungerer fra kompatible VS Code-agenter uden en `AGENTS.md`. Det deles ikke automatisk med andre AI-klienter, der ikke bruger udvidelsens værktøjs-API.

## Relaterede emner

- [Vis denne hjælp](../02-reading/help.md)
- [Sikkerhed og skrivegrænser](security.md)
