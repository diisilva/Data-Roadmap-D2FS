# Aula 19 — Qualidade no pipeline

**Navegação:** [← Aula 18](./18-camadas-de-armazenamento.md) | [Índice](../README.md) | [Próxima →](./20-pipeline-executavel.md)

## Objetivo

Inserir validações nos limites do pipeline e tratar registros inválidos sem perda silenciosa.

## Estude nesta ordem

1. [Testing Your Data Pipeline](<../materials/data-engineering-wiki/Guides/Testing Your Data Pipeline.md>).
2. [Data Unit Test](<../materials/data-engineering-wiki/Concepts/Software Engineering/Data Unit Test.md>).
3. [Testes do projeto dbt](../materials/analytics-engineering/models/schema.yml).

## Prática

Implemente validação de schema, chave, faixa, relacionamento e freshness. Direcione falhas de registro para quarentena.

## Entrega

Suíte de qualidade, tabela de quarentena e relatório de falhas.

## Avance quando

- [ ] Uma entrada inválida foi detectada em teste automatizado.
- [ ] O pipeline distingue falha de lote e falha de registro.
- [ ] Existe procedimento para corrigir e reprocessar a quarentena.

