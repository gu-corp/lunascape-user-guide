# Prohlížení neveřejného úložiště

Dokumenty neveřejných úložišť můžete po přihlášení přes GitHub prohlížet pouze u těch úložišť, ke kterým máte oprávnění ke čtení. Lunascape Docs nikdy nemá vlastní účty ani oprávnění.

## Přihlaste se a otevřete

1. Otevřete <https://docs.lunascape.org/>.
   Když zadáte neveřejný dokument nebo dosud nejste přihlášeni, zobrazí se přihlašovací obrazovka.
2. Stiskněte [Přihlásit se přes GitHub].
   Ověřovací obrazovka GitHubu se otevře ve vyskakovacím okně.
3. Po přihlášení stiskněte na panelu nástrojů [Otevřít dokumenty] a v nabídce [Vybrat z dostupných repozitářů] zvolte úložiště, které chcete otevřít.

> **Tip**
>
> - Název přihlášeného účtu se zobrazuje na panelu nástrojů. Odtud lze provést i akce [Odhlásit se] a [Přihlásit se jiným účtem].
> - V seznamu se zobrazují ta úložiště účtů (organizací nebo osob), kde je nainstalována aplikace GitHub App „Lunascape Docs“ a ke kterým máte oprávnění ke čtení.

## Nastavení, které provádí vlastník úložiště

Pokud se dané úložiště v seznamu neobjeví, musí vlastník úložiště nebo správce organizace nainstalovat aplikaci GitHub App „Lunascape Docs“.

- Požadovaná oprávnění jsou Contents (čtení a zápis) a Pull requests (čtení a zápis). Čtení slouží k prohlížení, zápis k žádosti o publikování z webu (Pull Request). Lunascape Docs obsah dokumentů neukládá.
- Aplikace se instaluje na úroveň účtu (organizace nebo osoby). Nastavíte, zda se má vztahovat na „All repositories“ (což automaticky zahrnuje i úložiště vytvořená později), nebo jen na vybraná úložiště.

| Situace | Postup |
|---|---|
| Nové zavedení v organizaci nebo osobním účtu | Proveďte z [instalační stránky](https://github.com/apps/lunascape-docs/installations/new) |
| Přidání úložišť v organizaci, kde je již zavedeno | Nastavte v Settings organizace → GitHub Apps → Lunascape Docs → Configure → Repository access |

I když aplikaci nainstalujete pro celou organizaci, každý člen může prohlížet pouze ta úložiště, ke kterým má sám oprávnění ke čtení. Žádost o publikování může odeslat rovněž jen do úložišť, ke kterým má sám oprávnění k zápisu.

> **Tip**
> - Při nové instalaci se požadovaná oprávnění zobrazí v seznamu na instalační obrazovce a stisknutím „Install“ je odsouhlasíte. Žádná další akce není potřeba.
> - Organizaci, která aplikaci nainstalovala dříve, než přibylo nové oprávnění, přijde správcům potvrzovací e-mail a v horní části Settings organizace → GitHub Apps → Lunascape Docs → Configure se zobrazí tlačítko pro schválení. Dokud oprávnění neschválí, může v dané organizaci pouze prohlížet, a při odeslání žádosti o publikování se zobrazí „Je nutné udělit oprávnění k zápisu“.
> - Jaká oprávnění jsou právě v platnosti, zjistíte na téže obrazovce Configure. U osobního účtu je to Settings → Applications → Installed GitHub Apps.
> - Pokud jste dané úložiště omylem vyřadili nebo aplikaci odinstalovali, obnovíte původní stav opětovnou instalací z [instalační stránky](https://github.com/apps/lunascape-docs/installations/new). Zpráva o zamítnutí žádosti o publikování obsahuje odkaz na obrazovku pro nápravu.
> - Pokud na straně úložiště nechcete žádosti o publikování přijímat, zapište do `lunascape-docs.json` `"publish": { "enabled": false }`. Prohlížení zůstává i nadále dostupné.

## Související témata

- [Otevření úložiště GitHub](open-repository.md)
- [Webovou verzi nelze otevřít nebo se v ní nelze přihlásit](../07-troubleshooting/web.md)
