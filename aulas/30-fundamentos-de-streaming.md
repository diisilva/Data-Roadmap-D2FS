# Aula 30 — Fundamentos de streaming

**Navegação:** [← Aula 29](./29-performance-distribuida.md) | [Índice](../README.md) | [Próxima →](./31-tempo-janelas-e-garantias.md)

## Objetivo

Modelar eventos, chaves, partições, offsets e consumidores antes de implementar streaming.

## Estude nesta ordem

1. [Stream Data Processing](<../materials/data-engineering-wiki/Concepts/Data Processing/Stream Data Processing.md>).
2. [Message Broker](<../materials/data-engineering-wiki/Concepts/Data Processing/Message Broker.md>).
3. [Publisher-Subscriber Pattern](<../materials/data-engineering-wiki/Concepts/Software Engineering/Publisher-Subscriber Pattern.md>).
4. [Zoomcamp — Streaming](https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/06-streaming).

## Prática

Defina um evento com chave, timestamp, schema e política de evolução. Produza e consuma eventos localmente.

## Entrega

Contrato do evento, produtor, consumidor e desenho de partições.

## Avance quando

- [ ] A chave preserva a ordem necessária.
- [ ] Retenção e replay estão definidos.
- [ ] Duplicidade e falha do consumidor possuem tratamento.
