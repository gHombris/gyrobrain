---
aliases: [Busca Linear, Busca Binária, Estruturas de Dados]
tags: [algoritmos, busca, estruturas-de-dados]
area: Estrutura de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

As estruturas de dados dividem-se inicialmente em contíguas (como arrays) e ligadas/encadeadas (como árvores e grafos usando ponteiros). Para encontrar informações nessas estruturas, utilizamos algoritmos como a **Busca Linear**, que é exaustiva, ou a **Busca Binária**, que é altamente otimizada, mas exige ordenação prévia.

## Conceitos Principais

- **Classificação das Estruturas:**
    
    - **Contíguas:** Matrizes e arrays.
        
    - **Ligadas/Encadeadas:** Utilizam ponteiros, como listas ligadas, grafos e árvores.
        
- **Busca Linear:**
    
    - Percorre os itens de um vetor não ordenado um por um.
        
    - Possui complexidade de tempo de $O(n)$.
        
- **Busca Binária:**
    
    - Requer obrigatoriamente que a lista esteja **ordenada**.
        
    - Compara o valor buscado com o meio da lista, reduzindo o espaço de busca pela metade a cada passo.
        
    - Tem complexidade extremamente eficiente de $O(\log n)$ (exemplo: buscar entre 240 mil itens gera apenas 18 tentativas, comparado a 240 mil da busca linear).
        
## Exemplos Práticos / Código
```python
# Busca Linear: O(n) - Percorre tudo exaustivamente
def busca_linear(lista, alvo):
    for i in range(len(lista)):
        if lista[i] == alvo:
            return i # Retorna o índice onde achou
    return -1 # Não encontrou

# Busca Binária: O(log n) - A lista PRECISA estar ordenada
def busca_binaria(lista, alvo):
    inicio, fim = 0, len(lista) - 1
    
    while inicio <= fim:
        meio = (inicio + fim) // 2
        
        if lista[meio] == alvo:
            return meio
        elif lista[meio] < alvo:
            inicio = meio + 1 # Ignora a metade esquerda
        else:
            fim = meio - 1    # Ignora a metade direita
            
    return -1
```
## 🔗 Conexões

- [[02 - Análise de Complexidade]]
    
- [[03 - Arrays]]