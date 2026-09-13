# Tillgängliga arbeten

Välj under [Arbete] på fliken [AI]. Varje arbete ändrar instruktionen som lämnas över och kontrollen som följer.

| Arbete | Innehåll | Kräver | API-typ |
|---|---|---|---|
| Översätt den här sidan | Översätter det visade dokumentet till det valda språket | Att dokumentet är öppet, ett målspråk | Ja |
| Översätt allt som saknas | Översätter det valda språkets saknade och inaktuella dokument, i tur och ordning | Ett målspråk | Endast sessionstyp |
| Korrekturläs den här sidan | Kontrollerar och rättar terminologi, stil och den kapitelindelning som dokumentstandarden kräver | Att dokumentet är öppet | Ja |
| Skapa ett nytt dokument | Skapar ett nytt dokument enligt dokumentstandarden och dess mallar | Ett ämne (kan utelämnas) | Endast sessionstyp |

## Vad instruktionen innehåller

| Nr | Innehåll |
|---|---|
| 1 | Dokumentrotens plats. Instruktionen säger att inget utanför den får ändras |
| 2 | Standardspråket (originaldokumentet) och var översättningarna ligger (`i18n/<språk>/` i samma mapp som dokumentet) |
| 3 | Att `navigation.order` bara hör till originaldokumentet och att en översättning enbart får skriva över `navigation.title` |
| 4 | Att krav-ID:n, länkar, kod, Mermaid, TeX och front matter-strukturen inte får ändras |
| 5 | Dokumentstandarden och ordlistan (`terminology` i `docs-lint.config.json`) |
| 6 | Att dokumentkontrollen ska köras efteråt, att de ändrade filerna ska rapporteras och att inga Git-åtgärder får utföras |

> **Tips**
>
> Vad ”Översätt allt som saknas” omfattar hämtas från liggaren, upp till 200 dokument per körning. Kör den igen om det är fler.

## Relaterade avsnitt

- [Lämna arbete till en AI](README.md)
- [Liggaren och dess poster](ledger.md)
