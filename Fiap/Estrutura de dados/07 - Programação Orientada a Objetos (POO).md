---
aliases: [OOP, Classes, Objetos, Instanciação]
tags: [programacao, python, oop, classes]
area: Engenharia de Software
status: Concluído
data: {{date}}
---

# 07 - Programação Orientada a Objetos (POO)

## Resumo (TL;DR)
A **Programação Orientada a Objetos (POO)** é um paradigma que organiza o código em torno de "objetos" em vez de funções e lógica pura. Um objeto é uma instância de uma **Classe**, que funciona como um molde, definindo **Atributos** (dados/estado) e **Métodos** (comportamento). Este paradigma facilita o reaproveitamento de código e a representação de entidades do mundo real no software.

## Conceitos Principais
- **Classe:** O projeto ou modelo (ex: Classe `Carro`).
- **Objeto/Instância:** A materialização do modelo (ex: O seu carro específico).
- **Atributos:** Variáveis que pertencem ao objeto (ex: `cor`, `modelo`, `ano`).
- **Métodos:** Funções que o objeto pode executar (ex: `acelerar()`, `frear()`).
- **Método Construtor (`__init__`):** Método especial chamado automaticamente quando um objeto é criado para inicializar seus atributos.
- **Self:** Parâmetro obrigatório em métodos Python que referencia a própria instância que está executando o código.

## Exemplos Práticos / Código

**Definição de uma Classe e Instanciação:**
```python
class Carro:
    def __init__(self, marca, modelo, ano):
        self.marca = marca
        self.modelo = modelo
        self.ano = ano
        self.odometro = 0

    def ler_odometro(self):
        print(f"Este carro tem {self.odometro} km rodados.")

    def atualizar_odometro(self, km):
        if km >= self.odometro:
            self.odometro = km

# Criando um objeto
meu_carro = Carro('Audi', 'A3', 2024)
meu_carro.atualizar_odometro(150)
meu_carro.ler_odometro()
```

# Referências
* FIAP. Python e orientação a objetos(1).pdf. Roberto Cândido, 2026.

## 🔗 Conexões
- [[Encapsulamento]]

- [[Herança e Polimorfismo]]

- [[05 - Listas Ligadas]] (frequentemente implementadas com classes)