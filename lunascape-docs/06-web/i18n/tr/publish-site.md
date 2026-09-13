# Belgelerinizi Web'de yayımlama

Kendi deponuzdaki belgeleri GitHub Pages üzerinde veya herhangi bir statik barındırma hizmetinde web sitesi olarak yayımlayabilirsiniz. Bunun iki yolu vardır. Bu adımlar, Lunascape Docs deposunu clone edip `npm` kullanabilen geliştiriciler içindir.

## 1. yol: görüntüleyicinin iki dosyasını yerleştirme

Yalnızca görüntüleyiciyi (`index.html` ve `lsdoc.js`) yerleştirip belgeleri GitHub'dan yükletme yöntemidir. Belgelerin kendisi siteye dahil olmadığından, özel depolar için de güvenlidir (okuyucular GitHub ile oturum açar).

1. Lunascape Docs deposunda aşağıdaki komutu çalıştırın.

   ```sh
   npm run build:viewer
   ```

   `dist/viewer/` içinde `index.html` ve `lsdoc.js` oluşturulur.
2. İki dosyayı, yayımlamak istediğiniz deponun `docs/` klasörüne koyun.
3. GitHub Pages'i etkinleştirin.

Gösterilecek belge kökü şu sırayla belirlenir.

1. `index.html` içindeki `source` ayarı
2. Aynı klasördeki `lunascape-docs.json` dosyasında yazan `repository`
3. `*.github.io` adresinden ve dal yapısından çıkarım

## 2. yol: belgeleri içeren statik site dışa aktarma

Görüntüleyiciyi ve belge dosyalarını birlikte dışa aktarıp olduğu gibi barındırma yöntemidir.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Çıktıda görüntüleyici takımı, `docs/` altındaki belgeler, liste dosyası `lunascape-docs-manifest.json` ve `.nojekyll` yer alır. Çıktıyı S3'e veya GitHub Pages'e yerleştirerek yayımlayabilirsiniz. GitHub Actions ile otomatik yayımlama örneği için deponun `examples/workflows/publish-docs-pages.yml` dosyasına bakın.

> **Not**
>
> - **Özel bir deponun belgelerini dışa aktarıp GitHub Pages'e koymayın.** Enterprise Cloud dışındaki GitHub Pages'i herkes görüntüleyebilir. Sınırlı yayımlama gerekiyorsa 1. yolu kullanın ve okuyucuların GitHub ile oturum açmasını sağlayın.
> - `index.html` dosyasını doğrudan `file://` ile açmak işe yaramaz. Tarayıcılar bu yolla komşu dosyaların yüklenmesini ve ES modüllerinin çalıştırılmasını engeller. Yerelde denemek için VS Code sürümünü veya bir HTTP sunucusu kullanın.
> - TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob ve Penrose çizim kitaplıkları görüntüleme sırasında yüklenir. Dışa aktardığınız sitede `vendor/` klasörünü de birlikte yerleştirin.

## İlgili konular

- [Web sürümüyle yapabilecekleriniz](README.md)
- [Özel bir depoyu görüntüleme](private-repository.md)
