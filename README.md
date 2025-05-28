# Documentação de alguns comandos git

## comando 1

## comando 2

## comando 3


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
