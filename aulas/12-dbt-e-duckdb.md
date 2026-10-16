# Aula 12 — dbt e DuckDB

**Navegação:** [← Aula 11](./11-modelagem-dimensional.md) | [Índice](../README.md) | [Próxima →](./13-testes-e-documentacao-dbt.md)

## Objetivo

Executar um projeto dbt local e entender sources, models, seeds e materializations.

## Estude nesta ordem

1. [Instruções do Jaffle Shop com DuckDB](../materials/analytics-engineering/README.md).
2. [Configuração do projeto](../materials/analytics-engineering/dbt_project.yml).
3. [Modelos de staging](../materials/analytics-engineering/models/staging/).
4. [Modelo de pedidos](../materials/analytics-engineering/models/orders.sql).

## Prática

Execute `dbt build` no projeto de exemplo. Depois crie um projeto separado e implemente staging para duas fontes do seu case.

## Entrega

Projeto dbt local com sources e modelos de staging.

## Avance quando

- [ ] `dbt build` termina sem erro.
- [ ] SQL de staging apenas renomeia, tipa e padroniza.
- [ ] O banco DuckDB pode ser recriado do zero.

