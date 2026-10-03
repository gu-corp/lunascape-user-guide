# Otevření úložiště GitHub

Ve webové verzi a v Lunascape můžete úložiště GitHub otevřít a číst přímo, aniž byste ho duplikovali. U veřejných úložišť není přihlášení nutné.

## Otevření z obrazovky

1. Na panelu nástrojů stiskněte [Otevřít dokumenty] (ikona složky). Otevře se obrazovka „Otevřít dokumenty“.
2. V levém sloupci vyberte, odkud chcete dokumenty otevřít.

   | Místo | Co se zobrazí |
   |---|---|
   | Vše | Všechno, co je uvedeno níže. Nedávno otevřené položky jsou na začátku |
   | Nedávno otevřené | Úložiště a složky, které jste dříve otevřeli |
   | Doporučené | Příručky, které web doporučuje |
   | Úložiště GitHub | Úložiště, která můžete číst, pokud jste přihlášeni ke službě GitHub |
   | Tento počítač | Složky v tomto zařízení. V Lunascape se zde zobrazují i duplikovaná úložiště |

3. U řádku, který chcete otevřít, stiskněte [Otevřít]. Řádky můžete vyfiltrovat zadáním textu do pole [Filtrovat podle názvu dokumentu nebo úložiště] nahoře.

Úložiště, které v seznamu není, zadáte v levém sloupci pomocí [Otevřít zadáním owner/repo].

> **Tip**
>
> - V seznamu se zobrazují úložiště GitHub, do kterých je nainstalována aplikace GitHub App „Lunascape Docs“ a ke kterým máte oprávnění ke čtení. Pokud úložiště v seznamu nenajdete, požádejte jeho vlastníka, aby aplikaci přidal.

## Ověření umístění dokumentu

Malá ikona v levé části panelu nástrojů (štítek umístění) ukazuje, kde je dokument, který právě čtete.

| Ikona | Umístění |
|---|---|
| Logo GitHub | Čtete ze služby GitHub. Dokument není uložen v tomto zařízení |
| Počítač | Složka v tomto zařízení, kterou spravuje Lunascape. Zobrazuje se také název větve Gitu a počet změněných souborů |
| Složka | Složka v tomto zařízení |

Po stisknutí ikony se zobrazí umístění, stav a akce, které jsou odtud k dispozici (například [Zobrazit ve službě GitHub] nebo [Kopírovat odkaz]).

## Duplikování úložiště v Lunascape

V Lunascape můžete úložiště GitHub duplikovat do tohoto zařízení a pak v něm pomocí Gitu upravovat soubory a vytvářet commity.

- Na obrazovce „Otevřít dokumenty“ stiskněte u řádku úložiště [Duplikovat].
- Pokud čtete úložiště otevřené ze služby GitHub, stiskněte štítek umístění a potom [Duplikovat do tohoto počítače]. Po dokončení duplikování se stejný dokument otevře z kopie v tomto zařízení.

Duplikované úložiště je v seznamu označeno „V tomto počítači“ a jako první je u něj uvedeno [Otevřít v tomto počítači].

## Otevření pomocí adresy URL

Adresa obsahuje úložiště a umístění dokumentu v tom pořadí, v jakém jdou za sebou. Cesta udává umístění v rámci úložiště, proto má stejné pořadí jako adresa URL ve službě GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Co zadat | Zápis |
|---|---|
| Pouze úložiště (výchozí větev) | `/github/owner/repo` |
| Dokument v úložišti | `/github/owner/repo/docs/01-product/vision.md` |
| Určitá větev nebo značka | Na konec připojte `?ref=v1.2.0` |

Při přechodu na jinou stránku se změní i adresa. Stisknutím [Sdílet tento dokument] na panelu nástrojů můžete předat odkaz na stránku, kterou právě čtete. Můžete také používat tlačítka prohlížeče [Zpět] a [Vpřed].

Adresy ve starším tvaru `?source=` lze otevřít stejně jako dosud. Po otevření se adresa přepíše do nového tvaru.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Upozornění**
>
> - Bez přihlášení platí omezení počtu požadavků na GitHub API (60 za hodinu). U úložišť s mnoha dokumenty nebo při opakovaném čtení stiskněte [Přihlásit se přes GitHub].
> - Názvy větví, které obsahují `/` (například `feature/xxx`), lze zadat pomocí `?ref=` v tvaru adresy uvedeném výše. V tvaru `?source=` je zapsat nelze.
> - Dokumenty se načítají s oprávněními, která má čtenář ve službě GitHub. Lidé bez oprávnění ke čtení je neuvidí.

## Otevření dokumentů z místní složky

Na panelu nástrojů stiskněte [Otevřít dokumenty], v levém sloupci stiskněte [Otevřít dokumenty z místní složky] a vyberte složku v zařízení. Soubory se zpracovávají v prohlížeči a nikam se neodesílají. Tato funkce je k dispozici v prohlížečích, které podporují výběr složky (Chrome, Edge a další).

## Související témata

- [Prohlížení neveřejného úložiště](private-repository.md)
- [Webovou verzi nelze otevřít nebo se nelze přihlásit](../07-troubleshooting/web.md)
