# Dokumenty se nezobrazují

## Zobrazí se „Nenašel se žádný Markdown ani složka docs, kterou lze otevřít"

- Pracovní prostor neobsahuje složku `docs`, nebo používá jiný název než `docs`.
  - Umístěte do dané složky soubor `lunascape-docs.json` a bude rozpoznána jako kořen dokumentace bez ohledu na svůj název.
  - Nebo přidejte název složky do nastavení `lunascapeDocEditor.rootDirectoryNames`.
- Pokud zatím žádné dokumenty nemáte, vytvořte je příkazem „Lunascape Docs: Vytvořit dokumentaci ze šablony".
- Lze také otevřít soubor Markdown v editoru a spustit „Lunascape Docs: Otevřít v prohlížeči specifikací".

## Dokument se nezobrazuje v INDEX

- Zkontrolujte, že přípona je `.md`, `.markdown` nebo `.mdx`.
- Tyto složky se nezobrazují: složky začínající tečkou `.`, `node_modules` a složky uvedené v `ignoredDirectories` (výchozí je `99-archive`).
- Překlady ve složce `i18n/` se v INDEX neuvádějí samostatně. Přepnete na ně v nabídce jazyků.
- Pokud se právě přidaný soubor nezobrazuje, stiskněte [Znovu načíst].
- Možná si prohlížíte jiný kořen dokumentace. Zkontrolujte název kořene dokumentace na levém okraji panelu nástrojů.

## Po stisknutí složky se nic nezobrazí

Soubor `README.md` této složky je „popisovač určený pouze pro nastavení", který obsahuje jen front matter a žádný text. Rozbalte složku v INDEX a vyberte dokument uvnitř.

## Otevře se nechtěný kořen dokumentace

- Je-li nastavení `lunascapeDocEditor.rootMode` nastaveno na `fixed`, otevírá se vždy kořen uvedený v `lunascapeDocEditor.root`.
- Při hodnotě `auto` se vybere kořen dokumentace nejbližší otevřenému souboru Markdown. Přepnout jej lze rozbalovací nabídkou na levém okraji panelu nástrojů.

## Název kořene dokumentace neodpovídá očekávání

Název se určuje v tomto pořadí: `title` v souboru `lunascape-docs.json` → `navigation.title` v kořenovém `README.md` → jeho nadpis H1 → `index.md` → název složky. Chcete-li jej pevně stanovit, nastavte `title`.

## INDEX zmizel

- V kořeni dokumentace s jediným dokumentem se INDEX poprvé automaticky zavře. Otevřete jej ikonou sloupců na panelu nástrojů. Vypnout to lze volbou [Skrýt, když je dokument jen jeden] v [Nastavení zobrazení].
- Na úzké obrazovce jej otevřete tlačítkem [Otevřít INDEX] (tři čárky) vlevo od [Zpět].

## Odkaz se po stisknutí neotevře

- „Cíl odkazu nebyl nalezen": cílový soubor neexistuje. Interní odkazy zkontrolujete pomocí [Kontrola] v Nástrojích dokumentu.
- „Nebezpečný nebo nepodporovaný odkaz nebyl otevřen": odkazy mimo kořen dokumentace a odkazy na jiná schémata než `https://` a `mailto:` se neotevírají.

## Zobrazuje se jiný jazyk, než jste chtěli

- V nabídce jazyků zkontrolujte jazyk zobrazené stránky a důvod jeho volby.
- Naposledy zvolený jazyk zobrazení se pamatuje. V nabídce jazyků znovu vyberte výchozí jazyk.
- Je-li nastaveno osobní nastavení `lunascapeDocEditor.locale`, má přednost překlad v tomto jazyce.

## Související témata

- [Přepnutí kořene dokumentace](../02-reading/roots.md)
- [Kořen dokumentace a konvence souborů](../04-document-tools/structure.md)
