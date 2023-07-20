# Documentação do Console Interativo Prefixo-Wine

## Descrição

Este é um script de shell que simula um console interativo para gerenciar um ambiente Wine com diferentes arquiteturas (Win32 ou Win64). Ele oferece uma série de comandos que permitem ao usuário interagir com o ambiente Wine, executar programas integrados, exibir informações sobre arquivos/diretórios e importar scripts .sh para estender o console.

## Uso

Antes de iniciar o console simulado, o usuário será solicitado a escolher a arquitetura do Wine (Win32 ou Win64). Em seguida, o console será iniciado e o usuário poderá digitar comandos e visualizar resultados conforme necessário.

### Comandos disponíveis

- `ajuda`: Exibe uma mensagem de ajuda com a lista de comandos disponíveis.
- `limpar`: Limpa a tela do console.
- `sair`: Sai do console e encerra a execução do script.
- `variaveis`: Lista informações sobre o prefixo do Wine atual, incluindo o caminho para o prefixo, a arquitetura do prefixo Wine e o diretório de comandos built-in.
- `informacoes <arquivo/diretorio>`: Exibe informações detalhadas sobre um arquivo ou diretório, incluindo tipo, tamanho, permissões, proprietário, grupo, último acesso e última modificação.
- `importar <caminho_do_script.sh>`: Importa um script .sh para estender o console com novas funcionalidades.
- `programas`: Lista os programas built-in do Wine e permite que o usuário escolha um para executar.

## Funções

O script possui as seguintes funções:

### `exibir_prompt()`

Exibe o prompt de comando personalizado, mostrando o prefixo, o diretório atual e um símbolo "$" no final.

### `exibir_ajuda()`

Exibe uma mensagem de boas-vindas e a lista de comandos disponíveis no console simulado.

### `variaveis()`

Exibe informações sobre o prefixo do Wine atual, incluindo o caminho para o prefixo, a arquitetura do prefixo Wine e o diretório de comandos built-in.

### `programas()`

Lista os programas built-in do Wine e permite que o usuário escolha um para executar. Os programas incluem WineCFG, Gerenciador de Tarefas, Bloco de Notas, Editor de Registro, Prompt de Comando, Painel de Controle e Internet Explorer.

### `informacoes()`

Exibe informações detalhadas sobre um arquivo ou diretório especificado pelo usuário. As informações incluem o tipo, tamanho, permissões, proprietário, grupo, último acesso e última modificação.

### `importar()`

Importa um script .sh para estender o console com novas funcionalidades. O usuário deve fornecer o caminho completo do script que deseja importar.

### `console()`

Função principal do console simulado. Exibe o prompt e permite que o usuário digite comandos. Os comandos digitados são interpretados pelo script e executados conforme a função correspondente.

## Configuração do Ambiente Wine

Antes de iniciar o console, o script solicitará que o usuário escolha a arquitetura do Wine (Win32 ou Win64). Com base na escolha, o script definirá as variáveis `$WINEARQUI` e `$WINEPREFIXO`, que são usadas para configurar o ambiente Wine.

## Como executar o console simulado

1. Salve o código do script em um arquivo chamado `console_wine.sh`.
2. No terminal, navegue até o diretório onde o arquivo `console_wine.sh` foi salvo.
3. Torne o arquivo executável com o seguinte comando:

```bash
chmod +x console_wine.sh
```

1. Execute o console simulado com o seguinte comando:
2. O script solicitará que você escolha a arquitetura do Wine (Win32 ou Win64). Digite o número correspondente e pressione Enter.
3. O console simulado será iniciado e você poderá digitar os comandos disponíveis.
