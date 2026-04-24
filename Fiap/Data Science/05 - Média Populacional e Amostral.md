---
aliases: [População, Amostra, Média Amostral, Média Populacional]
tags: [estatistica, data-science, python, inferencia]
area: Estatística
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

Na vida real, quase nunca temos acesso a todos os dados, o que nos obriga a extrair uma **amostra** para tentar compreender o comportamento de uma **população** inteira. A **Média Populacional** ($\mu$) é um valor exato e fixo que descreve o todo, enquanto a **Média Amostral** ($\overline{x}$) é apenas uma estimativa que contém incerteza, pois o seu valor varia a cada nova amostra coletada.

## Conceitos Principais

- **População:**
    
    - É o conjunto completo e absoluto de elementos de interesse em um estudo (ex: todos os clientes de uma empresa, todas as vendas do ano).
        
    - A **Média Populacional** utiliza absolutamente todos os dados, representando assim a verdade exata do cenário observado.
        
- **Amostra:**
    
    - É um subconjunto ou recorte da população, escolhida para representá-la quando a população é grande demais ou quando há severas limitações de custo e tempo.
        
    - A **Média Amostral** atua como uma aproximação e tenta estimar o verdadeiro valor populacional.
        
- **A Regra da Incerteza:**
    
    - Amostras diferentes de uma mesma população sempre vão gerar resultados diferentes entre si.
        
    - Amostras pequenas sofrem grandes oscilações, enquanto amostras maiores tendem a ser mais estáveis, produzindo estimativas muito mais próximas da média populacional real.
        

## Exemplos Práticos / Código
```python
import numpy as np

# 1. Definindo a População (O "Todo")
populacao = np.array([2000, 2200, 2500, 2700, 3000, 3200, 3500, 4000, 4200, 5000])

# Calculando a Média Populacional (Valor Exato e Fixo)
media_populacional = np.mean(populacao)
print(f"Média populacional exata: {media_populacional}") 

# 2. Extraindo uma Amostra Aleatória (tamanho 4)
amostra = np.random.choice(populacao, size=4, replace=False)

# Calculando a Média Amostral (Uma Estimativa)
media_amostral = np.mean(amostra)
print(f"Média amostral (Estimativa): {media_amostral}") # Este valor mudará a cada execução do código!
```
## 🔗 Conexões
- [[01 - Tendência Central - Média, Mediana e Moda]]

- [[06 - Intervalo de Confiança e Distribuições]]