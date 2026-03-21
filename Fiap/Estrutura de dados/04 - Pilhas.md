---
aliases: [Stack, LIFO]
tags: [estruturas-de-dados, pilhas, lifo]
area: Estrutura de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

A **Pilha** (Stack) é uma estrutura linear de dados que segue rigorosamente o princípio **LIFO** (Last In, First Out). É a estrutura ideal para rastrear o estado anterior de sistemas, sendo amplamente usada em históricos, funções de desfazer (Undo) e pilhas de chamadas de execução (call stack).

## Conceitos Principais

- **Conceito Base:**
    
    - Estrutura linear orientada pelo princípio **LIFO**.
        
    - O último elemento que for inserido será o primeiro a ser removido.
        
- **Operações Básicas:** (Todas possuem complexidade de $O(1)$)
    
    - `push`: Adiciona um elemento no topo da pilha.
        
    - `pop`: Remove o elemento localizado no topo.
        
    - `peek` / `top`: Consulta o valor do topo sem efetuar a remoção.
        
    - `is_empty`: Retorna se a pilha está vazia.
        
- **Casos de Uso Práticos:**
    
    - Controle de recursão em linguagens de programação (call stack).
        
    - Histórico de navegação em browsers.
        
    - Funcionalidades de Undo/Redo (Desfazer/Refazer).
        

## Exemplos Práticos / Código
```python
# Implementando uma Pilha (LIFO) usando listas nativas do Python
call_stack = []

# Operação Push - O(1)
call_stack.append("Função A")
call_stack.append("Função B")
call_stack.append("Função C")

# Operação Peek / Top - O(1)
topo = call_stack[-1]
print(f"No topo está: {topo}") # Saída: Função C

# Operação Pop - O(1)
removido = call_stack.pop()
print(f"Removido: {removido}") # Saída: Função C (O último a entrar foi o primeiro a sair)
```
## 🔗 Conexões

- [[03 - Arrays]]
    
- [[02 - Análise de Complexidade]]