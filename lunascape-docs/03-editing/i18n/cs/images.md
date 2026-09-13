# Úprava velikosti obrázků

Obrázky vložené do dokumentu se automaticky přizpůsobí šířce textu a výšce obrazovky. U obrázku, který se má zobrazit v určité velikosti, můžete nastavit jeho šířku.

## Jak funguje automatické přizpůsobení

- Běžný obrázek v Markdownu (`![popis](./images/screen.png)`) se zmenší tak, aby se vešel do šířky textu. Nikdy se nezvětší nad svou původní velikost.
- Vysoký snímek obrazovky je omezen na 72 % výšky obrazovky nebo na 720px, podle toho, která hodnota je menší.

## Nastavení šířky v editoru

1. Stiskněte [Upravit] a vyberte obrázek ve vizuálním zobrazení.
2. V panelu nástrojů zvolte šířku z nabídky [Šířka obrázku].
3. Stiskněte [Uložit].

| Možnost | Šířka |
|---|---|
| [Automaticky] | Neurčeno (automatické přizpůsobení) |
| [Malá (360px)] | 360px |
| [Střední (560px)] | 560px |
| [Velká (760px)] | 760px |
| [Šířka textu (920px)] | 920px |
| [Vlastní…] | Libovolné celé číslo od 16 do 4096px |

## Nastavení šířky v Markdownu

Zadejte HTML značce `img` číselnou hodnotu `width`. Tento zápis se stejně zobrazí jako obrázek i na GitHubu a v MDX.

```html
<img src="./images/screen.png" alt="Obrazovka nastavení" width="360" />
```

> **Poznámka**
>
> - Hodnota `width` přijímá pouze číslo, bez `px` nebo `%`. I když zadáte hodnotu větší než šířka textu, obrázek se při zobrazení vejde do šířky textu.
> - Cesty k obrázkům se zadávají relativně vůči dokumentu. Obrázky mimo kořen dokumentace se nezobrazí.

## Související témata

- [Úprava dokumentu](README.md)
- [Diagramy, vzorce nebo obrázky se nezobrazují](../07-troubleshooting/rendering.md)
