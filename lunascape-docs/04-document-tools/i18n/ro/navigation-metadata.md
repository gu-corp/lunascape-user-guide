# Configurarea informațiilor de navigare

Numele și ordinea afișate în INDEX se scriu în YAML front matter din fiecare document. Documentele se afișează și fără acestea, folosind titlul (H1) și ordinea numelor de fișier.

## Numele și ordinea documentului

Scrieți următoarele la începutul documentului.

```yaml
---
navigation:
  title: Primii pași
  order: 200
---
```

| Câmp | Conținut |
|---|---|
| `navigation.title` | Numele afișat în INDEX. Dacă este omis, se folosește H1, iar în lipsa acestuia numele fișierului |
| `navigation.order` | Un număr întreg care stabilește ordinea, crescător. Dacă este omis, se aplică o ordine implicită stabilă (după numele fișierului) |

> **Sfat**
>
> - Atribuiți valorile `order` din 100 în 100, de exemplu 100, 200, 300, ca să puteți insera ulterior 150 între ele.
> - Valorile `order` lipsă, incorecte sau duplicate nu ascund niciodată un document.
> - Reordonarea în INDEX scrie automat `navigation.order`; nu este nevoie să îl scrieți de mână.

## Numele și ordinea folderului

Numele și ordinea unui folder aparțin front matter-ului din `README.md` al acestuia (sau din `index.md`, dacă nu există README). Pagina de deschidere nu are nevoie de conținut în corp.

```yaml
---
navigation:
  title: Planificarea produsului
  order: 100
---
```

Un folder fără pagină de deschidere se afișează cu numele folderului și cu ordinea implicită. Când o schimbare de titlu sau o reordonare în INDEX o cere, se creează un `README.md` care conține doar front matter. Simpla consultare nu creează niciodată un fișier.

## Tratarea în versiunile traduse

- Ordinea și rolul unui folder (pagină de deschidere sau doar configurare) sunt stabilite numai de documentul în limba implicită.
- O traducere poate suprascrie doar `navigation.title`. Când documentul canonic are conținut în corp, H1 al traducerii este folosit și el ca nume.
- O traducere de una singură nu adaugă niciodată o pagină.

## Ordinea și pliereaelementelor secundare

În pagina de deschidere a unui folder sunt definite `navigation.children.sort` și `navigation.children.defaultCollapsed`, pentru a stabili cum se ordonează elementele secundare directe și dacă acestea pornesc pliate. Citirea și editarea lor în VS Code urmează să fie acceptate.

## Subiecte conexe

- [Modificarea ordinii documentelor](../03-editing/reorder.md)
- [Rădăcina documentației și convențiile de fișiere](structure.md)
