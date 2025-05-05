📦 API de Usuários com Express + Prisma + MongoDB
Esta é uma API RESTful simples para gerenciar usuários utilizando:

Node.js + Express

Prisma ORM

Banco de dados MongoDB

Requisições JSON

🚀 Instalação
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seu-usuario/project1.git
cd project1
Instale as dependências:

bash
Copiar
Editar
npm install
Configure o .env com sua URL do MongoDB:

Crie um arquivo .env e adicione:

ini
Copiar
Editar
DATABASE_URL="sua_url_do_mongodb"
Gere o cliente Prisma:

bash
Copiar
Editar
npx prisma generate
Suba o banco de dados:

bash
Copiar
Editar
npx prisma db push
Inicie o servidor:

bash
Copiar
Editar
node server.js
🧩 Endpoints
📥 Criar usuário
POST /usuarios

json
Copiar
Editar
{
  "email": "exemplo@email.com",
  "name": "João",
  "age": "25"
}
📌 Resposta: 201 Created

📄 Listar usuários
GET /usuarios

📌 Resposta: Lista todos os usuários cadastrados.

🔍 Filtros opcionais por query params:

name

email

age

Exemplo:

pgsql
Copiar
Editar
GET /usuarios?name=joao
✏️ Atualizar usuário
PUT /usuarios/:id

json
Copiar
Editar
{
  "email": "novo@email.com",
  "name": "Novo Nome",
  "age": "30"
}
📌 Resposta: 201 Updated

🗑️ Deletar usuário
DELETE /usuarios/:id

📌 Resposta: 204 No Content

🛠️ Tecnologias usadas
Node.js

Express

Prisma ORM

MongoDB

JavaScript (ESM)

📂 Estrutura do Projeto
pgsql
Copiar
Editar
project1/
│
├── prisma/
│   └── schema.prisma
├── .env
├── server.js
├── package.json
