# Postavljanje navigacijskih podataka

Naziv i redoslijed koji se prikazuju u INDEX-u upisuju se u YAML front matter svakog dokumenta. Dokumenti se prikazuju i bez toga, pri čemu se koriste naslov (H1) i redoslijed po nazivu datoteke.

## Naziv i redoslijed dokumenta

Na početak dokumenta upišite sljedeće.

```yaml
---
navigation:
  title: Početak rada
  order: 200
---
```

| Stavka | Značenje |
|---|---|
| `navigation.title` | Naziv koji se prikazuje u INDEX-u. Ako se izostavi, koristi se H1, a ako ni njega nema, naziv datoteke |
| `navigation.order` | Cijeli broj koji određuje redoslijed, uzlazno. Ako se izostavi, primjenjuje se stabilan zadani redoslijed (po nazivu datoteke) |

> **Savjet**
>
> - Vrijednosti za `order` dodjeljujte u koracima od 100, primjerice 100, 200, 300, kako biste kasnije mogli umetnuti 150 između njih.
> - Nedostajuće, neispravne ili ponovljene vrijednosti `order` nikada ne skrivaju dokument.
> - Promjenom redoslijeda u INDEX-u `navigation.order` upisuje se automatski; nije ga potrebno pisati ručno.

## Naziv i redoslijed mape

Naziv i redoslijed mape nalaze se u front matteru njezine datoteke `README.md` (ili `index.md` ako README ne postoji). Naslovna stranica ne mora imati sadržaj.

```yaml
---
navigation:
  title: Planiranje proizvoda
  order: 100
---
```

Mapa bez naslovne stranice prikazuje se s nazivom mape i zadanim redoslijedom. Kada je to potrebno zbog promjene naslova ili redoslijeda u INDEX-u, stvara se `README.md` koji sadrži samo front matter. Samo čitanje nikada ne stvara datoteku.

## Postupanje s prijevodima

- Redoslijed i ulogu mape (naslovna stranica ili samo postavke) određuje isključivo dokument na zadanom jeziku.
- Prijevod može nadjačati samo `navigation.title`. Kada izvornik ima sadržaj, kao naziv se koristi i H1 prijevoda.
- Prijevod sam po sebi nikada ne dodaje stranicu.

## Redoslijed i sažimanje podstavki

Na naslovnoj stranici mape definirani su `navigation.children.sort` i `navigation.children.defaultCollapsed`, kojima se određuje redoslijed izravnih podstavki i njihovo početno stanje sažetosti. Čitanje i uređivanje u VS Code planirani su za budućnost.

## Povezane teme

- [Promjena redoslijeda dokumenata](../03-editing/reorder.md)
- [Korijen dokumentacije i pravila za datoteke](structure.md)
