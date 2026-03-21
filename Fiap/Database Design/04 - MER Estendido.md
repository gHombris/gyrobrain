---
aliases: [MER Estendido, Agregação, Generalização, Especialização]
tags: [banco-de-dados, modelagem-conceitual, mer, arquitetura]
area: Banco de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

O **MER Estendido** adiciona conceitos avançados à modelagem de dados tradicional, permitindo representar cenários complexos do mundo real. Ele introduz abstrações como a **Agregação** (para relacionar relacionamentos) e a **Generalização/Especialização** (semelhante à herança em programação), além de classificar os atributos em diferentes categorias operacionais.

## Conceitos Principais

- **Agregação (Entidade Associativa):**
    
    - Permite que um relacionamento seja tratado e visualizado como uma entidade.
        
    - Resolve a limitação estrutural de não poder haver relacionamentos ligados diretamente a outros relacionamentos.
        
- **Generalização / Especialização:**
    
    - Consiste na divisão de uma entidade genérica em supertipos e subtipos, operando de forma semelhante à herança orientada a objetos.
        
    - **Total ou Parcial:** A generalização Total exige que absolutamente toda ocorrência do supertipo seja classificada em um subtipo. A Parcial admite exceções.
        
    - **Exclusiva ou Compartilhada:** A Exclusiva restringe a ocorrência a apenas um único subtipo. A Compartilhada permite que pertença a múltiplos subtipos simultaneamente.
        
- **Relacionamento Exclusivo (Arco):**
    
    - Uma ocorrência de uma entidade pode se relacionar com a entidade B ou com a entidade C, mas nunca com as duas em simultâneo.
        
- **Tipos de Atributos:**
    
    - **Simples:** Atributos comuns e indivisíveis (ex: nome).
        
    - **Identificadores:** Garantem a unicidade do registro (ex: CPF).
        
    - **Compostos:** São estruturados e divididos em sub-atributos menores (ex: um endereço dividido em rua e número).
        
    - **Multivalorados:** Representam listas de valores para um mesmo atributo (ex: múltiplos números de telefones).
        
## 🔗 Conexões

- [[03 - Modelo Entidade-Relacionamento (MER)]]
    
- [[02 - Os 3 Níveis de Modelagem de Dados]]