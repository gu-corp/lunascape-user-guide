# Co umí webová verze

Webová verze prohlížeče Lunascape Docs je dostupná na <https://docs.lunascape.org/>. Bez jakékoli instalace můžete číst dokumenty na GitHubu jako webové stránky.

## Funkce

| Funkce | Popis |
|---|---|
| Veřejná úložiště | Otevře dokumenty veřejného úložiště na GitHubu bez přihlášení |
| Neveřejná úložiště | Po přihlášení přes GitHub otevře úložiště, ke kterým máte oprávnění ke čtení |
| Místní složky | Volbou [Otevřít dokumenty] a poté [Otevřít dokumenty z místní složky] otevřete složku ve svém zařízení (jen v podporovaných prohlížečích) |
| Čtení | INDEX, odkazy, historie, filtrování, obsah stránky, přepínání jazyka a přepínání motivu, stejně jako ve VS Code |
| Diagramy a vzorce | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose a vzorce KaTeX |
| Koncepty | Upravujte dokumenty a uchovávejte změny jako koncepty ve svém zařízení. Do úložiště se nic nezapisuje |
| Přímé odkazy na stránku | Adresa URL může určit úložiště i stránku, takže lze konkrétní stránku otevřít přímo |

## Rozdíly oproti verzi pro VS Code

- Kontroly dokumentů, vytváření ze šablon, generování návrhů překladu a uspořádání z panelu INDEX ve webové verzi nejsou.
- Obrázky TikZ se nevykreslují.
- Úpravy se nezapisují do úložiště, stanou se koncepty ve vašem zařízení. Funkce „Žádost o publikování“, která odesílá koncepty jako pull request, je sice implementovaná, ale ve veřejném prohlížeči není zapnutá. Chcete-li změny promítnout do úložiště, upravujte je ve verzi pro VS Code nebo v místním klonu.

## Související témata

- [Otevření úložiště na GitHubu](open-repository.md)
- [Čtení neveřejného úložiště](private-repository.md)
- [Ukládání konceptů](drafts.md)
