---
aliases: [SGBD, CRUD, Hierarquia de Dados]
tags: [banco-de-dados, sgbd, crud, backend]
area: Banco de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

Um Banco de Dados é essencialmente o estágio mais evoluído na hierarquia do armazenamento computacional, servindo para dar contexto aos dados puros e transformá-los em **informação**. Essa informação é gerida por um software específico (SGBD) através de operações de CRUD, normalmente integrado em uma arquitetura de sistemas de 3 camadas.

## Conceitos Principais

- **Dado vs. Informação:**
    
    - Computadores processam **dados** puros (ex: o número isolado "192").
        
    - A **informação** é quando atribuímos contexto e significado a esse dado (ex: "Altura = 192 cm").
        
- **Hierarquia do Armazenamento:**
    
    - Cresce na seguinte ordem lógica: Bit $\rightarrow$ Byte $\rightarrow$ Campo (atributo) $\rightarrow$ Registro (uma linha da tabela) $\rightarrow$ Arquivo (a tabela inteira) $\rightarrow$ Banco de Dados (arquivos relacionados em conjunto).
        
- **CRUD no SGBD:**
    
    - **SGBD** (Sistema Gerenciador de Banco de Dados) é o software responsável por gerenciar a hierarquia de armazenamento.
        
    - Realiza as 4 operações fundamentais (**CRUD**): Inclusão (Insert), Leitura (Select), Atualização (Update) e Exclusão (Delete).
        
- **Arquitetura em Camadas:**
    
    - Sistemas modernos geralmente são divididos em 3 camadas operacionais:
        
        1. Interface com o usuário (Front).
            
        2. Aplicação (Regras de negócio e Backend, como Spring Boot).
            
        3. Dados (SGBD).
            

## 🔗 Conexões

- [[02 - Os 3 Níveis de Modelagem de Dados]]
    
