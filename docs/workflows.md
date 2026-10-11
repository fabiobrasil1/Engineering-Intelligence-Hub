# Fluxos de trabalho — V1

Os comandos da CLI citados abaixo são a interface-alvo. Eles passam a existir nas etapas P2–P6. Até lá, use este documento como roteiro, não como garantia de que os binários já rodaram.

## Uma etapa de implementação por conversa

P0–P8: uma etapa por janela de contexto no Cursor. Após o aceite, atualize `implementation-progress.md` e abra uma nova conversa para a etapa seguinte.

## Diagnóstico após uma entrevista (alvo)

1. Criar registro `interview` em draft (`hub new` em P2).
2. Revisar fidelidade das notas e marcar a fonte como revisada.
3. `validate` e `index`.
4. Gerar pacote `context` com a entrevista e entidades pertinentes.
5. Pedir extração no Cursor; a saída vai para `proposals/`.
6. Conferir evidências, referências e duplicatas.
7. Aceitar somente itens corretos; `proposal apply` com IDs explícitos.
8. Validar de novo e gerar diagnóstico parcial.
9. Definir próxima coleta para corroborar relatos relevantes.

## Regras de operação

- Entrevistas e observações são fontes. Extração não as altera.
- Proposta não é decisão. Aprovação estratégica exige solicitação específica.
- Relatórios normais excluem drafts. Pendências podem aparecer rotuladas.
- Dados `restricted` ficam fora do pacote de contexto por padrão.

## Papéis lógicos no Cursor

Curador de entrevista, analista de evidências, analista de sistemas, analista estratégico, redator executivo e revisor. Na V1, o papel muda pelo prompt; não há processos paralelos de agentes.
