# Otevření úložiště GitHub

Ve webové verzi otevřete dokumenty zadáním úložiště GitHub. U veřejných úložišť není přihlášení potřeba.

## Otevření z obrazovky

1. Otevřete <https://docs.lunascape.org/>.
2. Na panelu nástrojů stiskněte [Otevřít dokumenty] (ikona složky).
3. Do pole [Zadat repozitář] zadejte úložiště a stiskněte [Otevřít].
   Když jste přihlášeni ke GitHubu, můžete také vybrat ze seznamu v části [Vybrat z dostupných repozitářů].

> **Tip**
>
> - Ikona GitHubu vedle otevře dokument, který právě čtete, na github.com. Neslouží k otevírání dokumentů.

## Otevření pomocí URL

Adresa uvádí úložiště a umístění dokumentu ve stejném pořadí. Cesta je umístěním uvnitř úložiště, takže pořadí odpovídá adrese na GitHubu.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Zadání | Zápis |
|---|---|
| Pouze úložiště (výchozí větev) | `/github/owner/repo` |
| Dokument uvnitř úložiště | `/github/owner/repo/docs/01-product/vision.md` |
| Určení větve nebo značky | na konec připojte `?ref=v1.2.0` |

Při přechodu na jinou stránku se změní i adresa. Stisknutím [Sdílet tento dokument] na panelu nástrojů předáte odkaz na stránku, kterou právě čtete. Funguje i [Zpět] a [Vpřed] v prohlížeči.

Dřívější zápis `?source=` lze otevřít i nadále. Po otevření se přepíše na nový tvar.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Poznámka**
>
> - Bez přihlášení platí omezení využití GitHub API (60 požadavků za hodinu). U úložišť s mnoha dokumenty nebo při opakovaném čtení použijte [Přihlásit se přes GitHub].
> - Názvy větví obsahující `/` (například `feature/xxx`) lze zadat pomocí `?ref=` ve výše uvedeném tvaru adresy. V zápisu `?source=` je zapsat nelze.
> - Dokumenty se načítají s oprávněními čtenáře na GitHubu. Komu chybí oprávnění ke čtení, ten je neuvidí.

## Otevření dokumentů v místní složce

Na panelu nástrojů stiskněte [Otevřít dokumenty] a pod seznamem zvolte [Otevřít dokumenty z místní složky]; poté vyberte složku ve svém zařízení. Soubory se zpracovávají uvnitř prohlížeče a nikam se neodesílají. Funkce je dostupná v prohlížečích, které podporují výběr složky (Chrome, Edge a další).

## Související témata

- [Čtení neveřejného úložiště](private-repository.md)
- [Webová verze nejde otevřít nebo se nelze přihlásit](../07-troubleshooting/web.md)
