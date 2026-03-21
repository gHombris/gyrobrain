---
aliases: [Variância, Desvio-Padrão, Dispersão]
tags: [estatistica, analise-de-dados, variabilidade]
area: Estatística
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

Medidas de variabilidade explicam o quão "espalhados" os dados estão em relação ao centro. A **Variância** ($s^2$) calcula esse afastamento ao quadrado (para lidar com números negativos), enquanto o **Desvio-Padrão** ($s$) aplica a raiz quadrada para devolver a métrica à sua unidade de medida original e facilitar a interpretação.

## Conceitos Principais

- **Variância Amostral ($s^2$):**
    
    - Mede o "espalhamento" ou a dispersão dos dados em torno da média matemática.
        
    - Calcula o quadrado dos desvios para garantir que os números negativos não cancelem os positivos.
        
    - Utiliza a divisão por $(n-1)$ em vez de $n$ para corrigir possíveis subestimativas quando lidamos com uma amostra.
        
- **Desvio-Padrão ($s$):**
    
    - É matematicamente a raiz quadrada da variância.
        
    - Tem a grande vantagem de trazer a medida de volta para a unidade original dos dados (exemplo: converte de milissegundos quadrados de volta para milissegundos).
        
    - **Leitura prática:** Um desvio-padrão baixo significa que um sistema (como uma API) é estável e previsível. Um desvio-padrão alto significa instabilidade e imprevisibilidade, mesmo que a média central pareça boa.
        
## Exemplos Práticos / Código
```python
import statistics

api_estavel = [10, 11, 10, 12, 11]
api_instavel = [2, 20, 5, 18, 9]

# Ambas podem ter médias parecidas, mas a variabilidade conta a história real:
desvio_estavel = statistics.stdev(api_estavel)
desvio_instavel = statistics.stdev(api_instavel)

print(f"Desvio Padrão (Estável): {desvio_estavel:.2f}")   # ~0.84 ms (Altamente previsível)
print(f"Desvio Padrão (Instável): {desvio_instavel:.2f}") # ~7.76 ms (Totalmente imprevisível)
```
## 🔗 Conexões

- [[01 - Tendência Central - Média, Mediana e Moda]]
    
- [[04 - Probabilidade e Distribuição]]