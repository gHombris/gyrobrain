---
aliases: [Notação Big O, Complexidade de Algoritmos]
tags: [algoritmos, big-o, performance]
area: Estrutura de Dados
status: Concluído
data: 2026-03-20
---

## Resumo (TL;DR)

A **Análise de Complexidade** avalia a eficiência de um algoritmo ignorando o hardware, focando no tempo ou memória consumidos em relação ao tamanho da entrada ($n$). A ferramenta principal para isso é a **Notação Big O ($O$)**, que descarta constantes para focar no pior cenário possível.

## Conceitos Principais

- **Casos de Análise:**
    
    - **Pior Caso:** É o cenário mais importante, pois garante o limite superior e o pior cenário possível de tempo de execução.
        
    - **Caso Médio:** Representa o desempenho do algoritmo numa entrada típica de dados.
        
    - **Melhor Caso:** Cenário de menor trabalho (como achar o elemento logo na primeira tentativa em uma busca).
        
- **Notação Big O ($O$):**
    
    - Regra de ouro: descartam-se sempre as constantes ou os fatores de ordem mais baixa.
        
    - $O(1)$ **(Constante):** Tempo fixo independente da entrada, como atribuições e instruções `if`.
        
    - $O(n)$ **(Linear):** O tempo cresce proporcionalmente à entrada, como em um laço simples.
        
    - $O(n^2)$ **(Quadrática):** Tempo cresce exponencialmente, típico de loops aninhados (dois laços encadeados).
        
    - $O(\log n)$ **(Logarítmica):** Alta eficiência, comum ao dividir um espaço de busca ao meio a cada iteração.
        

## 🔗 Conexões

- [[01 - Introdução e Busca]]