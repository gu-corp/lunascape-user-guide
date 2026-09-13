# Parancsok listája

A parancspalettán (`⇧⌘P` / `Ctrl+Shift+P`) a „Lunascape Docs” beírásával a következő parancsokat futtathatja.

| Parancs | Funkció |
|---|---|
| Lunascape Docs: Specifikációnézegető megnyitása | Megnyitja a legközelebbi dokumentumgyökeret a nézegetőben. Az olvasás, a szerkesztés, az ellenőrzés és a fordítás ezen a képernyőn történik |
| Lunascape Docs: Megnyitás a specifikációnézegetőben | A szerkesztőben megnyitott Markdown fájlt jeleníti meg a nézegetőben |
| Lunascape Docs: Dokumentum létrehozása sablonból | Létrehozza az első dokumentumkészletet olyan projektben, amelyben nincs dokumentummappa |
| Lunascape Docs: Dokumentumgyökér ellenőrzése | A teljes dokumentumgyökeret ellenőrzi a docs-lint eszközzel, az eredményt pedig a Dokumentumeszközökben és a „Problémák” panelen jeleníti meg |
| Lunascape Docs: Súgó megnyitása | Megnyitja ezt a súgóútmutatót |

## Műveletek a Fájlkezelőből

A Fájlkezelőben kattintson a jobb gombbal egy `.md`, `.markdown` vagy `.mdx` fájlra, és válassza a [Lunascape Docs: Megnyitás a specifikációnézegetőben] parancsot.

> **Tipp**
>
> Ha azt szeretné, hogy a Markdown fájlok a szokásos megnyitáskor is a Lunascape Docsban jelenjenek meg, vegyen fel egy szerkesztő-hozzárendelést a munkaterület beállításaiba.
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## Bemutató

A VS Code [Súgó] menüjének „Üdvözlés” pontjában található „Ismerkedés a Lunascape Docs programmal” bemutatóból sorban kipróbálhatja az első műveleteket.

## Kapcsolódó témák

- [Alapvető műveletek](../02-reading/README.md)
- [Billentyűparancsok listája](../08-reference/keyboard.md)
