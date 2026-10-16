# Aula 18 — Camadas de armazenamento

**Navegação:** [← Aula 17](./17-formatos-e-particionamento.md) | [Índice](../README.md) | [Próxima →](./19-qualidade-no-pipeline.md)

## Objetivo

Separar preservação, padronização e consumo sem criar camadas sem função.

## Estude nesta ordem

1. [Medallion Architecture](<../materials/data-engineering-wiki/Concepts/Data Architecture/Medallion Architecture.md>).
2. [Data Lake](<../materials/data-engineering-wiki/Concepts/Data Architecture/Data Lake.md>).
3. [Data Warehouse](<../materials/data-engineering-wiki/Concepts/Data Architecture/Data Warehouse.md>).

## Prática

Organize seu pipeline em raw, staging e curated. Para cada camada, defina finalidade, mutabilidade, retenção, formato e consumidores.

## Entrega

Estrutura de armazenamento e diagrama do fluxo de dados.

## Avance quando

- [ ] O dado bruto pode ser usado para reprocessamento.
- [ ] A camada analítica possui contratos e grão definidos.
- [ ] Cada cópia adicional tem uma justificativa.

