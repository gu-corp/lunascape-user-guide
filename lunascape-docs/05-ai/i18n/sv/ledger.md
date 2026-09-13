# Register och poster

Registret högst upp på fliken [AI] visar översättningsläget för varje språk som stöds. Du kan se vad som saknas även utan att använda AI.

| Visning | Betydelse |
|---|---|
| Saknad översättning | Antal dokument som ännu inte har någon översättning |
| Inaktuell | Antal dokument som har en översättning, men vars originaldokument är nyare än posten |
| Översatt | Antal översättningar som följer sitt originaldokument |

Registret beräknas genom att dokumentroten gås igenom. Varken AI eller språkmodell är inblandad.

## Uppdatera översättningsposterna

För att avgöra vad som är ”inaktuellt” måste originaldokumentet och översättningen registreras så som de såg ut vid översättningstillfället. Sessionsbaserad AI skriver filerna direkt, så posterna skapas inte automatiskt.

1. När översättningen är klar och du har granskat innehållet trycker du på [Uppdatera översättningsposter].
2. Översättningar utan post registreras som motsvarande det aktuella originaldokumentet.

Sessioner i Claude Code och sparande via API-leverantörer registrerar detta automatiskt (en session uppmanas att använda MCP-verktyget `record_translation_freshness`). Knappen behövs när du har översatt i Codex eller i chatten i VS Code.

Därefter visas översättningen som ”inaktuell” när du ändrar originaldokumentet.

> **Observera**
>
> - Översättningar som redan har en post skrivs inte över. Det är för att ett befintligt läge som ”inaktuell” inte ska försvinna.
> - Posterna sparas i `.lunascape-docs/translation-freshness.json`. Det som sparas är bara relativa sökvägar, språk, innehållshashar och tidsstämpel – aldrig själva texten.

## Relaterade ämnen

- [Arbete att lämna över](tasks.md)
- [Läsa på ett annat språk](../02-reading/languages.md)
