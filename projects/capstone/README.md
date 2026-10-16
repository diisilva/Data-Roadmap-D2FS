# Capstone — Data Roadmap D2FS

O capstone deve demonstrar uma plataforma de dados pequena, confiável e justificável. Quantidade de serviços não conta como complexidade relevante.

## Proposta

Antes de implementar, registre:

- problema e decisão que os dados apoiarão;
- usuários e consumidores;
- fontes, ownership, licença e sensibilidade dos dados;
- volume atual, crescimento, frequência e freshness esperada;
- três requisitos funcionais;
- três atributos de qualidade mensuráveis;
- restrições de custo, prazo, infraestrutura e segurança;
- arquitetura proposta e uma alternativa rejeitada;
- critérios de aceitação.

## Fluxo mínimo

```text
Fonte
  -> ingestão reproduzível
  -> dados brutos imutáveis ou recuperáveis
  -> validação e quarentena
  -> transformação e modelo analítico
  -> consumo por SQL, relatório ou dashboard
  -> métricas operacionais, alertas e runbook
```

## Entregáveis obrigatórios

- `README.md` com contexto, arquitetura e instruções de execução;
- dependências declaradas e configuração sem segredos versionados;
- pipeline idempotente com carga inicial e incremental;
- camada bruta e camada analítica com grão documentado;
- testes de schema, conteúdo e ao menos uma regra de negócio;
- tratamento de dado inválido e schema drift;
- orquestração, logs estruturados e uma métrica de freshness;
- caso analítico ou dashboard com definições de métricas;
- diagrama de contexto e diagrama de containers ou componentes;
- pelo menos três ADRs;
- data contract da principal interface;
- runbook com falhas esperadas, diagnóstico e recuperação;
- estimativa de custo e capacidade, mesmo quando a execução for local;
- demonstração de uma falha provocada e sua recuperação;
- limitações, riscos e plano de evolução.

## Restrições saudáveis

- Use um domínio e uma pergunta central.
- Use uma ferramenta por responsabilidade.
- Não use Spark se o ganho não puder ser medido.
- Não use streaming se o requisito tolerar processamento batch.
- Não crie recursos pagos sem budget e alertas de custo.
- Não armazene dado pessoal real quando dados sintéticos forem suficientes.

## Rubrica

| Critério | Peso | Evidência esperada |
|---|---:|---|
| Análise e comunicação | 10% | Pergunta, métricas, visualização e conclusões defensáveis |
| Modelagem e qualidade | 15% | Grão, fatos/dimensões ou modelo equivalente, testes e contratos |
| Engenharia e reprodutibilidade | 25% | Ingestão incremental, idempotência, testes e execução limpa |
| Confiabilidade e operação | 15% | Logs, SLIs, alertas, backfill, runbook e recuperação demonstrada |
| Arquitetura e trade-offs | 20% | Requisitos, diagramas, ADRs, alternativas e plano de evolução |
| Segurança e governança | 10% | Classificação, acesso, retenção, linhagem e auditoria |
| Custos e capacidade | 5% | Hipóteses, estimativas, limites e forma de medição |

O projeto está concluído com pelo menos 75%, sem nota zero em qualquer critério e com outra pessoa conseguindo executar o caminho principal usando apenas a documentação.

## Sugestões de domínio

- mobilidade urbana com dados públicos;
- preços, inflação e indicadores econômicos;
- clima e eventos extremos;
- transparência orçamentária;
- energia e consumo;
- vendas sintéticas de marketplace;
- qualidade de serviço e chamados anonimizados.

## Checklist de encerramento

- [ ] Uma instalação limpa funciona.
- [ ] A carga inicial e a incremental foram testadas.
- [ ] Reexecutar não duplica dados.
- [ ] Um registro inválido foi detectado e tratado.
- [ ] Uma falha operacional foi simulada e recuperada.
- [ ] As métricas de negócio possuem definição e grão.
- [ ] Diagramas e ADRs representam o que foi implementado.
- [ ] Custos e limitações foram declarados.
- [ ] Não existem credenciais ou dados sensíveis versionados.

