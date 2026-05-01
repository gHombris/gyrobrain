---
aliases: [ANOVA, Tamanho de Efeito, Eta Squared, Significância Prática]
tags: [estatistica, data-science, anova, testes-de-hipotese]
area: Estatística
status: Pendente
data: 2026-04-30
---
## Resumo (TL;DR)

A **ANOVA (Análise de Variância)** é o teste paramétrico utilizado para comparar as médias de **três ou mais grupos independentes** simultaneamente. No entanto, saber apenas se existe diferença estatística (p-valor < 0,05) não é suficiente; precisamos do **Tamanho de Efeito** para entender a magnitude e a relevância prática dessa diferença. Na ANOVA, utilizamos a métrica **Eta Squared ($\eta^{2}$)** para quantificar o impacto da variação entre os grupos.

## Conceitos Principais

- **A Necessidade da ANOVA:**
    - Quando testamos 3 ou mais grupos (ex: comparar a acurácia de três modelos de ML diferentes), testes 't' simples não bastam.
    - **Hipótese Nula ($H_0$):** Todas as médias são iguais.
    - **Hipótese Alternativa ($H_1$):** Pelo menos uma média é significativamente diferente das demais.
- **Significância vs. Relevância:**
    - Significância estatística (p-valor) responde: "A diferença é real ou acaso?".
    - Relevância prática (Tamanho do Efeito) responde: "Essa diferença é grande o suficiente para importar no mundo real?".
- **Tamanho de Efeito (Eta Squared - $\eta^{2}$):**
    - Mede a proporção da variação total que é explicada pela diferença entre os grupos.
    - **Leitura Geral:** ~0,01 (Efeito Pequeno), ~0,06 (Efeito Médio), ~0,14 ou maior (Efeito Grande).

## Exemplos Práticos / Código
```python
import numpy as np
import scipy.stats as stats

# Acurácias de 3 Modelos de ML
modelo_A = np.array([0.82, 0.84, 0.83, 0.85, 0.81, 0.84])
modelo_B = np.array([0.78, 0.79, 0.80, 0.77, 0.79, 0.78])
modelo_C = np.array([0.86, 0.87, 0.88, 0.85, 0.87, 0.86])

# Teste ANOVA (f_oneway)
resultado_anova = stats.f_oneway(modelo_A, modelo_B, modelo_C)
print("Estatística F:", resultado_anova.statistic)
print("p-valor:", resultado_anova.pvalue)

# Se p < 0.05, calculamos o Eta Squared manualmente para ver o impacto
todos = np.concatenate([modelo_A, modelo_B, modelo_C])
media_geral = np.mean(todos)
ss_total = np.sum((todos - media_geral) ** 2)

ss_entre = (
    len(modelo_A) * (np.mean(modelo_A) - media_geral)**2 +
    len(modelo_B) * (np.mean(modelo_B) - media_geral)**2 +
    len(modelo_C) * (np.mean(modelo_C) - media_geral)**2
)

eta_squared = ss_entre / ss_total
print("Eta squared:", eta_squared) # Vai mostrar se o efeito foi pequeno, médio ou grande
```
## 🔗 Conexões
- [[07 - Introdução aos Testes de Hipóteses e Pressupostos]]

- [[11 - Qui-Quadrado e Associação de Categóricas]]