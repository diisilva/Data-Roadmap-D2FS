# Aula 13 — Testes e documentação dbt

**Navegação:** [← Aula 12](./12-dbt-e-duckdb.md) | [Índice](../README.md) | [Próxima →](./14-incrementalidade-e-linhagem.md)

## Objetivo

Proteger o data mart com testes de estrutura, conteúdo e regras de negócio.

## Estude nesta ordem

1. [Schema e testes do exemplo](../materials/analytics-engineering/models/schema.yml).
2. [Schema da camada staging](../materials/analytics-engineering/models/staging/schema.yml).
3. [Documentação dos modelos](../materials/analytics-engineering/models/docs.md).
4. [Testing Your Data Pipeline](<../materials/data-engineering-wiki/Guides/Testing Your Data Pipeline.md>).

## Prática

Adicione testes de `not_null`, `unique`, relacionamentos e pelo menos uma regra singular. Gere a documentação do projeto.

## Entrega

Data mart testado, descrito e navegável em `dbt docs`.

## Avance quando

- [ ] Uma violação proposital faz o build falhar.
- [ ] Modelos e colunas críticas possuem descrição.
- [ ] Cada teste possui uma resposta operacional definida.

