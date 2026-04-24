---
aliases: [POO, Classes, Atributos, Objetos, Instância]
tags: [java, poo, objetos, design-pattern]
area: Java / DDD
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

A Programação Orientada a Objetos baseia-se em mapear elementos do mundo real para o código. Uma **Classe** atua como uma estrutura teórica ou "receita" de algo, possuindo **Atributos** (características) e Métodos (ações). Quando alocamos essa classe na memória e damos vida a ela, criamos um **Objeto** (ou Instância).

## Conceitos Principais

- **Classe:**
    - É o molde. Exemplo: A receita de um bolo.
    - Usa o modificador `public` para ser visível no projeto (ex: `public class Pessoa`).
- **Atributos:**
    - São as propriedades/variáveis declaradas dentro da classe.
    - Quando o objeto for criado, os atributos viram os "campos" reais dele.
- **Objeto (Instância):**
    - É a criação física da classe na memória do computador.
    - Instanciamos usando a palavra reservada `new` (ex: `Pessoa p = new Pessoa();`).

## Exemplos Práticos / Código
```java
// O Molde (Classe e Atributos)
public class Pessoa {
    public int id;
    public String nome;
}

// O Uso (Objeto)
public class Programa {
    public static void main(String[] args) {
        // Criando uma Instância (Objeto p)
        Pessoa p = new Pessoa();
        
        // Populando os atributos do objeto criado
        p.id = 1;
        p.nome = "Gyro Zeppeli";
        
        System.out.println("ID: " + p.id + " | Nome: " + p.nome);
    }
}
```

## 🔗 Conexões

- [[06 - Construtores e Métodos]]
    
- [[Fundamentos do Domain Driven Design]]