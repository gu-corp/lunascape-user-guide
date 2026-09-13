# Editarea unui document

Documentele pot fi editate direct în vizualizator. Ecranul de editare are o vizualizare vizuală, în care editezi ceea ce vezi, și o vizualizare a sursei Markdown; un singur buton comută între ele.

## Începerea editării

Apasă oricare dintre următoarele. Toate deschid același ecran de editare.

- [Editează], în dreapta jos a documentului
- [⋯] (Alte acțiuni), în dreapta sus a documentului → [Editează]
- Meniul elementului din INDEX → [Editează]

## Editarea

1. Editează textul direct.
   Bara de instrumente din partea de sus a ecranului de editare oferă formatul de paragraf (text, titluri 1–4, citat, cod), [Aldin], [Cursiv], [Listă cu marcatori], [Listă numerotată], [Link], [Inserează un tabel], [Lățimea imaginii], [Anulează] și [Refă].
2. Pentru a edita direct sursa Markdown, apasă [Markdown].
   Apasă din nou pentru a reveni la vizualizarea vizuală. Vizualizarea folosită ultima dată este reținută și restabilită data viitoare când apeși [Editează].
3. Apasă [Salvează].
   Fișierul Markdown este scris și se revine la modul de citire. Pentru a renunța, apasă [Anulează].

> **Notă**
>
> - Salvarea doar scrie în fișier. Pregătirea (staging) și comiterea în Git nu se fac automat.
> - Formulele matematice și diagramele precum Mermaid, TikZ și Vega-Lite sunt afișate randate în vizualizarea vizuală. Pentru a le modifica conținutul, comută la [Markdown].
> - Documentele care conțin sintaxă specifică MDX (componente, `import` și altele) se editează doar în vizualizarea Markdown, pentru a păstra acea sintaxă.
> - Blocul front matter (setările dintre liniile `---` de la început) se păstrează și atunci când editezi în vizualizarea vizuală.

> **Sfat**
>
> - [Deschide în VS Code] deschide fișierul în editorul de text obișnuit. Dacă salvezi acolo, afișarea din vizualizator se actualizează automat.
> - Dacă nu vrei să se afișeze butonul [Editează], dezactivează [Butonul de editare] din [Setări de afișare]. Pentru a-l ascunde în întregul proiect, setează `editor.showEditButton` pe `false` în `lunascape-docs.json`.
> - Vizualizarea implicită la deschidere (vizuală sau Markdown) se schimbă din setarea `lunascapeDocEditor.editor.defaultMode` sau din `editor.defaultMode` în `lunascape-docs.json`.

## Subiecte conexe

- [Crearea și organizarea documentelor și folderelor](organize.md)
- [Ajustarea dimensiunii imaginilor](images.md)
- [Scrierea formulelor matematice](math.md)
- [Scrierea diagramelor și a graficelor](diagrams.md)
