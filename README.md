# digitaelio

# Etapa 1

## Passo 1

node -v

npm -v

npx -v

git init

## Passo 2

npx @nestjs/cli@latest new backend --package-manager npm --skip-install

cd backend

rm -rf .git

npm install
npm run start:dev

git add .
git commit -m "chore(backend): inicializa backend NestJS"

## Passo 3

npm install @nestjs/config class-validator class-transformer

[.env.example](backend/.env.example)

[env.validation.ts](backend/config/env.validation.ts)

[app.module.ts](backend/src/app.module.ts)

git add .
git commit -m "chore(backend): adiciona configuracao inicial do projeto"

## Passo 4

npm install @nestjs/typeorm typeorm mysql2

# Stack

Backend:
- NestJS
- TypeScript
- TypeORM
- MySQL
- JWT
- bcrypt
- Passport

Infra:
- Git
- npm

# Roteiro

🧭 VISÃO GERAL DO PROJETO

Você está construindo:

👉 SaaS de Cardápio Digital (multiempresa)

🪜 ROADMAP MACRO (ordem ideal)
🧱 1. Fundação do Projeto (Base Técnica)

Aqui você prepara o terreno.

Backend
Criar projeto (Node.js + Express ou NestJS)
Configurar banco (PostgreSQL)
ORM (Prisma ou TypeORM)
Estrutura de pastas
Frontend
Criar projeto (React + Vite ou Next.js)
Configurar UI (Chakra UI)
Estrutura de rotas

📌 Objetivo: projeto rodando + estrutura limpa

🔐 2. Autenticação e Empresas

Sistema de contas (core do sistema)

Backend
Cadastro de empresa
Login (JWT)
Hash de senha
Validação de CPF/CNPJ
Frontend
Tela de cadastro
Tela de login
Armazenamento do token

📌 Objetivo: empresa consegue entrar no sistema

🏢 3. Multiempresa (Regra de Negócio)

Garantir isolamento dos dados

Backend
Middleware de autenticação
Injetar empresa_id em todas as requisições
Filtrar queries por empresa
Frontend
Contexto global (AuthContext)
Controle de sessão

📌 Objetivo: uma empresa não acessa dados da outra

🍽️ 4. Cardápio (CRUD principal)

Aqui nasce o produto de verdade

Backend
CRUD de cardápio
CRUD de categorias
CRUD de produtos
Frontend
Tela de dashboard
Criar/editar produtos
Listagem de itens

📌 Objetivo: empresa monta seu cardápio

🖼️ 5. Upload de imagens

Essencial para UX

Backend
Integração com Cloudinary ou S3
Frontend
Upload de imagem no produto

📌 Objetivo: produtos com foto

🌐 6. Cardápio público

Parte que o cliente final vê

Backend
Endpoint público (sem login)
Buscar cardápio por empresa
Frontend
Página pública
Listagem de produtos
UI amigável

📌 Exemplo de rota:

/cardapio/:empresaId

📌 Objetivo: cliente visualiza o cardápio

📱 7. Melhorias de UX

Deixar profissional

Responsivo (mobile first)
Loading states
Mensagens de erro
Skeletons
📊 8. Funcionalidades extras (diferencial)

Aqui vira produto de mercado

Ativar/desativar produtos
Horário de funcionamento
Link WhatsApp
Ordenação de itens
Destaques
💳 9. Monetização (SaaS real)

Opcional, mas avançado

Plano gratuito vs pago
Integração com pagamento (Stripe, etc.)
Limites por plano
🚀 10. Deploy e produção

Colocar no ar

Frontend
Vercel
Backend
Railway / Render
Banco
PostgreSQL (Railway/Supabase)
🧩 DIVISÃO CLARA: BACKEND vs FRONTEND
🔵 Backend (Responsabilidades)
Regras de negócio
Segurança
Autenticação
Banco de dados
APIs

👉 Ele manda no sistema

🟣 Frontend (Responsabilidades)
Interface
Experiência do usuário
Consumo da API
Estado da aplicação

👉 Ele mostra o sistema

📌 ORDEM RECOMENDADA (MUITO IMPORTANTE)

Não faça tudo ao mesmo tempo.

👉 Siga essa ordem:

Backend (auth + empresa)
Backend (CRUD produtos)
Frontend (login + dashboard)
Frontend (CRUD)
Página pública
🧠 VISÃO DE SENIOR (DICA DE OURO)

Divida sempre em:

Core (obrigatório)
Nice-to-have (depois)
Core:
Login
CRUD produtos
Cardápio público
Depois:
Imagem
Plano pago
Analytics
🗂️ Exemplo de organização (monorepo)
/projeto
  /backend
  /frontend
🔥 Próximo passo ideal

Se quiser seguir comigo passo a passo, podemos começar já:

👉 Etapa 1: Setup do Backend (estrutura profissional)
ou
👉 Etapa 1: Modelagem do banco (Prisma)

Só me fala:
👉 quer começar pelo backend na prática?