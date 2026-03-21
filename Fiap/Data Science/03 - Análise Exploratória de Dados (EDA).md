---
aliases: [EDA, Histograma, Boxplot, Correlação de Pearson, Outliers]
tags: [analise-de-dados, eda, graficos, estatistica]
area: Análise de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

A **Análise Exploratória de Dados (EDA)** é a fase investigativa onde utilizamos gráficos e estatísticas para entender o comportamento de um dataset. Ferramentas visuais como **Histogramas** revelam o formato da distribuição, **Boxplots** isolam anomalias (outliers) e análises de **Correlação** identificam relações lineares entre variáveis distintas.

## Conceitos Principais

- **Histograma:**
    
    - Gráfico que agrupa números em faixas (bins) para que possamos ver o formato real da distribuição dos dados.
        
    - Pode apresentar formatos simétricos, assimétricos (com uma cauda longa) ou bimodais.
        
    - Uma distribuição bimodal (dois "picos") é um forte indicativo de que você provavelmente misturou dois perfis muito diferentes de usuários ou entidades no mesmo gráfico.
        
- **Boxplot e Outliers:**
    
    - É um gráfico excelente para encontrar anomalias baseadas puramente no Método IQR (Intervalo Interquartil).
        
    - O IQR representa o "miolo" dos dados, estendendo-se do quartil 1 ao quartil 3 (ou seja, os 50% centrais da distribuição).
        
    - Valores que caem muito acima ou muito abaixo dessa caixa central são marcados visualmente como outliers (os pontos soltos no gráfico).
        
- **Correlação (Pearson):**
    
    - Mede a força e a direção da relação linear entre duas coisas.
        
    - A escala vai de -1 (variáveis inversamente proporcionais) a +1 (variáveis diretamente proporcionais).
        
    - **Regra de Ouro:** Correlação **não prova causa**.
        
    - Visualizamos correlações frequentemente usando _Scatterplots_ (gráficos de dispersão clássicos) ou _Heatmaps_ (mapas de calor).
        
## Exemplos Práticos / Código
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Criando um DataFrame com um claro Outlier na idade
dados = pd.DataFrame({'idade': [22, 25, 24, 23, 22, 26, 85]}) # 85 foge do padrão

# Gerando um Boxplot para encontrar anomalias via método IQR
sns.boxplot(x=dados['idade'])
plt.title("Boxplot revelando o Outlier (Ponto fora da caixa)")
plt.show()

# Para calcular a Correlação de Pearson num dataset real:
# matriz_correlacao = dados.corr(method='pearson')
```
## Conexões

- [[01 - Tendência Central - Média, Mediana e Moda]]
    
- [[02 - Variabilidade - Variância e Desvio-Padrão]]