# Uzantıyı kurma

VS Code uzantısı "Lunascape Docs Pro", VSIX dosyası olarak dağıtılır. Ücretsizdir; "Pro", işi bir yapay zekâya devreden ve kendini güncelleyen sürümü belirtir.

## Gereksinimler

- VS Code 1.90 veya sonrası
- Dosyaya yazan özellikler — belge oluşturma, INDEX'i düzenleme, denetim ayarlarını kaydetme, çeviri — yalnızca VS Code'da güvenilir olarak işaretlediğiniz bir çalışma alanında çalışır.

## Kurma

1. VSIX dosyasını edinin. Bu bağlantı her zaman güncel sürümü gösterir.

   [lunascape-docs-pro.vsix dosyasını indir](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Uzantılar görünümünü açın (`⇧⌘X` / `Ctrl+Shift+X`).
3. Sağ üstteki `…` menüsünden [VSIX'ten Yükle...] seçeneğini seçin ve indirdiğiniz dosyayı belirtin.

### Komut satırından

Terminalden çıkmak istemezseniz tek satır yeter. İndirir ve kurar.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Not**
> `code` bulunamazsa, Komut Paleti'nden (`⇧⌘P` / `Ctrl+Shift+P`) [Kabuk Komutu: PATH içine 'code' komutunu yükle] seçeneğini çalıştırın.

## Güncelleme

Yeni bir sürüm yayımlandığında, uzantı bunu kendisi indirir ve kurar. VS Code pencereyi yeniden yüklemenizi önerir; asıl geçiş o anda olur. Ayarlarınız ve belgeleriniz olduğu gibi kalır.

Denetim günde bir kez yapılır. Hemen denetlemek isterseniz, Komut Paleti'nden (`⇧⌘P` / `Ctrl+Shift+P`) [Lunascape Docs: Güncellemeleri denetle] seçeneğini çalıştırın.

Davranış, `lunascapeDocEditor.update.check` ayarıyla değiştirilebilir.

| Ayar | Davranış |
|---|---|
| Yeni bir sürüm yayımlandığında kur | Varsayılan |
| Bildir; kurup kurmamaya her seferinde ben karar vereyim | Bir bildirim çıkar ve yalnızca [Güncelle] düğmesine bastığınızda değişir |
| Denetleme | Hiçbir şey yapmaz |

### Güncellenemediğinde

"Güncelleme alınamadı: No Servers" iletisi çıkıyorsa, kurulu sürüm 0.22.18 veya öncesidir. O sürümün güncelleme özelliği indirdikten sonraki adımda her zaman başarısız olduğu için kendini yenileyemez. Yukarıdaki adımlarla bir kez elle yeniden kurun. Bundan sonra kendini günceller.

## Sürümü denetleme

Uzantılar görünümünde "Lunascape Docs Pro" öğesini açtığınızda kurulu sürüm görüntülenir. Bir sorunu bildirirken bu gereklidir.

## İlgili konular

- [İlk belgelerinizi oluşturma](first-documents.md)
- [Bir sorunu bildirme](../07-troubleshooting/report.md)
