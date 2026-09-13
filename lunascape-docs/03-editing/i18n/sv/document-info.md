# Visa dokumentinformation

En ”dokumentkontrolltabell” högst upp i ett dokument (dokument-ID, version, uppdateringsdatum, status och så vidare) visas vid läsning samlad i en liten rad med dokumentinformation. Själva Markdown-koden förblir en vanlig tabell, så den går att läsa som den är även på GitHub.

## Villkor för att den ska visas

Placera en tabell med två kolumner, som nedan, direkt efter rubriken (H1).

```markdown
# Funktionskravspecifikation

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Tabellen måste innehålla en rad med dokument-ID och flera hanteringsfält.
- En tabell under rubriken `## 文書管理` eller `## Document information` räknas också.
- Tabeller mitt i brödtexten och vanliga tabeller av typen post/innehåll konverteras inte.

## Så visas den

- Vid läsning visas bara status och uppdateringsdatum, i liten stil.
- Tryck på raden för att visa alla fält.
- Vid utskrift visas alla fält.
- I redigeringsvyn visas den som en vanlig tabell och kan redigeras som den är.

> **Tips**
>
> Om du alltid vill visa tabellen i stället för att fälla ihop den stänger du av [Fäll ihop dokumentuppgifterna] i [Visningsinställningar].

## Relaterade avsnitt

- [Redigera ett dokument](README.md)
- [Ändra visningsinställningar](../02-reading/display-settings.md)
