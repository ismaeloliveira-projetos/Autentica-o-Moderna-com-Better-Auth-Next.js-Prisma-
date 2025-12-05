# 🚀 Autenticação Moderna com Better Auth, Next.js e Prisma

Este projeto implementa um sistema de autenticação moderno utilizando **Better Auth**, integrando com **Next.js**, **Prisma ORM** e **PostgreSQL**.  
O objetivo é criar uma base sólida, segura e tipada para aplicações que precisam de login, criação de conta, gerenciamento de sessão e proteção de rotas.

---

## 🛠 Tecnologias Utilizadas

- **Next.js**
- **TypeScript**
- **Better Auth**
- **Prisma ORM**
- **PostgreSQL**
- **Shadcn/UI** (caso esteja utilizando)
- **Node.js**

---

## 📌 Funcionalidades

- 🔐 Criação de conta  
- 🔑 Login com Better Auth  
- 🧭 Sessão persistida com cookies seguros  
- 🔄 Logout  
- 🧱 Rotas protegidas (server e client)  
- 🗂 Integração com Prisma via Adaptador oficial  
- ⚡ Tipagem automática no client e no server  

---

---

## ⚙️ Configuração do Better Auth (Server)

```ts
import { betterAuth } from "better-auth";
import { prisma } from "./prisma";
import { prismaAdapter } from "better-auth/adapters/prisma";

export const auth = betterAuth({
  database: prismaAdapter(prisma, {
    provider: "postgresql",
  }),
});

💻 Configuração do Auth Client (Client)
import { createAuthClient } from "better-auth/client";

export const authClient = createAuthClient({
  baseURL: "http://localhost:3000",
});

🗄️ Banco de Dados (Prisma)

Antes de rodar o projeto, gere as tabelas:

npx prisma generate
npx prisma db push


▶️ Como Rodar o Projeto

Clone o repositório:

git clone https://github.com/ismaeloliveira-projetos/Autentica-o-Moderna-com-Better-Auth-Next.js-Prisma-.git


Instale as dependências:

npm install
# ou yarn install


Configure o .env:

DATABASE_URL="sua_url_do_postgres"


Rodar o projeto:

npm run dev

🚀 Como Usar

Acesse /api/auth para visualizar as rotas de autenticação.

Utilize authClient no front para login, logout e criação de usuários.

Use auth no server para proteger páginas ou recuperar sessões.

📘 Objetivo do Projeto

Este repositório foi criado para servir como base de estudos e implementação prática de autenticação moderna, tipada e segura.
Ideal para quem quer aprender:

Autenticação com Next.js 14

Prisma ORM

Better Auth

Arquitetura de autenticação server-first

📄 Licença

Projeto livre para estudos e uso pessoal.
