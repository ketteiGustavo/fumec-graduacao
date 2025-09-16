# Graduação Fumec

## 📝 Descrição

Repositório voltado a pratica de git e controle de código, bem como projetos e atividades de programação.

Este repositório foi criado para centralizar o desenvolvimento de projetos e atividades da graduação. O objetivo é que todos possam colaborar de forma organizada, aprendendo e aplicando os conceitos de Git e GitHub.

[![Maintained](https://img.shields.io/maintenance/yes/2025?style=flat-square&label=mantido)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-bem_vindos-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Conventional Commits](https://img.shields.io/badge/commits-conventional-blue.svg?style=flat-square)](https://www.conventionalcommits.org/pt-br/v1.0.0/)
[![Changelog](https://img.shields.io/badge/Changelog-MD-blueviolet.svg?style=flat-square)](./CHANGELOG.md)
[![Code of Conduct](https://img.shields.io/badge/code%20of%20conduct-v1.4-orange.svg?style=flat-square)](./CODE_OF_CONDUCT.md)
[![Contributing](https://img.shields.io/badge/Contribuir-Guia-blue.svg?style=flat-square)](./CONTRIBUTING.md)



<div align="center">
  Nos ajude com esse projeto
  <br />
  <br />
  <a href="https://github.com/ketteiGustavo/fumec-graduacao/issues/new?assignees=&labels=&projects=&template=bug_report.md&title=">Reporte um Bug</a>
  ·
  <a href="https://github.com/ketteiGustavo/fumec-graduacao/issues/new?assignees=&labels=&projects=&template=solicitar_recurso.md&title=">Solicitar um Recurso</a>
  ·
  <a href="https://github.com/ketteiGustavo/fumec-graduacao/discussions">Faça uma pergunta</a>
</div>

<div align="center">
<br />
</div>

## ⚙️ Pré-requisitos

Antes de começar, você precisa ter o Git instalado na sua máquina.
- **Para instalar o Git:** [Clique aqui para baixar](https://git-scm.com/downloads)
- **Git para Windows:** Caso esteja no Windows, recomendamos instalar o Git for Windows, que já vem com o Git Bash, facilitando o uso de comandos no terminal.
- Para verificar se a instalação funcionou, abra um terminal e digite:
  ```bash
  git --version
  ```

## 🚀 Começando (Primeiro Acesso)

Para ter uma cópia do projeto na sua máquina, você precisa "clonar" o repositório.

1.  Abra um terminal ou a pasta onde você quer salvar o projeto.
2.  Execute o comando abaixo (copie a URL do repositório no próprio GitHub, no botão "Code"):

    ```bash
    git clone https://github.com/seu-usuario/graduacao-fumec.git
    ```
3.  Acesse a pasta que foi criada:
    ```bash
    cd graduacao-fumec
    ```

Pronto! Agora você tem o projeto localmente.

## 🌟 Adicionando e Divulgando Novos Projetos

Qualquer membro pode adicionar novos projetos ou atividades neste repositório.

1.  **Crie uma Nova Pasta:** Dentro do repositório, crie uma pasta com o nome do seu projeto (ex: `calculadora-cientifica`).
2.  **Adicione a Documentação:** Dentro da pasta do seu projeto, crie uma subpasta chamada `docs` e adicione um arquivo `README.md` explicando do que se trata seu projeto, como executá-lo, etc.
3.  **Divulgue no README Principal (Opcional):** Se quiser que seu projeto tenha visibilidade na página inicial, edite este `README.md` principal, adicionando um link para a pasta do seu projeto. Depois, siga o fluxo de contribuição normal (crie uma branch, commite a alteração e abra um Pull Request).

## 🌊 Fluxo de Trabalho (Workflow)

Para manter nosso projeto organizado, vamos usar um fluxo de trabalho simples baseado em branches.

- **`main`**: Esta branch contém a versão estável e final do repositório. Ninguém deve enviar código diretamente para ela. Ela só é atualizada a partir da `staging`.
- **`develop`**: Esta é a nossa branch principal de desenvolvimento. Todas as novas funcionalidades, projetos e correções partem dela e voltam para ela.
- **`staging`**: Esta branch é uma cópia de segurança da branch `main`. E tudo que vai subir para `main`, deve passar em `staging`, testado e aprovado.
- **`feature/nome-da-tarefa`**: Sempre que você for trabalhar em algo novo (um projeto, uma função, uma correção), você vai criar uma branch a partir da `develop` com esse padrão de nome.

O ciclo é: `develop` -> cria sua `feature` -> finaliza -> junta com a `develop` de novo.

## 📖 Passo a Passo para Contribuir

Siga estes passos sempre que for começar a trabalhar em uma nova tarefa.

**Passo 1: Sincronize seu repositório local com o remoto**

Antes de criar uma nova branch, garanta que sua `develop` local está atualizada.

```bash
# Mude para a branch develop
git checkout develop

# Puxe as últimas atualizações do repositório remoto
git pull origin develop
```

**Passo 2: Crie uma nova branch para sua tarefa**

Crie uma branch a partir da `develop`. Use um nome claro e descritivo.

```bash
# O comando -b já cria a branch e muda para ela
git checkout -b feature/exemplo-login-usuario
```

**Passo 3: Faça suas alterações**

Agora é a hora de codificar! Crie, edite e delete os arquivos necessários para a sua tarefa.

**Passo 4: Salve suas alterações (Commit)**

Quando terminar (ou atingir um ponto que faça sentido salvar), adicione e "commite" suas alterações seguindo o padrão de **Commits Convencionais**.

```bash
# Adiciona todos os arquivos modificados para serem salvos
git add .

# Salva as alterações com uma mensagem padronizada
git commit -m "feat: adiciona tela de login inicial"
```
> ### Padrão de Commits Convencionais
> A mensagem de commit deve seguir o formato: `<tipo>(<escopo>): <assunto>`
> - **Tipos comuns:**
>   - `feat`: Uma nova funcionalidade.
>   - `fix`: Uma correção de bug.
>   - `docs`: Alterações na documentação.
>   - `style`: Alterações de formatação, sem impacto no código (ponto e vírgula, etc).
>   - `refactor`: Refatoração de código que não corrige bug nem adiciona feature.
>   - `test`: Adicionando ou corrigindo testes.
>   - `chore`: Atualização de tarefas de build, pacotes, etc.
> - **Exemplos:**
>   - `git commit -m "feat(login): adiciona autenticação com Google"`
>   - `git commit -m "fix: corrige cálculo de imposto na tela de checkout"`
>   - `git commit -m "docs: atualiza guia de instalação"`
> - **Todos os Padrões de Commit**
>   - Para acessar todos os padrões de commit, cliquei em [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)

**Passo 5: Envie sua branch para o GitHub**

Envie as alterações da sua branch local para o repositório remoto.

```bash
git push origin feature/exemplo-login-usuario
```

**Passo 6: Crie um Pull Request (PR)**

Agora que suas alterações estão no GitHub, você precisa pedir para que elas sejam incorporadas na `develop`.

1.  Vá para a página do repositório no GitHub.
2.  O GitHub geralmente mostrará um aviso para criar um **Pull Request**. Clique nele.
3.  **Base:** `develop` | **Compare:** `sua-feature-branch`
4.  Escreva um título e uma descrição para o seu Pull Request, explicando o que você fez.
5.  Clique em "Create Pull Request".

**Passo 7: Revisão e Merge**

Outro colega irá revisar o código e, se estiver tudo certo, fará o "merge" do seu Pull Request. Isso irá juntar suas alterações com a branch `develop`.

**Passo 8: Limpeza (Opcional, mas recomendado)**

Depois que seu PR for aprovado e "mergido", você pode apagar sua branch local.

```bash
# Volte para a develop
git checkout develop

# Atualize-a novamente
git pull origin develop

# Apague a branch que não será mais usada
git branch -d feature/exemplo-login-usuario
```

## 📚 Documentação

- [Guia de Markdown](./docs/guia-markdown.md): aprenda a escrever arquivos **.md** para documentar seus projetos.
- [Guia de Uso Git](./docs/guia-git.md): aprenda alguns comandos básicos de GIT para contribuir com o projeto.
