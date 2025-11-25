<p align="center">
  <img width="120" src="/readme-assets/logo-circle.png" alt="E2B Logo">
</p>

<h1 align="center">E2B Dashboard</h1>

<p align="center">
  <strong>Painel de controle moderno para gerenciar sandboxes, templates e recursos da plataforma E2B</strong>
</p>

<p align="center">
  <a href="https://e2b.dev">Website</a> •
  <a href="https://e2b.dev/docs">Documentacao</a> •
  <a href="https://discord.gg/e2b">Discord</a> •
  <a href="#-inicio-rapido">Inicio Rapido</a> •
  <a href="./README-en.md">English</a>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/licen%C3%A7a-Apache--2.0-blue.svg" alt="Licenca"></a>
  <a href="https://discord.com/channels/1092455714431180995"><img src="https://img.shields.io/discord/1092455714431180995?color=7289DA&label=Discord&logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://github.com/e2b-dev/dashboard"><img src="https://img.shields.io/github/stars/e2b-dev/dashboard?style=social" alt="GitHub Stars"></a>
  <img src="https://img.shields.io/badge/Next.js-16-black?logo=next.js" alt="Next.js">
  <img src="https://img.shields.io/badge/React-19-61DAFB?logo=react" alt="React">
  <img src="https://img.shields.io/badge/TypeScript-5.7-3178C6?logo=typescript" alt="TypeScript">
</p>

---

![Dashboard Preview Dark](/readme-assets/dashboard-preview-dark.png#gh-dark-mode-only)
![Dashboard Preview Light](/readme-assets/dashboard-preview-light.png#gh-light-mode-only)

---

## Indice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Stack Tecnologico](#-stack-tecnologico)
- [Arquitetura](#-arquitetura)
- [Inicio Rapido](#-inicio-rapido)
- [Configuracao de Servicos](#-configuracao-de-servicos)
- [Scripts Disponiveis](#-scripts-disponiveis)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Testes](#-testes)
- [Deploy em Producao](#-deploy-em-producao)
- [Variaveis de Ambiente](#-variaveis-de-ambiente)
- [Solucao de Problemas](#-solucao-de-problemas)
- [Contribuindo](#-contribuindo)
- [Suporte](#-suporte)
- [Licenca](#-licenca)

---

## Sobre o Projeto

O **E2B Dashboard** e o painel de controle oficial da plataforma E2B, uma solucao de infraestrutura que permite executar codigo de forma segura em sandboxes isolados na nuvem. Este dashboard oferece uma interface moderna e intuitiva para:

- **Gerenciar Sandboxes**: Visualize, monitore e controle seus ambientes de execucao em tempo real
- **Administrar Templates**: Crie e gerencie templates customizados para seus sandboxes
- **Controlar Chaves de API**: Gere e gerencie suas credenciais de acesso de forma segura
- **Monitorar Uso**: Acompanhe metricas de utilizacao, custos e performance
- **Gerenciar Times**: Convide membros, defina permissoes e colabore em equipe
- **Configurar Webhooks**: Integre com sistemas externos atraves de eventos
- **Controlar Faturamento**: Visualize faturas, configure limites e gerencie planos

### Por que usar o E2B Dashboard?

| Beneficio | Descricao |
|-----------|-----------|
| **Interface Intuitiva** | Design moderno com suporte a tema claro/escuro |
| **Tempo Real** | Monitoramento ao vivo de sandboxes e metricas |
| **Seguranca** | Autenticacao robusta com Supabase e multiplos providers |
| **Performance** | Construido com as tecnologias mais modernas do ecossistema React |
| **Extensivel** | Arquitetura modular facilmente customizavel |
| **Open Source** | Codigo aberto sob licenca Apache 2.0 |

---

## Funcionalidades

### Gerenciamento de Sandboxes
- Listagem em tempo real de todos os sandboxes ativos
- Visualizacao detalhada com logs e metricas
- Monitoramento de recursos (CPU, memoria, rede)
- Acoes rapidas: pausar, retomar, encerrar

### Templates
- Biblioteca de templates pre-configurados
- Criacao de templates customizados
- Versionamento e historico de alteracoes
- Compartilhamento entre membros do time

### Chaves de API
- Geracao segura de chaves
- Rotacao automatica
- Permissoes granulares
- Historico de uso por chave

### Analytics e Uso
- Graficos interativos de consumo
- Filtros por periodo, template e sandbox
- Exportacao de relatorios
- Alertas de limites

### Gerenciamento de Times
- Convites por email
- Niveis de permissao (Admin, Membro)
- Auditoria de acoes
- Configuracoes por time

### Faturamento
- Integracao com Stripe
- Historico de faturas
- Configuracao de limites de gasto
- Multiplos metodos de pagamento

### Webhooks
- Configuracao de endpoints
- Eventos disponiveis: sandbox criado, encerrado, erro
- Logs de entregas
- Retry automatico

---

## Stack Tecnologico

### Frontend

| Tecnologia | Versao | Descricao |
|------------|--------|-----------|
| [Next.js](https://nextjs.org/) | 16 | Framework React com App Router e Turbopack |
| [React](https://react.dev/) | 19 | Biblioteca UI com React Compiler |
| [TypeScript](https://www.typescriptlang.org/) | 5.7 | Tipagem estatica |
| [Tailwind CSS](https://tailwindcss.com/) | 4.0 | Framework CSS utility-first |
| [Radix UI](https://www.radix-ui.com/) | - | Componentes acessiveis e sem estilo |
| [shadcn/ui](https://ui.shadcn.com/) | - | Componentes reutilizaveis |
| [Lucide](https://lucide.dev/) | - | Icones consistentes |
| [Motion](https://motion.dev/) | 12 | Animacoes fluidas |
| [ECharts](https://echarts.apache.org/) | 6 | Graficos interativos |
| [Recharts](https://recharts.org/) | 2.15 | Graficos React |

### Backend & APIs

| Tecnologia | Descricao |
|------------|-----------|
| [tRPC](https://trpc.io/) | APIs tipadas end-to-end |
| [TanStack Query](https://tanstack.com/query) | Gerenciamento de estado do servidor |
| [next-safe-action](https://next-safe-action.dev/) | Server Actions tipadas e seguras |
| [Zod](https://zod.dev/) | Validacao de schemas |
| [OpenAPI](https://www.openapis.org/) | Especificacoes de API |

### Banco de Dados & Auth

| Tecnologia | Descricao |
|------------|-----------|
| [Supabase](https://supabase.com/) | Backend-as-a-Service (PostgreSQL + Auth) |
| [Postgres](https://www.postgresql.org/) | Banco de dados relacional |
| [Vercel KV](https://vercel.com/docs/storage/vercel-kv) | Cache Redis-compatible |

### Pagamentos & Analytics

| Tecnologia | Descricao |
|------------|-----------|
| [Stripe](https://stripe.com/) | Processamento de pagamentos |
| [PostHog](https://posthog.com/) | Product analytics |
| [Vercel Analytics](https://vercel.com/analytics) | Web analytics |
| [OpenTelemetry](https://opentelemetry.io/) | Observabilidade distribuida |

### Ferramentas de Desenvolvimento

| Tecnologia | Descricao |
|------------|-----------|
| [Bun](https://bun.sh/) | Runtime JavaScript e gerenciador de pacotes |
| [Vitest](https://vitest.dev/) | Framework de testes |
| [ESLint](https://eslint.org/) | Linting de codigo |
| [Prettier](https://prettier.io/) | Formatacao de codigo |
| [pino](https://getpino.io/) | Logging estruturado |

---

## Arquitetura

```
┌─────────────────────────────────────────────────────────────────┐
│                         CLIENTE                                  │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐              │
│  │   Next.js   │  │    React    │  │  TanStack   │              │
│  │  App Router │  │     19      │  │    Query    │              │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘              │
└─────────┼────────────────┼────────────────┼─────────────────────┘
          │                │                │
          ▼                ▼                ▼
┌─────────────────────────────────────────────────────────────────┐
│                      CAMADA DE API                               │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐              │
│  │    tRPC     │  │   Server    │  │   Route     │              │
│  │   Router    │  │   Actions   │  │  Handlers   │              │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘              │
└─────────┼────────────────┼────────────────┼─────────────────────┘
          │                │                │
          ▼                ▼                ▼
┌─────────────────────────────────────────────────────────────────┐
│                    SERVICOS EXTERNOS                             │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐            │
│  │Supabase │  │ Stripe  │  │  E2B    │  │ PostHog │            │
│  │  Auth   │  │Payments │  │  Infra  │  │Analytics│            │
│  └─────────┘  └─────────┘  └─────────┘  └─────────┘            │
└─────────────────────────────────────────────────────────────────┘
```

### Fluxo de Dados

1. **Requisicao do Usuario** → Componentes React fazem requisicoes via tRPC ou Server Actions
2. **Validacao** → Zod valida todos os inputs antes do processamento
3. **Autenticacao** → Supabase verifica a sessao do usuario
4. **Processamento** → Logica de negocios executa no servidor
5. **Resposta** → Dados tipados retornam para o cliente
6. **Cache** → TanStack Query gerencia cache e invalidacao

---

## Inicio Rapido

### Pre-requisitos

Antes de comecar, certifique-se de ter instalado:

| Requisito | Versao Minima | Verificar |
|-----------|---------------|-----------|
| Node.js | 18+ | `node --version` |
| Bun (recomendado) | 1.2+ | `bun --version` |
| Git | 2.0+ | `git --version` |

### Contas Necessarias

- [Supabase](https://supabase.com/) - Banco de dados e autenticacao
- [Vercel](https://vercel.com/) (opcional) - Deploy e KV Storage
- [PostHog](https://posthog.com/) (opcional) - Analytics
- [Stripe](https://stripe.com/) (opcional) - Pagamentos

> **Nota sobre Self-Hosting**: Se voce planeja hospedar este dashboard por conta propria, provavelmente vai querer primeiro hospedar nossa infraestrutura. Consulte nosso [repositorio de infraestrutura](https://github.com/e2b-dev/infra) para orientacoes sobre como configurar a plataforma E2B em sua propria infraestrutura.

### Instalacao

```bash
# 1. Clone o repositorio
git clone https://github.com/e2b-dev/dashboard.git
cd dashboard

# 2. Instale as dependencias
bun install
# ou com npm
npm install --legacy-peer-deps

# 3. Copie o arquivo de ambiente
cp .env.example .env.local

# 4. Configure as variaveis de ambiente (veja secao abaixo)

# 5. Inicie o servidor de desenvolvimento
bun run dev
```

A aplicacao estara disponivel em `http://localhost:3000`

---

## Configuracao de Servicos

### 1. Key-Value Store (Redis)

O projeto requer um store key-value compativel com Redis para cache e sessoes.

#### Opcao A: Vercel KV (Recomendado para producao)

1. Acesse o painel do Vercel
2. Va em Storage → Create Database → KV
3. As variaveis serao configuradas automaticamente

#### Opcao B: Redis Self-Hosted

Configure as seguintes variaveis no `.env.local`:

```env
KV_URL=redis://localhost:6379
KV_REST_API_URL=http://localhost:8079
KV_REST_API_TOKEN=seu_token_de_escrita
KV_REST_API_READ_ONLY_TOKEN=seu_token_de_leitura
```

### 2. Supabase

#### 2.1 Criar Projeto

1. Acesse [supabase.com](https://supabase.com) e crie um novo projeto
2. Anote a `URL do projeto` e as chaves de API

#### 2.2 Configurar Variaveis

```env
NEXT_PUBLIC_SUPABASE_URL=https://seu-projeto.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=sua_anon_key
SUPABASE_SERVICE_ROLE_KEY=sua_service_role_key
```

#### 2.3 Configurar Autenticacao

1. Va em **Authentication → URL Configuration**
2. Configure:
   - **Site URL**: URL do seu dashboard (ex: `https://dashboard.seudominio.com`)
   - **Redirect URLs**: Adicione `http://localhost:3000/**` para desenvolvimento

3. Va em **Authentication → Providers**
4. Habilite os providers desejados:
   - **Email**: Ative para login com email/senha
   - **GitHub**: Configure com OAuth App do GitHub
   - **Google**: Configure com credenciais do Google Cloud

#### 2.4 Configurar Templates de Email

Va em **Authentication → Templates** e atualize os URLs:

**Reset Password:**
```
{{ .SiteURL }}/api/auth/confirm?token_hash={{ .TokenHash }}&type=recovery&next={{ .RedirectTo }}&confirmation_url={{ .ConfirmationURL }}
```

**Confirm Sign-Up:**
```
{{ .SiteURL }}/api/auth/confirm?token_hash={{ .TokenHash }}&type=email&next={{ .RedirectTo }}&confirmation_url={{ .ConfirmationURL }}
```

#### 2.5 Executar Migrations

As migrations estao na pasta `/migrations`. Execute em ordem:

```bash
# Usando o script do projeto
bun run db:migrations:apply

# Ou manualmente no SQL Editor do Supabase
# Execute cada arquivo .sql em ordem cronologica
```

#### 2.6 Configurar Storage

1. Va em **Storage → Buckets**
2. Crie um novo bucket **publico** chamado `profile-pictures`

### 3. Stripe (Opcional)

Para habilitar pagamentos:

```env
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_...
```

### 4. PostHog (Opcional)

Para analytics:

```env
NEXT_PUBLIC_POSTHOG_KEY=phc_...
NEXT_PUBLIC_POSTHOG_HOST=https://app.posthog.com
```

---

## Scripts Disponiveis

### Desenvolvimento

| Comando | Descricao |
|---------|-----------|
| `bun run dev` | Inicia servidor de desenvolvimento com Turbopack |
| `bun run build` | Cria build de producao |
| `bun run start` | Inicia servidor de producao |
| `bun run preview` | Build + inicia servidor de producao |
| `bun run clean` | Remove .next e node_modules, reinstala deps |

### Qualidade de Codigo

| Comando | Descricao |
|---------|-----------|
| `bun run lint` | Executa ESLint |
| `bun run lint:fix` | Corrige problemas automaticamente |
| `bun run format` | Formata codigo com Prettier |

### Banco de Dados

| Comando | Descricao |
|---------|-----------|
| `bun run db:migrations:create` | Cria nova migration |
| `bun run db:migrations:apply` | Aplica migrations pendentes |

### Geracao de Tipos

| Comando | Descricao |
|---------|-----------|
| `bun run generate:supabase` | Gera tipos do banco de dados |
| `bun run generate:infra` | Gera tipos da API de infraestrutura |
| `bun run generate:argus` | Gera tipos da API Argus |

### Testes

| Comando | Descricao |
|---------|-----------|
| `bun run test:run` | Executa todos os testes |
| `bun run test:unit` | Executa apenas testes unitarios |
| `bun run test:integration` | Executa apenas testes de integracao |
| `bun run test:e2e` | Executa testes end-to-end |
| `bun run test:watch` | Modo watch para desenvolvimento |
| `bun run test:ui` | Interface grafica do Vitest |

---

## Estrutura do Projeto

```
dashboard/
├── migrations/              # Migrations SQL do banco de dados
├── readme-assets/           # Imagens do README
├── scripts/                 # Scripts de automacao
├── spec/                    # Especificacoes OpenAPI
├── src/
│   ├── app/                 # Next.js App Router
│   │   ├── (auth)/          # Rotas de autenticacao
│   │   │   ├── sign-in/     # Pagina de login
│   │   │   ├── sign-up/     # Pagina de cadastro
│   │   │   └── forgot-password/
│   │   ├── (rewrites)/      # Rewrites e redirects
│   │   ├── api/             # API Routes
│   │   └── dashboard/       # Area autenticada
│   │       └── [teamIdOrSlug]/
│   │           ├── sandboxes/   # Gerenciamento de sandboxes
│   │           ├── templates/   # Gerenciamento de templates
│   │           ├── keys/        # Chaves de API
│   │           ├── usage/       # Analytics de uso
│   │           ├── billing/     # Faturamento
│   │           ├── budget/      # Limites de gasto
│   │           ├── members/     # Membros do time
│   │           ├── webhooks/    # Configuracao de webhooks
│   │           ├── general/     # Configuracoes gerais
│   │           └── account/     # Configuracoes da conta
│   ├── features/            # Componentes por funcionalidade
│   │   ├── dashboard/       # Features do dashboard
│   │   │   ├── sandboxes/   # Componentes de sandboxes
│   │   │   ├── templates/   # Componentes de templates
│   │   │   ├── usage/       # Graficos e metricas
│   │   │   └── sidebar/     # Navegacao lateral
│   │   └── ...
│   ├── ui/                  # Componentes de UI reutilizaveis
│   │   ├── primitives/      # Componentes base (Button, Input, etc)
│   │   └── ...
│   ├── lib/                 # Utilitarios e logica compartilhada
│   │   ├── env.ts           # Validacao de variaveis de ambiente
│   │   └── ...
│   ├── server/              # Logica exclusiva do servidor
│   │   ├── trpc/            # Configuracao tRPC
│   │   └── actions/         # Server Actions
│   ├── styles/              # Estilos globais
│   ├── types/               # Definicoes de tipos TypeScript
│   └── __test__/            # Testes
│       ├── unit/            # Testes unitarios
│       ├── integration/     # Testes de integracao
│       ├── e2e/             # Testes end-to-end
│       └── development/     # Testes de desenvolvimento
├── .env.example             # Exemplo de variaveis de ambiente
├── next.config.mjs          # Configuracao do Next.js
├── tailwind.config.ts       # Configuracao do Tailwind
├── tsconfig.json            # Configuracao do TypeScript
└── vitest.config.ts         # Configuracao do Vitest
```

---

## Testes

O projeto utiliza uma estrategia de testes abrangente com Vitest.

### Tipos de Testes

#### Testes Unitarios
Testam funcoes, componentes e modulos isoladamente.

```bash
bun run test:unit
```

**Localizacao:** `src/__test__/unit/`

#### Testes de Integracao
Verificam se diferentes partes da aplicacao funcionam juntas.

```bash
bun run test:integration
```

**Localizacao:** `src/__test__/integration/`

#### Testes End-to-End
Testam fluxos completos do usuario.

```bash
bun run test:e2e
```

**Localizacao:** `src/__test__/e2e/`

### Interface Grafica

Execute os testes com interface visual:

```bash
bun run test:ui
```

### Cobertura

Para gerar relatorio de cobertura:

```bash
bun run test:run --coverage
```

Para mais detalhes sobre a estrategia de testes, consulte o [README de Testes](src/__test__/README.md).

---

## Deploy em Producao

### Vercel (Recomendado)

A aplicacao esta otimizada para deploy na Vercel:

1. Faca push do codigo para o GitHub
2. Importe o repositorio na Vercel
3. Configure as variaveis de ambiente
4. Deploy!

> **Nota**: A aplicacao utiliza Partial Prerendering (PPR) que atualmente so e suportado na infraestrutura da Vercel. Para desabilitar, edite `next.config.mjs`.

### Outras Plataformas

Para deploy em outras plataformas:

1. Desabilite PPR em `next.config.mjs`:
```js
experimental: {
  ppr: false,
}
```

2. Configure um Redis externo para KV storage
3. Configure as variaveis de ambiente da plataforma
4. Execute `bun run build && bun run start`

---

## Variaveis de Ambiente

Todas as variaveis de ambiente estao validadas em [`src/lib/env.ts`](./src/lib/env.ts).

### Variaveis Obrigatorias

| Variavel | Descricao |
|----------|-----------|
| `NEXT_PUBLIC_SUPABASE_URL` | URL do projeto Supabase |
| `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Chave anonima do Supabase |
| `SUPABASE_SERVICE_ROLE_KEY` | Chave de servico do Supabase |
| `KV_URL` | URL de conexao Redis |
| `KV_REST_API_URL` | URL da API REST do KV |
| `KV_REST_API_TOKEN` | Token de escrita do KV |
| `KV_REST_API_READ_ONLY_TOKEN` | Token de leitura do KV |

### Variaveis Opcionais

| Variavel | Descricao |
|----------|-----------|
| `STRIPE_SECRET_KEY` | Chave secreta do Stripe |
| `STRIPE_WEBHOOK_SECRET` | Secret do webhook Stripe |
| `NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY` | Chave publica do Stripe |
| `NEXT_PUBLIC_POSTHOG_KEY` | Chave do PostHog |
| `NEXT_PUBLIC_POSTHOG_HOST` | Host do PostHog |

---

## Solucao de Problemas

### Erro: "Missing environment variables"

**Causa**: Variaveis de ambiente nao configuradas.

**Solucao**:
1. Verifique se `.env.local` existe
2. Confirme que todas as variaveis obrigatorias estao preenchidas
3. Reinicie o servidor de desenvolvimento

### Erro: "Supabase connection failed"

**Causa**: Credenciais do Supabase invalidas ou projeto pausado.

**Solucao**:
1. Verifique as chaves no painel do Supabase
2. Confirme que o projeto esta ativo
3. Verifique se as URLs estao corretas

### Erro: "KV connection refused"

**Causa**: Redis nao esta rodando ou credenciais invalidas.

**Solucao**:
1. Para desenvolvimento local, inicie um Redis: `docker run -p 6379:6379 redis`
2. Verifique as credenciais do KV
3. Para Vercel KV, verifique a integracao no painel

### Build falha com "Type errors"

**Causa**: Tipos desatualizados ou incorretos.

**Solucao**:
```bash
# Regenere os tipos
bun run generate:supabase
bun run generate:infra

# Limpe e reinstale
bun run clean
```

### Pagina em branco apos login

**Causa**: Configuracao de redirect incorreta no Supabase.

**Solucao**:
1. Verifique Site URL em Authentication → URL Configuration
2. Adicione todos os URLs de redirect necessarios
3. Verifique os templates de email

---

## Contribuindo

Contribuicoes sao bem-vindas! Veja nosso [Guia de Contribuicao](CONTRIBUTING.md) para mais detalhes.

### Como Contribuir

1. Faca um fork do repositorio
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Faca commit das suas alteracoes (`git commit -m 'feat: adiciona nova feature'`)
4. Faca push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

### Padroes de Codigo

- Use TypeScript para todo codigo novo
- Siga o estilo do ESLint e Prettier configurados
- Escreva testes para novas funcionalidades
- Atualize a documentacao quando necessario

---

## Suporte

Precisa de ajuda? Temos varias opcoes:

| Canal | Descricao | Link |
|-------|-----------|------|
| Documentacao | Guias e referencias | [e2b.dev/docs](https://e2b.dev/docs) |
| Discord | Comunidade e suporte | [discord.gg/e2b](https://discord.gg/e2b) |
| Issues | Reportar bugs | [GitHub Issues](https://github.com/e2b-dev/dashboard/issues) |
| Discussions | Perguntas e ideias | [GitHub Discussions](https://github.com/e2b-dev/dashboard/discussions) |

---

## Licenca

Este projeto esta licenciado sob a Licenca Apache 2.0 - veja o arquivo [LICENSE](LICENSE) para detalhes.

```
Copyright 2025 FoundryLabs, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

<p align="center">
  Feito com <3 pela equipe <a href="https://e2b.dev">E2B</a>
</p>

<p align="center">
  <a href="https://e2b.dev">Website</a> •
  <a href="https://twitter.com/e2aboratories">Twitter</a> •
  <a href="https://discord.gg/e2b">Discord</a> •
  <a href="https://github.com/e2b-dev">GitHub</a>
</p>
