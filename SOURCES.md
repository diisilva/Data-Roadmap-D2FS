# Fontes, licenças e decisões de curadoria

Pesquisa e snapshots atualizados em 16 de outubro de 2026.

## Critérios

Os materiais foram avaliados por:

1. aderência exclusiva a análise, engenharia ou arquitetura de dados;
2. utilidade para estudantes intermediários e avançados;
3. presença de exercícios, código executável ou casos de decisão;
4. manutenção recente e clareza das instruções;
5. licença explícita para redistribuição;
6. sobreposição mínima com os demais materiais;
7. possibilidade de uso local antes de gerar custos em cloud.

Popularidade ajudou a localizar candidatos, mas não foi usada como prova de qualidade.

## Snapshots incluídos

| Diretório | Projeto original | Branch | Commit | Licença | Papel na trilha |
|---|---|---|---|---|---|
| `materials/python-data-analysis` | [wesm/pydata-book](https://github.com/wesm/pydata-book) | `3rd-edition` | `a892791ce5a3831134cfa2989033ecbb9289f1ea` | MIT para os exemplos de código | Manipulação, limpeza, agregação e séries temporais |
| `materials/sql-data-analytics` | [PacktPublishing/SQL-for-Data-Analytics-Fourth-Edition](https://github.com/PacktPublishing/SQL-for-Data-Analytics-Fourth-Edition) | `main` | `aca7c89f4f260b43708b7e14da807c0a03278fd4` | MIT | SQL analítico, performance, JSON, geoespacial e estudo de caso |
| `materials/data-visualization` | [uwdata/visualization-curriculum](https://github.com/uwdata/visualization-curriculum) | `main` | `86d1c323572b7c40079ad29da2d3f46cb1b13d95` | BSD-3-Clause | Visualização declarativa e interativa com Altair/Vega-Lite |
| `materials/analytics-engineering` | [dbt-labs/jaffle_shop_duckdb](https://github.com/dbt-labs/jaffle_shop_duckdb) | `duckdb` | `20cc904370818ceab08cf19f8fd196e9e81def88` | Apache-2.0 | Ambiente local para dbt, DuckDB, modelos, testes e documentação |
| `materials/orchestration` | [dagster-io/project-dagster-university](https://github.com/dagster-io/project-dagster-university) | `main` | `bf4fab228d5112dc10eb0afaddf521f40c218f6a` | Apache-2.0 | Orquestração, ETL, integração com dbt e testes |
| `materials/data-engineering-cookbook` | [andkret/Cookbook](https://github.com/andkret/Cookbook) | `master` | `bf463f65b173aa4ecf02425456bd31c75878c188` | Apache-2.0 | Sistemas distribuídos, plataformas, processamento e decisões arquiteturais |
| `materials/data-engineering-wiki` | [data-engineering-community/data-engineering-wiki](https://github.com/data-engineering-community/data-engineering-wiki) | `main` | `05a85902a00fde086465f2f3e184f4712397ebd4` | CC0-1.0 | Conceitos, guias de decisão e referência de engenharia |

Os arquivos de licença originais permanecem dentro de cada snapshot. A licença MIT da documentação D2FS não altera essas condições.

Os snapshots não incluem os diretórios `.git` dos projetos originais. O arquivo opcional `datasets/fec/P00000001-ALL.csv` do `pydata-book` também foi omitido porque possui aproximadamente 150 MB e ultrapassa o limite normal de arquivo do GitHub. Essa exceção está registrada dentro do próprio material e o artefato pode ser obtido no upstream quando o estudo do exemplo FEC exigir.

## Fontes externas essenciais

| Fonte | Papel | Motivo para não incorporar |
|---|---|---|
| [DataTalksClub Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) | Pipeline ponta a ponta, warehouse, dbt, Spark e streaming | Curso atualizado por coorte e sem licença explícita identificada no repositório durante a curadoria |
| [DataExpert.io Data Engineer Handbook](https://github.com/DataExpert-io/data-engineer-handbook) | Bootcamp intermediário, modelagem, Spark e Flink | Sem licença explícita identificada no repositório durante a curadoria |
| [dbt Learn](https://learn.getdbt.com/) | Aulas oficiais e atualizadas de dbt | Plataforma mantida continuamente; o snapshot perderia atualizações |
| [PostgreSQL Documentation](https://www.postgresql.org/docs/current/) | SQL, índices, `EXPLAIN`, transações e administração | Documentação versionada e mais confiável na origem |
| [DuckDB Documentation](https://duckdb.org/docs/stable/) | SQL analítico local, formatos e performance | Documentação versionada e mantida pelo projeto |
| [Apache Spark Documentation](https://spark.apache.org/docs/latest/) | Processamento distribuído e Spark SQL | Projeto grande; somente módulos selecionados são necessários |
| [Apache Kafka Documentation](https://kafka.apache.org/documentation/) | Log de eventos, partições, consumidores e garantias | Projeto grande; usar a documentação da versão instalada |
| [Apache Flink Documentation](https://flink.apache.org/what-is-flink/flink-architecture/) | Estado, event time, janelas e processamento de streams | Projeto grande e de evolução rápida |

## Referências de arquitetura

Estas fontes são usadas para comparar alternativas, não para copiar uma arquitetura de fornecedor:

- [AWS Modern Data Architecture Accelerator](https://github.com/aws/modern-data-architecture-accelerator);
- [Azure Architecture Center — Big data architectures](https://learn.microsoft.com/azure/architecture/databases/guide/big-data-architectures);
- [Azure Modern Data Warehouse DataOps](https://github.com/Azure-Samples/modern-data-warehouse-dataops);
- [Google Cloud Architecture Framework — System design](https://cloud.google.com/architecture/framework/system-design);
- [AWS Well-Architected — Data Analytics Lens](https://docs.aws.amazon.com/wellarchitected/latest/analytics-lens/analytics-lens.html).

Use ao menos duas perspectivas ao justificar uma decisão importante e converta nomes de serviços em capacidades: armazenamento, catálogo, processamento, mensageria, identidade, observabilidade e consumo.

## Projetos avaliados, mas não selecionados como snapshot

| Projeto | Decisão |
|---|---|
| `dbt-labs/jaffle-shop` | O projeto atual é relevante, mas o clone pesquisado não continha arquivo de licença. Foi substituído pela variante oficial `jaffle_shop_duckdb`, licenciada e executável localmente. |
| `dbt-labs/jaffle-shop-classic` | Possui Apache-2.0, mas foi arquivado e substituído pelos projetos atuais. |
| `OSSU/data-science` | Currículo amplo demais e com grande sobreposição de estatística, ciência de dados e machine learning. |
| Repositórios completos de Spark, Kafka e ferramentas de BI | São produtos, não currículos; cloná-los aumentaria muito o repositório sem melhorar a trilha. |
| Blueprints completos de uma única nuvem | Permanecem externos para evitar que arquitetura seja ensinada como memorização de serviços de um fornecedor. |

## Política de atualização

Antes de substituir um snapshot:

1. clone o upstream em uma pasta temporária;
2. confira licença, branch recomendada, dependências e breaking changes;
3. execute os exemplos usados na trilha;
4. registre o novo commit nesta tabela;
5. atualize o roteiro se a estrutura do material mudou;
6. faça a atualização em um commit isolado.

