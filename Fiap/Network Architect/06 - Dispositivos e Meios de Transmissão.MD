---
aliases: [Dispositivos de Rede, Meios de Transmissão, Switch, Roteador, Endereço MAC]
tags: [redes, hardware, switch, mac-address, camada-2, camada-3]
area: Redes
status: Concluído
data: {{date}}
---

# 06 - Dispositivos e Meios de Transmissão

## Resumo (TL;DR)
A comunicação de rede depende de três componentes primários: **Dispositivos Finais** (hosts como PCs e servidores), **Dispositivos Intermediários** (switches, roteadores e access points) e **Meios de Transmissão** (cabos ou espectro sem fio)[cite: 3355, 3356, 3357]. Switches operam primariamente na Camada 2 (Enlace) baseados em endereços MAC, enquanto roteadores operam na Camada 3 (Rede) baseados em IPs.

## Conceitos Principais
* **Meios de Transmissão:**
    * *Cabos Metálicos:* Transmitem dados via impulsos elétricos (ex: Cat5e, Cat6)[cite: 3363].
    * *Cabos Ópticos:* Transmitem dados codificados em pulsos de luz[cite: 3368].
    * *Sinal Wireless:* Transmissão via ondas do espectro eletromagnético (Wi-Fi, Bluetooth)[cite: 3369].
* **Endereço MAC (Media Access Control):**
    * Identificador único de hardware atrelado à placa de rede (NIC)[cite: 3491, 3518].
    * Possui **48 bits (6 bytes)**, representado em formato hexadecimal[cite: 3528, 3532].
    * Os 3 primeiros bytes indicam o fabricante (OUI - definido pelo IEEE) e os 3 últimos são definidos pelo fabricante[cite: 3522, 3523].
* **Switches:**
    * **Camada 2 (L2):** Decidem o encaminhamento de quadros filtrando endereços MAC, criando dinamicamente uma tabela associando portas a MACs aprendidos[cite: 3489, 3511, 3570, 3571]. Exemplo: Cisco 2960[cite: 3718].
    * **Camada 3 (L3):** Além de MACs, operam com endereçamento IP, permitindo roteamento entre VLANs (Inter-VLAN routing) internamente[cite: 3677, 3678, 3731]. Exemplo: Cisco 3560[cite: 3727].
* **Modos de Transmissão (Duplex):**
    * *Half-Duplex:* Fluxo unidirecional. Envia *ou* recebe, não simultaneamente (causa colisões, comum em hubs antigos)[cite: 3655, 3657, 3658].
    * *Full-Duplex:* Fluxo bidirecional. Envia e recebe dados ao mesmo tempo, desativando circuitos de detecção de colisão[cite: 3663, 3666].
* **Roteadores e Access Points (APs):**
    * *Roteador:* Dispositivo de Camada 3 que interconecta redes diferentes e determina o melhor caminho (roteamento) para os pacotes[cite: 3757, 3784].
    * *Access Point:* Converte sinais da rede cabeada em sem fio[cite: 3793].
    * *Roteador Wireless:* Combina funções de AP, roteamento, DHCP e firewall (comum em ambientes domésticos)[cite: 3799, 3800].

## Exemplos Práticos / Código

**Matemática de Rede (Bits e Bytes):**
Um byte contém 8 bits. Portanto, 6 bytes $\times$ 8 bits = 48 bits totais do endereço MAC[cite: 3549, 3550].
O byte `10101010` em binário equivale a `170` em decimal:
$1\times128 + 0\times64 + 1\times32 + 0\times16 + 1\times8 + 0\times4 + 1\times2 + 0\times1 = 170$
*[cite: 3561, 3564]*

**Visualizando a Tabela MAC em um Switch Cisco (CLI):**
```bash
Switch> enable
Switch# show mac address-table
```

# Referências
* FIAP. ES - Aula 05 - Dispositivos e Meio de Transmissão (3).pdf. Karlos Miguel, 2026.

## 🔗 Conexões
- [[Endereçamento IPv4 e IPv6]]

- [[Camada de Enlace]]

- [[VLANs e Segmentação]]

- [[Equipamentos de Camada 3]]