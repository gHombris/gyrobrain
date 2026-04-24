---
aliases: [Encapsulamento, Modificadores de Acesso, Getters, Setters]
tags: [java, poo, encapsulamento, seguranca]
area: Java / DDD
status: Pendente
data: 2026-04-23
---

## Resumo (TL;DR)

O **Encapsulamento** é o mecanismo da POO que blinda e protege o estado interno de um objeto. Em vez de deixar variáveis abertas e desprotegidas, utilizamos **Modificadores de Acesso** como o `private` para esconder os atributos, e criamos métodos controlados (`public` **Getters e Setters**) para permitir que outras partes do sistema leiam ou alterem esses dados de forma segura.

## Conceitos Principais

- **Modificadores de Acesso:**
    - Define a visibilidade de classes, métodos e atributos.
    - **`public`:** Pode ser acessado de qualquer lugar do projeto.
    - **`private`:** Oculto. Só pode ser acessado, lido ou alterado por código que esteja *dentro da própria classe*.
    - **`protected`:** Acessível no mesmo pacote ou por classes filhas (herança).
    - **`default`:** Acessível apenas dentro do mesmo pacote.
- **Getters e Setters:**
    - Como os atributos agora são `private`, precisamos criar portas oficiais de acesso.
    - `get`: Método que retorna (lê) o valor do atributo (ex: `getNome()`).
    - `set`: Método que recebe e altera o valor do atributo, podendo possuir lógica de validação dentro dele (ex: `setNome(String nome)`).

## Exemplos Práticos / Código
```java
public class Cliente {
   // 1. Dados Protegidos
   private int id;
   private String nome;
   private double saldo;

   // 2. Método Getter (Lê a informação)
   public double getSaldo() {
       return this.saldo;
   }

   // 3. Método Setter com validação (Grava a informação controlada)
   public void setNome(String nome) {
       this.nome = nome;
   }
   
   // Métodos normais de negócio (o saldo é alterado por aqui, e não por Setter)
   public void depositar(double valor){
       this.saldo = this.saldo + valor;
   }
}

// Em outra classe:
// c3.saldo = 1000; // ISSO DÁ ERRO! É private.
// c3.depositar(1000); // ISSO FUNCIONA! É a regra controlada.
```

## 🔗 Conexões

- [[05 - Classe e Atributo]]
    
- [[Domain Driven Design (DDD) - Entidades e Value Objects]]