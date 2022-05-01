# EXERCÍCIO SEMANA 2, MÓDULO 2

Este repositório se refere à entrega do exercício de fixação para o Módulo 2, semana 2 da Gama Academy para o iLab.


## Compare e descreva as diferenças e o objetivo entre a Amazon SQS e a Amazon SNS.
O Amazon SQS é um serviço de filas de mensagens usado para enviar, armazenar e receber mensagens entre componentes de software.
Já o Amazon SNS é um serviço de mensagens para comunicação de aplicação para aplicação (A2A) e de aplicação para pessoa (A2P).

Ou seja, o SNS permite, por exemplo, o envio de notificações vários assinantes, enquanto o SQS permite a troca de mensagens entre componentes da aplicação, podendo ser usado para desacoplamento de componentes de envio e recebimento.


## Como o exercício foi desenvolvido
Foi criada uma aplicação Spring Boot simples para recebimento e envio de mensagens via AWS SQS. O foco foi treinar o serviço de AWS SQS, portanto a aplicação e a interface é bastante simples e de importância secundária.
Foram utilizadas 3 rotas, uma inicial com apenas uma mensagem de boas vindas, uma rota para enviar uma mensagem padrão (/send) contendo data e hora e uma rota (/receive) para apresentar em tela as mensagens recebidas.


## Para rodar a aplicação
* Fazer o download ou clonar o repositório
* Incluir nas variáveis de ambiente os dados do usuário da AWS
AWS_ACCESS_KEY=""
AWS_SECRET_KEY=""
* Alterar no código: Incluir o ID de sua conta AWS; Incluir nome de uma queue.fifo. Opcionalmente o corpo da mensagem também pode ser alterado.
* No terminal, na pasta do projeto: mvn clean package
* No terminal, na pasta do projeto: java -jar target/ilab-exercicio-semana2-aws-sqs-0.0.1-SNAPSHOT.jar
* A aplicação estará rodando na porta 8080
* No navegador, acessar: localhost:8080
* Para enviar mensagem: localhost:8080/send
* Para receber mensagens: localhost:8080/receive
