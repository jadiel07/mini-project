# 🚀 Project1 - API REST com Express, Prisma e MongoDB

Seja bem-vindo à **API de Usuários** construída com **Node.js**, **Express**, **Prisma ORM** e **MongoDB**.  
Com esta API, é possível **cadastrar, listar, filtrar, atualizar e deletar usuários** de forma simples e eficaz.

---

## 🛠️ Tecnologias Utilizadas

- ⚙️ Node.js
- 🌐 Express
- 🧬 Prisma ORM
- 🍃 MongoDB
- 📦 JavaScript (ESM)
- 🔐 Dotenv

---

## 📁 Estrutura do Projeto

project1/
│
├── prisma/
│ └── schema.prisma # Schema do banco de dados Prisma
├── .env # Variáveis de ambiente (MongoDB)
├── server.js # Servidor Express
├── package.json # Dependências do projeto

yaml
Copiar
Editar

---

## ⚙️ Instalação e Configuração

1. **Clone o repositório:**

```bash
git clone https://github.com/seu-usuario/project1.git
cd project1
Instale as dependências:

bash
Copiar
Editar
npm install
Configure o arquivo .env:

env
Copiar
Editar
DATABASE_URL="sua_url_do_mongodb"
Gere o Prisma Client:

bash
Copiar
Editar
npx prisma generate
Atualize o banco com o schema:

bash
Copiar
Editar
npx prisma db push
Inicie o servidor:

bash
Copiar
Editar
node server.js
📌 Endpoints da API
🔹 Criar Usuário
POST /usuarios

📥 Corpo da Requisição:
json
Copiar
Editar
{
  "email": "usuario@email.com",
  "name": "João Silva",
  "age": "25"
}
✅ Resposta: 201 Created
🔹 Listar Usuários
GET /usuarios

🔍 Parâmetros de busca opcionais:
name

email

age

Exemplo:

pgsql
Copiar
Editar
GET /usuarios?name=joao
✅ Resposta: 200 OK
🔹 Atualizar Usuário
PUT /usuarios/:id

📥 Corpo da Requisição:
json
Copiar
Editar
{
  "email": "novo@email.com",
  "name": "Novo Nome",
  "age": "30"
}
✅ Resposta: 201 Updated
🔹 Deletar Usuário
DELETE /usuarios/:id

✅ Resposta: 204 No Content
📘 Exemplo de schema.prisma
prisma
Copiar
Editar
generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "mongodb"
  url      = env("DATABASE_URL")
}

model User {
  id    String  @id @default(auto()) @map("_id") @db.ObjectId
  email String  @unique
  name  String?
  age   String
}
💡 Observações
Prisma Client precisa ser gerado com npx prisma generate

Projeto configurado com "type": "module" no package.json

Requisições em JSON com express.json()

📄 Licença
Este projeto está sob a licença MIT.
Feito com 💙 por Jadiel

yaml
Copiar
Editar

---

### ✅ Dicas finais:
- Substitua `seu-usuario` pela sua URL real do GitHub.

