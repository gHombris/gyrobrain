---
aliases: [Introdução a Serviços de Rede, DNS, HTTP, Portas de Rede]
tags: [redes, servicos, dns, http, tcp-ip]
area: Redes
status: Concluído
data: {{date}}
---

# 04 - Introdução a Serviços de Rede (DNS e HTTP)

## Resumo (TL;DR)
[cite_start]Os serviços de rede são fundamentais para a comunicação, operando na camada de aplicação da arquitetura **TCP/IP**[cite: 1957, 1967]. [cite_start]As camadas inferiores garantem o transporte confiável (via TCP ou UDP), enquanto os serviços entregam valor direto ao usuário, como transferência de arquivos, e-mails e navegação web[cite: 1968, 1999, 2043]. [cite_start]Os serviços mais notáveis incluem o **HTTP** para a web e o **DNS** para resolução de nomes[cite: 1980, 1981].

## Conceitos Principais
* **Modelo Cliente-Servidor:** A comunicação é dividida em dois papéis. [cite_start]O **Cliente** solicita ou envia informações (ex: navegador web), e o **Servidor** responde ou armazena essas informações (ex: Apache)[cite: 2028, 2029, 2030, 2031].
* [cite_start]**Portas de Comunicação (Sockets):** Processos trocam mensagens através de portas padronizadas na Internet[cite: 2042, 2045].
    * [cite_start]*Porta 20/21:* **FTP** (Transferência de arquivos)[cite: 2054].
    * [cite_start]*Porta 22:* **SSH** (Login remoto seguro)[cite: 2054].
    * [cite_start]*Porta 25/587:* **SMTP** (Envio de e-mails)[cite: 2054].
    * [cite_start]*Porta 53:* **DNS** (Resolução de nomes)[cite: 2054].
    * [cite_start]*Porta 80:* **HTTP** (Transferência de hipertexto)[cite: 2054].
    * [cite_start]*Porta 110:* **POP3** (Recebimento de e-mail)[cite: 2054].
* [cite_start]**Serviço DNS (Domain Name System):** Traduz nomes de domínio fáceis de lembrar para endereços IP necessários para a comunicação[cite: 2262]. [cite_start]É hierárquico, utilizando domínio raiz (.), Top-level-domains (.com, .gov, .br) e subdomínios[cite: 2345, 2353, 2354, 2386]. [cite_start]O **DDNS (DNS Dinâmico)** atualiza automaticamente nomes de host para IPs dinâmicos[cite: 2492, 2494].
* [cite_start]**Protocolo HTTP:** Baseado no paradigma requisição/resposta (Request/Response)[cite: 2231]. 
    * *Evolução:* HTTP/1.1 usa múltiplas conexões TCP sequenciais; [cite_start]HTTP/2 otimiza usando uma única conexão TCP com multiplexing (requisições e respostas paralelas), reduzindo a latência[cite: 2171, 2193, 2204].

## Exemplos Práticos / Código

**Estrutura de uma Requisição HTTP (Request):**
```http
GET /diretorio/pagina.html HTTP/1.1
Host: [www.fiap.com](https://www.fiap.com).br
Connection: close
User-agent: Mozilla/4.0
Accept-language: pt
```

# Referências
 FIAP. ES Serviços - Introdução (DNS e HTTP).pdf. Karlos Miguel, 2026.

## 🔗 Conexões
- [[Modelo TCP-IP]]

- [[Camada de Aplicação]]

- [[Endereçamento IP]]

- [[Cabeamento de Rede]]


