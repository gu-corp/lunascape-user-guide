# Vis dokumentoplysninger

Et "dokumentstyringsskema" øverst i dokumentet (et skema med dokument-id, version, opdateringsdato, status og lignende) vises under læsning samlet i en lille linje med "dokumentoplysninger". Selve Markdown-koden forbliver et almindeligt skema, så det kan også læses som det er på GitHub.

## Betingelser for visning

Placer et skema med to kolonner som det følgende umiddelbart efter overskriften (H1).

```markdown
# Kravspecifikation

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Det er en betingelse, at der er en linje med dokument-id og flere styringsfelter.
- Et skema, der er placeret under overskriften `## 文書管理` eller `## Document information`, medtages også.
- Skemaer midt i brødteksten og almindelige "felt/indhold"-skemaer bliver ikke omdannet.

## Sådan vises det

- Under læsning vises kun status og opdateringsdato med lille skrift.
- Tryk på linjen for at vise alle felter.
- Ved udskrivning vises alle felter.
- I redigeringsvisningen vises det som et almindeligt skema og kan redigeres direkte.

> **Tip**
>
> Hvis du altid vil have det vist som et skema uden sammenfoldning, skal du slå [Fold dokumentoplysningerne sammen] fra under [Visningsindstillinger].

## Relaterede emner

- [Rediger et dokument](README.md)
- [Skift visningsindstillinger](../02-reading/display-settings.md)
