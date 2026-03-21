---
aliases: [Vetores, Arrays Dinâmicos, Arrays Estáticos]
tags: [estruturas-de-dados, arrays, memoria, python]
area: Estrutura de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

Os **Arrays** são estruturas de dados que armazenam informações de forma contígua na memória, permitindo um acesso extremamente rápido aos elementos através de um índice numérico. Podem ser estáticos (tamanho fixo na criação) ou dinâmicos (tamanho ajustável em tempo de execução).

## Conceitos Principais

- **Conceito Base:**
    
    - Armazenam vários dados de forma contígua na memória.
        
    - Permitem acesso direto utilizando índice numérico que começa no zero.
        
    - A posição na memória é calculada via uma fórmula simples, garantindo grande rapidez.
        
- **Array Estático:**
    
    - Possuem tamanho fixo definido logo no momento da criação.
        
    - São opções mais rápidas, mas menos flexíveis.
        
- **Array Dinâmico:**
    
    - Conseguem crescer de tamanho durante a execução, como as Listas em Python.
        
    - Quando enchem, ativam internamente uma realocação da memória, copiando ponteiros para um espaço físico maior.
        
- **Python (Módulo `array`):**
    
    - Ao contrário das listas habituais do Python (que aceitam dados heterogêneos), o módulo `array` guarda apenas tipos primitivos homogêneos.
        
    - Isso faz com que ocupem muito menos memória.
        
## Exemplos Práticos / Código
```python
import array

# 1. Array Dinâmico clássico do Python (Listas)
# Aceita dados heterogêneos, menos eficiente em memória
lista_dinamica = [1, "texto", 3.14, True]
lista_dinamica.append(99) # Cresce dinamicamente

# 2. Array Estrito e Otimizado (Módulo 'array' do Python)
# O código 'i' obriga que a estrutura seja homogênea (apenas Inteiros)
array_tipado = array.array('i', [10, 20, 30, 40])

# array_tipado.append("erro") --> Isso geraria um TypeError!
array_tipado.append(50) # Funciona perfeitamente
```
## 🔗 Conexões

- [[01 - Introdução e Busca]]
    
- [[04 - Pilhas]]