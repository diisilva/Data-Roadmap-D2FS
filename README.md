# Data Roadmap D2FS

Uma trilha prática de 40 semanas, em nível intermediário e avançado, dedicada a **análise, engenharia e arquitetura de dados**.

O objetivo não é acumular cursos ou conhecer o maior número possível de ferramentas. O objetivo é produzir evidências profissionais: análises reproduzíveis, modelos de dados, pipelines confiáveis, testes, observabilidade, decisões arquiteturais e uma plataforma de dados documentada.

Machine learning, IA generativa e desenvolvimento de agentes estão deliberadamente fora do escopo.

## Para quem é

Esta trilha é indicada para quem já possui os fundamentos e quer avançar para projetos de portfólio com profundidade técnica. Antes de começar, você deve conseguir:

- escrever funções e pequenos programas em Python;
- consultar tabelas com `SELECT`, `JOIN`, `GROUP BY` e subconsultas;
- usar terminal, Git e ambientes virtuais;
- instalar ferramentas e investigar erros usando documentação;
- ler material técnico em inglês com apoio de tradução quando necessário.

Se o diagnóstico inicial revelar dificuldade nesses pontos, revise primeiro a trilha ampla do repositório D2FS original.

## Resultado esperado

Ao concluir a trilha, você deverá conseguir:

- transformar uma pergunta de negócio em métricas, consultas e visualizações defensáveis;
- analisar dados com SQL e Python sem etapas manuais ocultas;
- projetar modelos relacionais, dimensionais e camadas analíticas;
- construir pipelines batch incrementais, idempotentes e testáveis;
- orquestrar, observar e recuperar workloads de dados;
- explicar quando usar warehouse, lake, lakehouse, batch ou streaming;
- registrar requisitos, restrições e trade-offs em documentos de arquitetura;
- incorporar qualidade, segurança, governança, confiabilidade e custos ao desenho;
- entregar uma plataforma de dados pequena que outra pessoa consiga executar e avaliar.

## Carga e método

- Duração: 40 semanas.
- Ritmo recomendado: 8 a 12 horas por semana.
- Regra de estudo: um material principal e, no máximo, uma referência por vez.
- Regra de avanço: conclua a entrega e o critério da fase antes de seguir.
- Evidências: registre sessões, commits e demonstrações em [PROGRESS.md](./PROGRESS.md).
- Dados: prefira conjuntos públicos pequenos; aumente volume somente quando isso testar uma hipótese de arquitetura.
- Cloud: use primeiro uma implementação local; escolha somente uma nuvem para a especialização.

## Visão da trilha

| Etapa | Semanas | Foco | Evidência principal |
|---|---:|---|---|
| Diagnóstico técnico | 1–2 | Reprodutibilidade, profiling e desenho inicial | Auditoria de um conjunto de dados |
| Análise avançada | 3–8 | SQL, Python, estatística aplicada e visualização | Case analítico reproduzível |
| Revisão 1 | 9 | Qualidade da análise e comunicação | Case revisado por rubrica |
| Modelagem e Analytics Engineering | 10–14 | Modelagem dimensional, dbt, testes e linhagem | Data mart documentado |
| Engenharia de pipelines | 15–20 | Ingestão, formatos, incrementalidade e armazenamento | Pipeline batch idempotente |
| Revisão 2 | 21 | Reexecução limpa e eliminação de débito técnico | Release reproduzível |
| Orquestração e confiabilidade | 22–26 | Dagster, testes, backfill, SLIs e incidentes | Pipeline orquestrado e observável |
| Dados distribuídos e streaming | 27–31 | Spark, Kafka/Flink, particionamento e semântica de entrega | Protótipo batch e streaming |
| Arquitetura de dados | 32–36 | Plataformas, governança, segurança, FinOps e ADRs | Pacote de arquitetura |
| Capstone | 37–40 | Integração ponta a ponta | Plataforma de dados de portfólio |

## Fase 0 — Diagnóstico técnico (semanas 1–2)

Competências: leitura de repositórios, ambientes reproduzíveis, profiling, contratos básicos, identificação de riscos e decomposição de um problema de dados.

Atividades:

- escolher um dataset com contexto e dicionário de dados;
- criar ambiente reproduzível e comandos de qualidade;
- medir completude, unicidade, validade e consistência;
- desenhar o fluxo atual e registrar três riscos;
- criar o primeiro Architecture Decision Record (ADR).

Entrega: relatório de auditoria, script reproduzível e diagrama do fluxo.

Critério: outra pessoa consegue reproduzir o perfil dos dados e localizar cada premissa registrada.

## Fase 1 — Análise avançada (semanas 3–8)

Competências: window functions, CTEs, planos de execução, índices, JSON, séries temporais, estatística aplicada, manipulação vetorizada, desenho de métricas e visualização interativa.

Sequência sugerida:

- Semana 3: perguntas, grão, dimensões, métricas e vieses.
- Semana 4: CTEs, subconsultas, joins complexos e window functions.
- Semana 5: planos de execução, índices e SQL orientado a desempenho.
- Semana 6: limpeza, reshaping, agregações e séries temporais em Python.
- Semana 7: incerteza, distribuições, testes de hipótese e comunicação de limitações.
- Semana 8: visualização, interação e narrativa analítica.

Materiais principais:

- [SQL for Data Analytics](./materials/sql-data-analytics/);
- [Python for Data Analysis](./materials/python-data-analysis/);
- [Data Visualization Curriculum](./materials/data-visualization/).

Entrega: case com perguntas, consultas, notebook ou script, visualizações e recomendações, incluindo ao menos uma análise de desempenho SQL.

Critério: os resultados são regenerados a partir dos dados brutos e cada conclusão está ligada a uma evidência.

## Revisão 1 — Qualidade analítica (semana 9)

- separar exploração de transformação reproduzível;
- verificar definições de métricas e denominadores;
- testar casos ausentes, duplicados e extremos;
- reduzir gráficos que não apoiam uma decisão;
- pedir revisão de outra pessoa ou fazer uma revisão adversarial documentada.

## Fase 2 — Modelagem e Analytics Engineering (semanas 10–14)

Competências: normalização, modelo dimensional, fatos e dimensões, SCD, camadas staging/intermediate/marts, transformações incrementais, testes, documentação e linhagem.

Sequência sugerida:

- Semana 10: modelagem conceitual, lógica e física.
- Semana 11: esquema estrela, grão, fatos, dimensões e histórico.
- Semana 12: projeto dbt local com DuckDB.
- Semana 13: testes genéricos, singulares, contratos e documentação.
- Semana 14: modelos incrementais, snapshots, linhagem e revisão do DAG.

Material principal: [Jaffle Shop com dbt e DuckDB](./materials/analytics-engineering/).

Entrega: data mart versionado com fontes, modelos, testes, documentação e ao menos uma tabela incremental.

Critério: `dbt build` funciona em ambiente limpo e uma mudança incompatível de dados é detectada por teste ou contrato.

## Fase 3 — Engenharia de pipelines (semanas 15–20)

Competências: APIs, paginação, retries, carga incremental, CDC conceitual, idempotência, Parquet, particionamento, storage em camadas, metadados e tratamento de schema drift.

Sequência sugerida:

- Semana 15: desenho de interfaces de ingestão e contratos.
- Semana 16: ingestão incremental, checkpoints e deduplicação.
- Semana 17: CSV, JSON, Parquet, compressão e particionamento.
- Semana 18: raw, staging e curated; retenção e reprocessamento.
- Semana 19: qualidade no pipeline e quarentena de registros.
- Semana 20: empacotamento, logs estruturados e execução por comando.

Materiais principais:

- [Data Engineering Wiki](./materials/data-engineering-wiki/);
- módulos selecionados do [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp), usado como fonte externa.

Entrega: pipeline batch incremental que ingere uma API ou banco, preserva a camada bruta e publica tabelas analíticas.

Critério: repetir uma execução não duplica dados; uma falha intermediária pode ser recuperada sem apagar todo o ambiente.

## Revisão 2 — Release reproduzível (semana 21)

- executar o projeto em ambiente limpo;
- testar carga inicial, carga incremental, reprocessamento e dado inválido;
- eliminar caminhos absolutos e segredos versionados;
- medir tempo, volume processado e custo quando houver cloud;
- publicar uma release com limitações conhecidas.

## Fase 4 — Orquestração e confiabilidade (semanas 22–26)

Competências: assets, dependências, schedules, sensors, retries, backfills, testes unitários e de integração, SLIs/SLOs, alertas, runbooks e resposta a incidentes.

Sequência sugerida:

- Semana 22: modelagem do pipeline como grafo de ativos.
- Semana 23: schedules, sensores, recursos e configurações.
- Semana 24: integração entre orquestrador, dbt e armazenamento.
- Semana 25: testes, particionamento, backfills e recuperação.
- Semana 26: métricas operacionais, alertas e simulação de incidente.

Material principal: [Dagster University](./materials/orchestration/), especialmente os cursos Essentials, ETL, dbt e Testing.

Entrega: pipeline orquestrado com agenda, backfill, testes, observações operacionais e runbook.

Critério: demonstrar uma falha proposital, detectar o problema, recuperar a execução e explicar o impacto nos dados publicados.

## Fase 5 — Dados distribuídos e streaming (semanas 27–31)

Competências: processamento distribuído, shuffle, particionamento, skew, Spark SQL, eventos, Kafka, event time, janelas, late data e garantias at-most-once, at-least-once e effectively-once.

Sequência sugerida:

- Semana 27: quando processamento distribuído é justificável.
- Semana 28: DataFrames, Spark SQL, joins, shuffle e particionamento.
- Semana 29: otimização, skew, formatos colunares e medição.
- Semana 30: log de eventos, chaves, partições, offsets e schemas.
- Semana 31: janelas, late data, reprocessamento e comparação batch/streaming.

Materiais principais:

- módulos Batch e Streaming do [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp);
- seções de processamento do [Data Engineering Cookbook](./materials/data-engineering-cookbook/).

Entrega: duas implementações pequenas do mesmo requisito, uma batch e outra orientada a eventos, acompanhadas por uma decisão documentada.

Critério: explicar custos, consistência, latência, operação e modo de falha de cada alternativa sem escolher streaming apenas por preferência tecnológica.

## Fase 6 — Arquitetura de dados (semanas 32–36)

Competências: requisitos de qualidade, arquitetura evolutiva, warehouse/lake/lakehouse, data mesh, integração batch e streaming, catálogo, linhagem, segurança, privacidade, continuidade, capacidade e FinOps.

Sequência sugerida:

- Semana 32: requisitos funcionais, atributos de qualidade e restrições.
- Semana 33: comparação entre warehouse, lake e lakehouse.
- Semana 34: governança, ownership, catálogo, linhagem e contratos.
- Semana 35: IAM, classificação, criptografia, retenção e auditoria.
- Semana 36: capacidade, disponibilidade, RPO/RTO, custos e plano de evolução.

Materiais principais:

- [Data Engineering Cookbook](./materials/data-engineering-cookbook/);
- [Data Engineering Wiki](./materials/data-engineering-wiki/);
- centros oficiais de arquitetura listados em [SOURCES.md](./SOURCES.md).

Entrega: pacote de arquitetura contendo contexto, requisitos, diagramas, modelo de dados, fluxo, ameaças, estimativa de custos, SLOs, plano de recuperação e pelo menos três ADRs.

Critério: cada componente do desenho responde a um requisito ou restrição; alternativas rejeitadas e consequências estão registradas.

## Fase 7 — Capstone (semanas 37–40)

Construa uma plataforma pequena que conecte fonte, ingestão, armazenamento, transformação, consumo e operação. Não é obrigatório usar cloud, Spark ou Kafka: a arquitetura deve ser proporcional ao problema.

- Semana 37: proposta, arquitetura, dados e critérios de aceitação.
- Semana 38: ingestão, armazenamento, modelagem e qualidade.
- Semana 39: orquestração, observabilidade, consumo e testes.
- Semana 40: teste de recuperação, documentação, demonstração e retrospectiva.

O escopo completo e a rubrica estão em [projects/capstone/README.md](./projects/capstone/README.md).

## Stack de referência

| Necessidade | Escolha principal | Alternativa de aprofundamento |
|---|---|---|
| Linguagem | Python | Java ou Scala para ecossistemas específicos |
| SQL local | DuckDB | PostgreSQL |
| Banco relacional | PostgreSQL | Serviço gerenciado da nuvem escolhida |
| Formato analítico | Parquet | Iceberg, Delta Lake ou Hudi |
| Transformação | dbt | SQLMesh |
| Orquestração | Dagster | Airflow ou Kestra |
| Batch distribuído | Spark | Polars/DuckDB antes de distribuir |
| Streaming | Kafka + Flink | Serviços gerenciados equivalentes |
| Visualização | Altair e uma ferramenta BI | Metabase, Power BI ou Superset |
| Infraestrutura | Docker e Terraform | IaC nativa da nuvem escolhida |

As alternativas não são tarefas extras obrigatórias. Trocar de ferramenta sem uma necessidade concreta reduz a profundidade do estudo.

## Estrutura do repositório

```text
Data-Roadmap-D2FS/
├── README.md
├── PROGRESS.md
├── SOURCES.md
├── LICENSE
├── docs/
│   └── templates/
├── materials/             # snapshots licenciados e versionados
└── projects/
    └── capstone/
```

## Como preparar um projeto

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
```

Cada material possui suas próprias dependências. Não instale todos os projetos no mesmo ambiente e não instale dependências globalmente.

## Curadoria, snapshots e licenças

Os materiais foram escolhidos por profundidade, aplicabilidade, manutenção, reprodutibilidade e licença. Somente repositórios com licença explícita foram incorporados. Projetos grandes, voláteis ou sem permissão clara permanecem como links externos.

Consulte [SOURCES.md](./SOURCES.md) para origem, commit, licença, papel na trilha e decisão de inclusão.

Os textos originais da D2FS usam a licença MIT disponível em [LICENSE](./LICENSE). Cada material de terceiro continua sujeito exclusivamente à sua própria licença.

## Próxima ação

Preencha o diagnóstico em [PROGRESS.md](./PROGRESS.md). Depois escolha um conjunto de dados e produza a auditoria da Fase 0 antes de instalar ferramentas distribuídas ou criar recursos em cloud.

