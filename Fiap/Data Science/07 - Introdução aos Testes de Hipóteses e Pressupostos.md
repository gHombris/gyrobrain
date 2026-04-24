---
aliases: [Testes Paramétricos, Testes Não Paramétricos, P-valor, Shapiro-Wilk, Mann-Whitney]
tags: [estatistica, data-science, testes-de-hipotese, python]
area: Estatística
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

O **Teste de Hipótese** avalia as evidências nos dados para decidir estatisticamente se a diferença entre dois grupos é real ou mero fruto do acaso, comparando a **Hipótese Nula ($H_0$)** com a **Hipótese Alternativa ($H_1$)** por meio do **p-valor**. Antes de aplicar os testes, devemos checar pressupostos (Normalidade e Homocedasticidade): se eles forem aprovados, usamos os clássicos **Testes Paramétricos** (como Teste t e ANOVA); se falharem (ex: presença de outliers severos), recorremos aos robustos **Testes Não Paramétricos** (como Mann-Whitney e Kruskal-Wallis).

## Conceitos Principais

- **Estrutura do Teste:**
    
    - **Hipótese Nula ($H_0$):** Premissa padrão de que não existe diferença ou efeito real entre os grupos.
        
    - **Hipótese Alternativa ($H_1$):** A premissa de que existe uma diferença, e é exatamente o que você deseja investigar e provar.
        
    - **Decisão (p-valor vs $\alpha$):** Se o p-valor for menor ou igual à significância $\alpha$ (geralmente 0,05), nós **rejeitamos $H_0$**. Se for maior, **não rejeitamos $H_0$** (o correto em estatística é nunca dizer "aceitar").
        
- **A Checagem de Pressupostos:**
    
    - **Normalidade:** O teste de **Shapiro-Wilk** avalia se os dados seguem a curva de sino (Se $p \le 0,05$, os dados *não* são normais).
        
    - **Homocedasticidade:** O teste de **Levene** avalia se as variâncias dos grupos são semelhantes (se $p \le 0,05$, elas são diferentes, ou seja, heterocedásticas).
        
- **Escolha da "Ferramenta":**
    
    - **Paramétricos:** Exigem normalidade, variâncias iguais e independência. Exemplos: Teste t Independente (2 grupos), Teste t Pareado (antes/depois) e ANOVA (3+ grupos).
        
    - **Não Paramétricos:** Entram em cena quando há assimetria forte ou distorção por *outliers*. Trabalham usando *ranks* (postos) ao invés dos números brutos. Exemplos: Mann-Whitney (substitui t Independente) e Kruskal-Wallis (substitui ANOVA).
        

## Exemplos Práticos / Código
```python
import scipy.stats as stats

# Cenário Prático: Tempo de Resposta de Duas APIs Diferentes
api_antiga = [120, 130, 125, 140, 128, 500] # Repare no '500'. É um Outlier brutal!
api_nova = [118, 122, 121, 124, 119, 123]

# 1. Validando Pressupostos (O Teste de Shapiro-Wilk)
_, p_shapiro = stats.shapiro(api_antiga)
print(f"P-valor Shapiro: {p_shapiro}") 
# Como existe um 500, o p-valor será < 0.05, indicando FALHA na Normalidade.

# 2. Tomada de Decisão do Algoritmo
# Se os dados fossem perfeitos e normais, usaríamos Paramétrico: stats.ttest_ind()
# Como a normalidade quebrou, usamos o Não Paramétrico, muito mais robusto a outliers:
teste_mann_whitney = stats.mannwhitneyu(api_antiga, api_nova, alternative='two-sided')
print("P-valor (Mann-Whitney):", teste_mann_whitney.pvalue)

# Se o p-valor final for < 0.05, rejeitamos H0 e concluímos que a API Nova é estatisticamente diferente!
```
## 🔗 Conexões
- [[03 - Análise Exploratória de Dados (EDA)]]

- [[02 - Variabilidade - Variância e Desvio-Padrão]]