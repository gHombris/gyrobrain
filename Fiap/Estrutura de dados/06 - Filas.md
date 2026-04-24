---
aliases: [Queue, FIFO, Enfileiramento]
tags: [estruturas-de-dados, filas, fifo, algoritmos]
area: Estrutura de Dados
status: Concluído
data: {{date}}
---

# 06 - Filas

## Resumo (TL;DR)
Uma **Fila** é uma estrutura de dados que segue o protocolo **FIFO (First-In, First-Out)**: o primeiro elemento a entrar é obrigatoriamente o primeiro a sair. É amplamente utilizada em sistemas computacionais para gerenciar tarefas que aguardam processamento, como buffers de impressão ou filas de mensagens em aplicações distribuídas.

## Conceitos Principais
- **Operações Fundamentais:**
    - **Enqueue (Inserir):** Adiciona um elemento ao final (*Rear/Tail*) da fila.
    - **Dequeue (Remover):** Remove o elemento do início (*Front/Head*) da fila.
- **Aplicações:** Escalonamento de processos no SO, processamento de pedidos em segundo plano (workers), e buffers de transmissão de dados.
- **Implementação:** Pode ser feita usando listas comuns (com custo $O(n)$ para remoção no início) ou a biblioteca `collections.deque` em Python para máxima performance ($O(1)$).



## Exemplos Práticos / Código

**Uso de Fila com a biblioteca padrão do Python:**
```python
from queue import Queue

fila = Queue()

# Adicionando itens (Enqueue)
fila.put("Pedido 01")
fila.put("Pedido 02")

# Removendo itens (Dequeue)
if not fila.empty():
    processado = fila.get()
    print(f"Processando: {processado}") # Saída: Pedido 01
```

# Referências
* FIAP. Aula_05_-_Filas.pdf. Roberto Cândido, 2026.

## 🔗 Conexões
- [[05 - Listas Ligadas]]

- [[Sistemas Operacionais]]

- [[Multithreading]]