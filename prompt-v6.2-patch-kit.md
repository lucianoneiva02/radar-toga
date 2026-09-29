# Patch V6.2 — kit de entregável em toda edição

Cole no prompt da rotina em https://claude.ai/code/routines/trig_019MqpmvHxW9w2PcFxx4Vfhv (a rotina foi criada via API e o agente não pode editá-la).

## 1. Inserir ANTES de "=== GRAVAR NA MEMÓRIA"
=== KIT DE ENTREGÁVEL (todo dia com edição, depois do bloco pronto) ===
Leia entregaveis/_modelo.md e crie entregaveis/AAAA-MM-DD-kit-entregavel.md seguindo a estrutura das 5 seções, adaptada ao assunto do dia: requisitos reais de acesso, 3 cenários de teste específicos do recurso, ficha de uso no escritório, checklist final, fechamento de feedback. Use só caso fictício. Sem promessa de resultado. O kit não é técnica de prompt: é roteiro de teste e ficha de aplicação da novidade. Não cite produto nem preço do Toga. Não copie exemplos do kit de outra edição. Em "SEM NOVIDADE QUALIFICADA HOJE" não gere kit.

## 2. Na SAÍDA, adicionar após 'Prompt de imagem:'
'Kit de entregável:' caminho do arquivo criado e o kit inteiro colado abaixo para copiar

## 3. No feedback, acrescentar exemplo
"Alguém enviou a ficha do kit?"

## 4. Passo 5 de GRAVAR (git)
Se o repositório estiver em HEAD destacado, faça `git checkout main` antes e `git push origin main`.

## 5. Busca
Se um domínio oficial estiver bloqueado no WebFetch (openai.com, blog.google), use firecrawl_scrape com maxAge 0.
