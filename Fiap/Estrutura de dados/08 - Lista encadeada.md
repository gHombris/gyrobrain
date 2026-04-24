---
aliases: [Linked List, Lista Encadeada, Nós, Ponteiros]
tags: [estruturas-de-dados, listas, ponteiros, python]
area: Estrutura de Dados
status: Concluído
data: {{date}}
---

# 08 - Listas Ligadas (Encadeadas)

## Resumo (TL;DR)
Diferente dos arrays (matrizes), as **Listas Ligadas** não armazenam elementos de forma contígua na memória. Elas consistem em uma sequência de **Nós**, onde cada nó contém o dado e um **Ponteiro (Referência)** para o próximo elemento. É uma estrutura dinâmica, o que facilita a inserção e remoção de itens sem a necessidade de realocar toda a estrutura, embora o acesso aleatório seja mais lento ($O(n)$).

## Conceitos Principais
- **Nó (Node):** A unidade básica que contém o dado e a referência (`next`).
- **Ponteiro/Referência:** Variável que armazena o endereço de memória do próximo nó.
- **Head (Cabeça):** O primeiro nó da lista. Se a `head` for `None`, a lista está vazia.
- **Vantagens:**
    - Tamanho dinâmico (cresce conforme a necessidade).
    - Inserção e remoção eficientes no início da lista.
- **Desvantagens:**
    - Gasto extra de memória para armazenar os ponteiros.
    - Acesso sequencial: para chegar ao elemento $n$, deve-se percorrer todos os anteriores.



## Exemplos Práticos / Código

**Implementação Básica de Nó e Lista em Python:**
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None # Ponteiro para o próximo

class LinkedList:
    def __init__(self):
        self.head = None

    def inserir_no_inicio(self, data):
        novo_no = Node(data)
        novo_no.next = self.head
        self.head = novo_no
```

# Referências
* FIAP. Aula 6 - Lista Ligada(1).pdf. Roberto Cândido, 2026.

## 🔗 Conexões
- [[04 - Funções Recursivas]]

- [[06 - Filas]]

- [[Alocação Dinâmica de Memória]]