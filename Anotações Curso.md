# 📚 Anotações de Aprofundamento no Git

Este arquivo resume os principais tópicos e comandos de Git, organizados para consulta rápida.

---

## 1. Fundamentos do Git e Operações Iniciais

### O que é Git?
O **Git** é um **Sistema de Controle de Versão Distribuído (DVCS)** que rastreia e gerencia todas as mudanças no código ao longo do tempo. É a "máquina do tempo" do seu projeto.

### Diferença entre Git e GitHub
* **Git:** O **software** instalado localmente para controle de versão.
* **GitHub (GitLab/Bitbucket):** Um **serviço de hospedagem online** para armazenar repositórios na nuvem, facilitando backup e colaboração.

### Instalação e Configuração
Comandos essenciais para identificar o autor dos seus commits:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```
### Fluxo de Trabalho Básico
1.  **Criar Repositório:** `git init` (inicializa a pasta como um repositório Git).
2.  **Preparar Mudanças (Staging Area):** `git add nome_do_arquivo` ou `git add .` (seleciona as mudanças para o próximo commit).
3.  **Salvar Versão (Commit):** `git commit -m "Mensagem clara descrevendo o que foi feito"`

### Branches (Ramos)
* **Conceito:** Linhas de desenvolvimento isoladas.
* **Função:** Permite desenvolver funcionalidades ou corrigir bugs sem afetar a versão principal estável.
* **Criar e Trocar:**
    ```bash
    git checkout -b nome_da_nova_branch  # Cria e muda para a nova branch
    ```
* **Fusão (Merge):**
    ```bash
    git checkout branch_destino # Ex: main
    git merge branch_fonte      # Traz as mudanças da fonte para o destino
    ```

### Ajuda
* **Documentação:** Use `git help comando` ou `git comando --help` (Ex: `git help commit`).

---

## 2. Aprofundando no Git e Controle Avançado

### Gitignore
* **Arquivo:** `.gitignore`
* **Função:** Lista arquivos e pastas (ex: logs, dependências como `node_modules`) que o Git deve **ignorar** e não rastrear.

### Corrigindo o Último Commit
* **Comando:** `git commit --amend -m "Nova Mensagem"`
* **Uso:** Altera a mensagem do último commit. Se não mudar a mensagem, permite adicionar arquivos que foram esquecidos no commit anterior.

### Voltando no Tempo (Undo)

| Comando | Descrição | Uso Recomendado |
| :--- | :--- | :--- |
| **`git reset --hard HASH`** | Move o HEAD e **apaga** as mudanças locais. | Para commits **locais** que ainda não foram compartilhados. |
| **`git revert HASH`** | Cria um **novo commit** que desfaz o commit alvo. | Para commits que **já foram compartilhados** (mais seguro). |

### Saber Diferença entre Commits
* **Comando:** `git diff HASH1 HASH2`
* **Função:** Mostra exatamente o que mudou (linhas adicionadas/removidas) entre dois pontos da história.

### Jogando Nova Funcionalidade (Pushing)
* **Comando:** `git push`
* **Função:** Envia os commits da sua máquina local para o repositório remoto (ex: GitHub).

### Resolvendo Conflito de Merge
* **Ocorrência:** Quando o Git não consegue integrar automaticamente mudanças feitas no mesmo trecho de código em duas branches.
* **Passos para Resolver:**
    1.  **Edição Manual:** Abra o arquivo e remova os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`), escolhendo o código final.
    2.  **Adicionar:** `git add arquivo_conflitado`
    3.  **Finalizar:** `git commit` (para registrar a resolução do conflito).
