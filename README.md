# APIusuario

👤 Sobre o Projetoapiusuario é um micro-serviço de backend (API REST) desenvolvido em Java (provavelmente usando Spring Boot, devido ao uso do Maven e do comando de execução padrão), com a finalidade de fornecer um serviço centralizado para o gerenciamento completo de dados de usuários em um banco de dados SQL.Este projeto implementa as operações fundamentais de um sistema de gerenciamento de dados, conhecidas como CRUD (Create, Read, Update, Delete).🎯 Funcionalidade (O que a API faz)A principal função desta API é ser o intermediário entre sua aplicação cliente (web, mobile ou outro micro-serviço) e o banco de dados SQL. Ela garante que as requisições de criação, consulta, modificação e exclusão de dados de usuário sejam realizadas de forma segura e padronizada.Criação (Create): Recebe os dados de um novo usuário via requisição HTTP e os insere no banco de dados.Leitura (Read): Permite buscar a lista completa de usuários ou consultar os dados de um usuário específico.Atualização (Update): Recebe novos dados e altera as informações de um usuário já existente.Deleção (Delete): Remove permanentemente o registro de um usuário do banco de dados.💻 Tecnologias UtilizadasTecnologiaDescriçãoLinguagemJavaBuild ToolMaven (pom.xml)ArquiteturaAPI RESTful (Micro-serviço)PersistênciaConexão com Banco de Dados SQL (Configuração via application.properties)🛠️ Configuração e Execução LocalPara rodar o apiusuario em sua máquina local, você precisará ter o JDK (Java Development Kit) e o Maven instalados.1. Pré-requisitosJava (versão compatível com o projeto)MavenUm banco de dados SQL (MySQL, PostgreSQL, etc.) rodando localmente ou acessível.2. Configuração do Banco de DadosAntes de executar, você deve configurar as credenciais do seu banco de dados no arquivo de configuração do projeto (geralmente src/main/resources/application.properties ou application.yml).Exemplo para um banco de dados MySQL:Properties# Exemplo de configuração no application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/nome_do_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
3. Passos para RodarBash# 1. Clone o repositório
git clone https://github.com/RestoDeTripas/apiusuario.git

# 2. Acesse o diretório do projeto
cd apiusuario

# 3. Compile o projeto e baixe as dependências (Maven)
mvn clean install

# 4. Execute a aplicação (Spring Boot)
mvn spring-boot:run
A API estará acessível, por padrão, em http://localhost:8080 (a porta pode variar dependendo da configuração).🚀 Endpoints da API (Uso)A API segue o padrão RESTful para operações CRUD, utilizando o recurso principal /usuarios.Método HTTPPathAçãoDescriçãoPOST/usuariosCREATECria um novo usuário. O corpo da requisição deve conter o JSON com os dados do usuário (nome, email, senha, etc.).GET/usuariosREAD AllRetorna uma lista com todos os usuários cadastrados no banco de dados.GET/usuarios/{id}READ OneRetorna os dados de um usuário específico, identificado pelo seu {id}.PUT/usuarios/{id}UPDATEAtualiza todos os dados de um usuário específico. O corpo da requisição deve conter o JSON com os dados completos a serem substituídos.DELETE/usuarios/{id}DELETERemove o usuário especificado pelo {id} do banco de dados.Exemplo de Requisição (POST /usuarios)Para criar um novo usuário:URL: POST http://localhost:8080/usuariosCorpo da Requisição (JSON):JSON{
  "nome": "João da Silva",
  "email": "joao.silva@exemplo.com",
  "senha": "senha123"
}
Resposta de Sucesso (Status 201 Created):JSON{
  "id": 1,
  "nome": "João da Silva",
  "email": "joao.silva@exemplo.com"
}
Observação: O esquema JSON exato (campos e tipos de dados) é definido no código-fonte Java do projeto (entidade/modelo de usuário).
└── README.md  # este arquivo
