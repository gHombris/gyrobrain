---
aliases: [Packet Tracer, Simulador de Redes, CLI Cisco]
tags: [redes, cisco, packet-tracer, simulador, cli]
area: Redes
status: Concluído
data: {{date}}
---

# 05 - Cisco Packet Tracer (Onboard)

## Resumo (TL;DR)
O **Cisco Packet Tracer** é uma ferramenta inovadora de simulação visual que permite criar e configurar redes de comunicação de forma virtual[cite: 2559]. Ele possibilita a inserção de dispositivos (roteadores, switches, PCs), conexão via cabos ou wireless, e a inspeção do tráfego[cite: 2576, 2577, 2578]. É uma ferramenta essencial para o aprendizado prático antes da implementação em hardware real.

## Conceitos Principais
* **Modos de Visualização:**
    * **Logical Mode (Modo Lógico):** Mostra a topologia e como os dispositivos estão conectados na rede, ignorando o aspecto físico[cite: 3240, 3338].
    * **Physical Mode (Modo Físico):** Mostra a escala física, racks, mesas, prateleiras e onde os equipamentos estão alocados espacialmente (ex: Data Centers, Wiring Closets)[cite: 3241, 3339].
* **Personalização (Preferences):** Em `Options > Preferences`, é possível ativar rótulos de portas, mostrar modelos dos dispositivos, ajustar fontes do terminal e ativar o backup automático[cite: 2629, 2634, 2656, 2691].
* **Guias de Configuração de Dispositivos:**
    * *Physical (Físico):* Interface para ligar/desligar o aparelho e instalar módulos de hardware (ex: placa wireless WMP300N)[cite: 2927, 2951].
    * *Config:* Interface Gráfica (GUI) exclusiva do simulador para definições básicas (gera os comandos CLI equivalentes)[cite: 3014, 3015, 3016].
    * *CLI:* Interface de Linha de Comando real do Cisco IOS[cite: 3060].
    * *Desktop:* Para dispositivos finais (PCs), simula um sistema operacional com Prompt de Comando, Configuração de IP e Navegador Web[cite: 3094].
    * *Services (Serviços):* Exclusivo para Servidores, permite configurar HTTP, DHCP, DNS, entre outros[cite: 3129, 3130].

## Exemplos Práticos / Código

**Configuração Básica de Hostname via CLI em um Roteador:**
```bash
# Entra no modo de usuário privilegiado (Privileged EXEC)
Router> enable 

# Entra no modo de configuração global
Router# configure terminal 

# Altera o nome do dispositivo
Router(config)# hostname Edge_Router_Backup 

# Sai do modo de configuração
Edge_Router_Backup(config)# end
``` 

# Referências
* FIAP. ES - Onboard - Cisco Packet Tracer.pdf. Karlos Miguel, 2026.

## 🔗 Conexões
- [[Comandos Cisco IOS]]

- [[Dispositivos de Rede]]

- [[Topologias de Rede]]