# Vise dokumentopplysninger

En «dokumentkontrolltabell» øverst i et dokument (en tabell med dokument-ID, versjon, oppdateringsdato, status og så videre) vises ved lesing samlet i en kompakt «dokumentopplysninger»-rad. Selve Markdown-en forblir en vanlig tabell, så den leses også som normalt på GitHub.

## Vilkår

Plasser en tokolonnetabell som følgende rett etter overskriften (H1).

```markdown
# Funksjonelle krav

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Tabellen må inneholde en dokument-ID-rad og flere administrasjonsfelt.
- En tabell under en overskrift med `## 文書管理` eller `## Document information` gjenkjennes også.
- Tabeller midt i teksten, og vanlige «element/innhold»-tabeller, blir ikke konvertert.

## Hvordan det vises

- Ved lesing vises bare status og oppdateringsdato i liten skrift.
- Trykk på raden for å vise alle feltene.
- Ved utskrift vises alle feltene.
- I redigeringsvisningen vises tabellen som en vanlig tabell og kan redigeres som sådan.

> **Tips**
>
> Hvis du alltid vil vise tabellen i stedet for å slå den sammen, slår du av [Slå sammen dokumentopplysningene] i [Visningsinnstillinger].

## Relaterte emner

- [Redigere et dokument](README.md)
- [Endre visningsinnstillinger](../02-reading/display-settings.md)
