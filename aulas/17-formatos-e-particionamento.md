# Aula 17 — Formatos e particionamento

**Navegação:** [← Aula 16](./16-carga-incremental-e-idempotencia.md) | [Índice](../README.md) | [Próxima →](./18-camadas-de-armazenamento.md)

## Objetivo

Escolher formato, compressão e particionamento com base em medição.

## Estude nesta ordem

1. [Capítulo 6 — carregamento e formatos](../materials/python-data-analysis/ch06.ipynb).
2. [Column-oriented Database](<../materials/data-engineering-wiki/Concepts/Data Storage/Column-oriented Database.md>).
3. [Data Storage](<../materials/data-engineering-wiki/Concepts/Data Storage/Data Storage.md>).

## Prática

Grave a mesma amostra em CSV, JSON e Parquet. Compare tamanho, tempo de escrita, leitura total e leitura de poucas colunas.

## Entrega

Benchmark reproduzível e ADR do formato escolhido.

## Avance quando

- [ ] O benchmark registra volume e ambiente.
- [ ] O particionamento corresponde aos filtros reais.
- [ ] O problema de muitos arquivos pequenos foi considerado.

