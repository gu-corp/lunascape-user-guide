# Raízes da documentação e convenções de arquivos

As regras que o Lunascape Docs segue para encontrar documentos e montar o INDEX. O próprio sistema de arquivos é o que serve de fonte de verdade, portanto não é necessário nenhum registro nem configuração de build.

## Raiz da documentação

- A pasta `docs` mais próxima, ou uma pasta que contenha `lunascape-docs.json`, torna-se a Raiz da documentação.
- Com um `lunascape-docs.json`, a pasta não precisa se chamar `docs`.
- Ao abrir um arquivo Markdown que não pertence a nenhuma Raiz da documentação, sua pasta é exibida como uma Raiz da documentação temporária.

## Arquivos exibidos no INDEX

- São exibidos os arquivos `.md`, `.markdown` e `.mdx`. Arquivos novos sempre aparecem, mesmo sem front matter ou informações de navegação.
- Pastas que começam com `.`, `node_modules` e as pastas indicadas em `ignoredDirectories` (por padrão `99-archive`) não são exibidas.
- Tudo o que está sob `i18n/` é tratado como Tradução e não é listado separadamente no INDEX.

## Páginas de capa das pastas

- Um `README.md` (ou `index.md`, quando não há README) que tenha conteúdo no corpo é a página de capa daquela pasta. Ao pressionar o nome da pasta no INDEX, a capa é aberta.
- Um `README.md` que contém apenas front matter, sem corpo, é tratado como um "descritor exclusivo de configuração" e não é exibido como página. Use-o quando a pasta precisa apenas de um título ou de uma Ordem.
- Quando existem tanto `README.md` quanto `index.md`, o `README.md` tem prioridade.

## Idioma padrão e Traduções

- Os documentos no Idioma padrão (o Documento canônico) permanecem no lugar.
- A Tradução vai em uma pasta `i18n/<idioma>/` ao lado do documento, com o mesmo nome de arquivo. Recriar a estrutura de pastas sob `i18n/` não é reconhecido.
- Esse é o único local a partir do qual uma Tradução é resolvida. O mesmo arquivo colocado em qualquer outro lugar é um arquivo órfão que nenhum documento reivindica como sua Tradução.

```text
docs/
  lunascape-docs.json
  README.md                  ← página de capa da raiz (página inicial)
  i18n/en/README.md          ← sua versão em inglês
  01-product/
    README.md                ← página de capa da pasta
    requirements.md
    i18n/en/README.md        ← as versões em inglês dos dois documentos acima
    i18n/en/requirements.md
  99-archive/                ← excluída do INDEX por padrão
```

## Sobre o `_meta.json`

O `_meta.json` do Nextra não é usado para navegação. Os arquivos existentes não são modificados nem excluídos. No futuro, um recurso explícito de importação/exportação será a única coisa a lidar com eles.

## Tópicos relacionados

- [Definir informações de navegação](navigation-metadata.md)
- [Configuração do projeto](project-configuration.md)
- [Alternar a Raiz da documentação](../02-reading/roots.md)
