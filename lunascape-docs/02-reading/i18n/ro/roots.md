# Comutarea între rădăcinile documentației

Rădăcina documentației este folderul de nivel superior al unui set de documente. INDEX, filtrarea, verificarea și traducerea funcționează toate la nivel de rădăcină a documentației.

## Cum este găsită rădăcina documentației

Lunascape Docs urcă din fișierul Markdown deschis prin folderele părinte și folosește ca rădăcină a documentației cel mai apropiat folder care corespunde uneia dintre situațiile următoare.

- Un folder care conține `lunascape-docs.json` (numele folderului nu contează)
- Un folder numit `docs` (puteți adăuga alte nume din setarea `lunascapeDocEditor.rootDirectoryNames`)

Când executați „Lunascape Docs: Deschide vizualizatorul de specificații”, se deschide rădăcina documentației din setarea `lunascapeDocEditor.root` (implicit `docs`).

## Comutarea la o altă rădăcină a documentației

Când spațiul de lucru conține mai multe rădăcini ale documentației, numele rădăcinii din capătul din stânga al barei de instrumente devine o listă derulantă.

1. Apăsați numele rădăcinii documentației din capătul din stânga al barei de instrumente.
2. Alegeți o rădăcină a documentației din listă.
   Se afișează pagina de start a rădăcinii alese, iar INDEX comută.

> **Sfat**
>
> Numele afișate în listă se stabilesc în ordinea următoare. Ele nu se schimbă atunci când comutați limba interfeței.
>
> 1. `title` din `lunascape-docs.json`
> 2. `navigation.title` din `README.md` al rădăcinii, iar în lipsa acestuia titlul H1
> 3. `navigation.title` din `index.md` al rădăcinii, iar în lipsa acestuia titlul H1
> 4. Numele folderului (pentru un folder `docs` standard, numele folderului părinte)

## Deschiderea unui fișier Markdown din afara unei rădăcini a documentației

Când deschideți un fișier Markdown care nu se află într-o rădăcină a documentației, folderul acelui fișier se afișează ca rădăcină temporară a documentației. În INDEX apar fișierele Markdown din acel folder și din subfolderele sale.

- Apăsați [La folderul superior] din bara de instrumente pentru a extinde domeniul afișat până la folderul părinte din spațiul de lucru.
- În această vizualizare, setările de limbă ale proiectului și traducerea în bloc nu sunt disponibile. Puneți un fișier `lunascape-docs.json` în acel folder pentru a-l transforma în rădăcină a documentației și a le activa.

## Deschiderea permanentă a unei anumite rădăcini a documentației

Dacă setați `lunascapeDocEditor.rootMode` la `fixed`, se deschide întotdeauna rădăcina documentației din `lunascapeDocEditor.root`, indiferent de fișierul Markdown pe care îl deschideți.

## Subiecte asociate

- [Rădăcinile documentației și convențiile pentru fișiere](../04-document-tools/structure.md)
- [Configurarea proiectului](../04-document-tools/project-configuration.md)
- [Lista setărilor VS Code](../08-reference/settings.md)
