---
aliases: [Estrutura Condicional, If Else, Decisão]
tags: [java, if-else, condicional, logica]
area: Java / DDD
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

Além do fluxo contínuo de entrada, processamento e saída, os programas precisam tomar rumos diferentes baseados em condições lógicas. Em Java, a principal estrutura de decisão é o bloco **If..Else**, que avalia uma expressão booleana e executa um trecho de código específico caso seja verdadeira (`if`), ou outro trecho caso seja falsa (`else`).

## Conceitos Principais

- **O Bloco `if..else`:**
    - Traduz um losango de decisão de um fluxograma para o código.
    - É acionado baseado em testes lógicos relacionais (ex: `>=`, `<=`, `==`, `!=`).
    - *Ação:* Se o teste for verdadeiro, o programa entra no escopo do `if`. Se for falso, ele desvia para o `else`.

## Exemplos Práticos / Código
```java
import java.util.Scanner;

public class ValidacaoAprovacao {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        double media;
       
        System.out.print("Digite a sua média: ");
        media = ler.nextDouble();
       
        // Estrutura de Decisão
        if (media >= 5.0) {
            System.out.printf("A sua média foi %.1f. Portanto você está APROVADO!", media);
        } else {
            System.out.printf("A sua média foi %.1f. Portanto você está REPROVADO!", media);
        }
        
        ler.close();
    }
}
```
## 🔗 Conexões

- [[02 - Entrada, Processamento e Saída]]
    
- [[04 - Estruturas de Repetição]]