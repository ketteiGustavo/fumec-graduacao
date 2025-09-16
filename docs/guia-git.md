# 🚀 Guia Rápido de Git

Este guia é para iniciantes que vão contribuir neste repositório.
Aqui estão os comandos mais usados no dia a dia.

---

## 🔍 Verificar o status do repositório
Mostra arquivos modificados e não versionados.

```bash
git status
```

---

## ➕ Adicionar arquivos para commit
Adiciona todos os arquivos modificados:

```bash
git add .
```

Ou apenas um arquivo específico:

```bash
git add caminho/arquivo.txt
```

---

## 💾 Fazer um commit
Cria um ponto de salvamento no histórico.

```bash
git commit -m "feat: adiciona funcionalidade X"
```

---

## ⬆️ Enviar alterações para o GitHub
```bash
git push origin nome-da-branch
```

---

## ⬇️ Puxar atualizações do repositório remoto
```bash
git pull origin develop
```

---

## ❌ Desfazer alterações
- Descartar mudanças em um arquivo:
```bash
git checkout -- caminho/arquivo.txt
```

- Desfazer último commit mas manter alterações no diretório:
```bash
git reset --soft HEAD~1
```

- Desfazer último commit e também descartar alterações:
```bash
git reset --hard HEAD~1
```

---

## 🌱 Criar uma nova branch
```bash
git checkout -b feature/nome-da-tarefa
```

---

## 🔀 Fazer merge de uma branch
Primeiro vá para a branch de destino (ex: `develop`):

```bash
git checkout develop
git merge feature/nome-da-tarefa
```

---

## 🔄 Resolver conflitos de merge
1. Edite os arquivos marcados com `<<<<<<<`, `=======`, `>>>>>>>`.
2. Após resolver:
```bash
git add arquivo_resolvido.txt
git commit
```

---

## 📥 Criar um Pull Request (PR)
1. Envie sua branch para o GitHub:
```bash
git push origin feature/nome-da-tarefa
```
2. Abra a página do repositório no GitHub.
3. Clique em **Compare & Pull Request**.
4. Descreva suas mudanças e crie o PR.

---

## 🍒 Usar cherry-pick
Aplica um commit específico de outra branch na branch atual.

```bash
git cherry-pick <hash-do-commit>
```

---

## 🗑️ Apagar uma branch
- Local:
```bash
git branch -d feature/nome-da-tarefa
```

- Remoto:
```bash
git push origin --delete feature/nome-da-tarefa
```

---

## 📚 Dicas úteis
- Ver histórico de commits:
```bash
git log --oneline --graph --decorate --all
```

- Mostrar diferenças:
```bash
git diff
```

- Configurar usuário:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```
