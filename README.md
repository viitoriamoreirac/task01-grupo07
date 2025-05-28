# Documentação de alguns comandos git

## comando 1

## 📚 Git Cherry-Pick

#### 🧩 O que é `git Cherry-Pick` 

O comando `git cherry-pick` é usado para **aplicar commits específicos de uma branch em outra**. Ele é útil quando você quer trazer uma mudança feita em um commit isolado para outra linha de desenvolvimento, sem fazer um merge completo.

---

## 📌 Funcionamento

O `git cherry-pick` copia o conteúdo de um commit específico (ou uma sequência de commits) e o aplica na branch atual como um novo commit.

Esse comando **não mescla** historicamente as branches. Ele apenas aplica o conteúdo do commit escolhido como se fosse uma nova alteração feita na branch atual.

---

## 🧾 Sintaxe

```bash
git cherry-pick <commit>
```

## 📚 Git Revert

### 🧩 O que é `git revert`?

O **Git Revert** é um comando usado para **desfazer um commit específico**, criando um **novo commit** que reverte as alterações feitas anteriormente.  
Diferente de comandos que reescrevem o histórico (como `git reset`), o `git revert` é **seguro para uso em repositórios compartilhados**, pois preserva todo o histórico do projeto.

---

### ⚙️ Funcionamento

Ao utilizar `git revert`, o Git gera um novo commit que contém as alterações contrárias ao commit alvo.  
Isso significa que o conteúdo do commit selecionado será desfeito, **mas o commit original ainda estará presente no histórico**.

Ideal para corrigir erros sem impactar o trabalho de outros colaboradores que já possam ter feito *pull* ou *clone* do repositório.

---

### 🖊️ Sintaxe

```bash
git revert <hash-do-commit>
```
## 📚 Git Squash

### 🧩 O que é `git squash`?

O **Git Squash** é uma técnica usada para **combinar múltiplos commits em um só**. Isso é útil para manter o histórico do projeto mais limpo e organizado, especialmente ao finalizar uma feature ou corrigir uma sequência de erros antes de fazer o merge para a branch principal.

---

### ⚙️ Funcionamento

O `squash` faz parte do comando `git rebase`, mais especificamente em um **rebase interativo** (`git rebase -i`).

Durante o rebase interativo, você pode escolher combinar (`squash`) commits. Isso significa que os commits selecionados serão agrupados em um único commit, unificando suas alterações e mensagens (caso queira).

---

### 🖊️ Sintaxe

```bash
git rebase -i <commit-base>
