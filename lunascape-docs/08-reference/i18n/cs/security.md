# Zabezpečení a hranice zápisu

Hranice, které Lunascape Docs udržuje, aby chránil vaše dokumenty a vaše zařízení.

## Zobrazení

- HTML vygenerované z Markdownu a SVG vygenerované z diagramů se před zobrazením ošetří knihovnou DOMPurify 3.4.14.
- Libovolné skripty obsažené v MDX se nespouštějí.
- KaTeX běží s nastavením `trust: false`, `maxSize: 50` a `maxExpand: 1000` a nedůvěřuje externímu HTML ani libovolným příkazům.
- Vykreslovací knihovny Markmap, WaveDrom, Svgbob, Vega-Lite a Penrose se načítají v zařízení v pevně daných verzích, a to jen tehdy, když je přítomen odpovídající blok. Odkazy na externí zdroje, surové HTML a spustitelné zápisy nejsou povoleny a z vygenerovaného SVG se odstraňují skripty, externí obrázky, `link`, `style` a `foreignObject`.
- Vykreslování TikZ nespouští LaTeX v hostitelském systému. Probíhá postupně ve WebAssembly workeru TeXu s vlastním souborovým systémem v paměti, má omezen vstup, frontu, paměť, dobu běhu (15 sekund) i výstupní SVG a odmítá instrukce pro souborové I/O.

## Přístup k dokumentům a souborům

- Odkazy v dokumentech ani operace se soubory nemohou opustit Kořen dokumentace.
- Vytvoření, přejmenování, přesunutí a smazání z panelu INDEX se před provedením znovu ověří na straně rozšíření: Kořen dokumentace, verze panelu INDEX, cesta k originálu, typ cíle, hranice symbolických odkazů a neuložené dokumenty. Požadavky ze zastaralé nabídky nebo z jiného Kořene dokumentace se neprovedou.
- Během úprav dokumentu nebo během provádění jiné operace v panelu INDEX jsou změnové operace v panelu INDEX vypnuté.
- Vytvoření ze Šablony po náhledu znovu ověří důvěryhodnost pracovního prostoru, identitu Kořene dokumentace, verzi panelu INDEX, Standard Pack a generovaný obsah, cílové umístění a hranice symbolických odkazů. Nikdy nepřepíše existující soubor a nevytvoří obsah, který se liší od náhledu nebo jehož rozbalený výsledek přesahuje 4 MiB.
- Uložení konfiguračního souboru těsně předtím zkontroluje jeho verzi a při zjištění externí změny se přeruší.

## Odesílání mimo zařízení

- Dokumenty se kvůli prohlížení, úpravám ani kontrole nikam neodesílají. Kontrola dokumentů probíhá v zařízení a deterministicky.
- Pouze Překlad (překlad této stránky a hromadný překlad) odesílá dokumenty jazykovému modelu, a to po předchozím zobrazení cíle a rozsahu odeslání a jen při výslovném schválení. <!-- ai-only -->
- Návrhy překladu se zobrazí jako rozdíl, znovu se ověří verze originálu i cílového překladu a návrh se použije jen tehdy, když jej člověk výslovně uloží. <!-- ai-only -->
- Nástroj se Specifikací pro AI agenty nevrací text dokumentů, názvy pracovních prostorů ani místní cesty. <!-- ai-only -->

## Git

- Uložení pouze zapíše soubor. Žádná funkce neprovádí přípravu ke commitu ani commit v Gitu automaticky.
- Existující soubory, například `_meta.json`, se nikdy tiše nemažou ani nemění. Osamocené překlady se rovněž nemažou ani nepřesouvají automaticky.

## Související témata

- [Hlavní specifikace](README.md)
- [Použití z AI](ai-agents.md)
