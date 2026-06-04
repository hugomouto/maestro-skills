# maestro-skills

Slash commands do [Claude Code](https://docs.claude.com/en/docs/claude-code) usados no fluxo de discovery do Maestro.

Cada comando é um arquivo `.md` com frontmatter (`description`, `title`) e as instruções que o Claude Code executa quando o comando é invocado via `/<nome>`.

## Comandos

| Comando | O que faz |
|---|---|
| [`/discovery-problem`](./discovery-problem.md) | Elicitação guiada de **Problem Spec** — define problema, hipótese falsificável, evidências, riscos SVPG e perguntas abertas. |
| [`/discovery-research`](./discovery-research.md) | Elicitação guiada de **Research Spec** — plano de LEARN/BUILD/MEASURE. Requer Problem Spec gerado previamente. |

Os dois funcionam em sequência: `/discovery-problem` enquadra o problema, `/discovery-research` planeja como investigá-lo.

## Como instalar

Copie os arquivos para `.claude/commands/` do seu projeto (compartilhado com o time) ou para `~/.claude/commands/` (pessoal):

```bash
git clone https://github.com/hugomouto/maestro-skills.git
cp maestro-skills/discovery-*.md .claude/commands/
```

Na próxima sessão, `/discovery-problem` e `/discovery-research` aparecem como slash commands.
