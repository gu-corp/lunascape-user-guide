# Ajustar o tamanho das imagens

As imagens inseridas em um documento se ajustam automaticamente à largura do texto e à altura da tela. Para uma imagem que você quer mostrar em um tamanho específico, é possível definir a largura.

## Como funciona o ajuste automático

- Uma imagem comum em Markdown (`![descrição](./images/screen.png)`) é reduzida para caber na largura do texto. Ela nunca é ampliada além do seu tamanho original.
- Uma captura de tela vertical fica limitada a 72% da altura da tela ou a 720px, o que for menor.

## Definir a largura no editor

1. Pressione [Editar] e selecione a imagem na exibição visual.
2. Escolha uma largura em [Tamanho da imagem] na barra de ferramentas.
3. Pressione [Salvar].

| Opção | Largura |
|---|---|
| [Automática] | Não especificada (ajuste automático) |
| [Pequena (360px)] | 360px |
| [Média (560px)] | 560px |
| [Grande (760px)] | 760px |
| [Largura do texto (920px)] | 920px |
| [Personalizada…] | Qualquer número inteiro de 16 a 4096px |

## Definir a largura em Markdown

Atribua um `width` numérico à tag HTML `img`. Essa forma também é exibida como imagem no GitHub e em MDX.

```html
<img src="./images/screen.png" alt="Tela de configurações" width="360" />
```

> **Nota**
>
> - `width` recebe apenas um número, sem `px` ou `%`. Um valor maior que a largura do texto ainda se ajusta à largura do texto ao ser exibido.
> - Os caminhos das imagens são relativos ao documento. Imagens fora da raiz da documentação não são exibidas.

## Tópicos relacionados

- [Editar um documento](README.md)
- [Diagramas, fórmulas ou imagens não são exibidos](../07-troubleshooting/rendering.md)
