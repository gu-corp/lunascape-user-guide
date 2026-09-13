# Instalace rozšíření

Rozšíření „Lunascape Docs Pro“ pro VS Code se distribuuje jako soubor VSIX. Je zdarma; „Pro“ označuje edici, která předává práci AI a aktualizuje se sama.

## Požadavky

- VS Code 1.90 nebo novější
- Funkce, které zapisují soubory — vytváření dokumentů, uspořádání panelu INDEX, ukládání nastavení kontrol, překlad — fungují jen v pracovním prostoru, který jste ve VS Code označili jako důvěryhodný.

## Instalace

1. Získejte soubor VSIX. Tento odkaz vždy míří na aktuální verzi.

   [Stáhnout lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Otevřete zobrazení Rozšíření (`⇧⌘X` / `Ctrl+Shift+X`).
3. V nabídce `…` vpravo nahoře vyberte [Instalovat z VSIX…] a zvolte stažený soubor.

### Z příkazového řádku

Jeden řádek, pokud raději neopouštíte terminál. Stáhne a nainstaluje.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Poznámka**
> Pokud se `code` nenajde, spusťte z palety příkazů (`⇧⌘P` / `Ctrl+Shift+P`) příkaz [Příkaz shellu: Nainstalovat příkaz „code“ do PATH].

## Aktualizace

Když je zveřejněna novější verze, rozšíření si ji samo stáhne a nainstaluje. VS Code vás vyzve k opětovnému načtení okna a právě tehdy začnete používat novou verzi. Vaše nastavení a dokumenty zůstanou beze změny.

Kontrola probíhá jednou denně. Chcete-li zkontrolovat hned, spusťte z palety příkazů (`⇧⌘P` / `Ctrl+Shift+P`) příkaz [Lunascape Docs: Zkontrolovat novější verzi].

Chování změníte nastavením `lunascapeDocEditor.update.check`.

| Nastavení | Chování |
|---|---|
| Nainstalovat novější verzi, jakmile je zveřejněna | Výchozí |
| Upozornit a nechat rozhodnout pokaždé | Objeví se oznámení a nic se nezmění, dokud nestisknete [Aktualizovat] |
| Nekontrolovat | Nestane se nic |

### Když nelze aktualizovat

Zpráva „Aktualizaci se nepodařilo stáhnout: No Servers“ znamená, že nainstalovaná verze je 0.22.18 nebo starší. Její aktualizační postup po stažení v posledním kroku vždy selže, takže se sama na novější verzi nedostane. Nainstalujte ji jednou ručně podle výše uvedeného postupu; od té chvíle se aktualizuje sama.

## Kontrola verze

Otevřete „Lunascape Docs Pro“ v zobrazení Rozšíření a uvidíte nainstalovanou verzi. Budete ji potřebovat při hlášení problému.

## Související témata

- [Vytvoření prvních dokumentů](first-documents.md)
- [Nahlášení problému](../07-troubleshooting/report.md)
