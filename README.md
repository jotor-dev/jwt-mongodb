# JWT MongoDB Auth API 🔐

Uma API RESTful desenvolvida com **Node.js**, **TypeScript** e **MongoDB** para autenticação de usuários usando **JSON Web Tokens (JWT)**.

## 🚀 Funcionalidades

- **Registro de Usuários**: Criação de novos usuários com armazenamento seguro.
- **Login**: Autenticação e geração de tokens JWT.
- **Proteção de Rotas**: Middleware de validação para acesso a recursos privados.
- **TypeScript**: Tipagem estática para maior segurança e produtividade.
- **Banco de Dados**: Conexão robusta com MongoDB via Mongoose.

## 🛠️ Tecnologias Utilizadas

- **Runtime**: [Node.js](https://nodejs.org/) v22+
- **Linguagem**: [TypeScript](https://www.typescriptlang.org/)
- **Framework**: [Express](https://expressjs.com/)
- **ORM/ODM**: [Mongoose](https://mongoosejs.com/)
- **Segurança**: [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken) e [bcryptjs](https://github.com/dcodeIO/bcrypt.js)
- **Ferramentas**: [ts-node-dev](https://github.com/wclr/ts-node-dev) (auto-reload)

## 📋 Pré-requisitos

- [Node.js](https://nodejs.org/) instalado.
- [MongoDB](https://www.mongodb.com/) rodando (local ou Atlas).

## 🔧 Configuração e Instalação

1. **Clone o repositório:**
```bash
   git clone [https://github.com/jotor-dev/jwt-mongodb.git](https://github.com/jotor-dev/jwt-mongodb.git)
   cd jwt-mongodb
```

2. **Instale as dependências:**
```bash
npm install

```

3. **Variáveis de Ambiente:**
Configure um arquivo `.env` (já existe) na raiz do projeto:
```env
PORT=3000
MONGO_URI=sua_string_de_conexao_mongodb
JWT_SECRET=sua_chave_secreta_aqui

```

4. **Execução:**
```bash
# Modo de desenvolvimento (com auto-reload)
npm run dev

```

## 🛣️ Rotas Principais

A API está estruturada sob os seguintes prefixos:

| Método | Rota | Descrição | Acesso |
| --- | --- | --- | --- |
| **POST** | `/auth/register` | Registro de novo usuário | Público |
| **POST** | `/auth/login` | Login e emissão de Token | Público |
| **GET** | `/user/profile` | Acesso ao perfil do usuário | Privado (JWT) |

> **Nota:** Para rotas privadas, envie o token no Header: `Authorization: Bearer <seu_token>`

## 📁 Estrutura de Arquivos (Resumo)

* `src/server.ts`: Ponto de entrada e conexão com banco de dados.
* `src/auth.ts`: Definição das rotas de autenticação.
* `src/user.ts`: Definição das rotas de usuário.
