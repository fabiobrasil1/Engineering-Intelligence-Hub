# ADR 0003 — Propostas de IA com revisão humana

- Status: aceito
- Data: 2026-10-11

## Contexto

O Cursor ajuda a extrair evidências e redigir análises. Incorporar automaticamente essas saídas corromperia fontes e misturaria hipótese com decisão.

## Decisão

Saídas de análise vão para `proposals/` no workspace. Aplicação exige `proposal apply` com `item_ids` escolhidos. Extração não altera entrevistas nem observações. Aceitar extração não aprova decisão estratégica. A V1 não chama API de modelo.

## Consequências

- Há um passo explícito de revisão.
- Hashes base detectam alteração da fonte entre proposta e aplicação.
- Papéis de agentes são prompts sequenciais, não infraestrutura multiagente.
