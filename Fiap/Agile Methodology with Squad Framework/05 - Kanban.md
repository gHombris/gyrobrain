```markdown
---
aliases: [Kanban Board, Sistema Puxado, WIP Limit]
tags: [agil, kanban, lean, toyota, fluxo]
area: Gestão de Projetos
status: Concluído
data: {{date}}
---

# 05 - Kanban

## Resumo (TL;DR)
O **Kanban** (literalmente "Cartão Visual" em japonês) nasceu na fábrica da Toyota (década de 1950) e foi adaptado para o trabalho do conhecimento. É um método visual de gestão de fluxo de trabalho. Seu principal diferencial é ser um **Sistema Puxado**, onde novas tarefas só entram no fluxo quando há capacidade disponível (limitando o Work in Progress - WIP), focando em eliminar gargalos e garantir que o trabalho flua sem interrupções.

## Conceitos Principais
* **Sistema Empurrado vs. Puxado:**
    * *Empurrado (Push):* Produz baseado em previsões, empurrando trabalho para a próxima etapa sem ligar para a capacidade (gera gargalos e estresse).
    * *Puxado (Pull):* Uma etapa "puxa" o trabalho da etapa anterior apenas quando termina o que está fazendo.
* **Princípios Fundamentais:**
    * Comece com o que você faz agora (não exige mudanças drásticas na estrutura da empresa).
    * Busque mudanças incrementais e evolutivas.
    * Respeite os papéis e cargos existentes.
* **Limites de WIP (Work in Progress):** A regra de ouro. Se o limite da coluna "Em Desenvolvimento" é 3, os devs não podem puxar uma quarta tarefa até que uma das três passe para a fase de testes.
* **Cerimônias:**
    * *Replenishment Meeting:* Reabastecimento da fila de "A Fazer".
    * *Workflow Meeting:* Sincronização diária do fluxo.

## Exemplos Práticos / Código

**Representação em Texto de um Quadro Kanban com WIP Limit:**
```text
| BACKLOG   | TO DO     | DOING (WIP: 2) | REVIEW (WIP: 2) | DONE       |
|-----------|-----------|----------------|-----------------|------------|
| Tarefa 7  | Tarefa 4  | [Tarefa 2]     | [Tarefa 1]      | Tarefa 0   |
| Tarefa 8  | Tarefa 5  | [Tarefa 3]     |                 |            |
| Tarefa 9  | Tarefa 6  |                |                 |            |

-> ATENÇÃO: A coluna "DOING" está cheia (WIP de 2). Nenhum dev pode
"puxar" a Tarefa 4 até que a Tarefa 2 ou 3 vá para o "REVIEW".
Isso previne a troca de contexto excessiva e força a equipe a TERMINAR antes de COMEÇAR.
```
# Referências
    FIAP. Aula 5 - Kanban.pptx. 2026.

## 🔗 Conexões
- [[02 - Projetos Tradicionais e Projetos Ágeis]]

- [[03 - Scrum]] (Diferença-chave: Scrum tem iterações de tempo fixo; Kanban é um fluxo contínuo).

- [[Sistemas Lean]]