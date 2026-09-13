# Sikkerhed og skrivegrænser

De grænser, Lunascape Docs opretholder for at beskytte dine dokumenter og din enhed.

## Visning

- HTML genereret fra Markdown og SVG genereret fra diagrammer renses med DOMPurify 3.4.14 før visning.
- Vilkårlige scripts i MDX udføres aldrig.
- KaTeX kører med `trust: false`, `maxSize: 50` og `maxExpand: 1000` og har hverken tillid til ekstern HTML eller vilkårlige kommandoer.
- Tegnebibliotekerne Markmap, WaveDrom, Svgbob, Vega-Lite og Penrose indlæses lokalt i fastlåste versioner, kun når den tilsvarende blok er til stede. Referencer til eksterne ressourcer, rå HTML og eksekverbare notationer er ikke tilladt, og scripts, eksterne billeder, `link`, `style` og `foreignObject` fjernes fra genereret SVG.
- Tegning med TikZ starter aldrig værtens LaTeX. Den kører sekventielt i en WebAssembly-TeX-worker med et filsystem i hukommelsen, begrænset i input, kø, hukommelse, køretid (15 sekunder) og SVG-output, og afviser fil-I/O-instruktioner.

## Adgang til dokumenter og filer

- Dokumentlinks og filhandlinger kan ikke forlade dokumentroden.
- Oprettelse, omdøbning, flytning og sletning fra INDEX bliver kontrolleret på ny på udvidelsens side — dokumentrod, INDEX-version, originaldokumentets sti, målets type, symbolske links' grænser og ugemte dokumenter — før de anvendes. Anmodninger fra en forældet menu eller en anden dokumentrod anvendes ikke.
- Ændringer i INDEX er deaktiveret, mens et dokument redigeres, eller mens en anden INDEX-handling anvendes.
- Oprettelse fra en skabelon kontrollerer på ny arbejdsområdets tillid, dokumentrodens identitet, INDEX-versionen, Standard Pack og det genererede indhold, destinationen og symbolske links' grænser efter forhåndsvisningen. Den overskriver aldrig en eksisterende fil og opretter aldrig indhold, der afviger fra forhåndsvisningen eller overstiger 4 MiB.
- Ved gemning af en konfigurationsfil kontrolleres versionen umiddelbart forinden, og handlingen afbrydes, hvis der registreres en ekstern ændring.

## Afsendelse til eksterne

- Dokumenter sendes aldrig nogen steder hen med henblik på visning, redigering eller kontrol. Dokumentkontroller kører lokalt og deterministisk.
- Kun oversættelse (af denne side eller samlet) sender dokumenter til en sprogmodel, efter at destinationen og omfanget er blevet oplyst, og kun med udtrykkelig godkendelse. <!-- ai-only -->
- Oversættelsesforslag præsenteres som en forskel, versionerne af originaldokumentet og oversættelsesmålet kontrolleres på ny, og et forslag anvendes kun, når en person gemmer det udtrykkeligt. <!-- ai-only -->
- Specifikationsværktøjet til AI-agenter returnerer intet dokumentindhold, ingen navne på arbejdsområder og ingen lokale stier. <!-- ai-only -->

## Git

- Gemning skriver kun til filen. Ingen funktion udfører staging eller commits i Git automatisk.
- Eksisterende filer som `_meta.json` slettes eller ændres aldrig i det skjulte. Forældreløse oversættelser slettes eller flyttes aldrig automatisk.

## Relaterede emner

- [Vigtigste specifikationer](README.md)
- [Brug fra AI-agenter](ai-agents.md)
