# Verificarea documentelor

docs-lint verifică structura titlurilor, legăturile întrerupte, documentele și capitolele obligatorii lipsă, neconcordanțele de terminologie, coerența ID-urilor de cerință și altele. Verificarea se face întotdeauna asupra întregii rădăcini a documentației.

## Executarea unei verificări

1. Apăsați [Instrumente pentru documente] din bara de instrumente și deschideți fila [Verificare].
2. Apăsați [Verifică rădăcina documentației].
   Puteți executa verificarea și din paleta de comenzi, cu „Lunascape Docs: Verifică rădăcina documentației".
3. Consultați lista rezultatelor.

## Citirea rezultatelor

- Cu [Acest document] / [Toate], deasupra listei, schimbați domeniul afișat. Domeniul verificării în sine este întotdeauna întreaga rădăcină a documentației.
- Semnalările au patru niveluri: „eroare", „avertisment", „informație" și „sugestie". Pe [Instrumente pentru documente], în bara de instrumente, se afișează numărul de erori și de avertismente.
- Dacă apăsați o semnalare, se deschide în editorul VS Code poziția corespunzătoare din sursa Markdown.
- Semnalările care privesc întreaga rădăcină a documentației (de exemplu lipsa unui document de test) apar ca elemente „Întreaga rădăcină a documentației" și nu au o poziție.
- Aceleași semnalări apar și în panoul „Probleme" din VS Code.

## Ce se verifică

Dacă apăsați [Verifică și modifică regulile], se afișează lista verificărilor active și scopul fiecăreia. Principalele elemente sunt următoarele.

| Element | Descriere |
|---|---|
| Structura titlurilor | Există un singur H1 și nivelurile de titlu nu sar peste trepte |
| Legături interne | Documentele țintă există și nu ies în afara rădăcinii documentației |
| Limbajul blocurilor de cod | Blocurile de cod au indicat un nume de limbaj |
| Folderele și documentele necesare | Există folderele și documentele cerute de profilul Standard Pack |
| Capitolele necesare într-un document | Fiecare tip de document are capitolele necesare |
| Uniformitatea terminologiei | Sunt detectate expresiile de evitat și se recomandă termenii preferați |
| Denumirea și duplicarea ID-urilor de cerință | ID-urile de cerință respectă regula de denumire și nu sunt definite de două ori |
| Coerența referințelor la ID-urile de cerință | ID-urile de cerință la care se face referire din proiectare, teste sau tabelele de stare există cu adevărat |
| Corespondența dintre cerințe și teste | La ID-urile de cerință se face referire din documentele de test |

Elementele care devin active sunt stabilite de Standard Pack și de profilul alese în `lunascape-docs.json`, precum și de `docs-lint.config.json`.

> **Notă**
>
> - Dacă modificați un document sau o setare, rezultatul anterior devine „necesită reverificare". Nimic nu este considerat automat trecut. Apăsați din nou [Verifică rădăcina documentației].
> - Modificările nesalvate nu sunt luate în calcul la verificare. Salvați mai întâi.
> - Verificarea se execută determinist, pe calculatorul dumneavoastră. Rezultatele evaluărilor AI sau ale traducerilor nu se amestecă niciodată în rezultatele verificării.

## Subiecte conexe

- [Modificarea regulilor de verificare](rules.md)
- [Configurarea proiectului](project-configuration.md)
- [Verificarea, crearea sau traducerea nu funcționează](../07-troubleshooting/tools.md)
