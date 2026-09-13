# Başlıca şartname

## Çalışma ortamı

| Ortam | Gereksinimler |
|---|---|
| VS Code uzantısı | VS Code 1.90 veya üzeri. Yazma işlemi içeren özellikler güvenilen çalışma alanında çalışır |
| Web tarayıcı sürümü | Güncel Chrome, Edge, Safari, Firefox. Yerel klasörü görüntülemek için klasör seçimini (File System Access API) destekleyen bir tarayıcı gerekir |
| Chromium uzantısı | Manifest V3. Ana makine izni istenmez |

## Desteklenen belgeler

| Öğe | İçerik |
|---|---|
| Dosyalar | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tablolar, görev listeleri, kod blokları, üstü çizili metin), yerel görseller, YAML front matter |
| MDX | Yalnızca izin verilen bileşenler görüntülenir. Rastgele betikler çalıştırılmaz |
| HTML | DOMPurify 3.4.14 ile zararsız hâle getirilerek görüntülenir |

## Diyagramlar ve matematik

| Tür | Dil adı | Notlar |
|---|---|---|
| Matematik | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Yalnızca gömülü veriler. Dış URL'ler ve görsel işaretleri kullanılamaz |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Yalnızca katı JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Dağıtım sürümünde kaynak katlanmış olarak görüntülenir. Üst sınırlar: 64 KiB giriş, 15 saniye, 2 MiB SVG |
| Penrose (deneysel) | `penrose` | Yalnızca `set-theory` hazır ayarı |

## Üst sınırlar

| Öğe | Değer |
|---|---|
| Şablonun işlenmiş boyutu | 4 MiB |
| Çeviri başvuru bağlamı | Varsayılan 49.152 karakter, en fazla 1.048.576 karakter |
| Toplu çevirinin bir çalıştırmadaki kapsamı | 1.000 belge |
| Görselin isteğe bağlı genişliği | 16–4096px |

## Dosyalar

| Dosya | Görevi | Git yönetiminde |
|---|---|---|
| `lunascape-docs.json` | Belge kökü ayarları | Var |
| `docs-lint.config.json` | Denetim kurallarının ayarları | Var |
| `.lunascape-docs/translation-freshness.json` | Çevirinin tazelik kaydı (yalnızca yol, dil, karma değeri ve tarih-saat) | Var |
| VS Code ayarları ve çalışma alanı durumu | Kişisel görünüm ayarları, sağlayıcı seçimi, INDEX açık/kapalı durumu | Yok |

## Birlikte gelen Standard Pack

`builtin:gu-corp-software` — profiller: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## İlgili konular

- [VS Code ayarları listesi](settings.md)
- [Güvenlik ve kaydetme sınırları](security.md)
