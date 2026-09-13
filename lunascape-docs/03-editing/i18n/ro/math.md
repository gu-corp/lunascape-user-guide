# Scrierea formulelor matematice

Formulele matematice se scriu în notația TeX și se redau pe dispozitiv cu KaTeX. Nu se folosește rețeaua.

## Notația

| Tip | Delimitatori | Exemplu |
|---|---|---|
| Formulă în linie (în interiorul frazei) | `$...$` sau `\(...\)` | `Relația dintre masă și energie este $E = mc^2$.` |
| Formulă pe rând propriu | `$$...$$` sau `\[...\]` | Vedeți mai jos |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Nu sunt necesare spații în jurul delimitatorilor. Formula este recunoscută și când este alipită de textul japonez, ca în `値は$V=-H$である`.
- Un `$` aflat în cod în linie sau într-un bloc de cod nu este tratat ca formulă și este afișat ca atare.
- Textul care seamănă cu o sumă de bani, precum `$5 and $10`, nu este tratat ca formulă.

## Editarea

În afișarea vizuală, formulele apar redate. Pentru a le modifica, apăsați [Markdown] în ecranul de editare și editați sursa. La salvarea din afișarea vizuală, sursa TeX și forma inițială a delimitatorilor (`$` sau `\(`) se păstrează neschimbate.

> **Notă**
>
> - Din motive de siguranță, KaTeX rulează cu `trust: false` și limitează dimensiunea (`maxSize: 50`) și numărul de expandări de macrocomenzi (`maxExpand: 1000`). Formulele care depășesc aceste limite nu sunt redate.
> - Un `tikzpicture` scris în interiorul `$$...$$` sau `\[...\]` într-un document existent este recunoscut ca diagramă TikZ, nu ca formulă matematică.

## Subiecte conexe

- [Scrierea diagramelor și a graficelor](diagrams.md)
- [Diagramele, formulele matematice sau imaginile nu se afișează](../07-troubleshooting/rendering.md)
