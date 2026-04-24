---
aliases: [Scrum Framework, Sprints, Product Owner, Scrum Master]
tags: [agil, scrum, sprints, frameworks, gestao]
area: Gestão de Projetos
status: Concluído
data: {{date}}
---

# 03 - Scrum

## Resumo (TL;DR)
O **Scrum** é o framework ágil mais popular do mercado, desenhado para gerenciar projetos complexos de forma empírica. Ele divide o trabalho em ciclos curtos, iterativos e com tempo fixo (Timebox) chamados **Sprints** (geralmente de 1 a 4 semanas). O Scrum se baseia em papéis muito bem definidos, cerimônias (reuniões) específicas e artefatos focados na entrega contínua de valor.

## Conceitos Principais
* **Papéis do Scrum:**
    * **Product Owner (PO):** O dono do produto. Gerencia o *Backlog* e garante que o time construa o que traz mais valor ao negócio.
    * **Scrum Master:** O facilitador. Remove impedimentos e garante que a equipe siga os princípios do Scrum.
    * **Development Team (Time de Desenvolvimento):** Equipe multifuncional e autogerenciável que executa o trabalho.
* **Artefatos:**
    * **Product Backlog:** Lista priorizada de tudo que o produto precisa (histórias de usuário).
    * **Sprint Backlog:** Tarefas selecionadas para a Sprint atual.
* **Cerimônias (Eventos):**
    * *Sprint Planning:* Planejamento do que será feito na Sprint.
    * *Daily Scrum (Standup):* Reunião diária rápida (15 min) (O que fiz? O que farei? Há impedimentos?).
    * *Sprint Review:* Apresentação do software funcionando aos stakeholders no final da Sprint.
    * *Sprint Retrospective:* Reunião interna para discutir como melhorar o processo na próxima Sprint.

## Exemplos Práticos / Código

**Visualizando o Monitoramento (Burndown Chart):**
O *Burndown Chart* é um gráfico que desce. O Eixo Y mostra o esforço restante (ex: 100 pontos), e o Eixo X mostra os dias da Sprint.
```text
Pontos Restantes
100 | * (Dia 1)
 80 |   \
 60 |     * (Dia 3 - Atrasado em relação à linha ideal)
 40 |       \
 20 |         * (Dia 8)
  0 |_____________\* (Dia 10 - Sprint Concluída)
  ```

# Referências
FIAP. Aula 3 - Scrum.pptx. 2026.

## 🔗 Conexões
- [[01 - Projetos Tradicionais e Projetos Ágeis]]

- [[05 - Kanban]] (Muitas vezes usado em conjunto com Scrum, gerando o "Scrumban")

- [[04 - Extreme Programming (XP)]]