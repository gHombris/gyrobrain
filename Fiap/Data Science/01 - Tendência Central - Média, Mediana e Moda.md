---
aliases: [Média, Mediana, Moda, Estatística Básica]
tags: [estatistica, analise-de-dados, medidas-centrais]
area: Estatística
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

As medidas de **Tendência Central** servem para resumir um conjunto de dados em um único valor representativo. A **Média** é a mais comum, porém falha perante anomalias, enquanto a **Mediana** revela o verdadeiro centro de dados distorcidos, e a **Moda** aponta as repetições mais frequentes.

## Conceitos Principais

- **Média:**
    
    - É calculada através da soma de todos os valores dividida pela quantidade total de itens.
        
    - É extremamente sensível a **outliers** (valores muito fora do padrão normal).
        
- **Mediana:**
    
    - Representa o valor que fica exatamente no centro quando ordenamos os dados sequencialmente.
        
    - É a melhor métrica a ser usada se os seus dados possuem caudas longas ou outliers graves.
        
- **Moda:**
    
    - É simplesmente o valor que mais se repete dentro do conjunto.
        
    - É uma medida muito útil para analisar variáveis e dados categóricos.
        

## Exemplos Práticos / Código

Se uma API responde a 99 requisições em 10ms, e sofre um engasgo de 1 requisição em 5000ms:

- A **média** vai ser puxada para cima por causa dos 5000ms, mentindo sobre a experiência real da maioria dos usuários.
    
- A **mediana** ignorará esse pico isolado e contará a verdade: o usuário típico experimenta ~10ms de latência.
```python
import statistics

# Simulando tempos de resposta de uma API (em milissegundos)
# Note que o último valor (5000) é um outlier gravíssimo.
tempos_ms = [10, 11, 10, 12, 9, 10, 5000] 

media = statistics.mean(tempos_ms)
mediana = statistics.median(tempos_ms)
moda = statistics.mode(tempos_ms)

print(f"Média: {media:.2f} ms") # Resultado ruim: ~723.14 ms (Distorcida pelo outlier)
print(f"Mediana: {mediana} ms") # Resultado real: 10 ms (Ignora o outlier e mostra a verdade)
print(f"Moda: {moda} ms")       # Valor que mais repetiu: 10 ms
```

## 🔗 Conexões

- [[02 - Variabilidade - Variância e Desvio-Padrão]]
    
- [[03 - Análise Exploratória de Dados (EDA)]]