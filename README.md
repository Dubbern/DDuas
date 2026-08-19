# DDUAS — Data Science Consulting

### Data Science · Credit Risk · Credit Scoring · Model Validation · Risk Monitoring

## Status

🟢 **Concluído — Projeto de consultoria / Data Science aplicado a risco de crédito**

Projeto desenvolvido no contexto da minha atuação como **Consultor de Dados na DDUAS**, participando da construção de uma solução de **modelagem, validação e monitoramento de risco de crédito** para uma empresa do setor financeiro.

O trabalho envolveu desde o processamento e preparação das bases até a modelagem preditiva, validação temporal, análise de estabilidade, identificação de riscos metodológicos e geração automatizada de relatórios técnicos.

> 🔒 **Repositório privado:** o projeto envolve dados financeiros e informações confidenciais. O código e as bases utilizadas não são disponibilizados publicamente.

---

## Sobre o Projeto

A solução foi estruturada como um pipeline modular de Data Science para avaliação de modelos de credit scoring e acompanhamento da estabilidade das variáveis ao longo do tempo.

```text
Dados
  ↓
Data Preparation
  ↓
Feature Engineering
  ↓
WOE / IV / Binning
  ↓
Modelagem
  ↓
Validação Temporal
  ↓
Performance
  ↓
Stability / Drift
  ↓
Risk Checks
  ↓
Relatórios
```

A arquitetura foi desenvolvida com foco em **automação, rastreabilidade, comparabilidade e consistência da análise**.

---

## Objetivo

Desenvolver uma solução capaz de:

- Processar bases de crédito de forma automatizada;
- Preparar variáveis para modelagem;
- Criar e comparar modelos de credit scoring;
- Realizar validação temporal;
- Avaliar performance discriminatória;
- Monitorar estabilidade das variáveis;
- Identificar possíveis problemas metodológicos;
- Consolidar resultados em relatórios técnicos.

---

## Pipeline de Dados

O pipeline foi organizado em camadas independentes:

```text
1. Data Processing
        ↓
2. Feature Engineering
        ↓
3. Modeling
        ↓
4. Validation
        ↓
5. Stability Monitoring
        ↓
6. Consolidation / Reporting
```

Essa organização permite separar responsabilidades e facilitar a manutenção e evolução da solução.

---

## Feature Engineering

Foram automatizadas etapas de preparação e transformação das variáveis, incluindo:

- Tratamento de valores ausentes;
- Binning;
- Weight of Evidence (WOE);
- Information Value (IV);
- Seleção e tratamento de variáveis;
- Versionamento dos processamentos.

A automação permitiu processar dezenas de variáveis de forma estruturada, reduzindo esforço manual e aumentando a consistência das análises.

---

## Modelagem de Credit Scoring

Foram desenvolvidos e comparados modelos utilizando:

- **Regressão Logística**;
- **XGBoost**.

A comparação considerou métricas de discriminação e o comportamento dos modelos ao longo das diferentes amostras.

---

## Validação Temporal

A avaliação foi estruturada considerando:

```text
Treino
  ↓
Teste
  ↓
Out-of-Time
```

Essa abordagem permitiu avaliar não apenas a performance dentro da amostra, mas também o comportamento dos modelos em períodos temporais distintos.

### Métricas utilizadas

- AUC;
- KS;
- Gini.

---

## Estabilidade e Drift

Foi implementada uma camada específica para avaliar o comportamento das variáveis ao longo do tempo.

As análises incluíram:

- PSI;
- Análise temporal;
- Monotonicidade;
- Evolução das distribuições;
- Identificação de possíveis mudanças relevantes nas variáveis.

Fluxo:

```text
Variável
   ↓
Distribuição Temporal
   ↓
PSI
   ↓
Drift / Stability
   ↓
Análise
```

---

## Data Leakage e Variáveis Proxy

O pipeline também incorporou rotinas para identificar possíveis problemas que poderiam comprometer a validade da modelagem.

Entre as verificações:

- Possíveis casos de **data leakage**;
- Variáveis potencialmente relacionadas ao target de forma inadequada;
- Possíveis variáveis proxy do target.

Essas verificações foram utilizadas como camada adicional de controle metodológico.

---

## Relatórios Automatizados

Os resultados das diferentes etapas foram consolidados em relatórios técnicos em PDF.

```text
Pipeline
   ↓
Resultados
   ↓
Métricas
   ↓
Validações
   ↓
Stability Analysis
   ↓
PDF Consolidado
```

A automação dos relatórios facilitou:

- Avaliação técnica;
- Documentação;
- Comparação dos modelos;
- Comunicação dos resultados;
- Rastreabilidade das execuções.

---

## Arquitetura Conceitual

```text
                         ┌──────────────────────┐
                         │     Dados de Crédito │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │  Data Preparation    │
                         │ Missing / Binning    │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │ Feature Engineering  │
                         │ WOE / IV             │
                         └──────────┬───────────┘
                                    │
                          ┌─────────┴─────────┐
                          ▼                   ▼
                   ┌─────────────┐     ┌─────────────┐
                   │ Logistic    │     │  XGBoost    │
                   │ Regression  │     │             │
                   └──────┬──────┘     └──────┬──────┘
                          │                   │
                          └─────────┬─────────┘
                                    ▼
                         ┌──────────────────────┐
                         │ Temporal Validation  │
                         │ AUC / KS / Gini      │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │ Stability / Drift    │
                         │ PSI / Monotonicity   │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │ Risk Checks          │
                         │ Leakage / Proxy      │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │ PDF Reports          │
                         └──────────────────────┘
```

---

## Tecnologias

| Categoria | Tecnologias |
|---|---|
| Linguagem | **Python** |
| Manipulação de Dados | **Pandas** |
| Machine Learning | **Scikit-learn** |
| Gradient Boosting | **XGBoost** |
| Modelagem | Regressão Logística · XGBoost |
| Credit Scoring | AUC · KS · Gini |
| Feature Engineering | WOE · IV · Binning |
| Stability Monitoring | PSI · Análise Temporal |
| Reporting | Geração automatizada de PDF |
| Organização | Pipeline modular e automatizado |

---

## Competências Aplicadas

O projeto envolveu competências em:

- Data Science;
- Credit Risk;
- Credit Scoring;
- Modelagem preditiva;
- Feature Engineering;
- Statistical Validation;
- Model Stability;
- Drift Monitoring;
- Data Quality;
- Data Leakage Detection;
- Model Governance;
- Automatização de análises;
- Geração de relatórios.

---

## O que este projeto demonstra

- Desenvolvimento de pipelines de Data Science;
- Modelagem de risco de crédito;
- Credit scoring;
- Regressão Logística;
- XGBoost;
- WOE;
- IV;
- Binning;
- AUC;
- KS;
- Gini;
- PSI;
- Validação out-of-time;
- Monitoramento de estabilidade;
- Identificação de data leakage;
- Análise de variáveis proxy;
- Automação de processos analíticos;
- Geração automatizada de relatórios;
- Estruturação de soluções de modelagem com rastreabilidade.

---

## Contexto Profissional

Este projeto foi desenvolvido durante minha atuação como **Consultor de Dados na DDUAS**, em um contexto de aplicação de Data Science a **risco de crédito no setor financeiro**.

A experiência envolveu participação direta em aspectos técnicos como:

- Estruturação do pipeline;
- Tratamento e preparação dos dados;
- Modelagem;
- Validação;
- Análise de estabilidade;
- Automação;
- Consolidação de resultados;
- Apoio a decisões técnicas sobre variáveis e modelos.

---

## Privacidade e Disponibilidade

🔒 **Repositório privado**

O projeto utiliza **dados financeiros e informações confidenciais**, portanto o código-fonte completo e as bases utilizadas não são disponibilizados publicamente.

Esta documentação apresenta a arquitetura, metodologia e competências técnicas envolvidas sem expor informações proprietárias ou dados sensíveis.

---

## Limitações

- O projeto foi desenvolvido em contexto privado e seus dados não podem ser disponibilizados;
- As métricas e resultados específicos dependem das bases utilizadas no projeto;
- As implementações internas de algumas rotinas não são públicas;
- O pipeline foi desenvolvido para um contexto específico de risco de crédito e pode exigir adaptação para outros cenários.

---

## Melhorias Futuras

- Monitoramento contínuo de drift;
- Automação de model governance;
- Model registry;
- Monitoramento de performance pós-deploy;
- Dashboards de estabilidade;
- Alertas automáticos;
- Integração com MLflow;
- Feature Store;
- Monitoramento de fairness;
- Pipeline de revalidação automatizada;
- Integração com APIs e sistemas de decisão.

---

## Status Final

🟢 **Concluído — Consultoria em Data Science / Risco de Crédito**

O projeto foi concluído como uma solução de **modelagem e monitoramento de risco de crédito**, contemplando:

- ✅ Pipeline modular de dados;
- ✅ Feature Engineering;
- ✅ WOE;
- ✅ IV;
- ✅ Binning;
- ✅ Regressão Logística;
- ✅ XGBoost;
- ✅ Validação temporal;
- ✅ Out-of-Time;
- ✅ AUC;
- ✅ KS;
- ✅ Gini;
- ✅ PSI;
- ✅ Análise de estabilidade;
- ✅ Detecção de possíveis data leakage;
- ✅ Análise de variáveis proxy;
- ✅ Automação de processamento;
- ✅ Geração de relatórios PDF;
- ✅ Rastreabilidade e consolidação dos resultados.

O projeto permanece **privado devido à natureza confidencial dos dados utilizados**, sendo mantido como registro técnico da experiência em **Data Science, Credit Risk e Model Monitoring**.

---

## Autor

**Yuri Fernando Dubbern**

Data Science · Credit Risk · Machine Learning · Model Validation · Data Engineering

[LinkedIn](https://www.linkedin.com/in/yuridubbern) · [GitHub](https://github.com/Yuri-Fernando) · [Lattes](http://lattes.cnpq.br/7151392692642166) · [Linktree](https://linktr.ee/yuri.f.dubbern)
