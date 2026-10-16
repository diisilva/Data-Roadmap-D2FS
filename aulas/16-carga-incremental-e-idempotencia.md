# Aula 16 — Carga incremental e idempotência

**Navegação:** [← Aula 15](./15-ingestao-e-contratos.md) | [Índice](../README.md) | [Próxima →](./17-formatos-e-particionamento.md)

## Objetivo

Construir uma ingestão recuperável que processe somente mudanças e suporte reexecução.

## Estude nesta ordem

1. [Delta Load](<../materials/data-engineering-wiki/Concepts/Data Ingestion/Delta Load.md>).
2. [Change Data Capture](<../materials/data-engineering-wiki/Concepts/Data Ingestion/Change Data Capture.md>).
3. [Idempotence](<../materials/data-engineering-wiki/Concepts/Software Engineering/Idempotence.md>).

## Prática

Implemente checkpoint, paginação, retry com limite e deduplicação. Simule interrupção no meio da carga e reinicie.

## Entrega

Ingestão incremental com testes de primeira carga, repetição e recuperação.

## Avance quando

- [ ] Reexecutar produz o mesmo estado final.
- [ ] O checkpoint só avança após persistência bem-sucedida.
- [ ] Registros atrasados possuem tratamento conhecido.

