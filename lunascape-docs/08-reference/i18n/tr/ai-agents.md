# Yapay zekâ üzerinden kullanım

Uzantı, salt okunur Language Model Tool `lunascape_getDocsSpecification` aracını VS Code'a kaydeder. Uyumlu bir VS Code aracısına Lunascape Docs özellikleri, ayarları veya belge kuralları hakkında bir soru sorulduğunda, bu aracı kullanarak bu yardımın içeriğini (genel şartname) alabilir.

## Nasıl kullanılır

VS Code sohbetinde `#lunascapeDocs` ekleyerek soru sorun ya da Lunascape Docs ayarları veya belge yapısı hakkında sorun.

```text
#lunascapeDocs lunascape-docs.json içinde İngilizce çeviriyi nasıl etkinleştiririm?
```

## Aracın bağımsız değişkenleri

| Bağımsız değişken | İçerik |
|---|---|
| `topic` | Alınacak bölüm: `all`, `usage` (Temel işlemler), `structure` (Belge kökleri ve dosya kuralları), `editing` (Belge düzenleme), `configuration` (Proje ayarları), `security` (Güvenlik ve yazma sınırları), `ai` (Yapay zekâ üzerinden kullanım) |
| `locale` | Yardımın dili (`ja`, `en` gibi, birlikte gelen yardımın dil etiketi). Atlanırsa VS Code'un görüntüleme dili, yoksa Japonca yardım döndürülür |

> **Not**
>
> - Araç, belge içeriğini dışarıya göndermez.
> - Araç, çalışma alanı adlarını veya yerel yolları döndürmez.
> - Araç, dosyaları değiştirmez.
> - `AGENTS.md` olmadan da uyumlu VS Code aracılarından kullanılabilir. Uzantının araç API'sini kullanmayan başka bir yapay zekâ istemcisiyle otomatik olarak paylaşılmaz.

## İlgili konular

- [Yardımı görüntüleme](../02-reading/help.md)
- [Güvenlik ve yazma sınırları](security.md)
