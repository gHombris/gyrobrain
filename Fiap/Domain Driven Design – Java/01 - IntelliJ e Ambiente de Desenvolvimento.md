---
aliases: [Introdução ao Java, IntelliJ, Ambiente de Desenvolvimento]
tags: [java, ide, intellij, setup]
area: Java / DDD
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

O **Java** é uma linguagem de programação criada pela Sun Microsystems em 1995, amplamente utilizada em sistemas robustos como serviços bancários e aplicativos da Receita Federal. Para desenvolvermos de forma eficiente, utilizamos uma **IDE** (Integrated Development Environment), como o **IntelliJ IDEA** ou Eclipse, que compila e executa nossos códigos. Todo programa Java precisa de uma classe inicial e de um método executor chamado `main`.

## Conceitos Principais

- **Linguagem Java:**
    - Criada em 1995, tem foco em portabilidade e segurança, sendo muito comum no backend corporativo.
- **IDE (IntelliJ):**
    - É o programa onde codificamos. Facilita a criação do projeto e o gerenciamento de arquivos na pasta `src`.
- **Estrutura Básica:**
    - Todo arquivo de código é uma `Class` (ex: `public class Programa`).
    - O ponto de partida de qualquer execução é o método `main`. No IntelliJ, você pode usar o atalho `psvm` (`public static void main(String[] args)`) e apertar *Tab* para gerá-lo automaticamente.

## Exemplos Práticos / Código
```java
public class Programa {
    // Ponto de entrada do sistema
    public static void main(String[] args) {
        System.out.println("Nyo ho! Bem-vindo ao Java!");
    }
}
```

## 🔗 Conexões

- [[02 - Entrada, Processamento e Saída]]
    
- [[Arquitetura Java]]