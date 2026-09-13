# Alternar entre raízes da documentação

A raiz da documentação é a pasta de nível mais alto de um conjunto de documentos. O INDEX, a filtragem, a verificação e a tradução funcionam por raiz da documentação.

## Como a raiz da documentação é encontrada

O Lunascape Docs percorre as pastas superiores a partir do arquivo Markdown aberto e usa como raiz da documentação a pasta mais próxima que corresponda a um dos casos a seguir.

- Uma pasta que contenha `lunascape-docs.json` (o nome da pasta não importa)
- Uma pasta chamada `docs` (você pode acrescentar nomes na configuração `lunascapeDocEditor.rootDirectoryNames`)

Ao executar “Lunascape Docs: Abrir o visualizador de especificações”, abre-se a raiz da documentação indicada na configuração `lunascapeDocEditor.root` (padrão `docs`).

## Alternar para outra raiz da documentação

Quando o espaço de trabalho tem várias raízes da documentação, o nome da raiz na extremidade esquerda da barra de ferramentas vira uma lista suspensa.

1. Pressione o nome da raiz da documentação na extremidade esquerda da barra de ferramentas.
2. Escolha uma raiz da documentação na lista.
   A página inicial da raiz escolhida é exibida e o INDEX é trocado.

> **Dica**
>
> Os nomes exibidos na lista são definidos nesta ordem. Eles não mudam quando você troca o idioma de exibição.
>
> 1. `title` em `lunascape-docs.json`
> 2. `navigation.title` do `README.md` da raiz ou, na falta dele, seu H1
> 3. `navigation.title` do `index.md` da raiz ou, na falta dele, seu H1
> 4. O nome da pasta (em uma pasta `docs` padrão, o nome da pasta que a contém)

## Abrir um Markdown fora de qualquer raiz da documentação

Ao abrir um arquivo Markdown que não está em uma raiz da documentação, a pasta desse arquivo é exibida como raiz da documentação temporária. O INDEX lista os arquivos Markdown dessa pasta e das pastas abaixo dela.

- Pressione [Pasta acima] na barra de ferramentas para ampliar o escopo até a pasta superior dentro do espaço de trabalho.
- Nessa exibição, as configurações de idioma do projeto e a tradução em lote não estão disponíveis. Coloque um `lunascape-docs.json` na pasta para torná-la uma raiz da documentação e habilitá-las.

## Abrir sempre uma raiz da documentação fixa

Defina a configuração `lunascapeDocEditor.rootMode` como `fixed` para abrir sempre a raiz da documentação indicada em `lunascapeDocEditor.root`, qualquer que seja o Markdown aberto.

## Tópicos relacionados

- [Raízes da documentação e convenções de arquivos](../04-document-tools/structure.md)
- [Configuração do projeto](../04-document-tools/project-configuration.md)
- [Lista de configurações do VS Code](../08-reference/settings.md)
