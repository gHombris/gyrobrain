---
aliases: [Recursividade, Empilhamento, Caso Base, Stack Frame]
tags: [algoritmos, recursao, estrutura-de-dados, python]
area: Estrutura de Dados
status: Concluído
data: {{date}}
---

# 09 - Funções Recursivas

## Resumo (TL;DR)
A **recursividade** é uma técnica onde uma função chama a si mesma para resolver instâncias menores do mesmo problema. Ela depende fundamentalmente da **Pilha de Execução (Stack)** do sistema para gerenciar as chamadas e o retorno de valores. Para evitar loops infinitos (estouro de pilha), toda função recursiva deve possuir um **Caso Base** (condição de parada) e um **Caso Recursivo** que aproxima o problema da solução final.

## Conceitos Principais
- **Pilha de Execução (Stack):** Estrutura do tipo **LIFO** (Last-In, First-Out). Cada chamada de função cria um *Stack Frame* que armazena parâmetros, variáveis locais e o endereço de retorno.
- **Caso Base:** A condição que interrompe a recursão. Sem ele, ocorre o erro de *Stack Overflow*.
- **Caso Recursivo:** A parte da função que invoca a si mesma, geralmente com um argumento reduzido.
- **Recursão vs. Iteração:** Enquanto a iteração usa loops (`for`, `while`), a recursão usa a pilha de chamadas. A recursão é muitas vezes mais elegante para problemas como o cálculo de Fibonacci ou travessia de árvores, mas pode consumir mais memória.



## Exemplos Práticos / Código

**Cálculo de Fatorial em Python:**
```python
def fatorial(n):
    # Caso Base
    if n == 0 or n == 1:
        return 1
    # Caso Recursivo
    else:
        return n * fatorial(n - 1)

print(fatorial(5)) # Saída: 120
```
---

A recursividade pode ser confusa porque "esconde" o estado na pilha. O simulador abaixo permite-te ver o crescimento e a redução da pilha em tempo real.

```json?chameleon
{"component":"LlmGeneratedComponent","props":{"height":"700px","prompt":"Cria um visualizador interativo de Pilha de Execução para Funções Recursivas. \n\nObjetivo: Mostrar como os 'Stack Frames' são empilhados (Push) e desempilhados (Pop) durante uma chamada recursiva.\n\nFuncionalidades:\n1. O usuário pode escolher entre dois algoritmos: Fatorial (n!) ou Fibonacci (n-ésimo termo).\n2. Um controle deslizante para definir o valor de 'n' (limite de 1 a 6 para evitar excesso visual).\n3. Botões 'Passo a Passo' para avançar ou retroceder na execução.\n4. Uma área visual representando a 'Call Stack' (Pilha de Chamadas), onde cada frame novo é adicionado no topo com seus parâmetros locais (ex: n=5).\n5. Destaque visual quando um 'Caso Base' é atingido.\n6. Exibição do valor de retorno sendo 'passado' de volta para o frame anterior quando um item é desempilhado.\n\nLayout: Centralizado, com a representação vertical da pilha e uma área de texto ao lado explicando o que está acontecendo no passo atual. Use labels em Português.","id":"im_ff65c248fc11dc55"}}
```
# Referências
* FIAP. Aula 7 - Funções Recursivas.pdf. Roberto Cândido, 2026.

## 🔗 Conexões
- [[Estruturas de Dados Dinâmicas]]

- [[Busca Binária]] (implementação recursiva)

- [[Filas]]

- [[Listas Ligadas]]