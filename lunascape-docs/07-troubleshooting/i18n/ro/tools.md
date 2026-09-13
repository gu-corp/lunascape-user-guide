# Verificarea, crearea sau traducerea nu funcționează

## Verificare

### Se afișează „docs-lint nu este disponibil"

- Mediul de execuție docs-lint nu este inclus în extensie sau configurația are o problemă. Reinstalați extensia.
- „Pentru a încărca în siguranță pachetul local și configurația, acordați încredere acestui spațiu de lucru în VS Code": pentru a folosi un Standard Pack local este necesar un spațiu de lucru de încredere.

### Rezultatul rămâne la „necesită revalidare"

Modificarea unui document sau a unei setări anulează rezultatul anterior. Apăsați din nou [Verifică rădăcina documentației]. Modificările nesalvate nu sunt luate în considerare.

### Apăsarea unei observații nu deschide nimic

Observațiile pentru „întreaga rădăcină a documentației" nu sunt legate de un anumit document și nu au o poziție. Verificați documentele indicate în conținutul observației.

### Regulile nu pot fi salvate

- Este necesar un spațiu de lucru de încredere.
- „Configurația de lint a fost modificată de altă operațiune": fișierul `docs-lint.config.json` a fost modificat din exterior. Reîncărcați starea cea mai recentă și încercați din nou.
- Fișierele de configurare care sunt legături simbolice sau care se află în afara rădăcinii documentației nu pot fi editate.

## Creare dintr-un șablon

- „Previzualizarea șablonului a expirat" / „Datele introduse au fost modificate": apăsați din nou [Previzualizare] înainte de creare.
- „Documentul de destinație există deja": fișierele existente nu sunt suprascrise. Indicați o altă destinație.
- Destinația are nevoie de o cale relativă la rădăcina documentației și de extensia `.md` / `.mdx`. Sub `i18n` nu se poate crea nimic.
- „Pentru a crea documente, acordați încredere spațiului de lucru": acordați încredere spațiului de lucru în VS Code.

<!-- ai-only:start -->
## Traducere

### Butoanele de traducere nu pot fi apăsate

- „Traducerea cu AI nu este activată pentru această rădăcină a documentației": setați `translation.enabled` pe `true` în `lunascape-docs.json`.
- „Limba implicită a proiectului nu este setată": salvați limba implicită conform [Modificarea setărilor de afișare](../02-reading/display-settings.md).
- „Adăugați limba țintă la limbile acceptate": adăugați limba de destinație în `locales`.
- „Nu a fost găsit documentul canonic de tradus": este deschisă o pagină tradusă. Treceți la pagina în limba implicită.
- Traducerea în bloc nu este disponibilă când un folder este deschis temporar. Puneți un fișier `lunascape-docs.json` în acel folder pentru a-l transforma în rădăcină a documentației.

### Propunerea este respinsă sau trebuie refăcută

- „Documentul canonic a fost modificat. Refaceți propunerea de traducere": documentul canonic sau destinația s-au modificat după generarea propunerii. Traduceți din nou.
- Un răspuns al modelului de limbaj din care lipsesc identificatori sau cod ce trebuie protejate nu este acceptat. Conținutul răspunsului poate fi consultat în panoul de ieșire „Lunascape Docs Traducere".
- „Traducerea în bloc acceptă cel mult 1000 de documente pe rulare": împărțiți domeniul pe foldere sau printr-o selecție explicită.
<!-- ai-only:end -->

## Subiecte conexe

- [Verificarea documentelor](../04-document-tools/check.md)
- [Crearea unui document dintr-un șablon](../04-document-tools/templates.md)
- [Predarea lucrului către un AI](../05-ai/README.md)
