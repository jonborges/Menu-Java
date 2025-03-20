# Menu Virtual - Backend

Este projeto consiste no backend de um **Menu Virtual** (ou **Cardápio**), responsável por fornecer uma API para gerenciar uma lista de itens disponíveis.

## 🔥 Tecnologias Utilizadas

- **Java 17+**
- **Spring Boot**
- **PostgreSQL** (banco de dados utilizado, mas pode ser alterado)
- **Lombok** (para evitar código boilerplate)

## 🚀 Funcionalidades

- **Listar todos os itens do cardápio** (`GET /food`)
- **Adicionar novos itens ao cardápio** (`POST /food`)
- **Integração com banco de dados**
- **Suporte a CORS liberado temporariamente** (`@CrossOrigin`)

## 📂 Estrutura do Projeto

```
📦 src/main/java/com/example/cardapio
 ┣ 📂food
 ┃ ┣ 📜Food.java           # Entidade do banco de dados
 ┃ ┣ 📜FoodRepository.java # Interface para comunicação com o banco
 ┃ ┣ 📜FoodController.java # Controlador para mapeamento das rotas
 ┃ ┣ 📜FoodResponseDTO.java # DTO para boas práticas na resposta da API
 ┃ ┗ 📜FoodService.java    # (Opcional) Lógica de negócios, se necessário
```

## 🛠️ Passo a Passo da Implementação

### 1️⃣ Criação do `FoodController`
   - Define o endpoint `@RequestMapping("/food")`.
   - Cria o método `getAll()` com `@GetMapping` para retornar todos os itens.
   
### 2️⃣ Banco de Dados
   - Utiliza **PostgreSQL** (mas pode ser qualquer banco SQL).
   - Conexão configurada no `application.properties`.
   
### 3️⃣ Criação da entidade `Food`
   - Classe `Food` com os campos `id`, `title`, `image` e `price`.
   - Anotada com `@Entity`, `@Table` e `@Id`.
   - Utiliza **Lombok** para gerar `Getters`, `Setters` e `Construtores` automaticamente.
   
### 4️⃣ Uso de DTO (`FoodResponseDTO`)
   - Melhora a organização da resposta da API.
   - Converte `List<Food>` em `List<FoodResponseDTO>` via `map()`.
   
### 5️⃣ Adição de novos itens
   - Método `POST` criado para adicionar novas comidas ao banco.
   
### 6️⃣ Configuração do CORS
   - `@CrossOrigin` aplicado para permitir requisições de qualquer origem.

## 🏁 Como Executar o Projeto

1. **Clone este repositório:**
   ```sh
   git clone https://github.com/seu-usuario/menu-virtual.git
   ```
2. **Configure o banco de dados no `application.properties`.**
3. **Execute a aplicação:**
   ```sh
   mvn spring-boot:run
   ```
4. **A API estará disponível em:**
   ```sh
   http://localhost:8080/food
   ```

## 📌 Melhorias Futuras

- Criação do FrontEnd(Em breve).
- Adicionar mais validações nos endpoints.
- Novas fundionalidades, caracteristicas.

---

📌 **Desenvolvido por Jon B**

