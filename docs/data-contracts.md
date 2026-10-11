# Contratos de dados — V1

Este documento resume os contratos. A especificação normativa completa está na seção 6 de `plano.md`. Implementação dos modelos Pydantic ocorre em **P1**.

## Fonte de verdade

Registros canônicos: Markdown com YAML front matter. Campos desconhecidos são rejeitados. Pydantic será a fonte única do contrato; JSON Schema será gerado a partir dos modelos, não editado à mão como autoridade.

## Campos comuns (todo registro)

`schema_version` (literal `1`), `id` (prefixo + UUID v4), `kind`, `title`, `created_at`, `updated_at`, `created_by`, `review_status`, `reviewed_by`, `reviewed_at`, `classification`, `is_synthetic`, `tags`.

Nome de arquivo: `{id}--{slug}.md`. Links resolvem por ID.

## Tipos

| `kind` | Prefixo | Diretório |
|---|---|---|
| `interview` | `INT` | `discovery/interviews` |
| `observation` | `OBS` | `discovery/observations` |
| `team` | `TEAM` | `knowledge/teams` |
| `system` | `SYS` | `knowledge/systems` |
| `evidence` | `EVD` | `assessments/evidence` |
| `finding` | `FND` | `assessments/findings` |
| `initiative` | `INI` | `strategy/initiatives` |
| `metric` | `MET` | `metrics` |
| `decision` | `DEC` | `decisions` |

## Distinções obrigatórias

- Relato (`reported`) não vira fato verificado.
- Hipótese não admite `verification=verified`.
- `review_status` (draft/reviewed/archived) é separado de verificação epistemológica e de estado operacional.
- `null` e lista vazia significam ausência conhecida; `null` nunca vira zero em cálculos.
- Dependências de sistema existem só quando declaradas explicitamente com evidências.

## Corpo Markdown

A validação verificará headings mínimos definidos no plano (por tipo). Não alegar compreensão semântica de todo o texto.

## Workspace

`workspace.yaml` guarda `schema_version`, `workspace_id` (UUID), `mode`, `language` e `timezone`. Sem senhas ou tokens. Modo `demo` rejeitará registros com `is_synthetic: false` quando a CLI existir.

Exemplos deste repositório são sintéticos. Dataset executável completo entra em P3.
