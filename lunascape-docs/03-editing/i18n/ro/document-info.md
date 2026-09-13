# Afișarea informațiilor documentului

„Tabelul de gestiune a documentului" plasat la începutul documentului (tabelul cu ID-ul documentului, versiunea, data actualizării, starea și altele) este afișat la citire într-un rând compact, „Informațiile documentului". Markdown-ul rămâne un tabel obișnuit, așa că se citește la fel și pe GitHub.

## Condiții de afișare

Plasați imediat după titlu (H1) un tabel cu două coloane, ca cel de mai jos.

```markdown
# Cerințe funcționale

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Condiția este să existe rândul „文書ID" și mai multe câmpuri de gestiune.
- Este recunoscut și un tabel plasat sub un titlu `## 文書管理` sau `## Document information`.
- Tabelele aflate în mijlocul textului și tabelele obișnuite de tip „element/conținut" nu sunt convertite.

## Modul de afișare

- La citire se afișează cu caractere mici doar starea și data actualizării.
- Apăsați rândul pentru a afișa toate câmpurile.
- La tipărire se afișează toate câmpurile.
- În ecranul de editare apare ca tabel obișnuit și poate fi editat ca atare.

> **Sfat**
>
> Dacă doriți ca tabelul să fie afișat permanent, fără a fi restrâns, dezactivați [Restrânge informațiile documentului] din [Setări de afișare].

## Subiecte conexe

- [Editarea unui document](README.md)
- [Modificarea setărilor de afișare](../02-reading/display-settings.md)
