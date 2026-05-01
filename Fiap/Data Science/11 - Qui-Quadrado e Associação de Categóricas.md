---
aliases: [Qui-Quadrado, Tabelas de Frequência, Cramér's V, Variáveis Categóricas]
tags: [estatistica, data-science, qui-quadrado, testes-de-hipotese]
area: Estatística
status: Pendente
data: 2026-04-30
---
## Resumo (TL;DR)

O **Teste Qui-Quadrado** é utilizado para verificar se existe uma associação estatística entre duas **variáveis categóricas** (ex: analisar se o "Tipo de Plano" de um cliente influencia no "Cancelamento"). Assim como na ANOVA, precisamos medir a força dessa associação na prática, e para o Qui-Quadrado, a ferramenta utilizada para o cálculo do Tamanho do Efeito é o **Cramér's V**.

## Conceitos Principais

- **O Teste Qui-Quadrado:**
    - Aplicado em tabelas de contingência / frequência.
    - **Hipótese Nula ($H_0$):** As variáveis são independentes (não existe associação entre elas).
    - **Hipótese Alternativa ($H_1$):** As variáveis não são independentes (existe associação).
    - A lógica do teste é comparar os *Valores Observados* na realidade contra os *Valores Esperados* caso não houvesse nenhuma relação. Diferenças grandes indicam associação.
- **Tamanho do Efeito (Cramér's V):**
    - Mede a força da associação encontrada. Seus resultados variam entre 0 e 1.
    - Valores próximos de 0 indicam associação fraca, e valores próximos de 1 indicam associação forte.
    - *Atenção:* O teste prova associação, mas **não prova causalidade**.

## Exemplos Práticos / Código
```python
import pandas as pd
import scipy.stats as stats
import numpy as np

# Tabela de Contingência (Plano vs Cancelamento)
tabela = pd.DataFrame({
    "Cancelou": [30, 20, 10],
    "Não cancelou": [70, 80, 90]
}, index=["Básico", "Intermediário", "Premium"])

# Teste Qui-Quadrado
qui2, p, graus_liberdade, esperados = stats.chi2_contingency(tabela)
print("Qui-quadrado:", qui2)
print("p-valor:", p)

# Calculando a Força da Associação (Cramér's V)
n = tabela.to_numpy().sum()
linhas, colunas = tabela.shape

cramers_v = np.sqrt(qui2 / (n * (min(linhas, colunas) - 1)))
print("Cramér's V:", cramers_v)
```
## 🔗 Conexões
- [[10 - ANOVA e Tamanho de Efeito]]

- [[07 - Introdução aos Testes de Hipóteses e Pressupostos]]