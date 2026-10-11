# Métricas e priorização — V1

Cálculos entram em **P4**. Este documento fixa as regras para não improvisar números antes disso.

## Qualitativo

Temas iniciais: `documentation`, `onboarding`, `testing`, `delivery`, `observability`, `dependencies`, `ai_adoption`, `security`, `knowledge_concentration`.

Contar fontes originais distintas agrupadas por `source_group`. Dez evidências da mesma entrevista são uma fonte, não dez entrevistas. Relatório derivado não conta como nova fonte.

Não converter “N de M entrevistas mencionaram X” em prevalência da empresa nem atribuir perda de produtividade sem medição.

## Quantitativo

Observações de métrica exigem fase (`baseline | pilot | followup`), período, método, coorte, versão do método e evidências `measured` verificadas em fontes `OBS` quando houver valor.

Entrevista pode sugerir métrica ou estimativa; isso não é baseline quantitativo.

Comparar somente mesma métrica, unidade, agregação, `cohort` e `method_version`, com evidências atuais. Critérios incompatíveis → `not_comparable`. Baseline zero não produz delta percentual.

## Score de iniciativas

```text
score = impacto × 0,40
      + viabilidade × 0,25
      + alcance × 0,25
      + (6 − risco) × 0,10
```

Critérios 1–5. Exemplo fictício 5/4/5/2 → `4,65`. Critério `null` → `unscored`. `blocked_reason` prevalece. Só classificar iniciativas revisadas com descobertas elegíveis. Score não aprova iniciativa nem prova ROI.
