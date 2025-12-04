# 💾 APIusuario: Serviço REST de Gerenciamento de Usuários (CRUD)

![Badge do status do build (ex: Passing)](https://img.shields.io/badge/Status-Funcional-brightgreen) 
![Badge de Linguagem (Java)](https://img.shields.io/badge/Linguagem-Java-red) 
![Badge de Framework (Spring Boot)](https://img.shields.io/badge/Framework-Spring%20Boot-green)
---

## 📄 Sobre o Projeto

**`apiusuario`** é um **micro-serviço backend (API RESTful)** desenvolvido em **Java** (utilizando o framework Spring Boot), projetado para fornecer um serviço centralizado e padronizado para as operações básicas de **CRUD** (Create, Read, Update, Delete) de usuários em um banco de dados SQL.

### O Conceito CRUD

Esta API implementa o ciclo de vida completo de uma entidade `Usuario`:

| Operação | Método HTTP | Ação |
| :--- | :--- | :--- |
| **C**reate | `POST` | Cria um novo usuário. |
| **R**ead | `GET` | Busca um ou todos os usuários. |
| **U**pdate | `PUT` | Atualiza um usuário existente. |
| **D**elete | `DELETE` | Remove um usuário. |

---

## ⚙️ Tecnologias Principais

* **Linguagem:** Java (JDK 17+)
* **Framework:** Spring Boot 3+
* **Build Tool:** Apache Maven
* **Persistência:** Spring Data JPA (para abstração do SQL)
* **Banco de Dados:** Compatível com qualquer SQL (configurado via `application.properties`)

---

## 🚀 Configuração e Execução Local

Siga os passos abaixo para clonar o repositório e rodar a API em sua máquina local.

### Pré-requisitos

Certifique-se de ter instalado:
1.  **Java Development Kit (JDK)**
2.  **Apache Maven**
3.  Uma instância de banco de dados SQL (ex: MySQL, PostgreSQL, H2) rodando ou configurada.

### 1. Clonar o Repositório

```bash
git clone [https://github.com/RestoDeTripas/apiusuario.git](https://github.com/RestoDeTripas/apiusuario.git)
cd apiusuario
