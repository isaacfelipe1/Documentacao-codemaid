# 🧹 Guia de Instalação e Configuração: CodeMaid no Visual Studio

O **CodeMaid** é uma extensão de código aberto para o Visual Studio que ajuda a limpar, organizar e simplificar o seu código. Este guia foca na utilização do CodeMaid para projetos **.NET com C#**, garantindo que a formatação da sua equipe fique sempre padronizada.

---

## 📋 Pré-requisitos

* **Visual Studio** (2017, 2019 ou 2022) instalado.
* Um projeto .NET com arquivos em C# (`.cs`).

---

## 🚀 Como Instalar o CodeMaid

Existem duas maneiras de instalar a extensão. A instalação direta pelo Visual Studio é a mais rápida e recomendada.

### Método 1: Pelo Visual Studio (Recomendado)

1. Abra o Visual Studio.
2. Na barra de menus superior, clique em **Extensões** (ou *Extensions*).
3. Selecione **Gerenciar Extensões** (*Manage Extensions*).
4. No menu lateral esquerdo, clique em **Online** e pesquise por `CodeMaid` na barra de busca (canto superior direito).
5. Encontre o **CodeMaid** na lista e clique no botão **Baixar** (*Download*).
6. **Feche o Visual Studio.** A janela do instalador (VSIX) abrirá automaticamente.
7. Clique em **Modify** (Modificar) para concluir a instalação.
8. Abra o Visual Studio novamente e a extensão estará pronta para uso!

### Método 2: Pelo Visual Studio Marketplace

1. Acesse a página do [CodeMaid no Marketplace](https://marketplace.visualstudio.com/items?itemName=SteveCadwallader.CodeMaid).
2. Clique em **Download** para baixar o arquivo `.vsix`.
3. Com o Visual Studio fechado, dê um duplo clique no arquivo baixado e siga as instruções na tela.

---

## ⚙️ Configurações Recomendadas para C#

Para tirar o máximo proveito da extensão no dia a dia do desenvolvimento .NET, recomendamos configurar a **limpeza automática ao salvar o arquivo**.

1. No Visual Studio, vá em **Extensões > CodeMaid > Options** (Opções).
2. No menu lateral da janela do CodeMaid, vá até **Cleaning** (Limpeza) > **General** (Geral).
3. Marque a opção: `[x] Automatically run cleanup on file save` (Executar limpeza automaticamente ao salvar o arquivo).
4. Em **Cleaning** > **Visual Studio**, certifique-se de que a opção `[x] Run format document` está marcada. Isso garante que as regras de formatação nativas do C# sejam aplicadas antes da limpeza do CodeMaid.
5. Clique em **Save** (Salvar).

> **💡 Dica:** Com essa configuração, toda vez que você apertar `Ctrl + S`, o CodeMaid vai formatar a indentação, remover espaços em branco desnecessários e organizar os `using`s automaticamente.

---

## ⌨️ Principais Atalhos (Shortcuts)

Se você preferir executar a limpeza manualmente ou usar outros recursos, aqui estão os atalhos mais úteis:

| Ação | Atalho | Descrição |
| :--- | :--- | :--- |
| **Limpar o Documento Ativo** | `Ctrl+M, Espaço` | Executa a limpeza completa (remove usings não utilizados, alinha chaves, formata) no arquivo atual. |
| **Limpar Todos os Documentos** | `Ctrl+M, Shift+Espaço` | Aplica a limpeza em todos os arquivos abertos no Visual Studio. |
| **Abrir o Spade** | `Ctrl+M, ,` | Abre a janela de visualização do CodeMaid (Spade), que permite reorganizar métodos e propriedades com facilidade. |
| **Reorganizar Documento** | `Ctrl+M, Z` | Reorganiza o arquivo ativo de acordo com as regras de ordem do C# (campos, construtores, propriedades, métodos). |

---

## 🏗️ O que a limpeza (Cleanup) faz no C#?

Ao executar a limpeza no seu projeto `.NET`, o CodeMaid realiza (por padrão) as seguintes tarefas:

* **Remove blocos de `using`** que não estão sendo utilizados.
* **Ordena os `using`s** em ordem alfabética (colocando `System` no topo, se configurado).
* **Remove espaços em branco** no final de linhas ou linhas em branco consecutivas.
* **Adiciona modificadores de acesso** não especificados (ex: adiciona `private` implicitamente a métodos que não tem modificador).
* Formata o documento utilizando o padrão configurado no Visual Studio (`.editorconfig`).

---

## 🤝 Contribuindo

Sinta-se à vontade para abrir uma *Issue* ou enviar um *Pull Request* caso queira adicionar novas dicas de configuração do CodeMaid a este documento!