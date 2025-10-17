# 🎬 Movieflix API

API para busca e consulta de filmes, desenvolvida com **Node.js**, **TypeScript**, **Prisma**, **Docker** e **Swagger**.  
Permite listar, buscar e filtrar filmes, com documentação interativa e estrutura escalável para integração com front-ends web e mobile.

---

## 🧩 Tecnologias Utilizadas

- **Node.js** – ambiente de execução JavaScript  
- **TypeScript** – tipagem estática e melhor manutenção de código  
- **Prisma ORM** – mapeamento objeto-relacional para banco de dados  
- **Docker** e **Docker Compose** – containers para ambiente padronizado  
- **Swagger / OpenAPI** – documentação interativa dos endpoints  
- **Express.js** (ou framework HTTP utilizado)  
- Banco de dados relacional (ex: PostgreSQL, MySQL – conforme definido no `schema.prisma`)

---

## 🚀 Funcionalidades

- 🔍 Buscar filmes por título, gênero ou outros filtros  
- 🎞️ Listar e consultar detalhes de filmes  
- 🧾 Documentação completa via Swagger  
- 🐳 Ambiente de execução via Docker  
- 🧱 Estrutura modular com controllers, services e rotas  

---

## 🛠️ Requisitos

Antes de iniciar, certifique-se de ter instalado:

- [Node.js](https://nodejs.org/) (versão 18+)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- Banco de dados compatível com Prisma (PostgreSQL, MySQL etc.)

---

## ⚙️ Configuração e Execução Local

1. **Clone o repositório**

   ```bash
   git clone https://github.com/pamella-binotto/movieflix-api.git
   cd movieflix-api
   ```

2. **Configure o arquivo `.env`**

   Crie o arquivo `.env` na raiz do projeto com as variáveis de ambiente:

   ```env
   DATABASE_URL="sua_url_do_banco"
   PORT=3000
   ```

3. **Instale as dependências**

   ```bash
   npm install
   ```

4. **Gere as migrações com Prisma**

   ```bash
   npx prisma migrate dev
   ```

5. **Inicie o servidor**

   ```bash
   npm run dev
   ```

6. **Acesse a documentação Swagger**

   [http://localhost:3000/api-docs](http://localhost:3000/api-docs)

---

## 🐳 Executando com Docker

1. **Suba os containers**

   ```bash
   docker-compose up --build
   ```

2. O servidor e o banco de dados serão inicializados automaticamente.  
   Acesse a API e o Swagger conforme a configuração do `docker-compose.yml`.

---

## 📁 Estrutura do Projeto

```
.
├── src/
│   ├── controllers/      # Lógica de controle das rotas
│   ├── routes/           # Definições das rotas da API
│   ├── services/         # Regras de negócio
│   ├── middlewares/      # Middlewares de autenticação, erros, etc.
│   └── index.ts          # Ponto de entrada da aplicação
├── prisma/
│   └── schema.prisma     # Configuração do banco de dados
├── docker-compose.yml
├── Dockerfile
├── swagger.json
├── package.json
└── tsconfig.json
```

---

## 📦 Endpoints Principais

| Método | Rota | Descrição |
|--------|------|-----------|
| **GET** | `/movies` | Retorna a lista de filmes |
| **GET** | `/movies/:id` | Retorna detalhes de um filme específico |
| **GET** | `/movies?search=titulo` | Busca filmes por título |
| **GET** | `/movies?genre=ação` | Filtra filmes por gênero |

> Para visualizar todos os endpoints, acesse o Swagger UI.

---

## 🧪 Testes

Se o projeto incluir testes automatizados:

```bash
npm run test
```

---

## 💡 Melhorias Futuras

- Autenticação de usuários (JWT)  
- Sistema de favoritos / watchlist  
- Integração com APIs externas (TMDB, IMDb)  
- Paginação de resultados  

---

## 🧾 Licença

Este projeto está sob a licença **MIT**.  
Sinta-se livre para usar, estudar e contribuir. 💜

---

## 👩‍💻 Desenvolvido por

**Pamella Binotto**  
🔗 [GitHub](https://github.com/pamella-binotto)  
🔗 [LinkedIn](https://www.linkedin.com/in/pamellabinotto/)
