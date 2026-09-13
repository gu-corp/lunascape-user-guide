# Documentgegevens weergeven

Een "documentbeheertabel" boven aan een document (document-ID, versie, bijwerkdatum, status enzovoort) wordt tijdens het lezen samengevat in een kleine regel "Documentgegevens". De Markdown zelf blijft een gewone tabel, dus hij is ook op GitHub gewoon leesbaar.

## Voorwaarden voor de weergave

Plaats direct na de kop (H1) een tabel met twee kolommen, zoals hieronder.

```markdown
# Functionele specificatie

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- De tabel moet een regel met het document-ID bevatten en meerdere beheervelden.
- Een tabel onder de kop `## 文書管理` of `## Document information` wordt ook herkend.
- Tabellen midden in de tekst en gewone "item/waarde"-tabellen worden niet omgezet.

## Hoe de weergave werkt

- Tijdens het lezen worden alleen de status en de bijwerkdatum klein weergegeven.
- Druk op de regel om alle velden weer te geven.
- Bij het afdrukken worden alle velden weergegeven.
- In het bewerkingsscherm verschijnt de tabel als een gewone tabel en kunt u hem zo bewerken.

> **Tip**
>
> Wilt u de tabel altijd volledig weergeven in plaats van samengevouwen, schakel dan [Documentgegevens samenvouwen] uit bij [Weergave-instellingen].

## Verwante onderwerpen

- [Een document bewerken](README.md)
- [Weergave-instellingen wijzigen](../02-reading/display-settings.md)
