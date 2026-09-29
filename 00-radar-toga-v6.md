---
tipo: projeto
titulo: "Radar Toga V6 — hub: memória em vault e ciclo de feedback"
data: 2026-09-29
fonte: "C:\Users\lucia\OneDrive\Área de Trabalho\radar-toga-v6.md"
status: bruto
---

# Radar Toga V6 — hub

Proposta de substituição da V5 (snapshot de 29/09/2026 13:35 UTC). **Estado: proposta, NÃO aplicada.**
Editar o `.md` não muda a rotina: a aplicação é `RemoteTrigger update` no trigger
`trig_01JQ1sCBYrG6fBKS38yQMPUJ` e depende dos pré-requisitos abaixo.
Narrativa V1–V5 e causa raiz da repetição: [[radar-toga]].

## As três mudanças em relação à V5

1. **Memória.** A rotina lê e grava histórico no vault (git). Resolve a causa raiz registrada em
   [[radar-toga]]: sessão nova sem memória, lista de proibidos que não se atualizava sozinha.
2. **Novidade = data do lançamento, não da matéria.** Fonte primária obrigatória (anthropic.com/news,
   openai.com/news, blog.google, changelog oficial) e teste de primeira aparição (≤ 7 dias).
3. **Ciclo de feedback.** O Luciano registra a reação do grupo em `feedback.md`; a rotina lê antes
   de cada edição e cobra na saída se estiver em atraso.

## Calendário (só segunda e sexta exigem novidade)

| Dia | Tipo | Exige novidade |
|---|---|---|
| Seg | Novidade da semana | sim |
| Ter | Ferramenta ou técnica (recurso existente com ângulo novo; nunca chamar de "novo") | não |
| Qua | Fluxo aplicado ao escritório | não |
| Qui | Automação e integração (MCP/conector) | não |
| Sex | Fechamento: novidade, ou melhor técnica do banco de pautas | condicional |

Ordem de impacto: (1) muda o trabalho de todo usuário de Claude/ChatGPT/Gemini; (2) agente/MCP/conector
com uso claro no escritório; (3) terceiro só de grande alcance.

## Pré-requisitos de infraestrutura

1. Vault (ou só `10-projetos/radar-toga/`) em git, repositório **privado**, com Obsidian Git (pull/push a cada 5–10 min).
2. Repositório anexado à rotina com permissão de escrita.
3. Allowed tools: WebSearch, WebFetch, Read, Write, Edit, Bash (Bash só para git).
4. Modelo: `claude-sonnet-5` → `claude-sonnet-5-5`.
5. `persist_session` pode ficar `false` (memória mora no vault).
6. Notificação push/e-mail ao terminar.
7. Sigilo: o repo guarda só pauta, fontes e feedback agregado. Nunca nome/telefone de aluno, nem print com dado pessoal.

Conflito de git: a rotina só grava por **append**; nunca edita `feedback.md`; se o push falhar, faz
`git pull --rebase` uma vez e, falhando de novo, informa sem forçar.

## Arquivos desta pasta

- [[prompt-v6]] — texto integral do prompt para colar na rotina
- [[historico]] — 1 linha por edição + vetados + "já ensinado no Toga" + padrões esgotados (a rotina grava)
- [[novidades]] — catálogo de tudo que a pesquisa encontrou, usado ou descartado (a rotina grava)
- [[feedback]] — reações do grupo (o Luciano grava; a rotina só lê)
- [[banco-de-pautas]] — técnicas atemporais para dias sem novidade
- [[evolucao]] — changelog do prompt e aprendizados do feedback
- `edicoes/AAAA-MM-DD.md` — edição integral + fontes + auditoria (criado pela rotina)

## Riscos em aberto (declarados na própria V6)

- Recurso incremental sem nome próprio pode não ter data rastreável → descartado → menos notícias (intencional).
- Feedback depende de disciplina humana do Luciano.
- "Prompt de imagem" é marcador provisório: a rotina não gera imagem; falta o processo (Canva/outro modelo).
- Terça a quinta deixam de ser "novidade". Se novidade diária for contratual, o calendário precisa ser renegociado.

## Pontos de atenção levantados na leitura (Claude, 29/09/2026 — não constam na V6)

- **Vazamento de escopo no git.** Se o Obsidian Git versionar o vault inteiro, sobem para o GitHub
  também as notas de alunos/comunidade/pagamento (regra de sigilo). Versionar **só** a pasta
  `radar-toga/` (repo separado ou submódulo).
- **Caminhos do prompt** assumem que a raiz do repo contém `10-projetos/radar-toga/`. Se o repo for só
  a subpasta, os caminhos do prompt precisam ser reescritos.
- **Vault dentro do OneDrive** + pasta `.git` dentro do OneDrive costuma corromper o índice git
  (sincronização concorrente). Preferir o repo fora do OneDrive, com a pasta do vault como cópia/junction, ou pausar sync do `.git`.
- **Semente do histórico** não inclui a edição de 29/09 (Claude in Chrome, vetada) como edição publicada, só como veto. Conferir com o log real antes de aplicar.
