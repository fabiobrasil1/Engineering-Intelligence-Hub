# ADR 0002 — Workspaces externos para dados reais

- Status: aceito
- Data: 2026-10-11

## Contexto

O repositório de código será publicável. Entrevistas e sistemas reais não devem entrar nesse histórico.

## Decisão

O workspace operacional fica fora da árvore do repositório. A CLI recebe o caminho explicitamente (`--workspace` ou configuração local ignorada). `data/examples` contém apenas dados sintéticos com `is_synthetic: true`. Modo `demo` rejeita registros reais.

## Consequências

- Separação estrutural reduz o risco de commit acidental; não substitui política da organização.
- Regras `.mdc` deste repositório podem não se aplicar automaticamente a uma pasta de dados aberta à parte.
- Backup e versionamento dos dados reais, se permitidos, ocorrem em repositório privado independente.
