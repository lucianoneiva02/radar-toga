---
tipo: projeto
titulo: "Evolução do Radar Toga (changelog do prompt e aprendizados)"
data: 2026-09-29
fonte: "C:\Users\lucia\OneDrive\Área de Trabalho\radar-toga-v6.md (seção 2.4, semente)"
status: bruto
---

# Evolução do Radar Toga
Hub: [[00-radar-toga-v6]]. Narrativa V1–V4 em [[radar-toga]].

## Versões
- V1–V4: ver nota narrativa [[radar-toga]]
- V5 (21/09): pivô de notícia de Judiciário para dica de IA útil
- V5.1 (~28/09): padrões esgotados
- V5.2 (29/09 13:20 UTC): regra dura de 7 dias
- V5.3 (29/09 13:35 UTC): ordem de busca Anthropic → OpenAI → Google → terceiros
- V6 (29/09): memória em vault, teste de primeira aparição, fontes primárias, notícia só em dias fixos, ciclo de feedback. **APLICADA em 29/09/2026 (~15:30 UTC)** via RemoteTrigger update: modelo claude-sonnet-5-5, tools WebSearch/WebFetch/Read/Write/Edit/Bash, repo lucianoneiva02/radar-toga anexado, notificação e-mail+push. Rollback: prompts-anteriores/prompt-v5.3.md. Pendente: confirmar permissão de push em main
- V6.1 (29/09 ~15:53 UTC): novidade todos os dias (sem técnica nem banco de pautas), varredura de perfis e newsletters como pista, Microsoft entra nas fontes primárias, fallback = "SEM NOVIDADE QUALIFICADA HOJE". Aplicada na rotina NOVA trig_019MqpmvHxW9w2PcFxx4Vfhv (desativada até teste). Motivo: edição de teste de 29/09 ensinou técnica de prompt; Luciano quer novidade. Texto em prompt-v6.1.md

## Aprendizados do feedback
<!-- a rotina anexa aqui: data | sinal observado | ajuste aplicado -->
2026-10-02 | Sem feedback em 29/09 e 30/09 (grupo silencioso); 01/10 ainda sem registro | Sem sinal para ajustar; manter pauta pelo critério de impacto e evitar tom genérico (Luciano rejeitou Meetings em 02/10)
2026-10-02 | Feedback 01/10 (Gemini skills): 4 respostas em ~1h, tom positivo e de visão de mercado, 0 já conheciam, 0 testaram, sem dúvida de uso | Preferir pautas com ação testável no escritório e com aplicação clara, não só visão de mercado; corrige a linha anterior (01/10 agora tem registro)
2026-10-05 | Sem feedback novo registrado para 02/10 (v1 rejeitada e v2) | Dia sem pauta qualificada: não forçar; priorizei fonte primária e descartei repetição de padrão (Gemini skills, Copilot/PowerPoint)
2026-10-06 | Sem feedback novo registrado para 05/10 (sem edição) nem 02/10 | Dia sem pauta qualificada: não forçar; varredura das 4 fontes primárias sem item novo
2026-10-07 | Sem feedback novo registrado para 02/10, 05/10, 06/10 | Dia sem pauta qualificada: não forçar; Nano Banana 2.1 descartado por falta de data primária e uso no escritório
2026-10-08 | Sem feedback novo registrado para 02/10 a 07/10 (07/10 foi sem edição) | Voltei a pautar: capacidade nova de grande alcance com uso testável; evitei tom genérico, teste com dados fictícios sugerido
