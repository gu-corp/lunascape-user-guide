# Configurações do projeto

O arquivo `lunascape-docs.json`, localizado diretamente na raiz da documentação, contém as configurações da raiz da documentação compartilhadas pela equipe. Ele é gerenciado no Git.

## Criar ou editar o arquivo de configuração

- Pressione [Ferramentas de documento] na barra de ferramentas → a aba [Verificação] → [De onde vêm as regras e as configurações do documento] → [Editar as configurações do documento] para abrir o arquivo no VS Code. Se o arquivo não existir, um arquivo inicial é criado nesse momento.
- O nome de arquivo `lunascape-docs.json` é associado automaticamente ao JSON Schema incluído, que oferece preenchimento automático e a descrição de cada campo. Não é necessário incluir a entrada `$schema`.

## Exemplo de configuração

```json
{
  "id": "product-docs",
  "title": "Documentação do produto",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Descrição dos campos

| Campo | Conteúdo | Padrão |
|---|---|---|
| `id` | A chave sob a qual as configurações de exibição de cada usuário são salvas. Atribua um ID fixo quando quiser manter as configurações mesmo ao mover a pasta | O caminho da pasta |
| `title` | O nome exibido na extremidade esquerda da barra de ferramentas e na lista de raízes da documentação. Ele não muda ao alternar o idioma de exibição | O título do README/index da raiz e, na sua ausência, o nome da pasta |
| `indexTitle` | O título do INDEX | `INDEX` |
| `startPage` | O documento aberto primeiro (caminho relativo à raiz da documentação) | `README.md` |
| `appearance` | O esquema de cores: `light` (sempre claro) ou `auto` (segue o tema do VS Code) | `light` |
| `defaultLocale` | O idioma padrão (o idioma do documento canônico). Especificado com uma tag de idioma BCP 47 (`ja`, `en`, `zh-Hant` etc.). É a origem da tradução | Não definido (inferido do texto apenas para exibição) |
| `fallbackLocale` | O idioma mostrado primeiro aos leitores cujo idioma do ambiente de leitura não corresponde a nenhum dos idiomas suportados. Especifique um idioma incluído em `locales` | Não definido (usa `defaultLocale`) |
| `locales` | A lista de idiomas suportados. Inclua `defaultLocale`. Eles aparecem no menu de idiomas e são os destinos das traduções | Apenas `defaultLocale` |
| `ignoredDirectories` | Nomes de pastas excluídas do INDEX, da busca e das verificações. Especificá-lo substitui o padrão | `["99-archive"]` |
| `tree` | Os valores padrão da exibição do INDEX. O usuário pode substituí-los nas configurações de exibição | Como no exemplo acima |
| `editor.defaultMode` | A exibição de edição usada enquanto o usuário ainda não alternou: `visual` ou `source` | `visual` |
| `editor.showEditButton` | Se o botão [Editar] é exibido no canto inferior direito do documento | `true` |
| `documentStandards.pack` | O Standard Pack usado para a verificação de documentos e os modelos: `builtin:<nome>` ou um caminho relativo à raiz da documentação | Nenhum |
| `documentStandards.profile` | O nome de um perfil definido pelo Pack | Nenhum |
| `translation.enabled` | Ativa a criação de propostas de tradução e a tradução em lote | `true` |
| `translation.contextFiles` | Os arquivos Markdown canônicos (caminho relativo à raiz da documentação) passados na tradução como referência de terminologia e estilo | `[]` |
| `translation.maxContextCharacters` | O limite máximo do total de caracteres dos documentos de referência (máximo de 1048576) | `49152` |
| `description` | Uma descrição de uma linha do conjunto de documentos. Exibida no cartão da página inicial do repositório. Assim como `title`, pode ser escrita como uma string ou como um objeto por idioma | Nenhum |

## Informar onde os documentos estão no repositório

O `lunascape-docs.json` colocado diretamente na raiz do repositório pode conter, em vez das configurações daquela pasta, um **mapa do repositório**. Escrever qualquer um dos três campos a seguir o torna um mapa, e a própria pasta deixa de ser uma raiz da documentação.

| Campo | Conteúdo | Padrão |
|---|---|---|
| `defaultFolder` | Em que pasta estão os documentos (caminho relativo à raiz). A pasta indicada não precisa de arquivo de configuração próprio | Nenhum (usa `docs`) |
| `roots` | Quando houver vários conjuntos de documentos, a lista deles (caminhos relativos à raiz, em ordem de exibição). Nesse caso, a raiz torna-se a página inicial | Nenhum |
| `excludes` | Pastas a excluir da descoberta de raízes da documentação (caminhos relativos à raiz). Somadas às exclusões padrão, como `node_modules` | `[]` |
| `home.cards` | Se a página inicial exibe os cartões dos conjuntos de documentos abaixo do README. Defina como `false` quando você mesmo escrever os links no README | `true` |

A raiz da documentação é determinada na seguinte ordem. De cima para baixo, usa-se a primeira encontrada.

1. Quando uma pasta é indicada por uma configuração ou por um comando, essa pasta
2. O destino apontado por `defaultFolder` ou `roots` no `lunascape-docs.json` da raiz
3. A pasta que contém um `lunascape-docs.json` (se houver duas ou mais sob um mesmo pai, esse pai é a página inicial)
4. A pasta `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. A própria raiz do repositório

> **Dica**
>
> Se nada for escrito, o item 4 entra em ação, de modo que um repositório comum com um único `docs/` funciona como antes. Escreva `defaultFolder` apenas quando quiser que a pasta se chame `manual`.

### Exemplo de mapa

```json
{
  "title": "Ajuda do Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Ordem de precedência das configurações

Os campos relacionados à exibição têm precedência na seguinte ordem.

1. As configurações de exibição do usuário (painel [Configurações de exibição])
2. As configurações do VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Os valores padrão do produto

Apenas os idiomas (`defaultLocale`, `fallbackLocale`, `locales`) são exceção: o `lunascape-docs.json` é a fonte canônica. Não é possível substituir os idiomas do projeto pelas configurações pessoais do VS Code.

> **Nota**
>
> Um Standard Pack também pode ser especificado como `standard` no `docs-lint.config.json`. Quando estiver presente em ambos, o `docs-lint.config.json` tem precedência.

## Itens relacionados

- [Alterar as regras de verificação](rules.md)
- [Alterar as configurações de exibição](../02-reading/display-settings.md)
- [Lista de configurações do VS Code](../08-reference/settings.md)
