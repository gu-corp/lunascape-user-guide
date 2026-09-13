# Crearea primelor documente

Într-un proiect care nu are încă un folder de documentație, puteți crea un prim set de documente din paleta de comenzi.

1. Deschideți folderul proiectului în VS Code și acordați încredere spațiului de lucru.
2. Din paleta de comenzi (`⇧⌘P` / `Ctrl+Shift+P`), executați „Lunascape Docs: Creează documentație dintr-un șablon”.
   Dacă spațiul de lucru conține mai multe foldere, alegeți spațiul de lucru în care se face crearea.
3. Alegeți structura de creat.
   - [Document de o pagină]: structura minimă, doar `README.md`. Potrivită pentru o specificație scurtă, pentru notițe sau pentru un document explicativ de sine stătător.
   - [Set de documentație]: creează o pagină principală și paginile de intrare pentru `specification/` (specificație), `manual/` (manual) și `help/` (ajutor).
4. Introduceți titlul documentației. Se folosește pentru README și pentru titlurile fiecărui document.
5. Introduceți folderul de documentație de creat. Calea este relativă la spațiul de lucru, iar valoarea implicită este `docs`.
6. Verificați lista fișierelor care vor fi create și apăsați [Creează].
   La terminarea creării, noul `README.md` se deschide în vizualizator.

> **Notă**
>
> - Fișierele existente nu sunt niciodată suprascrise. Dacă fie și un singur fișier dintre cele de creat există deja, nu se creează nimic, iar operația se oprește.
> - Crearea nu este posibilă într-un spațiu de lucru fără încredere.

> **Sfat**
>
> - Dacă aveți deja un folder de documentație, acest pas nu este necesar. Treceți la [Operații de bază](../02-reading/README.md).
> - Pe măsură ce documentația crește, puteți adăuga documente unul câte unul, alegând un șablon din fila [Creează] a Instrumentelor pentru documente.

## Subiecte conexe

- [Crearea unui document dintr-un șablon](../04-document-tools/templates.md)
- [Rădăcina documentației și convențiile de fișiere](../04-document-tools/structure.md)
