# Aula 29 — Performance distribuída

**Navegação:** [← Aula 28](./28-spark-e-processamento-batch.md) | [Índice](../README.md) | [Próxima →](./30-fundamentos-de-streaming.md)

## Objetivo

Observar shuffle, skew, particionamento e impacto do formato colunar.

## Estude nesta ordem

1. Continue o [módulo Batch do Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/05-batch), nas partes de Spark internals, joins e group by.
2. [Cookbook — Advanced Engineering Skills](../materials/data-engineering-cookbook/sections/03-AdvancedSkills.md), partes sobre localidade e gerenciamento de recursos.
3. Revise a [Aula 17](./17-formatos-e-particionamento.md).

## Prática

Compare join sem particionamento, repartition e broadcast quando aplicável. Introduza uma chave desbalanceada e observe o plano.

## Entrega

Experimento com plano, duração, volume e conclusão.

## Avance quando

- [ ] O shuffle está identificado no plano.
- [ ] Skew foi medido por distribuição de chaves.
- [ ] A otimização melhora o requisito sem apenas mover o custo.

