---
aliases: [Loops, Laços de Repetição, While, Do-While, For]
tags: [java, loops, while, logica]
area: Java / DDD
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

As **Estruturas de Repetição** permitem que um bloco de código seja executado múltiplas vezes sem que tenhamos que escrevê-lo repetidamente. No Java, as principais ferramentas para iterar são o **While** (testa no início), o **Do..While** (garante execução de pelo menos uma vez) e o **For** (ideal para repetições contadas com início e fim explícitos).

## Conceitos Principais

- **While (Enquanto):**
    - Avalia a condição *antes* de executar o bloco.
    - Se a condição já começar falsa, o bloco interno nunca será executado.
    - Útil para validações de erro (ex: pedir para o usuário digitar de novo se colocar número negativo).
- **Do..While:**
    - Avalia a condição apenas no *final* do bloco.
    - Garante que a rotina rode pelo menos uma vez.
- **Lógica de Iteração:**
    - Sempre lembre de incrementar a variável de controle (ex: `i++`) dentro de loops `while` para evitar os temidos *loops infinitos*.

## Exemplos Práticos / Código
```java
import java.util.Scanner;

public class TabuadaWhile {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        int num, t, i;
       
        System.out.print("Digite um número positivo: ");
        num = ler.nextInt();
       
        // Validação usando o While para bloquear números errados
        while(num <= 0) {
            System.out.print("Erro! Digite um número positivo: ");
            num = ler.nextInt();
        }
       
        // Iteração usando While para montar a tabuada
        i = 1;
        while (i <= 10) {
            t = num * i;
            System.out.printf("%d X %d = %d\n", num, i, t);
            i++; // Incremento crucial
        }
        
        ler.close();
    }
}
```

## 🔗 Conexões

- [[03 - Estrutura de Decisão]]
    
- [[05 - Classe e Atributo]]