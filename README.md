# 🧑‍🔧 Agente Busca — Super App de Serviços

O **Agente Busca** é um super aplicativo projetado para conectar **clientes** a **prestadores de serviço** de forma rápida, inteligente e intuitiva.  
A plataforma permite criar pedidos, receber orçamentos gratuitos, comparar propostas, acompanhar o serviço e avaliar o profissional — tudo dentro do app.

Inspirado em modelos como **OLX**, **GetNinjas** e **Uber**, o Agente Busca traz:
- fluxo completo de orçamento → proposta → execução → finalização  
- ranking de prestadores baseado em desempenho  
- categorias organizadas  
- experiência simples e visual  

---

## 🚀 Status do Projeto
**Sprint Atual:** _Preparação do backend (Prisma + Auth + Categorias)_  
**Progresso:** Ambiente configurado · GitHub OK · Monorepo ativo · Copilot integrado

---

## ✨ Funcionalidades do MVP

### 👤 Cliente
- Cadastro e login  
- Criar pedidos com descrição e fotos  
- Receber **pré-orçamentos gratuitos**  
- Receber propostas detalhadas dos prestadores  
- Acompanhar o andamento do serviço  
- Avaliar prestador e serviço

### 👨‍🔧 Prestador
- Cadastro com categorias e raio de atendimento  
- Receber pedidos compatíveis  
- Enviar pré-orçamento estilo "Tinder" (aceitar/pular)  
- Enviar propostas completas  
- Receber avaliações e subir no ranking  

### 🧠 Sistema
- Ranking de prestadores por desempenho  
- Categorias estilo OLX  
- Fluxo completo: **requested → matched → scheduled → in_progress → delivered → completed**  
- Chat simples entre cliente e prestador (MVP)  
- Histórico de serviços  
- Autenticação moderna com tokens  

---

## 🛠️ Tecnologias Utilizadas

### **Backend**
- **AdonisJS 6**  
- **Prisma ORM**  
- **PostgreSQL**  
- Autenticação com Tokens  
- Validação com Zod  
- MVC + Services  

### **Frontend Web**
- **Next.js 15**  
- TailwindCSS  
- TanStack Query  
- shadcn/UI  

### **Mobile (Futuro MVP)**
- Expo / React Native  
- Expo Router  
- TanStack Query  

### **Infra & DevOps**
- Turborepo (monorepo)  
- pnpm  
- Docker (PostgreSQL e serviços)  
- GitHub Actions  
- SSH Keys + Versionamento  

---

## 🧱 Arquitetura do Projeto

agente-busca/
├── apps/
│ ├── api/ → Backend AdonisJS
│ └── web/ → Frontend Next.js
├── packages/
│ ├── ui/ → Componentes compartilhados
│ ├── types/ → Tipos compartilhados
│ └── config/ → ESLint, Tailwind, TS configs
├── infra/
│ └── docker/ → Banco, redis (futuro)
├── turbo.json → Configuração Turborepo
└── README.md

yaml
Copiar código

---

## 🗂️ Categorias do Sistema (versão inicial)

- 🏗️ Construção e Reforma  
- 🔌 Eletrônicos e TI  
- 🧹 Casa e Serviços Gerais  
- 💅 Beleza e Saúde  
- 🚗 Automotivo  
- 🎉 Eventos  
- 🐕 Pets  
- 📚 Aulas e Consultorias  
- 🔧 Outros  

---

# 📅 Roadmap Oficial (Sprints)

## **Sprint 0 — OK**  
✔️ Ambiente Linux + VSCode  
✔️ Git + SSH + GitHub  
✔️ Turborepo configurado  
✔️ API e Web rodando  
✔️ Copilot funcionando

---

## **Sprint 1 — Backend Base (Semana Atual)**  
🔸 PostgreSQL + Prisma  
🔸 Schema inicial: User e Category  
🔸 Migrations  
🔸 Auth (registro + login)  
🔸 Seeds de categorias  

---

## **Sprint 2 — Pedidos**  
🔸 Criar pedidos  
🔸 Upload de imagens  
🔸 Listagens do cliente  
🔸 Filtros básicos  

---

## **Sprint 3 — Prestadores & Pré-Orçamentos**  
🔸 Onboarding do prestador  
🔸 Configurar categorias e raio  
🔸 Tela estilo "Tinder" para pré-orçamentos  
🔸 Envio de pré-orçamento  

---

## **Sprint 4 — Propostas & Jobs**  
🔸 Envio de proposta completa  
🔸 Aceite do cliente  
🔸 Criação do job  
🔸 Mudança de status (workflow)

---

## **Sprint 5 — Chat & Acompanhamento**  
🔸 Chat básico cliente ↔ prestador  
🔸 Histórico  
🔸 Notificações locais (MVP)

---

## **Sprint 6 — Avaliações & Ranking**  
🔸 Avaliação do prestador  
🔸 Ranking global  
🔸 Ordenação por score

---

## **Sprint 7 — Deploy**  
🔸 API na Railway/Fly.io  
🔸 Web na Vercel  
🔸 Banco na Neon  
🔸 Variáveis de ambiente  
🔸 Testes finais

---

# ▶️ Como Rodar Localmente

### 1️⃣ Instalar dependências
```bash
pnpm install
2️⃣ Rodar API
bash
Copiar código
cd apps/api
pnpm dev
3️⃣ Rodar Web
bash
Copiar código
cd apps/web
pnpm dev
4️⃣ Configurar Banco
Criar arquivo .env na pasta api:

ini
Copiar código
DATABASE_URL="postgresql://postgres:postgres@localhost:5432/agente_busca"
Rodar migração:

bash
Copiar código
pnpm dlx prisma migrate dev
🤝 Contribuindo
Contribuições são bem-vindas!

Fork o repositório

Crie uma branch: feature/minha-ideia

Commit suas mudanças

Abra um Pull Request

📜 Licença
Este projeto está sob a licença MIT — uso livre para estudo e evolução da comunidade.

⭐ Apoie o Projeto
Se gostou da ideia, deixe uma ⭐ no repositório e acompanhe as próximas sprints!

md
Copiar código
Desenvolvido com ❤️ por Roger Reis (@rogerreistec)
yaml
Copiar código
