# Telecom X — Previsão de Churn

## Visão Geral

Este projeto analisa os fatores associados à evasão de clientes (churn) e desenvolve modelos preditivos para estimar a probabilidade de cancelamento.

A base utilizada contém 7.032 clientes após tratamento e padronização dos dados.

---

## Objetivo

- Identificar variáveis relevantes para churn.
- Avaliar padrões contratuais e comportamentais.
- Construir modelos de classificação para previsão de evasão.
- Apoiar estratégias de retenção baseadas em dados.

---

## Principais Análises

### Análise Exploratória

- Tempo de contrato apresentou correlação negativa moderada com churn (-0.35).
- Clientes com contrato mensal apresentam maior taxa de evasão.
- Valor mensal mais elevado está associado a maior risco.
- Ausência de serviços adicionais aumenta a probabilidade de cancelamento.

Esses padrões indicam que estabilidade contratual e nível de engajamento influenciam diretamente a evasão.

---

## Modelagem Preditiva

Modelos avaliados:

- Regressão Logística  
- Random Forest  

Devido ao desbalanceamento da base (~27% churn), foi aplicada versão com balanceamento de classes.

### Melhor desempenho

Regressão Logística balanceada:

- Recall (churn): ~79%
- F1-score: ~0.62

O modelo prioriza a identificação de clientes com maior risco de cancelamento, sendo adequado para estratégias preventivas.

---

## Impacto para o Negócio

A análise demonstra que o churn segue padrões identificáveis e pode ser antecipado.

### Segmentos de maior risco

- Clientes com contrato mensal.
- Clientes nos primeiros 12 meses.
- Clientes com valor mensal elevado.
- Clientes sem serviços adicionais.

### Ações recomendadas

- Incentivar migração para contratos anuais.
- Criar ações preventivas no início do relacionamento oferecendo descontos na mensalidade principalmente nos três primeiros meses.
- Oferecer pacotes com serviços adicionais.
- Revisar planos de clientes com ticket elevado.

### Uso prático do modelo

O modelo permite calcular a probabilidade individual de churn para cada cliente, possibilitando:

- Priorizar clientes com maior risco.
- Definir um threshold de atuação (ex.: agir acima de 0.70 de probabilidade).
- Otimizar orçamento de retenção.

No conjunto de teste, o modelo identificou aproximadamente 79% dos clientes que realmente cancelaram, permitindo atuação preventiva antes da perda de receita.

---

## Tecnologias

- Python  
- Pandas  
- NumPy  
- Seaborn  
- Matplotlib  
- Scikit-learn  

---

## Conclusão

A evasão apresenta padrões previsíveis e pode ser antecipada por meio de modelos de machine learning.

A regressão logística balanceada demonstrou bom equilíbrio entre desempenho e interpretabilidade, podendo ser utilizada como ferramenta estratégica de apoio à retenção.
