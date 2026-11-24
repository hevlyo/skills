# skills

> **Estas são as skills que eu uso.** Elas refletem as minhas máquinas, as
> minhas assinaturas, os projetos em que trabalho e o jeito como gosto que um
> agente se comporte. Publico como referência, sem promessa de que servem para
> você do jeito que estão. Quase todas vieram de outras pessoas, e o crédito
> de cada uma está na tabela abaixo: se uma delas te interessar, vá ao
> repositório original, que é mantido e está mais atualizado que a minha
> cópia. O melhor uso disto aqui é ler, ver o que faz sentido e pedir para o
> seu agente escrever a versão que serve ao seu caso.

Uso com Claude Code, Codex, Cursor e OpenCode, quase sempre por dentro do
[T3 Code](https://github.com/pingdotgg/t3code). A fonte fica em
`~/.agents/skills` no meu notebook e é espelhada para os servidores onde
rodo agentes. Cada harness tem na sua pasta `skills/` um link por skill
apontando para essa fonte, então uma edição vale para todos.

## O que tem aqui

A coluna "Alterei" diz o quanto a cópia se afasta do original. "Nada"
significa cópia fiel de alguma versão do upstream, que pode não ser a mais
recente.

### Engenharia

| Skill | O que faz | Origem | Alterei |
|---|---|---|---|
| `architect` | Desenha tipos, assinaturas e módulos antes do código | [pstack](https://github.com/cursor/plugins/tree/main/pstack) | Troquei as skills `arena` e `interrogate` por subagentes |
| `blast-radius` | Procura o que uma mudança quebra fora do diff | pstack | Ajustes de links e de skills citadas |
| `how` | Explica como um trecho funciona antes de mexer nele | pstack | Caminho do arquivo de modelos e nota para outros harnesses |
| `why` | Levanta o porquê de uma decisão ou regressão | pstack | Descoberta de MCP genérica |
| `astra-loop` | Revisão em rodadas com o GPT Astra, com limite de rodadas | [tstack](https://github.com/t3dotgg/tstack) (`sol-loop`) | Derivada: modelo revisor trocado e delegação reescrita para o T3 Code |
| `code-review` | Revisa um diff contra os padrões do repositório e contra a spec | [mattpocock/skills](https://github.com/mattpocock/skills) | Regra de segunda rodada e de citar `arquivo:linha`; sem a chamada à skill de setup do autor |
| `codebase-design` | Vocabulário para desenhar módulos profundos | mattpocock/skills | Só o frontmatter |
| `diagnosing-bugs` | Roteiro de diagnóstico para bug difícil | mattpocock/skills | Só o frontmatter |
| `domain-modeling` | Glossário e ADRs do domínio do projeto | mattpocock/skills | Só o frontmatter |
| `grill-me` | Entrevista insistente para apertar um plano | mattpocock/skills | Texto embutido no lugar da chamada a outra skill |
| `grill-with-docs` | A mesma entrevista, registrando ADRs e glossário | mattpocock/skills | Descrição e link |
| `implement` | Implementa a partir de uma spec ou de tickets | mattpocock/skills | Uma linha |
| `pr` | Escreve o corpo de um PR | mattpocock/skills, que credita [humanlayer/skills](https://github.com/humanlayer/skills) | Nada |
| `prototype` | Protótipo descartável para responder uma dúvida de design | mattpocock/skills | Só o frontmatter |
| `research` | Pesquisa em fontes primárias e grava o achado no repositório | mattpocock/skills | Nada |
| `resolving-merge-conflicts` | Resolve conflito de merge ou rebase em andamento | mattpocock/skills (já removida de lá) | Nada |
| `retro` | Retrospectiva de uma sessão de código | mattpocock/skills | Nada |
| `tdd` | Desenvolvimento guiado por teste | mattpocock/skills | Frontmatter e um link |
| `writing-for-agents` | Como escrever skills, `AGENTS.md` e `CLAUDE.md` | mattpocock/skills | Nada |

### Interface e design

| Skill | O que faz | Origem | Alterei |
|---|---|---|---|
| `better-interface` | Revisão única que junta todas as `better-*` | [jakubkrehel/skills](https://github.com/jakubkrehel/skills) | Links entre as skills |
| `better-accessibility` | Teclado, foco, ARIA e formulários contra a WCAG 2.2 | jakubkrehel/skills | Só o frontmatter |
| `better-colors` | Paleta, tokens semânticos e contraste | jakubkrehel/skills | Só o frontmatter |
| `better-layout` | Agrupamento, alinhamento e estrutura responsiva | jakubkrehel/skills | Só o frontmatter |
| `better-typography` | Escala, espaçamento, quebra e pontuação do texto | jakubkrehel/skills | Só o frontmatter |
| `better-ui` | Raio, alinhamento óptico, sombra, ícone e animação | jakubkrehel/skills | Só o frontmatter |
| `better-writing` | Texto de interface: rótulos, erros, estados vazios | jakubkrehel/skills | Só o frontmatter |
| `interface-review` | Revisa o que um branch ou PR piorou na interface | jakubkrehel/skills | Nada |
| `explain-interface` | Explica como um site ou efeito foi construído | jakubkrehel/skills | Nada |
| `break` | Renderiza um componente em todos os cenários e força os limites | jakubkrehel/skills | Nada |
| `variant` | Gera variantes de um componente para escolher | jakubkrehel/skills | Nada |
| `beautiful-shadows` | Sombras em camadas com valores exatos de Tailwind | [MengTo/Skills](https://github.com/MengTo/Skills) | Só o frontmatter; sem a pasta de demonstração |
| `emil-design-eng` | A filosofia de acabamento e animação do Emil Kowalski | [emilkowalski/skills](https://github.com/emilkowalski/skills) | Nada |
| `frontend-design` | Direção visual para interface que não pareça modelo pronto | [anthropics/skills](https://github.com/anthropics/skills) | Nada |
| `unslop-ui` | Tira cacoetes de IA do texto de interface e de gráficos | [felipebasurto/unslop-ui](https://github.com/felipebasurto/unslop-ui) | Nada |

### Escrita, navegador e o resto

| Skill | O que faz | Origem | Alterei |
|---|---|---|---|
| `humanizer` | Reescreve texto com cara de IA | [blader/humanizer](https://github.com/blader/humanizer) | Seção em português para mensagens enviadas em meu nome |
| `browser-use` | Controle direto do navegador por CDP | [browser-use](https://github.com/browser-use/browser-use) | Nada |
| `seo-audit` | Auditoria de SEO técnico e on-page | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | Frontmatter e uma nota |
| `find-skills` | Procura e instala skills | [vercel-labs/skills](https://github.com/vercel-labs/skills) | Só o frontmatter |
| `obsidian-vault` | Busca e cria notas no meu vault do Obsidian | mattpocock/skills (já removida de lá) | Caminho do vault e frontmatter |

"Só o frontmatter" quase sempre quer dizer `disable-model-invocation: true`:
a skill só roda quando eu chamo pelo nome e não ocupa espaço no contexto de
toda conversa. Em várias também acrescentei o `agents/openai.yaml`, ou a
`policy` dele, que faz o mesmo no Codex.

Alguns textos dizem que tal skill "is not installed here" ou apontam para
`~/.agents/pstack-models.md`. Isso descreve a minha máquina. Da mesma forma,
a `seo-audit` cita skills irmãs do repositório dela que eu não instalei.

## O que uso e não está aqui

Estas eu também tenho instaladas, mas não copiei para cá: ou têm repositório
próprio, ou a cópia local é praticamente a do autor, ou é pesada, ou traz
material que não é meu para redistribuir. Instale direto da origem.

| Skill | Origem |
|---|---|
| `ibx` | [hevlyo/ibx](https://github.com/hevlyo/ibx), a única que escrevi do zero: empresta uma sandbox descartável do instabox para trabalho pesado ou arriscado |
| `impeccable` | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) |
| `stageshow` | [benjitaylor/skills](https://github.com/benjitaylor/skills) |
| `revenue-centric-design` | [heliocosta-dev/revenue-centric-design](https://github.com/heliocosta-dev/revenue-centric-design) |
| `shadcn` | [shadcn-ui/ui](https://github.com/shadcn-ui/ui) |
| `supabase`, `supabase-postgres-best-practices` | [supabase/agent-skills](https://github.com/supabase/agent-skills) |
| `vercel-composition-patterns`, `vercel-react-best-practices` | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) |
| `omarchy`, `omarchy-app`, `diagnose-crash` | vêm com o pacote do [Omarchy](https://omarchy.org) e são trocadas a cada atualização do sistema |

Também ficou de fora o perfil de voz que a `humanizer` lê antes de escrever
em meu nome. Ele cita conversas e pessoas reais. O `SKILL.md` ainda aponta
para `voz-riquelme.md`; se for usar essa parte, escreva o seu.

## Instalar

Prefira o repositório original de cada skill. Se quiser mesmo a minha cópia:

```bash
git clone https://github.com/hevlyo/skills
cp -R skills/skills/<nome> ~/.claude/skills/   # Claude Code
cp -R skills/skills/<nome> ~/.codex/skills/    # Codex
```

Várias chamam outras por link relativo (`../outra-skill`). Copie também as
que o `SKILL.md` citar: `better-interface`, por exemplo, usa todas as
`better-*`, e `implement` usa `tdd` e `code-review`. A `astra-loop` precisa de um harness
que rode um modelo de outro provedor como subagente; no T3 Code isso é o
`delegate_task`.

## Licença

O que é meu (este README e as alterações descritas acima) está sob a
[MIT](LICENSE). Cada skill continua sob a licença do autor original. Todas as
que estão aqui são MIT, menos a `frontend-design`, que é Apache-2.0 e traz o
texto da licença na própria pasta. Os avisos de copyright de cada origem
estão em [`licenses/`](licenses).
