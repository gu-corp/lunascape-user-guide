# Zobrazení údajů o dokumentu

„Tabulka správy dokumentu" umístěná na začátku dokumentu (tabulka s ID dokumentu, verzí, datem aktualizace, stavem apod.) se při čtení sbalí do kompaktního řádku „údaje o dokumentu". Samotný Markdown zůstává běžnou tabulkou, takže se dá bez problémů číst i na GitHubu.

## Podmínky pro zobrazení

Bezprostředně za nadpis (H1) umístěte dvousloupcovou tabulku, jako je následující.

```markdown
# Definice funkčních požadavků

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Podmínkou je řádek s ID dokumentu a několik správních položek.
- Cílem je i tabulka umístěná pod nadpisem `## 文書管理` nebo `## Document information`.
- Tabulky uprostřed textu a běžné tabulky typu „položka/hodnota" se nepřevádějí.

## Jak se zobrazuje

- Při čtení se malým písmem zobrazuje pouze stav a datum aktualizace.
- Stisknutím řádku se zobrazí všechny položky.
- Při tisku se zobrazí všechny položky.
- V editoru se zobrazuje jako běžná tabulka a lze ji tak upravovat.

> **Tip**
>
> Chcete-li tabulku vždy zobrazovat místo sbalení, vypněte v [Nastavení zobrazení] možnost [Sbalit údaje o dokumentu].

## Související témata

- [Úprava dokumentu](README.md)
- [Změna nastavení zobrazení](../02-reading/display-settings.md)
