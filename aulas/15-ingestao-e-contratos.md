# Aula 15 — Ingestão e contratos

**Navegação:** [← Aula 14](./14-incrementalidade-e-linhagem.md) | [Índice](../README.md) | [Próxima →](./16-carga-incremental-e-idempotencia.md)

## Objetivo

Definir claramente a interface de uma fonte antes de programar sua ingestão.

## Estude nesta ordem

1. [Data Ingestion](<../materials/data-engineering-wiki/Concepts/Data Ingestion/Data Ingestion.md>).
2. [Full Load](<../materials/data-engineering-wiki/Concepts/Data Ingestion/Full Load.md>).
3. [Data Contract](<../materials/data-engineering-wiki/Concepts/Data Management/Data Contract.md>).
4. [Template de data contract](../docs/templates/DATA-CONTRACT-template.md).

## Prática

Escolha uma API ou banco. Documente autenticação, paginação, limites, schema, chave, timezone, frequência e tratamento de erro.

## Entrega

Data contract preenchido e desenho da ingestão.

## Avance quando

- [ ] Produtor, consumidor e ownership estão claros.
- [ ] Compatibilidade e mudança de schema possuem política.
- [ ] Nenhum segredo aparece no contrato ou no código.

