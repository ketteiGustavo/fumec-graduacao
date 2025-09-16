# 📦 Extensões do VS Code — Guia Rápido

Este guia descreve as extensões recomendadas para o repositório **Graduação FUMEC**, com o *porquê usar*, *como usar*, e *configurações sugeridas*.
Quando você abrir o projeto no VS Code, as extensões serão sugeridas automaticamente (arquivo `.vscode/extensions.json`).

---

## 📑 Sumário
- [📦 Extensões do VS Code — Guia Rápido](#-extensões-do-vs-code--guia-rápido)
  - [📑 Sumário](#-sumário)
  - [EditorConfig for VS Code](#editorconfig-for-vs-code)
  - [Markdown All in One](#markdown-all-in-one)
  - [Prettier – Code formatter](#prettier--code-formatter)
  - [GitLens](#gitlens)
  - [GitHub Pull Requests](#github-pull-requests)
  - [Emoji Sense](#emoji-sense)
  - [Better Align](#better-align)
  - [Better Comments](#better-comments)
  - [CodeSnap](#codesnap)
  - [TODO Highlight](#todo-highlight)
  - [Trailing Spaces](#trailing-spaces)
  - [Dicas rápidas](#dicas-rápidas)

---

## EditorConfig for VS Code
**ID:** `editorconfig.editorconfig`

**Por que usar:** aplica automaticamente as regras do `.editorconfig` (indentação, charset, LF).
**Como usar:** nada a fazer — apenas mantenha o arquivo `.editorconfig` na raiz do projeto.

**Configurações já no repositório:** `.editorconfig` define `indent_size=4`, `end_of_line=lf`, `trim_trailing_whitespace=true`, e exceções para `*.md`.

---

## Markdown All in One
**ID:** `yzhang.markdown-all-in-one`

**Por que usar:** atalhos e melhorias para edição de Markdown (`.md`), incluindo TOC, preview e formatação.
**Dica:** `Ctrl+Shift+V` abre o preview; `Alt+Shift+F` formata Markdown (com Prettier instalado).

**Sugestões de settings:**
```json
{
  "[markdown]": {
    "editor.wordWrap": "on",
    "editor.quickSuggestions": { "other": true, "comments": true, "strings": true }
  }
}
```

---

## Prettier – Code formatter
**ID:** `esbenp.prettier-vscode`

**Por que usar:** padroniza a formatação de código (JS/TS/JSON/Markdown etc.).
**Dica:** habilite *Format on Save* e deixe o Prettier como *default* quando aplicável.

**Sugestões de settings:**
```json
{
  "editor.formatOnSave": true
}
```

---

## GitLens
**ID:** `eamodio.gitlens`

**Por que usar:** visualiza histórico de commits, *blame* inline, comparação e navegação avançada no Git.
**Dica:** passe o mouse sobre a linha para ver o autor/commit.

---

## GitHub Pull Requests
**ID:** `github.vscode-pull-request-github`

**Por que usar:** cria, revisa e gerencia PRs do GitHub direto no VS Code.
**Dica:** use a aba *GitHub* para ver PRs abertos no repositório.

---

## Emoji Sense
**ID:** `bierner.emojisense`

**Por que usar:** auto-complete de emojis com `:shortcodes:` (útil em READMEs, docs e comentários).
**Dica:** digite `:` para abrir a lista e `Enter` para inserir.

---

## Better Align
**ID:** `Chouzz.vscode-better-align`

**Por que usar:** alinha rapidamente texto/código por um separador (por exemplo `=` ou `:`).
**Como usar:** selecione o trecho e execute o comando **Align** (via Paleta de Comandos).

**Sugestões de settings (projeto):**
```json
{
  "betterAlign.separator": "=",
  "betterAlign.padding": "auto",
  "betterAlign.ignore": ["node_modules/**", "dist/**", "build/**"]
}
```

---

## Better Comments
**ID:** `aaron-bond.better-comments`

**Por que usar:** destaca comentários por tipo (alerta, dúvida, TODO, nota etc.).
**Legenda sugerida:** `!` (alerta), `?` (dúvida), `todo`, `*` (informativo), `note`, `deprecated`.

**Sugestões de settings (projeto):**
```json
{
  "better-comments.tags": [
    { "tag": "!", "color": "#FF2D00", "bold": true },
    { "tag": "?", "color": "#3498DB", "bold": true },
    { "tag": "todo", "color": "#FF8C00" },
    { "tag": "*", "color": "#98C379" },
    { "tag": "note", "color": "#B392F0", "italic": true },
    { "tag": "deprecated", "color": "#999999", "strikethrough": true, "italic": true }
  ]
}
```

**Exemplos de uso:**
```js
// ! Atenção: operação pode demorar
// ? Rever regra de negócio X
// todo: implementar validação de CPF
// * Dica: use cache local para reduzir I/O
// note: este módulo será extraído no futuro
// deprecated: remover após versão 1.2
```

---

## CodeSnap
**ID:** `adpyke.codesnap`

**Por que usar:** gera “prints” bonitos de trechos de código (para docs, issues, LinkedIn etc.).
**Fluxo:** selecione o código → `Ctrl+Shift+P` → `CodeSnap` → copia/gera imagem.

**Sugestões de settings (projeto):**
```json
{
  "codesnap.backgroundColor": "transparent",
  "codesnap.boxShadow": "none",
  "codesnap.containerPadding": "24px",
  "codesnap.roundedCorners": true,
  "codesnap.target": "clipboard",
  "codesnap.transparentBackground": true,
  "codesnap.showWindowControls": false
}
```

---

## TODO Highlight
**ID:** `wayou.vscode-todo-highlight`

**Por que usar:** realça TODOs/NOTEs no editor e na régua lateral.
**Sugestões de settings (projeto):**
```json
{
  "todohighlight.isEnable": true,
  "todohighlight.keywords": [
    { "text": "TODO", "color": "#ffffff", "backgroundColor": "#FF8C00", "overviewRulerColor": "#FF8C00" },
    { "text": "FIXME", "color": "#ffffff", "backgroundColor": "#E74C3C", "overviewRulerColor": "#E74C3C" },
    { "text": "BUG", "color": "#ffffff", "backgroundColor": "#C0392B", "overviewRulerColor": "#C0392B" },
    { "text": "NOTE", "color": "#000000", "backgroundColor": "#F1C40F", "overviewRulerColor": "#F1C40F" },
    { "text": "HACK", "color": "#000000", "backgroundColor": "#1ABC9C", "overviewRulerColor": "#1ABC9C" }
  ]
}
```

---

## Trailing Spaces
**ID:** `shardulm94.trailing-spaces`

**Por que usar:** remove espaços em branco no fim das linhas automaticamente e destaca os restantes.
**Sugestões de settings (projeto):**
```json
{
  "files.trimTrailingWhitespace": true,
  "trailing-spaces.trimOnSave": true,
  "trailing-spaces.includeEmptyLines": true,
  "trailing-spaces.deleteModifiedLinesOnly": false,
  "trailing-spaces.highlightColor": "rgba(255,0,0,0.25)"
}
```

---

## Dicas rápidas
- Ative **Format on Save** para manter tudo consistente.
- Em Markdown, use o preview (`Ctrl+Shift+V`) e o atalho de TOC do *Markdown All in One*.
- Use o **Better Align** para alinhar blocos de configuração e tabelas em docs.
- Para compartilhar trechos de código com o time/LinkedIn, use o **CodeSnap**.

---
