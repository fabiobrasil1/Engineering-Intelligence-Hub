# Engineering Intelligence Hub

Ferramenta pessoal para diagnóstico de engenharia baseado em evidências, planejamento de adoção de IA e inteligência para modernização de sistemas legados.

A V1 registra entrevistas e observações em Markdown com YAML, transforma relatos em evidências rastreáveis, calcula métricas e prioridades de forma determinística e gera relatórios e mapas reproduzíveis. Análises assistidas pelo Cursor ficam em propostas até revisão humana.

**Estado atual:** etapa P0 (fundação e documentação). A CLI `hub` ainda não existe; ela entra a partir de P1/P2. Veja [docs/implementation-progress.md](docs/implementation-progress.md).

## O que a V1 fará

- Registrar entrevistas, observações, equipes, sistemas, evidências, descobertas, iniciativas, métricas e decisões.
- Separar fatos verificados, percepções, hipóteses e decisões aprovadas.
- Validar contratos e relacionamentos sem inventar entidades.
- Gerar índices, mapas Mermaid e relatórios Markdown a partir dos arquivos.
- Manter dados reais fora deste repositório publicável.

## O que está fora da V1

Frontend, servidor web, autenticação, banco vetorial, RAG operacional, ingestão automática de GitHub/Jira, integração com APIs de LLM, transcrição de áudio e orquestração multiagente.

## Princípios

- Fonte de verdade: registros Markdown + YAML revisados por você.
- Evidência antes de conclusão: descobertas apontam para evidências; evidências apontam para fontes.
- Cálculo determinístico em Python; o modelo interpreta, não inventa números.
- Propostas em `proposals/` até revisão explícita.
- Exemplos neste repositório são **inteiramente fictícios**. Dados reais ficam em um workspace externo.

## Estrutura

| Caminho | Papel |
|---|---|
| `plano.md` | Especificação normativa da V1 |
| `AGENTS.md` | Instruções invariantes para o agente |
| `.cursor/rules/` | Regras curtas do Cursor |
| `config/hub.example.yaml` | Configuração de demonstração |
| `docs/` | Arquitetura, contratos, fluxos, métricas e privacidade |
| `src/engineering_hub/` | Pacote Python (implementação a partir de P1) |
| `data/examples/` | Workspace sintético (dataset completo em P3) |

O workspace de trabalho real **não** deve ser criado como subpasta deste repositório. A CLI receberá o caminho por `--workspace` ou por `config/hub.local.yaml` (ignorado pelo Git).

## Como contribuir na implementação

Cada etapa P0–P8 deve ser feita em uma **janela de contexto diferente** no Cursor. Não peça ao agente para construir várias etapas na mesma conversa. Use o prompt de retomada em `plano.md` (seção 18).

## Instalação (planejada)

A partir de P1/P2:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements-dev.lock
python -m pip install --no-deps -e .
```

No Windows, ative o ambiente com `.venv\Scripts\activate`.

Comandos-alvo (ainda não implementados):

```bash
hub --workspace data/examples validate
hub --workspace data/examples index
hub --workspace data/examples report --type diagnosis --as-of 2026-11-01
```

## Licença

Todos os direitos reservados. O autor (Fabio Brasil) mantém o copyright exclusivo sobre o código original deste projeto. Não é concedida licença para uso, modificação ou distribuição desse código original.

Componentes de terceiros, se houver, permanecem sob as respectivas licenças. Esta declaração não cobre dados reais, materiais corporativos ou conteúdo de terceiros. Exemplos em `data/examples` são fictícios.

## Segurança

Não commite chaves, tokens, dumps produtivos ou entrevistas reais. `.gitignore` e `.cursorignore` limitam versionamento e indexação; não são controles de autorização. Relatar problemas de segurança: ver nota em P8 (`SECURITY.md` ainda não existe nesta etapa).
