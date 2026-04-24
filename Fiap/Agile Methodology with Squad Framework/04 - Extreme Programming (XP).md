---
aliases: [Extreme Programming, Pair Programming, TDD]
tags: [agil, xp, engenharia-de-software, qualidade-de-codigo]
area: Engenharia de Software
status: Concluído
data: {{date}}
---

# 04 - Extreme Programming (XP)

## Resumo (TL;DR)
O **Extreme Programming (XP)**, criado por Kent Beck, é uma metodologia ágil voltada estritamente para a **excelência técnica no desenvolvimento de software**. Enquanto o Scrum foca na gestão, o XP foca em *como* o código é escrito. Ele é ideal para equipes pequenas (até 12 pessoas) lidando com requisitos muito voláteis, impondo práticas rigorosas de engenharia, como programação em par e testes automatizados.

## Conceitos Principais
* **Valores do XP:** Comunicação, Simplicidade, Feedback, Coragem (para refatorar código) e Respeito.
* **Práticas de Engenharia (O Coração do XP):**
    * **Test-Driven Development (TDD):** Escrever o teste *antes* de escrever o código.
    * **Pair Programming (Programação em Par):** Dois programadores dividem um teclado e monitor. Um digita (piloto), o outro analisa a lógica e pensa estrategicamente (copiloto). Aumenta a qualidade e reduz bugs.
    * **Continuous Integration (CI):** O código é integrado e testado várias vezes ao dia.
    * **Refatoração:** Melhorar o design do código constantemente sem mudar seu comportamento externo.
    * **Small Releases:** Entregas em ciclos muito curtos, colocando o produto na mão do cliente o mais rápido possível.
* **Cerimônias:** *Planning Game* (estimativas com o cliente), *Daily Standup*, *Iteration Planning*.

## Exemplos Práticos / Código

**O Ciclo TDD (Test-Driven Development) no XP:**
O mantra do TDD é: **Red, Green, Refactor** (Falhar, Passar, Melhorar).

```python
# PASSO 1: RED (Escrevemos o teste que vai falhar, pois a função não existe)
def test_soma():
    assert soma(2, 3) == 5

# PASSO 2: GREEN (Escrevemos o código mais simples para o teste passar)
def soma(a, b):
    return a + b

# PASSO 3: REFACTOR (Se necessário, otimizamos o código mantendo o teste passando)
# (Neste exemplo simples, a função já está otimizada).
```
# Referências
    FIAP. Aula 4 - XP.pptx. 2026.

## 🔗 Conexões
- [[03 - Scrum]] (Scrum define as regras do jogo, XP define como jogar bem tecnicamente)

- [[01 - Projetos Tradicionais e Projetos Ágeis]]

- [[Integração Contínua e Deploy Contínuo (CI-CD)]]