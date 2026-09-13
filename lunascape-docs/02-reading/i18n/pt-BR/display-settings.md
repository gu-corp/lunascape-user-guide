# Alterar as configurações de exibição

Em [Configurações de exibição] (engrenagem), na barra de ferramentas, cada usuário pode alterar a aparência do INDEX e a exibição do botão de edição.

1. Pressione [Configurações de exibição] na barra de ferramentas.
2. Alterne os itens que deseja modificar. As alterações são aplicadas imediatamente.
3. Pressione [Configurações de exibição] novamente ou clique fora do painel para fechá-lo.

## Itens configuráveis

| Seção | Item | Função |
|---|---|---|
| Idioma do documento | (estado atual) | Mostra o idioma padrão do projeto e o idioma em exibição. [Definir os idiomas do projeto…] abre as configurações de idioma do projeto |
| Conteúdo | [Nomes de arquivo] | Mostra o nome do arquivo em vez do nome do documento |
| | [Ícones de documento] | Mostra um ícone nos itens de documento |
| | [Ícones de pasta] | Mostra um ícone nos itens de pasta |
| | [Número de itens na pasta] | Mostra a quantidade de documentos contidos na pasta |
| | [Guias de hierarquia] | Mostra linhas-guia que indicam a hierarquia |
| | [Ocultar automaticamente se houver apenas um documento] | Fecha o INDEX automaticamente, apenas na primeira vez, em uma raiz da documentação com um único documento |
| | [Recolher as informações do documento] | Recolhe a tabela de controle no início do documento em uma linha “Informações do documento”. Quando desativado, a tabela é exibida como está |
| | [Densidade de exibição] | Escolhe o espaçamento entre as linhas do INDEX: [Normal] / [Compacta] |
| | [Botão de edição] | Mostra [Editar] no canto inferior direito do texto |
| Ações | [Restaurar os padrões do projeto] | Apaga todas as alterações do usuário e volta às configurações do projeto |
| | [Abrir as configurações da extensão] | Abre as configurações do Lunascape Docs na tela de configurações do VS Code |

> **Dica**
>
> - As configurações de exibição são salvas por usuário e por raiz da documentação, e não são gravadas em arquivos controlados pelo Git.
> - As configurações têm a seguinte ordem de prioridade: “configurações de exibição do usuário → configurações do VS Code → `lunascape-docs.json` → padrões do produto”. Os padrões comuns da equipe são definidos em `tree` e `editor` no `lunascape-docs.json`.

## Alternar o esquema de cores

Pressione o alternador de tema (sol/lua) na barra de ferramentas para alternar entre o fundo branco e o esquema de cores do VS Code. O esquema usado na abertura é determinado pela configuração `lunascapeDocEditor.appearance` (`light` ou `auto`).

## Tópicos relacionados

- [Usar o INDEX](index-panel.md)
- [Configurações do projeto](../04-document-tools/project-configuration.md)
- [Lista de configurações do VS Code](../08-reference/settings.md)
