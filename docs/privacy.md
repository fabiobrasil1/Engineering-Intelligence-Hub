# Privacidade e publicação

## Dados reais

Workspace real fica **fora** deste repositório. Não criar `engineering-workspace` como subpasta do projeto público. Não copiar entrevistas reais para `data/examples`. Exemplos sintéticos não são anonimização de dados reais.

## Limites das ferramentas

`.gitignore` e `.cursorignore` reduzem o risco de versionar ou indexar arquivos locais. Eles não concedem autorização, não removem histórico já commitado e não bloqueiam todas as ferramentas.

A V1 não chama APIs de LLM. Processar informação real no Cursor exige política aprovada pela organização.

## Classificação

Ordem: `public < internal < restricted`. Evidências e descobertas revisadas herdam a maior classificação das fontes. Pacotes de contexto excluem `restricted` por padrão.

## Publicação

Publicar somente código, contratos, templates e exemplos fictícios. Aliases no lugar de nomes pessoais. Entrevistas não são avaliação de desempenho.

Se dados reais entrarem no histórico Git, interromper a publicação até resolver a exposição. Ignorar o arquivo depois não basta.

## Licença

MIT cobre o código original deste repositório. Não assume direitos sobre dados corporativos.
