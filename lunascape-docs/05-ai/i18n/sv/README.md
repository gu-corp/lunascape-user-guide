# Lämna över arbete till en AI

Lunascape Docs anropar ingen språkmodell. Programmet förbereder **sammanhang, verktyg och kontroller** och överlåter översättning, korrektur och skrivande till den AI du använder.

## Tanken bakom

| Det som produkten tillhandahåller | Innehåll |
|---|---|
| Sammanhang | Dokumentens konventioner (var översättningarna ligger, front matter, dokumentstandarden, ordlistan) och det aktuella dokumentets plats |
| Arbetsverktyg | Liggaren över saknade och inaktuella översättningar, läsning och skrivning av dokument, skapande från mallar |
| Kontroller | Granskning med docs-lint samt skillnaden i täckning och färskhet |

Instruktionen innehåller inte dokumentets brödtext. AI:n läser själv filerna, skriver själv och kontrollerar själv.

## Lämna över arbetet

1. Tryck på [Dokumentverktyg] i verktygsfältet och öppna fliken [AI].
2. Välj det arbete du vill lämna över under [Uppgift].
3. Fyll i det som behövs (målspråk, ämne).
4. Tryck på [Lämna över det här arbetet].
   En terminal öppnas i VS Code, och den AI du valt tar emot instruktionen och börjar arbeta.

> **Tips**
>
> En session i Claude Code följs åt av arbetsverktyg (MCP-servern `lunascape-docs`). Sessionen kan själv hämta listan över saknade och inaktuella översättningar, köra docs-lint och registrera färskheten efter en översättning.

## Kontrollera resultatet

| Leverantörens form | Var resultatet hamnar |
|---|---|
| Sessionsbaserad (Claude Code, Codex) | Skriver direkt i arbetsträdet. **Kontrollera i Git-diffen** |
| API-baserad (språkmodeller i VS Code, Anthropic, OpenAI-kompatibla) | Returnerar ett förslag i taget. Kontrollera med [Öppna diff] och skriv med [Spara] |

### Kontrollera ett förslag från en API-leverantör

När du kör med en API-leverantör kommer förslaget till fliken [AI].

1. Tryck på [Öppna diff] och jämför med det nuvarande innehållet.
2. Om det ser bra ut trycker du på [Spara]. För en översättning registreras även färskheten. Vill du avstå trycker du på [Förkasta].
   Tryck på [Avbryt] för att stoppa en generering som pågår.

> **Obs!**
>
> - Lunascape Docs utför aldrig någon Git-köläggning eller incheckning. Kontrollera alltid ändringarna i diffen.
> - I en arbetsyta som inte är betrodd, eller när du tillfälligt visar en mapp utanför en dokumentrot, går det inte att lämna över arbete.

## Se även

- [Arbete som kan lämnas över](tasks.md)
- [AI-inställningar](settings.md)
- [Liggare och register](ledger.md)
