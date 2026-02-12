Docker: Utilização prática no cenário de Microsserviços
Denilson Bonatti, Instrutor - Digital Innovation One

Muito se tem falado de containers e consequentemente do Docker no ambiente de desenvolvimento. Mas qual a real função de um container no cenários de microsserviços? Qual a real função e quais exemplos práticos podem ser aplicados no dia a dia? Essas são algumas das questões que serão abordadas de forma prática pelo Expert Instructor Denilson Bonatti nesta Live Coding. IMPORTANTE: Agora nossas Live Codings acontecerão no canal oficial da dio._ no YouTube. Então, já corre lá e ative o lembrete! Pré-requisitos: Conhecimentos básicos em Linux, Docker e AWS.


* <h2> MELHORIA PARA ENTREGA DE PROJETO DO BOOTCAMP
    <h3>Atualização: 12/02/2026

🏗 Resumo sobre a Arquitetura do Projeto

* 🐬 MySQL - Banco de Dados
* 🐘 PHP (PHP-FPM) - Processamento de aplicação
* 🌐 Nginx - Servidor web / Proxy reverso
* 🗄 Adminer - Interface web para gerenciamento de BD.

===================================================

📁 Estrutura do Projeto

    dio-desafio-docker/
    │
    ├── docker-compose.yml
    ├── banco.sql
    │
    ├── nginx/
    │   └── nginx.conf
    │
    ├── php/
    │   └── Dockerfile
    │
    └── src/
        └── index.php

===================================================

🧠 Conceitos Aplicados

* Containerização com Docker
* Orquestração com Docker Compose
* Comunicação entre containers via rede bridge
* Volume persistente para banco de dados
* Integração Nginx + PHP-FPM
* Infraestrutura como código

===================================================

⚙️ Tecnlogias Utilizadas

* Docker
* Docker Compose
* PHP 8.2 (FPM)
* MySQL 5.7
* Nginx
* Adminer
===================================================

🚀 Como Executar o projeto

1. Clone o repositório

    git clone https://github.com/seu-usuario/dio-desafio-docker.git

1. Entre na pasta do projeto: 

        cd dio-desafio-docker

2. Suba os containers

        docker compose up --build

3. Acesse a aplicação

    Aplicação PHP:
        http://localhost:4500
    
    Adminer
        http://localhost:8080

===================================================

🗄 Acesso ao Banco de Dados (Adminer)

* Servidor: mysqlsrv
* Usuário: root
* Senha: Senha123
* Banco: meubanco

===================================================

🔄 Fluxo da Aplicação

    Client → Nginx → PHP-FPM → MySQL → Response

O Nginx atua como proxy reverso e encaminha requisições PHP para o container php via FastCGI.

A comunicação entre serviços ocorre através da rede bridge interna do Docker, utilizando resolução DNS automática baseada no nome do serviço.

===================================================

🧩 Comunição Entre Containers

Os serviços se comunicam utilizando o nome definido no docker-compose.yml.

    Exemplo no index.php:
        $servername = "mysqlsrv";

O Docker fornece DNS interno automaticamente.

===================================================

📌 Principais Aprendizados

* Estruturação correta de um docker-compose.yml
* Separação de responsabilidades entre serviços
* Configuração de rede bridge
* Uso de volumes persistentes
* Build de imagem customizada com Dockerfile
* Integração entre múltiplos containers

===================================================

📖 Conclusão

Este projeto demonstra na prática a utilização do Docker no cenário de microserviços, organizando aplicação, bando de dados e servidor web em containers independentes e orquestrados via Docker Compose.
