# Nu se poate edita, salva sau reordona

## Nu există butonul [Editează]

- [Butonul de editare] din [Setări de afișare] este dezactivat. Activează-l sau folosește [⋯] → [Editează] din colțul din dreapta sus al documentului ori meniul elementului din INDEX → [Editează].
- Același lucru se întâmplă când `editor.showEditButton` din `lunascape-docs.json` este `false`.
- Cât timp este afișat Ajutorul, editarea nu este disponibilă. Închide Ajutorul.

## Nu se poate trece la vizualizarea vizuală

„Acest document conține sintaxă MDX, de aceea nu se poate trece la ecranul de editare obișnuit”: documentele care conțin sintaxă specifică MDX (componente, `import` și altele) se editează doar în vizualizarea Markdown, pentru a păstra sintaxa.

## Nu se pot edita direct formulele matematice sau diagramele

Vizualizarea vizuală afișează rezultatul randat. Apasă [Markdown] în ecranul de editare și editează sursa.

## Nu se poate reordona sau trage cu mouse-ul

- Reordonarea nu este disponibilă în timpul filtrării, în timpul editării unui document și cât timp se procesează o altă operație în INDEX.
- Când spațiul de lucru nu este de încredere, acțiunile de creare, organizare și ștergere nu sunt disponibile. Marchează spațiul de lucru ca fiind de încredere în VS Code.
- „INDEX a fost actualizat. Trage din nou.”: tocmai a fost aplicată o altă modificare. Repetă operația.
- Pagina de start (fișierul `README.md` din rădăcină) nu poate fi mutată.

## Se afișează „Există modificări nesalvate”

Fișierul vizat este în curs de editare în editorul VS Code. Salvează sau renunță la modificări, apoi încearcă din nou.

## Nu se poate redenumi

Următoarele nume nu pot fi folosite.

- Nume care încep cu `.`, `i18n` și numele rezervate de Windows (`CON` și altele)
- Nume care se termină cu punct sau spațiu și nume care conțin caractere de control ori caractere nepermise în numele de fișiere
- Nume care există deja în același folder (inclusiv nume care diferă doar prin literele mari și mici)
- Nume de documente fără extensie Markdown

## Am salvat, dar modificările nu apar în Git sau nu sunt comise

Lunascape Docs doar scrie în fișier; nu execută operații de staging sau de commit în Git. Verifică în vizualizarea Control sursă din VS Code și execută commit dacă este necesar.

## Subiecte conexe

- [Editarea unui document](../03-editing/README.md)
- [Crearea și organizarea documentelor și folderelor](../03-editing/organize.md)
- [Schimbarea ordinii documentelor](../03-editing/reorder.md)
