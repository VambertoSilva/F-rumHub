# Challenge API Fórum Hub 👥
API REST desenvolvida no Challenge Back End da Alura + Oracle Next Education para simular um fórum com múltiplos recursos e autenticação.

---
## Tecnologias

- Java 17+  
- Spring Boot 
- Spring Data JPA
- Spring Security JWT
- Banco relacional (MySql)
- Flyway
- Maven
- Swagger

---
## Endpoints principais

- **CRUD** para usuários, tópicos, cursos e respostas (operando via REST)  
  - **POST**: criar  
  - **GET**: consultar/listar  
  - **PUT**: atualizar  
  - **DELETE**: deletar  

- **Perfis de usuário**: administrador e usuário comum  
  - Administradores podem criar, atualizar e deletar qualquer recurso  
  - Usuários comuns podem criar tópicos/respostas e gerenciar apenas seus próprios dados  

- **Autenticação via JWT** (necessária para todos os endpoints, exceto login e cadastro)  
- **Validações de entrada**  
- **Persistência em banco relacional**

---
## Estrutura do Banco de Dados

- ```cursos(id, nome, categoria)```
- ```usuarios(id, nome, email, senha)```
- ```perfis(id, nome(administrador, usuario)```
- ```usuarios_perfis(usuario_id, perfil_id)```
- ```topicos(id, titulo, mensagem, data, status, autor_id, curso_id)```
- ```respostas(id, mensagem, data, solucao, topico_id, autor_id)```
