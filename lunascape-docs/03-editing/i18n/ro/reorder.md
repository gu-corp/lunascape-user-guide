# Modificarea ordinii documentelor

Ordinea afișată în INDEX poate fi modificată prin tragere și plasare sau de la tastatură. Ordinea modificată se salvează în front matter-ul documentului, ca `navigation.order`.

## Reordonarea prin tragere și plasare

1. Trageți un document sau un folder în INDEX.
2. Plasați-l înainte sau după un element de pe același nivel ori peste un folder.
   În cadrul aceluiași nivel se schimbă ordinea. Dacă îl plasați peste alt folder, elementul se mută în acel folder.

## Reordonarea de la tastatură sau din meniu

- Plasați focalizarea pe un element din INDEX și apăsați `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Alegeți [Mută mai sus] / [Mută mai jos] din meniul elementului.

## Ce se salvează

- La reordonarea în cadrul aceluiași nivel se actualizează `navigation.order` din front matter-ul documentului canonic. În cazul unui folder, valoarea se scrie în fișierul `README.md` al folderului. Dacă folderul nu are `README.md`, se creează un `README.md` care conține numai front matter.
- La mutarea într-un alt folder, documentul canonic și traducerile corespunzătoare se mută împreună. Înainte de mutare se afișează o confirmare privind efectul asupra legăturilor relative.
- Nu se efectuează pregătirea pentru comitere (staging) și nici comiterea în Git.

> **Notă**
>
> - Reordonarea nu este disponibilă în timpul filtrării, în timpul editării unui document și într-un spațiu de lucru care nu este de încredere.
> - Mesajul „INDEX a fost actualizat” apare imediat după aplicarea unei alte modificări. Repetați operațiunea.
> - Pagina de start nu poate fi mutată în alt folder.

> **Sugestie**
>
> Dacă atribuiți valori `navigation.order` din 100 în 100, precum 100, 200, 300, este mai ușor să inserați documente între ele ulterior. Pentru detalii, consultați [Configurarea informațiilor de navigare](../04-document-tools/navigation-metadata.md).

## Subiecte conexe

- [Crearea și organizarea documentelor și folderelor](organize.md)
- [Configurarea informațiilor de navigare](../04-document-tools/navigation-metadata.md)
