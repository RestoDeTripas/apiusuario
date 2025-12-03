# apiusuario

## O que é

`apiusuario` é um micro-serviço de backend (API REST) desenvolvido em Java, cujo objetivo é gerenciar operações relacionadas a usuários — por exemplo: criação, leitura, atualização e deleção de dados de usuário. 

## Para quem é / Em que contexto usar

Esta API se destina a projetos que precisam de um serviço centralizado de gerenciamento de usuários — seja para sistemas web, mobile ou microserviços — de maneira simples, padronizada e em Java.  

## Tecnologias usadas

- Java (versão compatível com o projeto)  
- Maven — conforme arquivo `pom.xml` presente na raiz  
- Estrutura de pastas padrão de projetos Java (fonte em `src/`)  

## 🔧 Como rodar localmente  

Para executar a API localmente, siga estes passos:

```bash
# 1. Clone o repositório
git clone https://github.com/RestoDeTripas/apiusuario.git

# 2. Acesse o diretório do projeto
cd apiusuario

# 3. Compile e gere o build com Maven
mvn clean install

# 4. Execute a aplicação
mvn spring-boot:run  # ou o comando equivalente conforme sua configuração
│       ├── java/       # código-fonte Java
│       └── resources/  # configurações, application.properties, etc
├── .gitignore
└── README.md  # este arquivo
