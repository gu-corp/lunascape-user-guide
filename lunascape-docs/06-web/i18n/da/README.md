# Hvad webvisningen kan

Webbrowserversionen af Lunascape Docs er tilgængelig på <https://docs.lunascape.org/>. Uden at installere noget kan du læse dokumenter på GitHub, som var de et websted.

## Hvad du kan

| Funktion | Indhold |
|---|---|
| Visning af offentlige lagre | Åbner dokumenter i et offentligt GitHub-lager uden at logge ind |
| Visning af private lagre | Når du logger ind med GitHub, kan du åbne de lagre, du har læseadgang til |
| Visning af lokale mapper | Med [Åbn dokumenter] og derefter [Åbn dokumenter fra en lokal mappe] åbner du en mappe på din enhed (kun understøttede browsere) |
| Læsefunktioner | INDEX, links, historik, filtrering, sideoversigt, sprogskift og temaskift. Det samme som i VS Code-versionen |
| Diagrammer og matematik | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose og KaTeX-matematik |
| Kladder | Rediger dokumenter, og behold ændringerne som kladder på din enhed. Der skrives intet til lageret |
| Direkte links til sider | En URL kan angive lager og side, så en bestemt side kan åbnes direkte |

## Forskelle fra VS Code-versionen

- Dokumentkontrol, oprettelse ud fra skabeloner, generering af oversættelsesforslag og organisering fra INDEX findes ikke i webversionen.
- TikZ-diagrammer gengives ikke.
- Redigeringer skrives ikke til lageret, men bliver til kladder på din enhed. "Anmodning om udgivelse", der sender kladder som en pull request, er implementeret, men er ikke aktiveret i den offentlige visning. For at afspejle ændringerne i lageret skal du redigere i VS Code-versionen eller i en lokal klon.

## Relaterede emner

- [Åbn et GitHub-lager](open-repository.md)
- [Se et privat lager](private-repository.md)
- [Gem kladder](drafts.md)
