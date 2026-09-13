# Operações básicas

As operações básicas desde abrir os documentos até chegar à página que você quer ler.

## Abrir os documentos

1. Abra o repositório no VS Code.
2. Na paleta de comandos (`⇧⌘P` / `Ctrl+Shift+P`), execute "Lunascape Docs: Abrir o visualizador de especificações".
   A raiz da documentação mais próxima (por padrão, a pasta `docs`) é localizada e sua página inicial é exibida.

> **Dica**
>
> - Clique com o botão direito em um arquivo Markdown no Explorador e escolha [Lunascape Docs: Abrir no visualizador de especificações] para começar por esse arquivo.
> - Ao abrir um arquivo Markdown que não pertence a nenhuma raiz da documentação, a pasta dele é exibida como raiz da documentação temporária.

## Navegar entre as páginas

| Ação | Como |
|---|---|
| Abrir pelo sumário | Pressione o nome de um documento no INDEX à esquerda |
| Seguir um link | Pressione um link no texto. Ele abre na mesma tela |
| Percorrer o histórico | [Voltar] e [Avançar] na barra de ferramentas, ou `Alt`+`←` / `Alt`+`→` |
| Voltar à página inicial | [Início da documentação] na barra de ferramentas |
| Subir um nível | [INDEX pai] na barra de ferramentas, ou um item da trilha de navegação |
| Mover-se dentro da página | Pressione um título em "Nesta página", à direita |

## Localizar um documento

Digite uma palavra em [Filtrar documentos], acima do INDEX, para exibir apenas os documentos cujos nomes correspondem. Apague o que foi digitado para voltar ao estado anterior.

## Atualizar para o conteúdo mais recente

Ao salvar um arquivo Markdown no editor do VS Code, a exibição é atualizada automaticamente. Quando os arquivos forem alterados por uma ferramenta externa, pressione [Recarregar] na barra de ferramentas.

> **Atenção**
>
> - Os links externos no texto (`https://` e semelhantes) abrem no navegador padrão. Links para arquivos fora da raiz da documentação não são abertos.
> - O documento que você lê é processado no seu dispositivo. Nada é enviado para fora para que um documento seja lido.

## Tópicos relacionados

- [Usar o INDEX](index-panel.md)
- [Alternar a raiz da documentação](roots.md)
- [Editar um documento](../03-editing/README.md)
