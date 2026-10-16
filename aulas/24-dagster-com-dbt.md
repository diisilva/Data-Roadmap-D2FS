# Aula 24 — Dagster com dbt

**Navegação:** [← Aula 23](./23-recursos-jobs-e-schedules.md) | [Índice](../README.md) | [Próxima →](./25-particoes-backfills-e-testes.md)

## Objetivo

Integrar o projeto dbt ao grafo de ativos sem duplicar sua lógica no orquestrador.

## Estude nesta ordem

1. [Curso Dagster + dbt](../materials/orchestration/course/pages/dagster-dbt.md).
2. [Projeto de exemplo Dagster + dbt](../materials/orchestration/dagster_university/dagster_and_dbt/README.md).
3. [Modelo incremental](../materials/orchestration/course/pages/dagster-dbt/lesson-6/2-creating-a-simple-incremental-model.md).

## Prática

Carregue o manifest do dbt, represente seus modelos como ativos e execute build/test pelo Dagster.

## Entrega

Grafo unificado de ingestão e modelos dbt.

## Avance quando

- [ ] Falha de teste dbt aparece como falha operacional.
- [ ] Seleção de ativos evita rebuild desnecessário.
- [ ] A linhagem inclui fontes, modelos e consumidores.

