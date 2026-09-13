# Vad webbversionen kan göra

Webbläsarversionen av Lunascape Docs finns på <https://docs.lunascape.org/>. Utan att installera något kan du läsa dokument på GitHub som om de vore en webbplats.

## Detta kan du göra

| Funktion | Innehåll |
|---|---|
| Visa offentliga lagringsplatser | Öppnar dokument i en offentlig lagringsplats på GitHub utan inloggning |
| Visa privata lagringsplatser | När du loggar in med GitHub kan du öppna de lagringsplatser du har läsbehörighet till |
| Visa lokala mappar | Med [Öppna dokument] och sedan [Öppna dokument från en lokal mapp] öppnar du en mapp på enheten (endast webbläsare som stöder det) |
| Läsfunktioner | INDEX, länkar, historik, filtrering, innehåll på sidan, byte av språk och byte av tema. Samma som i VS Code-versionen |
| Diagram och matematik | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose, KaTeX-matematik |
| Utkast | Redigera dokument och behåll ändringarna som utkast på enheten. Inget skrivs till lagringsplatsen |
| Direktlänk till en sida | En URL kan ange lagringsplats och sida, så att en viss sida öppnas direkt |

## Skillnader mot VS Code-versionen

- Dokumentkontroll, skapande från mallar, generering av översättningsförslag och ordning från INDEX finns inte i webbversionen.
- TikZ-diagram ritas inte upp.
- Redigeringar skrivs inte till lagringsplatsen utan blir utkast på enheten. ”Publiceringsbegäran”, som skickar utkast som en pull request, är implementerad men inte aktiverad i den offentliga visningen. Redigera med VS Code-versionen eller i en lokal klon för att ändra lagringsplatsen.

## Relaterade avsnitt

- [Öppna en lagringsplats på GitHub](open-repository.md)
- [Visa en privat lagringsplats](private-repository.md)
- [Spara utkast](drafts.md)
