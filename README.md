<h1 align="center">Rayder Bounty Workflow</h1>

<p align="center">
  <a href="#sobre">Sobre</a> •
  <a href="#instalação-do-rayder">Instalação</a> •
  <a href="#uso">Uso</a> •
  <a href="#módulos-disponíveis">Módulos</a> •
  <a href="#coming-soon-features">Coming Soon</a> •
  <a href="#contribuições">Contribua</a> 
</p>

![rayder](https://github.com/devanshbatham/rayder/blob/main/static/banner.png?raw=true)

## Sobre

Este repositório contém templates e fluxos de trabalho prontos para uso com a ferramenta [Rayder](https://github.com/devanshbatham/rayder). A ferramenta Rayder é uma solução leve para orquestrar e organizar fluxos de trabalho de linha de comando.

Os templates neste repositório foram organizados em módulos, cobrindo várias etapas de um teste de segurança, desde a enumeração de subdomínios até a execução de testes de vulnerabilidade. Eles são projetados para facilitar a execução de testes de bug bounty e auditorias de segurança.

## Instalação do Rayder

Certifique-se de ter o Go (1.16 ou superior) instalado no seu sistema. Em seguida, execute o seguinte comando para instalar o Rayder:

```sh
go install github.com/devanshbatham/rayder@v0.0.4
```

## Uso

Para executar um fluxo de trabalho específico, utilize o seguinte comando:

```sh
rayder -w path/to/workflow.yaml
```

## Módulos Disponíveis

<details>
  <summary>Instalação das tools necessárias</summary>
  
Instala as seguintes tools:

* Subfinder
* Amass
* Anew
* Notify
* Dnsx
* Naabu
* Httpx
* Waybackurls
* Gau
* Gauplus
* Hakrawler
* Dirsearch
* Katana
* GetJS
* Gospider
* Anti-burl
* Mantra
* Crlfuzz
* Ffuz
* Gf
* Qsreplace
* Subjack
* Subzy
* Gxss
  
</details>
<details>
  <summary>Enumeração e validação de Subdomínios</summary>

<br>

A etapa de enumeração e validação dos subdomínios utiliza as seguintes tools:

* Amass
* Subfinder
* DnsX
* Naabu
* Httpx
* Notify

Para executar o workflow de **enumeração**:

```sh
rayder -w path/to/Enum-subs.yaml TARGET=domain.com
```
Para executar o workflow de **validação**:

```sh
rayder -w path/to/Subs-resolver.yaml
```

<br>
  
</details>
<details>
  <summary>Enumeração, validação e análise de JavaScript</summary>

<br>

A etapa de enumeração, validação e análise de JavaScript utiliza as seguintes tools:

* Gau
* GetJS
* Katana
* Gospider
* Hakrawler
* Dirsearch
* Anti-burl
* Mantra
* Notify

Para executar o workflow de **enumeração**:

```sh
rayder -w path/to/JS/Enum-JS.yaml 
```
Para executar o workflow de **validação**:

```sh
rayder -w path/to/JS/JS-resolver.yaml
```

Para executar o workflow de **análise**:

```sh
rayder -w path/to/JS/JS-api-key.yaml
```

<br>
  
</details>
<details>
  <summary>Enumeração e validação de Endpoints</summary>

<br>

A etapa de enumeração e validação dos endpoints utiliza as seguintes tools:

* Gauplus
* Hakrawler
* Katana
* Arjun
* Paramspider
* Httpx
* Notify

Para executar o workflow de **enumeração**:

```sh
rayder -w path/to/Endpoints/Enum-endpoints.yaml
```
Para executar o workflow de **validação**:

```sh
rayder -w path/to/Endpoints/Enum-resolver.yaml
```
<br>
  
</details>
<details>
  <summary>Enumeração e validação de páginas 403 para testes de bypass</summary>

<br>
  
A etapa de enumeração e validação das páginas 403 utiliza as seguintes tools:

* Httpx
* Notify

Para executar o workflow de enumeração em **subs 403**:

```sh
rayder -w path/to/403/Enum-subs-403.yaml
```
Para executar o workflow de enumeração em **endpoints 403**:

```sh
rayder -w path/to/403/Enum-endpoints-403.yaml
```

<br>
  
</details>
<details>
  <summary>Testes de vulnerabilidades</summary>
  
<br>

1. Nuclei
* Descrição breve do que este módulo faz. 
* Exemplo de uso e configuração.
2. XSS
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
3. Takeover
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
4. SSTI
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
5. SSTI
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
6. SSRF
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
7. SQLI
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
8. Prototype Pollution
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
9. Open Redirect
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
10. LFI
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
11. Fuzzing Templates
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
12. CRLF
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.
13. Bypass 403
* Descrição breve do que este módulo faz.
* Exemplo de uso e configuração.

<br>
  
</details>

## Coming Soon Features

* Bypass 403 
* Extração de subdominínios por JS
* Extração de endpoints por JS
* Template para automação de monitoramento
* Template para integração dos templates com bot telegram

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir problemas, enviar solicitações de pull ou sugerir melhorias para os templates existentes.
