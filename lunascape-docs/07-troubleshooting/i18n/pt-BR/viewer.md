# Os documentos não aparecem

## Aparece a mensagem “Não foi encontrada nenhuma pasta Markdown ou docs que possa ser aberta”

- O espaço de trabalho não tem uma pasta `docs`, ou usa um nome diferente de `docs`.
  - Coloque um `lunascape-docs.json` nessa pasta para que ela seja reconhecida como raiz da documentação, independentemente do nome.
  - Ou acrescente o nome da pasta à configuração `lunascapeDocEditor.rootDirectoryNames`.
- Se ainda não houver documentos, crie-os com “Lunascape Docs: Criar documentação a partir de um modelo”.
- Também é possível abrir um arquivo Markdown no editor e executar “Lunascape Docs: Abrir no visualizador de especificações”.

## Um documento não aparece no INDEX

- Verifique se a extensão é `.md`, `.markdown` ou `.mdx`.
- As pastas a seguir não são exibidas: pastas que começam com `.`, `node_modules` e as pastas indicadas em `ignoredDirectories` (o padrão é `99-archive`).
- As traduções que ficam em `i18n/` não aparecem separadamente no INDEX. Alterne para elas pelo menu de idiomas.
- Se um arquivo recém-adicionado não aparecer, pressione [Recarregar].
- Você pode estar vendo outra raiz da documentação. Confira o nome da raiz na extremidade esquerda da barra de ferramentas.

## Nada aparece ao pressionar uma pasta

O `README.md` dessa pasta é um “descritor somente de configuração”, com front matter e sem corpo de texto. Abra a pasta no INDEX e escolha um documento dentro dela.

## Abre uma raiz da documentação inesperada

- Quando a configuração `lunascapeDocEditor.rootMode` está como `fixed`, sempre é aberta a raiz indicada em `lunascapeDocEditor.root`.
- Com `auto`, é escolhida a raiz da documentação mais próxima do arquivo Markdown aberto. Use a lista suspensa na extremidade esquerda da barra de ferramentas para alternar.

## O nome da raiz da documentação é diferente do esperado

O nome é definido nesta ordem: `title` do `lunascape-docs.json` → `navigation.title` do `README.md` da raiz → o H1 desse arquivo → `index.md` → o nome da pasta. Para fixá-lo, defina `title`.

## O INDEX desapareceu

- Em uma raiz da documentação com apenas um documento, o INDEX se fecha automaticamente na primeira vez. É possível abri-lo com o ícone de colunas da barra de ferramentas. Para desativar esse comportamento, use [Ocultar automaticamente se houver apenas um documento] em [Configurações de exibição].
- Em telas estreitas, abra-o com [Abrir o INDEX] (três linhas), à esquerda de [Voltar].

## Um link não abre ao ser pressionado

- “O destino do link não foi encontrado”: o arquivo de destino não existe. Use a [Verificação] das Ferramentas de documento para conferir os links internos.
- “Um link não seguro ou não suportado não foi aberto”: links para fora da raiz da documentação, ou com um esquema diferente de `https://` e `mailto:`, não são abertos.

## O idioma exibido é diferente do esperado

- No menu de idiomas, confira o idioma da página exibida e o motivo dessa escolha.
- O idioma de exibição escolhido da última vez fica memorizado. Escolha novamente o idioma padrão no menu de idiomas.
- Se a configuração pessoal `lunascapeDocEditor.locale` estiver definida, a tradução nesse idioma tem prioridade.

## Tópicos relacionados

- [Alternar entre raízes da documentação](../02-reading/roots.md)
- [Raízes da documentação e convenções de arquivos](../04-document-tools/structure.md)
