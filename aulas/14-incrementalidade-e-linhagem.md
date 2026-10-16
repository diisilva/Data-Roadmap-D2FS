# Aula 14 — Incrementalidade e linhagem

**Navegação:** [← Aula 13](./13-testes-e-documentacao-dbt.md) | [Índice](../README.md) | [Próxima →](./15-ingestao-e-contratos.md)

## Objetivo

Implementar transformação incremental e explicar o impacto de uma mudança por meio da linhagem.

## Estude nesta ordem

1. [Dagster + dbt — modelo incremental](../materials/orchestration/course/pages/dagster-dbt/lesson-6/2-creating-a-simple-incremental-model.md).
2. [Dagster + dbt — ativo particionado](../materials/orchestration/course/pages/dagster-dbt/lesson-6/3-creating-a-partitioned-dbt-asset.md).
3. [Data Contract](<../materials/data-engineering-wiki/Concepts/Data Management/Data Contract.md>).

## Prática

Converta um modelo para incremental. Teste primeira carga, nova carga, registro atualizado e full refresh. Identifique consumidores afetados por mudança de coluna.

## Entrega

Modelo incremental, matriz de cenários e diagrama de linhagem.

## Avance quando

- [ ] Nova execução não duplica registros.
- [ ] Atualizações e atrasos possuem comportamento definido.
- [ ] O procedimento de full refresh está documentado.

