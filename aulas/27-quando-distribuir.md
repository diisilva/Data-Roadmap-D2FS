# Aula 27 — Quando distribuir

**Navegação:** [← Aula 26](./26-observabilidade-e-incidentes.md) | [Índice](../README.md) | [Próxima →](./28-spark-e-processamento-batch.md)

## Objetivo

Reconhecer quando processamento distribuído resolve um requisito real e quando adiciona apenas custo.

## Estude nesta ordem

1. [Advanced Engineering Skills](../materials/data-engineering-cookbook/sections/03-AdvancedSkills.md), seções sobre escala e processamento.
2. [Horizontal Scaling](<../materials/data-engineering-wiki/Concepts/Software Engineering/Horizontal Scaling.md>).
3. [Vertical Scaling](<../materials/data-engineering-wiki/Concepts/Software Engineering/Vertical Scaling.md>).
4. [Batch Data Processing](<../materials/data-engineering-wiki/Concepts/Data Processing/Batch Data Processing.md>).

## Prática

Meça o pipeline atual e projete três cenários de crescimento. Compare escala vertical, particionamento local e cluster.

## Entrega

ADR local versus distribuído com gatilhos quantitativos.

## Avance quando

- [ ] A decisão usa volume, tempo, memória e custo.
- [ ] Complexidade operacional aparece nas consequências.
- [ ] Existe um gatilho claro para revisitar a decisão.

