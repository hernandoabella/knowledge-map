# 🗂️ Quick Decision Guide

> Fast answers for the most common architectural trade-off questions.

---

## 🗄️ What database should I use?

| Use case | Pick |
|----------|------|
| Default relational needs | **PostgreSQL** |
| Serverless / auto-scale | **Neon** or **PlanetScale** |
| Caching / sessions / pub-sub | **Redis** |
| Full-text search | **Elasticsearch** or **Typesense** |
| Massive write throughput | **Cassandra** |
| Document / flexible schema | **MongoDB** |
| Vector similarity / semantic search | **pgvector** or **Pinecone** |
| Analytics / OLAP | **DuckDB** (local) or **BigQuery** (cloud) |
| Graph / highly connected data | **Neo4j** |
| Time-series / metrics / IoT | **InfluxDB** or **TimescaleDB** |
| Files, blobs, media | **S3** or **GCS** |

---

## 🔐 What should I use for auth?

| Situation | Pick |
|-----------|------|
| Next.js app | **Auth.js (NextAuth)** |
| Need UI components + session management | **Clerk** |
| Enterprise / SSO / SAML / SCIM | **Auth0** |
| Simple JWT with full control | **jsonwebtoken** + **bcrypt** DIY |
| Supabase project | **Supabase Auth** |
| Firebase project | **Firebase Auth** |

---

## 🚀 What backend framework should I use?

| Situation | Pick |
|-----------|------|
| Node.js, new project | **Fastify** |
| Node.js, enterprise / large team | **NestJS** |
| Node.js, maximum compatibility | **Express** |
| Python, API-first | **FastAPI** |
| Python, full-stack with admin | **Django** |
| Edge / multi-runtime | **Hono** |
| Go service | **Gin** or **Fiber** |

---

## ⚛️ What frontend framework should I use?

| Situation | Pick |
|-----------|------|
| Full-stack app, SEO matters | **Next.js** |
| Pure SPA, no SSR needed | **Vite + React** |
| Content site / blog / docs | **Astro** |
| Vue preferred | **Nuxt** |
| Maximum performance | **SolidJS** or **Svelte** |
| Enterprise / large team | **Next.js** or **Angular** |

---

## 🏗️ Monolith vs Microservices?

| Situation | Recommendation |
|-----------|---------------|
| Early-stage product / MVP | **Monolith** — ship faster, easier to change |
| Single team, < 20 engineers | **Modular monolith** — enforce module boundaries first |
| Different scaling needs per feature | Extract that feature as its **own service** |
| Multiple teams, independent deploys | **Microservices** |
| Unclear domain boundaries | Stay monolith — let boundaries emerge naturally |
| Migrating a legacy monolith | **Strangler fig pattern** — extract incrementally |

---

## ☁️ Which cloud provider?

| Situation | Recommendation |
|-----------|---------------|
| Default / industry standard | **AWS** |
| Data-heavy / ML workloads | **GCP** |
| Microsoft / enterprise stack | **Azure** |
| Frontend + serverless | **Vercel** |
| Edge / low latency globally | **Cloudflare Workers** |
| Rapid prototyping | **Railway** or **Render** |
| Control + price for apps | **Fly.io** |

---

## 🔄 REST vs GraphQL vs tRPC?

| Situation | Pick |
|-----------|------|
| Public API, multiple clients | **REST + OpenAPI** |
| Complex UIs, varied data shapes | **GraphQL** |
| TypeScript full-stack monorepo | **tRPC** |
| Internal microservices | **gRPC** |
| Real-time bidirectional | **WebSockets** |
| Server push (AI streaming, notifications) | **SSE** |

---

## 📦 What ORM should I use?

| Situation | Pick |
|-----------|------|
| TypeScript + Next.js | **Prisma** |
| TypeScript, edge compatible | **Drizzle** |
| Python + FastAPI / Django | **SQLAlchemy** |
| Node.js, complex queries | **Kysely** (query builder) |
| Need maximum type safety | **Drizzle** or **Kysely** |

---

## 🧪 What testing tools should I use?

| Type | Pick |
|------|------|
| Unit / integration (Vite) | **Vitest** |
| Unit / integration (general) | **Jest** |
| Component testing | **Testing Library** + Vitest |
| E2E (cross-browser) | **Playwright** |
| E2E (visual debugging) | **Cypress** |
| API testing | **Supertest** or **Hoppscotch** |
| Load testing | **k6** |
| Python testing | **Pytest** |
