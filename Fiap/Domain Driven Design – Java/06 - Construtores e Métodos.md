---
aliases: [Construtor Padrão, Construtor com Parâmetros, Métodos]
tags: [java, poo, metodos, construtores]
area: Java / DDD
status: Pendente
data: 2026-04-23
---
## Resumo (TL;DR)

Enquanto a Classe define a estrutura, os **Construtores** são as portas de entrada que montam o Objeto no exato momento da sua criação (instância). Eles podem ser o **Construtor Padrão** (vazio e implícito) ou o **Construtor Não Padrão** (recebendo parâmetros para já nascer populado). Além disso, classes possuem **Métodos**, que definem as ações que aquele objeto é capaz de realizar.

## Conceitos Principais

- **Construtor Padrão:**
    - É um método especial, com o exato mesmo nome da classe e sem retorno.
    - Se você não declarar nada, o Java cria um implícito vazio, cuja única função é apenas alocar a memória (`Pessoa p = new Pessoa()`).
- **Construtor Não Padrão (Customizado):**
    - Criado com uma assinatura de parâmetros para popular os atributos no ato da criação.
    - O comando `this` é fundamental aqui: `this.nome = nome;` garante que a classe saiba que você está alterando o atributo interno dela, e não a variável local recebida.
- **Métodos:**
    - São ações/funções. Podem não retornar valor (declarados como `void`, ex: `public void depositar(double valor)`) ou podem retornar dados (`public String nomePessoa()`).

## Exemplos Práticos / Código
```java
public class Pessoa {
    public int id;
    public String nome;
   
    // Construtor Padrão explícito
    public Pessoa() { }

    // Construtor Não Padrão (Já nasce populado)
    public Pessoa(int id, String nome) {
         this.id = id;
         this.nome = nome;
    }
    
    // Método de Ação
    public void gritar() {
        System.out.println(this.nome + " diz: Nyo ho!");
    }
}

public class Projeto {
    public static void main(String[] args) {
        // Usando o construtor Não Padrão
        Pessoa a = new Pessoa(1, "Johnny Joestar");
        a.gritar();
    }
}
```

## 🔗 Conexões

- [[05 - Classe e Atributo]]
    
- [[07 - Encapsulamento]]