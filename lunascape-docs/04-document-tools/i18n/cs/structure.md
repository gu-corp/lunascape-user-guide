# Kořen dokumentace a konvence souborů

Pravidla, podle kterých Lunascape Docs vyhledává dokumenty a sestavuje INDEX. Zdrojem pravdy je samotný souborový systém, takže není potřeba žádný rejstřík ani konfigurace sestavení.

## Kořen dokumentace

- Kořenem dokumentace se stává nejbližší složka `docs` nebo složka, která obsahuje `lunascape-docs.json`.
- Se souborem `lunascape-docs.json` se složka nemusí jmenovat `docs`.
- Otevřete-li Markdown mimo jakýkoli kořen dokumentace, zobrazí se jeho složka jako dočasný kořen dokumentace.

## Soubory zobrazené v INDEX

- Zobrazují se soubory `.md`, `.markdown` a `.mdx`. Nové soubory se zobrazí vždy, i bez front matter nebo navigačních informací.
- Složky začínající tečkou `.`, `node_modules` a složky uvedené v `ignoredDirectories` (výchozí je `99-archive`) se nezobrazují.
- Vše pod `i18n/` se považuje za překlady a v INDEX se samostatně neuvádí.

## Titulní stránka složky

- Titulní stránkou složky je soubor `README.md` (nebo `index.md`, pokud README chybí), který má obsah. Stisknutím názvu složky v INDEX se titulní stránka otevře.
- Soubor `README.md`, který obsahuje pouze front matter a žádný obsah, se považuje za „deskriptor pouze pro nastavení“ a jako stránka se nezobrazuje. Použijte jej, když složka potřebuje mít jen titulek nebo pořadí.
- Existují-li současně `README.md` i `index.md`, má přednost `README.md`.

## Výchozí jazyk a překlady

- Dokumenty ve výchozím jazyce (Originál) zůstávají na svém místě.
- Překlad se umisťuje do složky `i18n/<jazyk>/` vedle originálu, pod stejným názvem souboru. Znovu vytvořená struktura složek pod `i18n/` rozpoznána není.
- To je jediné místo, ze kterého se překlad vyhledává. Stejný soubor umístěný kdekoli jinde je osamocený soubor, který si žádný dokument nenárokuje jako svůj překlad.

```text
docs/
  lunascape-docs.json
  README.md                  ← titulní stránka kořene (úvodní stránka)
  i18n/en/README.md          ← jeho anglická verze
  01-product/
    README.md                ← titulní stránka složky
    requirements.md
    i18n/en/README.md        ← anglické verze obou výše uvedených dokumentů
    i18n/en/requirements.md
  99-archive/                ← ve výchozím nastavení vyloučeno z INDEX
```

## O souboru `_meta.json`

Soubor `_meta.json` z Nextra se pro navigaci nepoužívá. Existující soubory se nemění ani nemažou. V budoucnu je bude zpracovávat pouze výslovná funkce importu a exportu.

## Související témata

- [Nastavení navigačních informací](navigation-metadata.md)
- [Nastavení projektu](project-configuration.md)
- [Přepínání kořenů dokumentace](../02-reading/roots.md)
