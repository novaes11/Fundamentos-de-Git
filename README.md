# 🎓 Resumo de Habilidades em Controle de Versão (Git Local)

**Curso:** Aprofundamento em Git (B7web, Prof. Bonieky)

Este resumo detalha as competências e técnicas avançadas em **Git** adquiridas, demonstrando proficiência no gerenciamento do histórico de código, controle de versões e manipulação do desenvolvimento em ambientes isolados.

---

## 1. Fundamentos e Gestão do Histórico

### Setup e Fluxo de Trabalho
* **Configuração de Identidade:** Domínio dos comandos `git config` para definir e manter a autoria dos **commits** (nome e e-mail).
* **Iniciação e Rastreamento:** Habilidade em inicializar um novo repositório com `git init` e aplicar o fluxo de trabalho fundamental:
    * `git add`: Preparar mudanças na **Staging Area**.
    * `git commit`: Criar *snapshots* (versões) do projeto com mensagens claras.
* **Otimização do Repositório:** Proficiência na criação e uso do arquivo **`.gitignore`** para listar e excluir arquivos não essenciais do rastreamento.

### Inspeção e Correção de Commits
* **Inspeção de Diferenças:** Uso eficaz do comando **`git diff`** para comparar as alterações entre o diretório de trabalho, a *Staging Area* e *commits* específicos.
* **Correção de Mensagem:** Capacidade de corrigir e refinar o último *commit* (mensagem ou inclusão de arquivos esquecidos) utilizando **`git commit --amend`**.

---

## 2. Técnicas de Branches e Reversão

### Gestão de Branches
* **Desenvolvimento Isolado:** Compreensão e aplicação da estratégia de **branches** (ramos) como linhas de desenvolvimento independentes.
* **Criação e Navegação:** Proficiência em criar novas branches (`git checkout -b`) e alternar entre elas (`git checkout nome_da_branch`) para isolar o desenvolvimento de novas funcionalidades ou correções (*hotfixes*).

### Integração e Conflitos
* **Fusão de Históricos:** Habilidade em integrar mudanças de uma branch para outra utilizando **`git merge`**.
* **Resolução de Conflitos:** Competência crítica na **resolução manual de conflitos de *merge***. Isso inclui entender, editar as marcações de conflito nos arquivos e usar `git add` e `git commit` para finalizar a fusão.

### Desfazer Mudanças
* **Reversão Segura (`git revert`):** Habilidade em desfazer mudanças registradas no histórico, criando um **novo *commit*** de reversão, mantendo a integridade do histórico.
* **Reescrita Local (`git reset`):** Uso de **`git reset --hard`** para mover o ponteiro do histórico, descartando *commits* e alterações no ambiente de trabalho local (aplicado em ambientes não compartilhados).
