# Nastavení navigačních metadat

Název a pořadí zobrazené v INDEX se zapisují do YAML front matter každého dokumentu. Dokumenty se zobrazí i bez nich – použije se nadpis (H1) a pořadí podle názvu souboru.

## Název a pořadí dokumentu

Na začátek dokumentu napište následující.

```yaml
---
navigation:
  title: Začínáme
  order: 200
---
```

| Položka | Význam |
|---|---|
| `navigation.title` | Název zobrazený v INDEX. Když je vynechán, použije se H1 a poté název souboru |
| `navigation.order` | Celé číslo, které určuje pořadí, vzestupně. Když je vynecháno, platí stabilní výchozí pořadí (podle názvu souboru) |

> **Tip**
>
> - Hodnoty `order` zadávejte po stovkách, například 100, 200, 300, abyste mezi ně mohli později vložit třeba 150.
> - Chybějící, neplatné ani duplicitní hodnoty `order` dokument nikdy neskryjí.
> - Při změně pořadí v INDEX se `navigation.order` zapíše za vás; není třeba ho psát ručně.

## Název a pořadí složky

Název a pořadí složky patří do front matter jejího souboru `README.md` (nebo `index.md`, pokud README chybí). Titulní stránka nemusí mít žádný obsah.

```yaml
---
navigation:
  title: Plánování produktu
  order: 100
---
```

Složka bez titulní stránky používá svůj název a výchozí pořadí. Když to změna názvu nebo změna pořadí v INDEX vyžaduje, vytvoří se `README.md` obsahující pouze front matter. Samotné prohlížení nikdy soubor nevytvoří.

## Zacházení v překladech

- Pořadí a roli složky (titulní stránka, nebo pouze konfigurace) určuje výhradně dokument ve výchozím jazyce.
- Překlad může přepsat pouze `navigation.title`. Když má originál obsah, použije se jako název i H1 překladu.
- Samotný překlad nikdy nepřidá stránku.

## Řazení a sbalení podřízených položek

`navigation.children.sort` a `navigation.children.defaultCollapsed` na titulní stránce složky slouží k tomu, jak se řadí přímé podřízené položky a zda mají být zpočátku sbalené. Jejich čtení a úprava ve VS Code se plánují.

## Související témata

- [Změna pořadí dokumentů](../03-editing/reorder.md)
- [Kořeny dokumentace a konvence souborů](structure.md)
