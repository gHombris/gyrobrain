---
aliases: [Probabilidade, Distribuição Normal, Gaussiana, Variáveis Aleatórias]
tags: [estatistica, probabilidade, distribuicao, matematica]
area: Estatística
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

A **Probabilidade** é a fundação matemática usada para medir incertezas, sustentar previsões e realizar análises de risco usando amostras de dados. Ela modela eventos através de variáveis aleatórias que seguem padrões conhecidos, chamados de **Distribuições** (como a Bernoulli, Binomial e a famosa Normal/Gaussiana), permitindo prever o comportamento de sistemas e populações.

## Conceitos Principais

- **Conceitos Básicos:**
    
    - **Espaço Amostral ($S$):** O conjunto de todos os resultados possíveis de um experimento.
        
    - **Evento ($A$):** Qualquer subconjunto do espaço amostral $S$.
        
    - **Probabilidade ($P$):** Sempre é um valor que fica entre 0 e 1.
        
    - A probabilidade complementar de um evento é calculada por $1 - P(A)$.
        
    - Eventos classificados como independentes não afetam a chance um do outro ocorrerem.
        
- **Variáveis Aleatórias:**
    
    - **Discreta:** Lida com valores contáveis e finitos (ex: nº de cliques em um botão).
        
    - **Contínua:** Lida com valores dentro de um intervalo infinito (ex: peso de uma pessoa, tempo de carregamento).
        
- **Principais Distribuições:**
    
    - **Bernoulli:** Usada estritamente para experimentos com apenas dois resultados possíveis (ex: o usuário converteu / não converteu).
        
    - **Binomial:** Usada para contar o número de sucessos em várias tentativas independentes entre si.
        
    - **Normal (Gaussiana):** A famosa curva em sino, perfeitamente simétrica. É vastamente usada para modelar tempo, peso e erros.
        
    - **Regra Empírica da Normal:** Dita que aproximadamente 68% dos dados estão a 1 desvio-padrão ($\sigma$) da média, ~95% estão a $2\sigma$ e ~99.7% estão a $3\sigma$.
        

## Exemplos Práticos / Código
```python
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

# Gerando 10.000 dados aleatórios que seguem uma Distribuição Normal (Curva de Sino)
# loc = Média (0), scale = Desvio Padrão (1)
dados_normais = np.random.normal(loc=0, scale=1, size=10000)

# Plotando a distribuição para visualizar a simetria Gaussiana
sns.histplot(dados_normais, kde=True, color="purple")
plt.title("Distribuição Normal (Gaussiana)")
plt.xlabel("Desvios da Média")
plt.show()
```
## 🔗 Conexões

- [[02 - Variabilidade - Variância e Desvio-Padrão]]
    
- [[01 - Tendência Central - Média, Mediana e Moda]]