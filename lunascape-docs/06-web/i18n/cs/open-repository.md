# Otevření úložiště GitHub

Ve webové verzi můžete úložiště GitHub otevřít a číst přímo, aniž byste ho klonovali. U veřejných úložišť není přihlášení nutné.

## Otevření z obrazovky

1. Na panelu nástrojů stiskněte [Otevřít dokumenty] (ikona složky). Otevře se obrazovka „Otevřít dokumenty“.
2. V levém sloupci vyberte umístění, ze kterého chcete otevírat.

   | Umístění | Co se zobrazí |
   |---|---|
   | Vše | Vše níže uvedené. Nedávno otevřené položky jsou na začátku |
   | Nedávno otevřené | Úložiště a složky, které jste dříve otevřeli |
   | Doporučené | Příručky, které web doporučuje |
   | Úložiště GitHub | Pokud jste přihlášeni přes GitHub, úložiště, která můžete číst |
   | Tento počítač | Složky v tomto zařízení |

3. U požadovaného řádku stiskněte [Otevřít]. Zadáním textu do pole [Filtrovat podle názvu dokumentu nebo úložiště] nahoře můžete řádky zúžit.

Úložiště, které v seznamu není, zadejte pomocí [Zadat owner/repo a otevřít] v levém sloupci.

> **Tip**
>
> - V seznamu se zobrazují úložiště GitHub, do kterých je nainstalována aplikace GitHub App „Lunascape Docs“ a ke kterým máte oprávnění ke čtení. Pokud některé chybí, požádejte vlastníka úložiště, aby aplikaci přidal.

## Ověření umístění dokumentu

Malá ikona v levé části panelu nástrojů (čip umístění) ukazuje, kde se právě čtený dokument nachází.

| Ikona | Umístění |
|---|---|
| Logo GitHub | Čtete ze služby GitHub. V tomto zařízení se nic neukládá |
| Složka | Složka v tomto zařízení |

Stisknutím ikony zobrazíte umístění, jeho stav a operace, které odtud můžete provést ([Zobrazit ve službě GitHub], [Kopírovat odkaz] apod.).

## Otevření pomocí adresy URL

Adresa obsahuje úložiště a umístění dokumentu v tomto pořadí. Cesta udává umístění uvnitř úložiště, takže pořadí odpovídá adrese URL na GitHubu.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Co zadat | Zápis |
|---|---|
| Pouze úložiště (výchozí větev) | `/github/owner/repo` |
| Dokument v úložišti | `/github/owner/repo/docs/01-product/vision.md` |
| Určení větve nebo značky | Na konec připojte `?ref=v1.2.0` |

Při přechodu na jinou stránku se změní i adresa. Stisknutím [Sdílet tento dokument] na panelu nástrojů můžete předat odkaz na právě čtenou stránku. Fungují i tlačítka prohlížeče [Zpět] a [Vpřed].

Starší tvar `?source=` lze otevřít i nadále. Po otevření se adresa přepíše do nového tvaru.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Upozornění**
>
> - Bez přihlášení platí omezení rozhraní GitHub API (60 požadavků za hodinu). U úložišť s mnoha dokumenty nebo při opakovaném čtení použijte [Přihlásit se přes GitHub].
> - Název větve obsahující `/` (např. `feature/xxx`) lze zadat pomocí `?ref=` v tvaru adresy uvedeném výše. V tvaru `?source=` jej zapsat nelze.
> - Dokumenty se načítají s oprávněními čtenáře na GitHubu. Kdo nemá oprávnění ke čtení, dokumenty neuvidí.

## Otevření dokumentů z místní složky

Na panelu nástrojů stiskněte [Otevřít dokumenty], v levém sloupci zvolte [Otevřít dokumenty z místní složky] a vyberte složku v zařízení. Soubory se zpracovávají v prohlížeči a nikam se neodesílají. Funguje v prohlížečích, které podporují výběr složky (Chrome, Edge apod.).

## Související témata

- [Prohlížení neveřejného úložiště](private-repository.md)
- [Webovou verzi nelze otevřít nebo se nelze přihlásit](../07-troubleshooting/web.md)
