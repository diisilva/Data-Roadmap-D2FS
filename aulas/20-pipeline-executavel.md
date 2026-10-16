# Aula 20 — Pipeline executável

**Navegação:** [← Aula 19](./19-qualidade-no-pipeline.md) | [Índice](../README.md) | [Próxima →](./21-revisao-de-engenharia.md)

## Objetivo

Empacotar ingestão, validação e transformação em comandos observáveis.

## Estude nesta ordem

1. [Data Pipeline](<../materials/data-engineering-wiki/Concepts/Data Pipeline.md>).
2. [Data Pipeline Best Practices](<../materials/data-engineering-wiki/Guides/Data Pipeline Best Practices.md>).
3. [Dagster ETL — visão do projeto](../materials/orchestration/course/pages/dagster-etl/lesson-1/3-project-preview.md).

## Prática

Crie comandos para carga inicial, incremental e reprocessamento. Emita logs estruturados com execução, etapa, volume, duração e erro.

## Entrega

Pipeline executável por comando e README operacional.

## Avance quando

- [ ] Códigos de saída indicam sucesso ou falha.
- [ ] Logs permitem localizar a etapa e o lote.
- [ ] Configuração e segredos não estão misturados ao código.
