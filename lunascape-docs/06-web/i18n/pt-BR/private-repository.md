# Ler um repositório privado

Depois de entrar com o GitHub, você pode ler os documentos de repositórios privados, limitados àqueles aos quais você tem acesso de leitura. O Lunascape Docs nunca tem contas nem permissões próprias.

## Entrar e abrir

1. Abra <https://docs.lunascape.org/>.
   Quando você indica um documento privado ou ainda não entrou, a tela de entrada aparece.
2. Pressione [Entrar com o GitHub].
   A tela de autorização do GitHub abre em uma janela pop-up.
3. Depois de entrar, pressione [Abrir documentos] na barra de ferramentas e escolha o repositório em [Escolher entre repositórios legíveis].

> **Dica**
>
> - A conta com que você entrou é mostrada na barra de ferramentas, onde você também pode [Sair] ou [Entrar com outra conta].
> - A lista mostra os repositórios das contas (organizações ou pessoas) em que o GitHub App "Lunascape Docs" está instalado, limitados àqueles que você pode ler.

## Configuração feita pelo proprietário do repositório

Se o repositório não aparecer na lista, o proprietário do repositório ou um administrador da organização precisa instalar o GitHub App "Lunascape Docs".

- As permissões solicitadas são Contents (leitura e escrita) e Pull requests (leitura e escrita). A leitura serve para o acesso aos documentos; a escrita serve para enviar a solicitação de publicação (Pull Request) a partir da Web. O Lunascape Docs nunca armazena o conteúdo dos documentos.
- A instalação é feita por conta (organização ou pessoa). Escolha entre "All repositories" (que inclui automaticamente os repositórios criados depois) ou apenas os repositórios selecionados.

| Situação | Procedimento |
|---|---|
| Instalar em uma nova organização ou conta pessoal | Faça isso a partir da [página de instalação](https://github.com/apps/lunascape-docs/installations/new) |
| Adicionar repositórios em uma organização que já tem o app | Configure em Settings da organização → GitHub Apps → Lunascape Docs → Configure → Repository access |

Mesmo que o app seja instalado para toda a organização, cada membro só consegue ver os repositórios aos quais tem acesso de leitura. Também só pode enviar uma solicitação de publicação para os repositórios aos quais tem acesso de escrita.

> **Dica**
> - Em uma nova instalação, as permissões solicitadas são exibidas em uma lista na tela de instalação, e pressionar "Install" equivale a aprová-las. Não é necessária nenhuma outra ação.
> - Uma organização que já tinha o app instalado antes de uma permissão ser adicionada recebe um e-mail de confirmação aos administradores, e um botão de aprovação aparece no topo de Settings da organização → GitHub Apps → Lunascape Docs → Configure. Até a aprovação, essa organização só consegue ler; ao enviar uma solicitação de publicação, aparece "é necessário conceder permissão de escrita".
> - Você pode conferir com quais permissões o app está instalado atualmente na mesma tela Configure. No caso de uma conta pessoal, é Settings → Applications → Installed GitHub Apps.
> - Se você remover por engano um repositório da seleção ou desinstalar o app, basta instalá-lo novamente a partir da [página de instalação](https://github.com/apps/lunascape-docs/installations/new) para voltar ao estado anterior. A mensagem de recusa da solicitação de publicação inclui um link para a tela onde isso é corrigido.
> - Se o repositório não deve aceitar solicitações de publicação, escreva `"publish": { "enabled": false }` em `lunascape-docs.json`. A leitura continua funcionando normalmente.

## Tópicos relacionados

- [Abrir um repositório do GitHub](open-repository.md)
- [Não é possível abrir ou entrar na versão Web](../07-troubleshooting/web.md)
