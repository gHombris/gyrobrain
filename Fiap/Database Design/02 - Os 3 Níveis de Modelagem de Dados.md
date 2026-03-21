---
aliases: [Modelo Lógico, Modelo Físico, Modelo Conceitual]
tags: [banco-de-dados, modelagem, arquitetura]
area: Banco de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

A construção de um banco de dados requer abstração antes do código. A modelagem divide-se em três etapas lógicas: O **Conceitual** (foco nas regras de negócio), o **Lógico** (foco no paradigma estrutural, como tabelas) e, finalmente, o **Físico** (código real para um SGBD específico).

## Conceitos Principais

- **Modelo Conceitual:**
    
    - Possui alto nível de abstração, mantendo o foco total nas regras e no "negócio".
        
    - É projetado sem considerar qual tecnologia ou SGBD será usado.
        
    - O Modelo Entidade-Relacionamento (MER) é aplicado nesta fase.
        
- **Modelo Lógico:**
    
    - Realiza a tradução do modelo conceitual para um paradigma estruturado (ex: tabelas e chaves relacionais).
        
    - Ainda não se trata de código SQL puro.
        
- **Modelo Físico:**
    
    - É a implementação concreta e real da estrutura.
        
    - Altamente ajustada para um banco de dados específico (como MySQL ou PostgreSQL), utilizando scripts SQL e definindo os tipos de dados nativos.
        

## 🔗 Conexões

- [[01 - Conceitos Básicos de Banco de Dados]]
    
- [[03 - Modelo Entidade-Relacionamento (MER)]]