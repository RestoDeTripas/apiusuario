# apiusuario
# apiusuario

## O que é

`apiusuario` é um micro-serviço de backend (API REST) desenvolvido em Java, cujo objetivo é gerenciar operações relacionadas a usuários — por exemplo: criação, leitura, atualização e deleção de dados de usuário. É parte do conjunto de ferramentas do grupo “RestoDeTripas”.

## Para quem é / Em que contexto usar

Esta API se destina a projetos que precisam de um serviço centralizado de gerenciamento de usuários — seja para sistemas web, mobile ou microserviços — de maneira simples, padronizada e em Java.  

## Tecnologias usadas

- Java (versão compatível com o projeto)  
- Maven — conforme arquivo `pom.xml` presente na raiz  
- Estrutura de pastas padrão de projetos Java (fonte em `src/`)  

## Como usar / Instalação

1. Clone o repositório  
   ```bash
   git clone https://github.com/RestoDeTripas/apiusuario.git
cd apiusuario
mvn clean install
mvn spring-boot:run   # ou o comando equivalente conforme sua configuração

curl -X POST http://localhost:8080/usuarios \
  -H "Content-Type: application/json" \
  -d '{
        "nome": "João Silva",
        "email": "joao@example.com",
        "senha": "********"
      }'

apiusuario/
├── pom.xml
├── mvnw     # wrapper do Maven
├── src/
│   └── main/
│       ├── java/       # código-fonte Java
│       └── resources/  # configurações, application.properties, etc
├── .gitignore
└── README.md  # este arquivo
