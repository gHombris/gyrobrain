---
aliases:
  - Modelo OSI
  - TCP/IP
  - Encapsulamento
tags:
  - redes
  - infraestrutura
  - internet
  - osi
area: Redes
data: 2026 - 03 - 20
---
## Resumo (TL;DR)

O **Modelo OSI** é um framework teórico universal dividido em 7 camadas que serve de base para a interoperabilidade entre fabricantes de hardware e rede. Em contrapartida, a **Arquitetura TCP/IP** é o modelo de 4 camadas utilizado nativamente na Internet, com foco prático no roteamento dinâmico de dados.

## Conceitos Principais

- **Modelo OSI:**
    
    - É um modelo teórico e universal de referência.
        
    - Está estruturado em **7 camadas**: Aplicação, Apresentação, Sessão, Transporte, Rede, Enlace/Acesso e Física.
        
- **Arquitetura TCP/IP:**
    
    - É o modelo utilizado nativamente na Internet.
        
    - Possui foco em roteamento dinâmico e é dividido em **4 camadas**:
        
        1. **Aplicação:** Interage com os softwares utilizando protocolos como DNS, HTTP, FTP e SMTP.
            
        2. **Transporte:** Forma os "Segmentos", utilizando portas lógicas e protocolos como TCP/UDP.
            
        3. **Rede/Internet:** Responsável pelo roteamento da morada fonte à de destino através de "Pacotes" utilizando o protocolo IP.
            
        4. **Acesso à Rede:** Forma os "Quadros" que seguem para o hardware, envolvendo Endereço MAC, drivers físicos e Ethernet.
            
- **Encapsulamento de dados:** * No envio, a máquina fonte inicia na camada de aplicação e "desce" pelas camadas, encapsulando e juntando cabeçalhos aos dados. * Na recepção, o router ou destino analisa a informação de "baixo para cima" até que os dados sejam lidos e entendidos pelas camadas superiores.
## Exemplos Práticos / Código

Embora este seja um conceito puramente arquitetural, podemos visualizar o **encapsulamento** de forma lógica. Quando você envia um email (SMTP):

1. **Aplicação:** O software cria a mensagem.
    
2. **Transporte:** A mensagem é dividida em _segmentos_ TCP (garantindo a entrega).
    
3. **Rede:** Os segmentos viram _pacotes_ IP (ganham endereço de origem e destino).
    
4. **Acesso:** Os pacotes viram _quadros_ e são convertidos em bits reais que viajam pelo seu Wi-Fi ou cabo de rede.

## Conexões

- [[01 - Introdução e IoT]] - Para entender como a Internet evoluiu até precisar desse roteamento dinâmico.
    
- [[02 - Classificação de redes]] - Para conectar os modelos lógicos (LAN, WAN) com o envio de pacotes através do TCP/IP.