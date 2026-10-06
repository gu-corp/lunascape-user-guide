# Editarea unui document

Documentele pot fi editate direct în vizualizator. Ecranul de editare are o „vizualizare vizuală”, unde editezi ceea ce vezi, și o „vizualizare a sursei Markdown”; un singur buton comută între ele.

## Începe editarea

Apasă oricare dintre următoarele. Toate deschid același ecran de editare.

- [Editează] din colțul din dreapta jos al documentului
- [⋯] (Alte acțiuni) din colțul din dreapta sus al documentului → [Editează]
- Meniul elementului din INDEX → [Editează]

## Editează

1. Editează direct textul.
   În bara de instrumente din partea de sus a ecranului de editare poți folosi formatul de paragraf (text, titluri 1–4, citat, cod), [Aldin], [Cursiv], [Listă cu marcatori], [Listă numerotată], [Link], [Inserează un tabel], [Lățimea imaginii], [Anulează] și [Refă].
2. Când vrei să editezi direct sursa Markdown, apasă [Markdown].
   Apasă din nou pentru a reveni la vizualizarea vizuală. Ultima vizualizare folosită este memorată și restabilită data următoare când apeși [Editează].
3. Apasă [Salvează] (poți salva și cu Ctrl+S / ⌘S).
   Se scrie în fișierul Markdown și se revine la vizualizarea de citire. Pentru a renunța la editare și a reveni la ultimul conținut salvat, apasă [Discard edits].

## Începe întotdeauna din ecranul de editare (modul de editare)

Apasă [Edit mode] din bara de instrumente pentru a-l activa: de atunci înainte, de fiecare dată când deschizi un document, pornești din ecranul de editare. Folosește-l atunci când scrii continuu, ca într-un carnet de notițe.

- Cât timp este activat, apăsarea [Salvează] nu închide ecranul de editare. [Discard edits] revine la ultimul conținut salvat și păstrează ecranul de editare deschis.
- Apasă din nou pentru a-l dezactiva și a reveni la vizualizarea de citire. Activarea/dezactivarea este memorată pentru fiecare utilizator.
- Nu este afișat pentru o rădăcină a documentației în care nu se poate scrie (de exemplu o sursă GitHub doar pentru citire).

## Editările nesalvate

Editările pe care nu le-ai salvat sunt păstrate automat pe acest dispozitiv. Nu se pierd nici dacă treci la alt document, nici dacă închizi fila sau fereastra.

- [Unsaved] din ecranul de editare arată că există diferențe față de ultimul conținut salvat.
- Data următoare când deschizi același document, se reia din editările păstrate și te anunță despre asta. Dacă documentul original a fost actualizat între timp, te anunță și despre acest lucru. Cu [Discard edits] poți reveni la conținutul cel mai recent.
- Editările păstrate dispar cu [Salvează] sau cu [Discard edits]. Deoarece nu au fost salvate, ele nu apar în Git și nici printre ciorne.

> **Notă**
>
> - Salvarea doar scrie fișierul. Pregătirea (staging) și confirmarea (commit) în Git nu se fac niciodată automat.
> - Diagramele precum formulele matematice, Mermaid, TikZ și Vega-Lite sunt afișate ca rezultat randat în vizualizarea vizuală. Pentru a le modifica conținutul, comută la [Markdown].
> - Documentele care conțin sintaxă specifică MDX (componente, `import` și altele) se editează doar în vizualizarea Markdown, pentru a păstra sintaxa.
> - Front matter-ul (setările încadrate de liniile `---` de la început) se păstrează chiar dacă editezi în vizualizarea vizuală.

> **Sfat**
>
> - [Deschide în VS Code] deschide fișierul în editorul de text obișnuit. Când salvezi în editorul de text, afișarea din vizualizator se actualizează automat.
> - Când nu vrei să apară butonul [Editează], dezactivează [Butonul de editare] din [Setări de afișare]. Pentru a-l ascunde în întregul proiect, setează `editor.showEditButton` la `false` în `lunascape-docs.json`.
> - Vizualizarea implicită de la prima deschidere (vizuală sau Markdown) poate fi schimbată din setarea `lunascapeDocEditor.editor.defaultMode` sau din `editor.defaultMode` în `lunascape-docs.json`.

## Vezi și

- [Crearea și organizarea documentelor și folderelor](organize.md)
- [Ajustarea dimensiunii imaginilor](images.md)
- [Scrierea formulelor matematice](math.md)
- [Realizarea diagramelor și graficelor](diagrams.md)
