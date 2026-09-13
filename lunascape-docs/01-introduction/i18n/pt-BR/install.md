# Instalar a extensão

A extensão do VS Code "Lunascape Docs Pro" é distribuída como um arquivo VSIX. É gratuita; "Pro" indica a edição que entrega o trabalho a uma IA e se atualiza sozinha.

## Requisitos

- VS Code 1.90 ou posterior
- Os recursos que gravam arquivos — criar documentos, organizar o INDEX, salvar configurações de verificação, traduzir — funcionam apenas em um espaço de trabalho que você tenha marcado como confiável no VS Code.

## Instalar

1. Obtenha o arquivo VSIX. Este link aponta sempre para a versão mais recente.

   [Baixar lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Abra a visão de extensões (`⇧⌘X` / `Ctrl+Shift+X`).
3. No menu `…` no canto superior direito, escolha [Instalar do VSIX...] e indique o arquivo que você baixou.

### Pela linha de comando

Em uma única linha, se você preferir não sair do terminal. Ela baixa e instala.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Nota**
> Se `code` não for encontrado, execute [Shell Command: Instalar o comando 'code' no PATH] na paleta de comandos (`⇧⌘P` / `Ctrl+Shift+P`).

## Atualizar

Quando uma versão mais recente é publicada, a extensão a obtém e instala sozinha. O VS Code sugere recarregar a janela, e é nesse momento que a mudança entra em vigor. Suas configurações e documentos permanecem como estão.

A verificação ocorre uma vez por dia. Para verificar agora mesmo, execute [Lunascape Docs: Verificar atualizações] na paleta de comandos (`⇧⌘P` / `Ctrl+Shift+P`).

O comportamento pode ser alterado pela configuração `lunascapeDocEditor.update.check`.

| Configuração | Comportamento |
|---|---|
| Instalar uma versão mais recente quando for publicada | Padrão |
| Avisar e deixar que eu decida a cada vez | Aparece uma notificação, e nada muda até você pressionar [Atualizar] |
| Nunca verificar | Nada acontece |

### Quando não é possível atualizar

Se aparecer "Não foi possível obter a atualização: No Servers", a versão instalada é a 0.22.18 ou anterior. O recurso de atualização dessa versão falha sempre na última etapa após a obtenção, de modo que ela não consegue se atualizar sozinha. Reinstale à mão uma única vez, conforme o procedimento acima; a partir daí, ela se atualiza sozinha.

## Verificar a versão

Abra "Lunascape Docs Pro" na visão de extensões para ver a versão instalada. Você precisará dela ao relatar um problema.

## Tópicos relacionados

- [Criar seus primeiros documentos](first-documents.md)
- [Relatar um problema](../07-troubleshooting/report.md)
