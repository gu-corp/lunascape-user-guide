# Kontrollera dokument

Med docs-lint kan du kontrollera rubrikstrukturen, brutna länkar, saknade obligatoriska dokument och avsnitt, inkonsekventa termer, överensstämmelse mellan krav-ID:n med mera. En kontroll omfattar alltid hela dokumentroten.

## Utför en kontroll

1. Tryck på [Dokumentverktyg] i verktygsfältet och öppna fliken [Kontroll].
2. Tryck på [Kontrollera dokumentroten].
   Du kan också köra ”Lunascape Docs: Kontrollera dokumentroten” från kommandopaletten.
3. Granska listan med resultat.

## Läs resultatet

- Med [Det här dokumentet] / [Alla] ovanför listan växlar du vad som visas. Själva kontrollens omfattning är alltid hela dokumentroten.
- Anmärkningarna har fyra nivåer: fel, varning, information och förslag. [Dokumentverktyg] i verktygsfältet visar antalet fel och varningar.
- Tryck på en anmärkning för att öppna motsvarande plats i Markdown-källan i VS Code-redigeraren.
- Anmärkningar som gäller hela dokumentroten (till exempel ett saknat testdokument) visas som poster under ”Hela dokumentroten” och har ingen plats.
- Samma anmärkningar visas även i panelen Problem i VS Code.

## Det som kontrolleras

Tryck på [Granska och ändra reglerna] för att se listan över aktiva kontroller och syftet med var och en. De viktigaste är följande.

| Kontroll | Innebörd |
|---|---|
| Rubrikstruktur | Det finns en H1 och rubriknivåerna hoppar inte över något steg |
| Interna länkar | De länkade dokumenten finns och ligger kvar inom dokumentroten |
| Kodblockets språk | Kodblocken anger ett språknamn |
| Nödvändiga mappar och dokument | De mappar och dokument som Standard Pack-profilen kräver finns |
| Nödvändiga avsnitt i dokumentet | Varje dokumenttyp har de avsnitt den kräver |
| Enhetlig terminologi | Uttryck som bör undvikas påtalas och de rekommenderade termerna föreslås |
| Namngivning och dubbletter av krav-ID | Krav-ID:n följer namngivningsregeln och är inte definierade två gånger |
| Referensöverensstämmelse för krav-ID | De krav-ID:n som design, tester och statustabeller hänvisar till finns |
| Koppling mellan krav och test | Krav-ID:n hänvisas till från testdokumenten |

Vilka kontroller som är aktiva avgörs av den Standard Pack och profil som valts i `lunascape-docs.json` och av `docs-lint.config.json`.

> **Obs!**
>
> - När du ändrar ett dokument eller en inställning blir det föregående resultatet ”behöver kontrolleras igen”. Ingenting godkänns automatiskt. Tryck på [Kontrollera dokumentroten] en gång till.
> - Ändringar som inte har sparats tas inte med i kontrollen. Spara först.
> - Kontrollen körs deterministiskt på den egna datorn. Bedömningar från AI och resultat av översättningar blandas aldrig in i kontrollresultatet.

## Relaterade avsnitt

- [Ändra kontrollreglerna](rules.md)
- [Projektinställningar](project-configuration.md)
- [Kontroll, skapande eller översättning fungerar inte](../07-troubleshooting/tools.md)
