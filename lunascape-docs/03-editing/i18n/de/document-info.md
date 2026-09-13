# Dokumentinformationen anzeigen

Eine „Dokumentverwaltungstabelle" am Anfang eines Dokuments (Dokument-ID, Version, Aktualisierungsdatum, Status usw.) wird beim Lesen als kompakte Zeile „Dokumentinformationen" zusammengefasst dargestellt. Das Markdown selbst bleibt eine gewöhnliche Tabelle, sodass es auch auf GitHub weiterhin lesbar ist.

## Voraussetzungen für die Anzeige

Platzieren Sie unmittelbar nach der Überschrift (H1) eine zweispaltige Tabelle wie die folgende.

```markdown
# Funktionale Anforderungen

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Voraussetzung ist eine Zeile „文書ID" sowie das Vorhandensein mehrerer Verwaltungsfelder.
- Auch eine Tabelle unter einer Überschrift `## 文書管理` oder `## Document information` wird erkannt.
- Tabellen mitten im Text sowie gewöhnliche Tabellen nach dem Muster „Element/Inhalt" werden nicht umgewandelt.

## So wird es angezeigt

- Beim Lesen werden nur der Status und das Aktualisierungsdatum in kleiner Schrift angezeigt.
- Beim Antippen der Zeile werden alle Felder angezeigt.
- Beim Drucken werden alle Felder angezeigt.
- Im Editor wird die Tabelle als gewöhnliche Tabelle dargestellt und kann direkt bearbeitet werden.

> **Tipp**
>
> Wenn Sie die Tabelle immer als Tabelle anzeigen möchten, statt sie einzuklappen, schalten Sie [Dokumentinformationen einklappen] unter [Anzeigeeinstellungen] aus.

## Verwandte Themen

- [Ein Dokument bearbeiten](README.md)
- [Anzeigeeinstellungen ändern](../02-reading/display-settings.md)
