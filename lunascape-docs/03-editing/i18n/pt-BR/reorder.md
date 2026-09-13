# Alterar a ordem dos documentos

A ordem exibida no INDEX pode ser alterada por arrastar e soltar ou pelo teclado. A nova ordem é salva no front matter do documento como `navigation.order`.

## Reordenar arrastando e soltando

1. Arraste um documento ou uma pasta no INDEX.
2. Solte-o antes ou depois de um item do mesmo nível, ou sobre uma pasta.
   Dentro do mesmo nível, a ordem muda. Ao soltar sobre outra pasta, o item é movido para essa pasta.

## Reordenar pelo teclado ou pelo menu

- Coloque o foco em um item do INDEX e pressione `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Escolha [Mover para cima] / [Mover para baixo] no menu do item.

## O que é salvo

- Ao reordenar dentro do mesmo nível, o `navigation.order` no front matter do documento canônico é atualizado. No caso de uma pasta, ele é gravado no `README.md` dessa pasta. Se a pasta não tiver um `README.md`, é criado um `README.md` apenas com o front matter.
- Ao mover para outra pasta, o documento canônico e as traduções correspondentes são movidos em conjunto. Antes da movimentação, aparece uma confirmação sobre o efeito nos links relativos.
- Não são feitos preparo (staging) nem commit no Git.

> **Nota**
>
> - Não é possível reordenar durante a filtragem, durante a edição de um documento nem em um espaço de trabalho não confiável.
> - Quando aparece "O INDEX foi atualizado", outra alteração acabou de ser aplicada. Repita a operação.
> - A página inicial não pode ser movida para outra pasta.

> **Dica**
>
> Definir os valores de `navigation.order` em intervalos de 100, como 100, 200, 300, facilita inserir documentos entre eles mais tarde. Para saber mais, consulte [Definir informações de navegação](../04-document-tools/navigation-metadata.md).

## Tópicos relacionados

- [Criar e organizar documentos e pastas](organize.md)
- [Definir informações de navegação](../04-document-tools/navigation-metadata.md)
