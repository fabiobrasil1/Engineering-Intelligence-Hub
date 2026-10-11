# ADR 0001 — Markdown como fonte de verdade

- Status: aceito
- Data: 2026-10-11

## Contexto

A V1 precisa de registros revisáveis por uma pessoa, com diff claro no Git e leitura no editor, sem servidor ou banco obrigatório.

## Decisão

Registros canônicos ficam em Markdown com YAML front matter. Índices, mapas, relatórios e pacotes de contexto são derivados e reconstruíveis. Modelos Pydantic validam o contrato; JSON Schema é gerado dos modelos.

## Consequências

- Você revisa o texto e os metadados no mesmo arquivo.
- Relacionamentos entre arquivos exigem validação na aplicação, não só JSON Schema isolado.
- Edição concorrente no mesmo arquivo não é resolvida por UUID; colaboração futura precisará de convenção ou outra persistência.
