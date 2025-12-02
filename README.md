# CRUD de Contatos – Java + MySQL + React

Este projeto é um sistema completo de **CRUD de contatos**, com backend em **Java (Spring Boot)**, banco de dados **MySQL**, e frontend em **React**.

## Tecnologias Utilizadas
- **Java 17**
- **Spring Boot**
- **MySQL**
- **React + Vite**
- **Axios**
- **Node.js / npm**

---

## Como rodar o projeto

### 1. Backend (Java + Spring Boot)
1. Abra o projeto
2. Configure `application.properties` com suas credenciais do MySQL:
   ```
   spring.datasource.url=jdbc:mysql://localhost:3306/contacts_db
   spring.datasource.username=root
   spring.datasource.password=suasenha
   spring.jpa.hibernate.ddl-auto=update
   ```
3. Execute o backend:
   ```
   ./mvnw spring-boot:run
   ```
   Ele rodará na porta **3001**

---

### 2. Frontend (React)
1. Acesse a pasta do frontend:
   ```
   cd frontend
   ```
2. Instale as dependências:
   ```
   npm install
   ```
3. Execute:
   ```
   npm run dev
   ```

---

## Banco de Dados MySQL

Execute no MySQL Workbench:

```
CREATE DATABASE IF NOT EXISTS contacts_db;

USE contacts_db;

CREATE TABLE IF NOT EXISTS contacts (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(200) NOT NULL,
  email VARCHAR(200) NOT NULL,
  phone VARCHAR(50),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

```

## Descrição Geral
O sistema permite:
- Criar contatos  
- Listar contatos  
- Atualizar contatos  
- Remover contatos  

Interface simples e intuitiva conectada ao backend Java via API REST.
