# skills

> **Estas são as skills que eu uso.** Elas refletem as minhas máquinas, as
> minhas assinaturas, os projetos em que trabalho e o jeito como gosto que um
> agente se comporte. Publico como referência, sem promessa de que servem para
> você do jeito que estão. Quase todas vieram de outras pessoas, e o crédito
> de cada uma está na tabela abaixo: se uma delas te interessar, vá ao
> repositório original, que é mantido pelo autor. O melhor uso disto aqui é
> ler, ver o que faz sentido e pedir para o seu agente escrever a versão que
> serve ao seu caso.

Uso com Claude Code, Codex, Cursor e OpenCode, quase sempre por dentro do
[T3 Code](https://github.com/pingdotgg/t3code). A fonte fica em
`~/.agents/skills` no meu notebook e é espelhada para os servidores onde
rodo agentes. Cada harness tem na sua pasta `skills/` um link por skill
apontando para essa fonte, então uma edição vale para todos.

A lista é curta de propósito. Já tive o dobro disso instalado e a maior
parte nunca foi chamada, então tirei o que não usava.

## O que tem aqui

A coluna "Alterei" diz o quanto a cópia se afasta do original. "Nada"
significa cópia fiel do upstream. A última sincronização com as origens foi
em 24/11/2026.

| Skill | O que faz | Origem | Alterei |
|---|---|---|---|
| `astra-loop` | Revisão em rodadas com o GPT Astra, com limite de rodadas | [tstack](https://github.com/t3dotgg/tstack) (`sol-loop`) | Derivada: modelo revisor trocado e delegação reescrita para o T3 Code |
| `code-review` | Revisa um diff contra os padrões do repositório e contra a spec | [mattpocock/skills](https://github.com/mattpocock/skills) | Regra de segunda rodada e de citar `arquivo:linha`; sem a chamada à skill de setup do autor |
| `pr` | Escreve o corpo de um PR | mattpocock/skills, que credita [humanlayer/skills](https://github.com/humanlayer/skills) | Nada |
| `research` | Pesquisa em fontes primárias e grava o achado no repositório | mattpocock/skills | Nada |
| `resolving-merge-conflicts` | Resolve conflito de merge ou rebase em andamento | mattpocock/skills (já removida de lá) | Nada |
| `writing-for-agents` | Como escrever skills, `AGENTS.md` e `CLAUDE.md` | mattpocock/skills | Nada |
| `humanizer` | Reescreve texto com cara de IA | [blader/humanizer](https://github.com/blader/humanizer) | Seção em português para mensagens enviadas em meu nome |
| `unslop-ui` | Tira cacoetes de IA do texto de interface e de gráficos | [felipebasurto/unslop-ui](https://github.com/felipebasurto/unslop-ui) | Nada |
| `frontend-design` | Direção visual para interface que não pareça modelo pronto | [anthropics/skills](https://github.com/anthropics/skills) | Nada |
| `emil-design-eng` | A filosofia de acabamento e animação do Emil Kowalski | [emilkowalski/skills](https://github.com/emilkowalski/skills) | Nada |
| `beautiful-shadows` | Sombras em camadas com valores exatos de Tailwind | [MengTo/Skills](https://github.com/MengTo/Skills) | Só o frontmatter; sem a pasta de demonstração |
| `browser-use` | Controle direto do navegador por CDP | [browser-use](https://github.com/browser-use/browser-use) | Nada |
| `find-skills` | Procura e instala skills | [vercel-labs/skills](https://github.com/vercel-labs/skills) | Só o frontmatter |

"Só o frontmatter" quer dizer `disable-model-invocation: true`: a skill só
roda quando eu chamo pelo nome e não ocupa espaço no contexto de toda
conversa. Nessas também acrescentei o `agents/openai.yaml`, ou a `policy`
dele, que faz o mesmo no Codex.

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

## O que tirei

Passaram por aqui e saíram por falta de uso, não por defeito. Valem a
visita: as skills de engenharia do
[mattpocock/skills](https://github.com/mattpocock/skills) (`tdd`,
`grill-me`, `diagnosing-bugs`, `codebase-design` e outras), a família
`better-*` do [jakubkrehel/skills](https://github.com/jakubkrehel/skills),
as do [pstack](https://github.com/cursor/plugins/tree/main/pstack)
(`architect`, `how`, `why`, `blast-radius`) e a `seo-audit` do
[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills).

## Instalar

Prefira o repositório original de cada skill. Se quiser mesmo a minha cópia:

```bash
git clone https://github.com/hevlyo/skills
cp -R skills/skills/<nome> ~/.claude/skills/   # Claude Code
cp -R skills/skills/<nome> ~/.codex/skills/    # Codex
```

A `astra-loop` precisa de um harness que rode um modelo de outro provedor
como subagente; no T3 Code isso é o `delegate_task`.

## Licença

O que é meu (este README e as alterações descritas acima) está sob a
[MIT](LICENSE). Cada skill continua sob a licença do autor original. Todas as
que estão aqui são MIT, menos a `frontend-design`, que é Apache-2.0 e traz o
texto da licença na própria pasta. Os avisos de copyright de cada origem
estão em [`licenses/`](licenses).
