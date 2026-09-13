# Belge bilgilerini gösterme

Belgenin başına yerleştirilen "belge yönetim tablosu" (belge kimliği, sürüm, güncelleme tarihi, durum vb. içeren tablo), okuma sırasında küçük bir "Belge bilgileri" satırında toplu olarak gösterilir. Markdown'ın kendisi sıradan bir tablo olarak kaldığından, GitHub'da da olduğu gibi okunabilir.

## Gösterilme koşulları

Başlığın (H1) hemen ardına, aşağıdaki gibi iki sütunlu bir tablo yerleştirin.

```markdown
# İşlevsel gereksinim tanımı

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Tabloda bir belge kimliği satırının ve birden çok yönetim alanının bulunması koşuldur.
- `## 文書管理` veya `## Document information` başlığının altına yerleştirilen bir tablo da tanınır.
- Metnin ortasındaki tablolar ve sıradan "öğe/değer" tabloları dönüştürülmez.

## Nasıl gösterilir

- Okuma sırasında yalnızca durum ve güncelleme tarihi küçük yazıyla gösterilir.
- Satıra basıldığında tüm alanlar gösterilir.
- Yazdırma sırasında tüm alanlar gösterilir.
- Düzenleme ekranında sıradan bir tablo olarak görünür ve olduğu gibi düzenlenebilir.

> **İpucu**
>
> Daraltmadan her zaman tablo olarak göstermek isterseniz, [Görünüm ayarları] içindeki [Belge bilgilerini daralt] seçeneğini kapatın.

## İlgili konular

- [Belgeyi düzenleme](README.md)
- [Görünüm ayarlarını değiştirme](../02-reading/display-settings.md)
