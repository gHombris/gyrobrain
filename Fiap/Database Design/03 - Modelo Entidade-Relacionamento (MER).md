---
aliases: [MER, Cardinalidade, Entidades e Relacionamentos]
tags: [banco-de-dados, mer, modelagem-conceitual]
area: Banco de Dados
status: Concluído
data: 2026-03-20
---
## Resumo (TL;DR)

O **Modelo Entidade-Relacionamento (MER)** é a principal ferramenta gráfica utilizada durante a modelagem conceitual de dados. Ele mapeia visualmente as **Entidades** do sistema (representadas por retângulos), seus **Atributos** e a forma como interagem por meio de **Relacionamentos** (losangos) baseados em regras de **Cardinalidade**.

## Conceitos Principais

- **Entidades:**
    
    - Representadas visualmente por retângulos.
        
    - Representam as "coisas" sobre as quais o sistema precisa armazenar dados.
        
    - _Exemplos:_ Em um app de futebol, `Usuaria` e `Treino`; em um app de Pokémon, `Pokemon` e `Egg_Group`.
        
- **Relacionamentos:**
    
    - Representados visualmente por losangos.
        
    - Indicam a interação entre as entidades, normalmente expressos por verbos.
        
    - _Exemplo:_ A entidade `Pokemon` se relaciona com `Egg_Group` através da interação "pertence".
        
- **Atributos:**
    
    - São as propriedades e características específicas de uma entidade (ex: email da usuária, nome do Pokémon).
        
- **Cardinalidade:**
    
    - Estabelece os limites lógicos das relações entre as entidades:
        
    - **Máxima:** Pode ser do tipo 1:1 (um para um), 1:n (um para muitos) ou n:n (muitos para muitos).
        
    - **Mínima:** Determina se a relação é obrigatória. O valor 0 indica opcionalidade, e o valor 1 indica obrigatoriedade.
        

## 🔗 Conexões

- [[02 - Os 3 Níveis de Modelagem de Dados]]
    
