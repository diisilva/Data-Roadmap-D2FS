# Aula 25 — Partições, backfills e testes

**Navegação:** [← Aula 24](./24-dagster-com-dbt.md) | [Índice](../README.md) | [Próxima →](./26-observabilidade-e-incidentes.md)

## Objetivo

Particionar dados por uma dimensão operacional, executar backfill e testar ativos isoladamente.

## Estude nesta ordem

1. [Partições e backfills](../materials/orchestration/course/pages/dagster-essentials/lesson-8/1-what-are-partitions-and-backfills.md).
2. [Adicionando partições](../materials/orchestration/course/pages/dagster-essentials/lesson-8/4-adding-partitions-to-assets.md).
3. [Unit tests de ativos](../materials/orchestration/course/pages/dagster-testing/lesson-3/1-unit-tests.md).
4. [Testando dependências](../materials/orchestration/course/pages/dagster-testing/lesson-3/2-testing-dependencies.md).

## Prática

Particione um ativo por data, execute duas partições e depois um backfill. Escreva testes para transformação e dependência.

## Entrega

Ativo particionado, evidência do backfill e testes automatizados.

## Avance quando

- [ ] Uma partição pode ser refeita sem afetar as demais.
- [ ] O backfill não duplica dados.
- [ ] Testes não dependem de serviços reais desnecessariamente.

