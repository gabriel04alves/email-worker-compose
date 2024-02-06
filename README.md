# Sistema de envio de emails

#### O projeto consiste em uma aplicação simulada desenvolvida durante o curso de Docker da Cod3r. Ele permite o envio simulado de e-mails e com o objetivo de praticar conceitos de Docker, como personalização de imagens, encapsulamento de contêineres e segregação de redes.

#### Projeto base: https://github.com/cod3rcursos/curso-docker/tree/master/email-worker-compose
 

###  ℹ️ Como iniciar projeto: 


##### Com o Docker e o Docker Compose já instalados na máquina host e o projeto clonado, acesse o repositório do projeto e execute:

#### 1. Iniciar em modo daemon:
~~~ 
docker-compose up -d  
~~~ 
ou, para iniciar e escalar os workers:
~~~
docker-compose up -d --scale worker=3
~~~

#### 2. Visualizar os logs dos serviços em tempo real:
~~~
docker-compose logs -f -t
~~~

#### 3. Visualizar a tabela 'emails' do DB :
~~~
docker-compose exec db psql -U postgres -d email_sender -c 'select * from emails'
~~~

#### 4. Encerrar os processos: 
~~~
docker-compose down
~~~