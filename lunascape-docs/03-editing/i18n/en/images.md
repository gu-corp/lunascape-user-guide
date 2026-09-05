# Sizing images

Images in a document automatically fit the width of the text and the height of the screen. For an image that should have a specific size, you can set its width.

## How automatic sizing works

- An ordinary Markdown image (`![description](./images/screen.png)`) is scaled down to fit the text width. It is never enlarged beyond its original size.
- A tall screenshot is limited to 72% of the screen height or 720px, whichever is smaller.

## Set the width in the editor

1. Press [編集] (Edit) and select the image in the visual view.
2. Choose a width from [画像サイズ] (Image size) in the toolbar.
3. Press [保存] (Save).

| Option | Width |
|---|---|
| [自動] (Automatic) | Not specified (automatic sizing) |
| [小 (360px)] (Small) | 360px |
| [中 (560px)] (Medium) | 560px |
| [大 (760px)] (Large) | 760px |
| [本文幅 (920px)] (Text width) | 920px |
| [任意…] (Custom…) | Any integer from 16 to 4096px |

## Set the width in Markdown

Give the HTML `img` tag a numeric `width`. This form also renders as an image on GitHub and in MDX.

```html
<img src="./images/screen.png" alt="Settings screen" width="360" />
```

> **Note**
>
> - `width` takes a number only, without `px` or `%`. A value larger than the text width still fits the text width when displayed.
> - Image paths are relative to the document. Images outside the documentation root are not shown.

## Related topics

- [Editing a document](README.md)
- [Diagrams, math or images do not render](../07-troubleshooting/rendering.md)
