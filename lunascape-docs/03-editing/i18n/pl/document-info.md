# Wyświetlanie informacji o dokumencie

Tabela zarządzania dokumentem umieszczona na początku dokumentu (identyfikator dokumentu, wersja, data aktualizacji, stan itd.) jest podczas czytania wyświetlana zbiorczo jako niewielki wiersz „Informacje o dokumencie". Sam kod Markdown pozostaje zwykłą tabelą, więc można go normalnie czytać także w serwisie GitHub.

## Warunki wyświetlania

Bezpośrednio po nagłówku (H1) umieść dwukolumnową tabelę taką jak poniższa.

```markdown
# Wymagania funkcjonalne

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Warunkiem jest obecność wiersza z identyfikatorem dokumentu oraz kilku pól zarządzania.
- Rozpoznawana jest również tabela umieszczona pod nagłówkiem `## 文書管理` lub `## Document information`.
- Tabele znajdujące się w środku tekstu oraz zwykłe tabele typu „element/wartość" nie są konwertowane.

## Sposób wyświetlania

- Podczas czytania w niewielkim rozmiarze wyświetlane są tylko stan i data aktualizacji.
- Naciśnij wiersz, aby wyświetlić wszystkie pola.
- Podczas drukowania wyświetlane są wszystkie pola.
- W widoku edycji tabela jest wyświetlana jako zwykła tabela i można ją tak edytować.

> **Wskazówka**
>
> Aby zamiast zwijania zawsze wyświetlać tabelę, wyłącz opcję [Zwiń informacje o dokumencie] w [Ustawienia widoku].

## Powiązane tematy

- [Edytowanie dokumentu](README.md)
- [Zmiana ustawień widoku](../02-reading/display-settings.md)
