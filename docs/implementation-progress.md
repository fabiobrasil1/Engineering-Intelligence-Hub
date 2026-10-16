# Progresso da implementação

Atualizado: 2026-10-11 · Etapa em foco nesta conversa: **P0** · Próxima etapa: **P1 em nova janela de contexto**

Regra: uma etapa (P0–P8) por conversa. Não continue a implementação neste arquivo como se P1 já estivesse autorizada.

## Checklist

| Etapa | Nome | Status |
|---|---|---|
| P0 | Fundação e documentação | Concluída (esta conversa) |
| P1 | Domínio e schemas | Pendente — nova conversa |
| P2 | Persistência, criação e integridade | Pendente |
| P3 | Dataset, índices e busca | Pendente |
| P4 | Métricas, priorização e relatórios | Pendente |
| P5 | Contexto e mapas | Pendente |
| P6 | Fluxo de IA, propostas e revisão | Pendente |
| P7 | Verificação ponta a ponta e uso diário | Pendente |
| P8 | Preparação completa para GitHub (CI, CONTRIBUTING, SECURITY, locks) | Pendente |

Publicação inicial no GitHub após P0 ocorre **somente** se solicitada nesta conversa. Isso não conclui P8.

## P0 — evidências

### Entregue

- `plano.md` atualizado com a regra obrigatória de uma etapa por janela de contexto (versão 1.1).
- `README.md`, `AGENTS.md` e declaração de direitos sobre o código original (sem licença MIT).
- `.gitignore`, `.cursorignore`.
- `.cursor/rules/{project,evidence,analysis,python}.mdc`.
- `config/hub.example.yaml` e `data/examples/workspace.yaml` (workspace demo vazio).
- Docs: arquitetura, contratos, fluxos, métricas, privacidade.
- ADRs 0001, 0002 e 0003.
- Esqueleto de pastas para código, templates, schemas, testes e exemplos, sem implementação Python.

### Fora de P0 (não feito de propósito)

- `pyproject.toml`, modelos Pydantic, JSON Schema, CLI `hub`.
- Dataset fictício completo.
- CONTRIBUTING.md, SECURITY.md, workflow de CI e locks de dependência (P8).
- Frontend, APIs de LLM, autenticação, banco vetorial.

### Verificações executadas

- Inspeção do diretório: antes da P0 havia apenas `plano.md`.
- Conferência documental: README declara estado P0; docs não afirmam que a CLI já existe.
- Nenhuma menção a empregador, cliente ou produto corporativo real nos arquivos criados.
- Nenhum código Python de domínio/CLI foi implementado nesta etapa.

### Pendências de P0

- Nenhuma pendência de aceite da P0.
- Snapshot GitHub: remoto [fabiobrasil1/Engineering-Intelligence-Hub](https://github.com/fabiobrasil1/Engineering-Intelligence-Hub) criado por você; push da P0 na branch `main`. Isso não conclui P8.

## Próximo prompt (P1 — nova conversa)

```text
Leia @plano.md, @AGENTS.md e @docs/implementation-progress.md. Execute somente P1.
Esta conversa deve conter apenas P1. Não inicie P2.

Implemente o pacote Python e os modelos Pydantic 2.x dos nove registros, configuração,
workspace, proposta e manifest. Todos os campos e invariantes da seção 6 são normativos.
Não crie formatos incompatíveis para facilitar exemplos.

Configure pyproject.toml, layout src/, entrypoint hub e dependências verificadas em
documentação oficial. Use modelos como fonte única dos JSON Schemas, exporte os
schemas e implemente schemas export/check. Documente limites de validação do corpo.

Crie templates válidos e taxonomia mínima. Faça testes relevantes de tipos, datas,
UUIDs, null, enums, fields extras, revisão/verificação e contratos quantitativos.
Não implementar ainda persistência completa ou cálculos de relatórios.

Rode checks pertinentes, registre resultados e pendências em implementation-progress.
Pare após os critérios de aceite de P1 e forneça o próximo prompt.
```
