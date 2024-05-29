# RabbitMQ com Node.js usando Docker

Este repositório contém uma configuração simples para utilizar RabbitMQ com Node.js, utilizando Docker para facilitar a execução do RabbitMQ.

## Pré-requisitos

- [Docker](https://www.docker.com/get-started)
- [Node.js](https://nodejs.org/)

## Configuração

###  Executar o RabbitMQ no Docker

Use o comando abaixo para baixar a imagem do RabbitMQ e executá-la em um contêiner Docker:

docker run -d --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management

### Acessar o Painel de Gerenciamento do RabbitMQ

Abra um navegador e vá para http://localhost:15672. Use as credenciais padrão (guest/guest) para fazer login.

### Instalar dependencia

npm install amqplib

### Execute os Scripts

Abra dois terminais. No primeiro terminal, execute o script receive.js para começar a consumir mensagens:

node receive.js

No segundo terminal, execute o script send.js para enviar uma mensagem para a fila:

node send.js