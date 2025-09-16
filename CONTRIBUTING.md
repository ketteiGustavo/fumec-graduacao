# Guia de Contribuição

Obrigado por querer contribuir! 🎉 Este documento explica como trabalhar no repositório **Graduação FUMEC**.

## Visão geral do fluxo

Usamos um fluxo simples baseado em *branches*:

- `main` → versão estável
- `staging` → aprovação final antes de ir para `main`
- `develop` → desenvolvimento ativo
- `feature/<nome-da-tarefa>` → suas mudanças partem **de** `develop` e retornam **para** `develop`

Fluxo: `develop` → cria `feature` → finaliza → PR para `develop`.

## Pré-requisitos

- Git instalado ([download](https://git-scm.com/downloads)). No Windows, recomendamos **Git for Windows** (com Git Bash).
- Editor recomendado: **VS Code** ([download](https://code.visualstudio.com/)).
- Extensões úteis do VS Code: *EditorConfig*, *Markdown All in One*, *GitHub Pull Requests* (opcional).

## Configuração do ambiente

```bash
git clone https://github.com/seu-usuario/graduacao-fumec.git
cd graduacao-fumec
git checkout develop
```

## Criando sua feature

```bash
git checkout -b feature/minha-tarefa
# ... edite o código ...
git add .
git commit -m "feat(minha-tarefa): descrição curta da mudança"
git push origin feature/minha-tarefa
```

## Padrão de commits

Seguimos **Conventional Commits**:
- `feat`: nova funcionalidade
- `fix`: correção de bug
- `docs`, `style`, `refactor`, `test`, `chore`

Ex.: `feat(login): adiciona autenticação com Google`

Mais detalhes: https://www.conventionalcommits.org/pt-br/v1.0.0/

## Abertura de Pull Request (PR)

1. Garanta que sua branch está atualizada com `develop`.
2. Abra o PR com **Base: `develop`** e **Compare: `feature/...`**.
3. Preencha o título e descrição explicando o contexto e o *porquê* da mudança.
4. Marque o PR com os rótulos apropriados (ex.: `feature`, `bugfix`, `docs`).

### Checklist do PR

- [ ] Título no formato *Conventional Commit*
- [ ] Descrição do que foi feito + motivação
- [ ] Testado localmente (quando aplicável)
- [ ] Atualizou documentação (`README.md` ou `docs/`), se necessário
- [ ] Seguiu o `.editorconfig` e o guia de Markdown (`docs/guia-markdown.md`)

## Estilo de código e documentação

- **EditorConfig**: configurado via `.editorconfig` na raiz
- **Markdown**: veja `docs/guia-markdown.md` para formatação
- **.gitignore**: respeite os arquivos/pastas ignorados

## Como abrir issues

Use os templates em `.github/ISSUE_TEMPLATE/`:
- `bug_report.md` para bugs
- `solicitar_recurso.md` para sugestões de funcionalidade

Inclua passos de reprodução, comportamento esperado/atual e, se possível, prints ou logs.

## Código de Conduta

Ao contribuir, você concorda em seguir nosso [Código de Conduta](CODE_OF_CONDUCT.md).

## Segurança

Para vulnerabilidades, **não** abra issues públicas. Siga `SECURITY.md`.
