---
aliases: [Lógica de Programação, Scanner, I/O, Operações Matemáticas]
tags: [java, logica, scanner, variaveis]
area: Java / DDD
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

A **Lógica de Programação** é a ciência de resolver problemas passo a passo. No desenvolvimento inicial em Java, essa lógica é dividida em três pilares: **Entrada** (receber dados do usuário via classe `Scanner`), **Processamento** (cálculos e manipulação em variáveis) e **Saída** (exibir resultados via `System.out.print` ou `printf`).

## Conceitos Principais

- **As Três Etapas da Lógica:**
    - Entender o problema.
    - Escrever os passos (frequentemente usando fluxogramas com formas geométricas que indicam início, processo e decisão).
    - Transformar em código Java.
- **Entrada de Dados (`Scanner`):**
    - Precisamos importar a biblioteca com `import java.util.Scanner;`.
    - Instanciamos o leitor: `Scanner sc = new Scanner(System.in);`.
    - Lemos dados usando `.nextInt()`, `.nextDouble()`, etc., dependendo do tipo da variável.
- **Saída Formatada:**
    - Usamos `System.out.printf()` para mesclar texto e variáveis formatadas (ex: `%.2f` para forçar duas casas decimais num valor em Reais).

## Exemplos Práticos / Código
```java
import java.util.Scanner;

public class CalculadoraSimples {
   public static void main(String[] args) {
       // Instancia o leitor
       Scanner sc = new Scanner(System.in);
       double p1, p2, media;

       // ENTRADA
       System.out.print("Digite a nota P1: ");
       p1 = sc.nextDouble();
       System.out.print("Digite a nota P2: ");
       p2 = sc.nextDouble();

       // PROCESSAMENTO
       media = (p1 + p2) / 2;

       // SAÍDA
       System.out.printf("Sua média final foi: %.2f", media);

       sc.close(); // Boa prática: fechar o leitor
   }
}
```
## 🔗 Conexões

- [[01 - IntelliJ e Ambiente de Desenvolvimento]]
    
- [[03 - Estrutura de Decisão]]