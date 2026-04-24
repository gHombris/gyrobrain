---
aliases: [Intervalo de Confiança, Distribuição Normal, Binomial, Exponencial]
tags: [estatistica, probabilidade, distribuicao, python]
area: Estatística
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

A inferência estatística exige que saibamos medir a incerteza das nossas previsões, motivo pelo qual abandonamos as estimativas pontuais em favor dos **Intervalos de Confiança**, que fornecem uma faixa de valores plausíveis baseada num grau de certeza (ex: 95%). Adicionalmente, modelamos a probabilidade dos eventos usando distribuições específicas: a **Normal** (para dados numéricos contínuos), a **Binomial** (para contagem de sucessos/falhas) e a **Exponencial** (para calcular tempos de espera).

## Conceitos Principais

- **Intervalo de Confiança (IC):**
    
    - Substitui o "chute" de um valor único por uma faixa de valores onde o parâmetro real da população provavelmente se encontra.
        
    - O cálculo utiliza o valor crítico $z$ (caso o desvio padrão da população seja conhecido) ou $t$ de Student (desvio desconhecido) multiplicado pelo erro padrão ($\frac{s}{\sqrt{n}}$).
        
- **Distribuição Normal (Gaussiana):**
    
    - É contínua, perfeitamente simétrica e apresenta forma de sino centrada na média.
        
    - **Regra 68-95-99,7:** 68% dos valores caem em 1 desvio padrão de distância da média, 95% em 2 desvios, e 99,7% em 3 desvios.
        
    - O **Z-score** ($z=\frac{x-\mu}{\sigma}$) mede exatamente a quantos desvios padrão um determinado valor está afastado do centro.
        
- **Distribuição Binomial:**
    
    - Modela variáveis discretas focando no número de sucessos alcançados num número fixo de tentativas independentes (ex: clicar / não clicar num e-mail).
        
- **Distribuição Exponencial:**
    
    - Modela eventos contínuos no tempo com foco no tempo de espera até a próxima ocorrência (ex: tempo até uma falha de sistema), sendo orientada por uma taxa média $\lambda$.
        

## Exemplos Práticos / Código
```python
import numpy as np
from scipy import stats
from scipy.stats import norm, binom, expon

# 1. Margem de Erro para um Intervalo de Confiança (t de Student)
# Amostra = 100, Desvio Padrão = 10, Confiança exigida = 95%
n = 100
valor_critico = stats.t.ppf(0.975, df=n-1) 
margem_erro = valor_critico * 10 / np.sqrt(n)
print(f"A margem de erro para o IC é de ± {margem_erro:.2f}")

# 2. Distribuição Normal: Qual a chance de um score de crédito ser > 780?
# Assumindo uma Média de 700 e Desvio Padrão de 50
prob_normal = 1 - norm.cdf(780, loc=700, scale=50)

# 3. Distribuição Binomial: Exatamente 3 cliques em 10 tentativas (Taxa média: 20%)
prob_binomial = binom.pmf(k=3, n=10, p=0.2)

# 4. Distribuição Exponencial: Demorar mais de 1 minuto para receber requisição (Taxa média: 2/min)
prob_exponencial = 1 - expon.cdf(1, scale=1/2)
```

## 🔗 Conexões
- [[05 - Média Populacional e Amostral]]

- [[04 - Probabilidade e Distribuição]]