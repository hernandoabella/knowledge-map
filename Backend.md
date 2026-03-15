# ⚙️ Backend

> The invisible engine. APIs, data, business logic — everything users depend on but never see.

---

## 🌐 Languages & Runtimes

| Tech | What it's for | Strengths |
|------|--------------|-----------|
| **Node.js** | JS server runtime — non-blocking I/O, huge npm ecosystem | Same language as frontend, fast I/O |
| **Python** | Readable syntax, dominant in data/ML, great for scripting | Scientific libraries, rapid dev |
| **Go** | Statically typed, compiled to binary, excellent concurrency | Low latency, simple deployment |
| **Rust** | Memory-safe systems language — no GC, zero-cost abstractions | Safety + performance, WASM, CLIs |
| **Java/Kotlin** | JVM ecosystem, battle-tested at scale | Enterprise reliability, mature tooling |
| **Elixir** | Erlang VM, Actor model, fault-tolerant by design | High-concurrency, distributed systems |
| **Deno** | Secure Node.js alternative, TypeScript native | Modern, secure, permissions system |

---

## 🚀 Backend Frameworks

| Framework | Language | What it's for |
|-----------|----------|--------------|
| **Express.js** | Node.js | Minimal, flexible, most widespread — huge ecosystem |
| **Fastify** | Node.js | 2× faster than Express + schema-based validation |
| **NestJS** | TypeScript | Angular-style DI + decorators — enterprise-grade |
| **Hono** | Node/Bun/Deno/Edge | Ultra-lightweight, multi-runtime, great for edge |
| **FastAPI** | Python | Async, typed, auto-generates OpenAPI docs |
| **Django** | Python | Batteries-included: ORM, admin, auth, migrations |
| **Flask** | Python | Minimal, flexible microframework |
| **Gin** | Go | Fast, minimalist, good middleware support |
| **Spring Boot** | Java/Kotlin | Enterprise standard, comprehensive ecosystem |
| **Axum** | Rust | Fast, type-safe web framework built on Tokio |

---

## 🗄️ Databases — Relational (SQL)

| DB | What it's for |
|----|--------------|
| **PostgreSQL** | The standard. ACID, extensible (JSON, full-text, PostGIS) |
| **MySQL / MariaDB** | Widely deployed, good replication, familiar to many teams |
| **SQLite** | Embedded, serverless — dev environments, mobile, small apps |
| **Neon** | Serverless PostgreSQL with branching and auto-scaling |
| **PlanetScale** | Serverless MySQL via Vitess — schema branching, zero-downtime migrations |
| **CockroachDB** | Distributed SQL — horizontal scaling with ACID compliance |

---

## 🗄️ Databases — NoSQL

| DB | Type | What it's for |
|----|------|--------------|
| **Redis** | In-memory key-value | Cache, sessions, pub/sub, rate limiting, job queues |
| **MongoDB** | Document | Flexible JSON-like schema, horizontal scaling |
| **Elasticsearch** | Search | Full-text search, aggregations, log analytics |
| **Cassandra** | Wide-column | Write-heavy workloads at massive scale — IoT, time-series |
| **DynamoDB** | Key-value + document | AWS managed, serverless, single-digit ms latency |
| **Firestore** | Document | Google managed, real-time sync, offline support |
| **Neo4j** | Graph | Connected data — fraud, social networks, recommendations |
| **InfluxDB** | Time-series | Metrics, monitoring data, IoT sensor readings |

---

## 🔗 ORMs & Query Builders

| Tech | Language | What it's for |
|------|----------|--------------|
| **Prisma** | TypeScript | Schema-driven ORM with type-safe client and migrations |
| **Drizzle** | TypeScript | Lightweight ORM with SQL-like syntax, edge compatible |
| **SQLAlchemy** | Python | Powerful ORM + Core SQL toolkit — very flexible |
| **Sequelize** | Node.js | Feature-rich ORM for PostgreSQL/MySQL/SQLite |
| **TypeORM** | TypeScript | Decorator-based ORM, similar to Hibernate |
| **Kysely** | TypeScript | Type-safe SQL query builder, no magic |
| **Knex** | Node.js | SQL query builder, foundation for other ORMs |

---

## 🔗 API Paradigms

| Paradigm | What it's for | When to use |
|----------|--------------|-------------|
| **REST** | Resources + HTTP verbs + stateless + cacheable | Standard public APIs, mobile backends |
| **GraphQL** | Client requests exactly what it needs | Complex UIs with varied data needs |
| **gRPC** | Binary protocol, strong contracts (protobuf), streaming | Internal microservices, high-throughput |
| **tRPC** | End-to-end TypeScript types, no schema codegen | TypeScript full-stack monorepos |
| **WebSockets** | Persistent bidirectional connection | Chat, collaboration, live dashboards |
| **Server-Sent Events** | Unidirectional server push — simpler than WebSockets | Notifications, live feeds, streaming AI |
| **OpenAPI / Swagger** | Standard REST API spec and documentation | All REST APIs |

---

## 🔐 Auth & Identity

| Tech | What it's for |
|------|--------------|
| **JWT** | Stateless signed tokens — store in httpOnly cookies, not localStorage |
| **Sessions** | Server-side state in Redis — more control, supports revocation |
| **OAuth 2.0** | Delegated authorization — "Login with Google/GitHub" |
| **OpenID Connect** | Identity layer on top of OAuth 2.0 — gives you `id_token` |
| **PKCE** | Proof Key for Code Exchange — secure OAuth for SPAs and mobile |
| **Passport.js** | Auth middleware for Node.js — 500+ strategies |
| **Auth.js (NextAuth)** | Auth for Next.js — 40+ providers out of the box |
| **Clerk** | Auth as a service — UI components + session management + MFA |
| **Auth0** | Enterprise identity platform — SSO, MFA, RBAC, audit logs |
| **bcrypt / Argon2** | Secure password hashing with salt — never store plaintext |

---

## 📬 Queues & Messaging

| Tech | What it's for |
|------|--------------|
| **BullMQ** | Robust job queues for Node.js backed by Redis — retries, scheduling |
| **RabbitMQ** | AMQP message broker — flexible routing topologies |
| **Apache Kafka** | Distributed event streaming at massive scale — durable, replayable |
| **AWS SQS/SNS** | Managed queues + pub/sub notifications |
| **Temporal** | Workflow orchestration — durable execution, long-running processes |
| **Celery** | Distributed task queue for Python with Redis or RabbitMQ |

---

## 🔄 Caching Patterns

| Pattern | What it is |
|---------|-----------|
| **Cache-aside** | App checks cache first, reads DB on miss, writes to cache |
| **Write-through** | Write to cache and DB simultaneously — always consistent |
| **Write-behind** | Write to cache immediately, async write to DB |
| **Read-through** | Cache sits in front of DB, handles reads transparently |
| **Cache invalidation** | TTL-based expiry, event-based invalidation, versioned keys |
| **HTTP caching** | Cache-Control, ETag, Last-Modified headers |

---

## 🗺️ Suggested Roadmap

```
HTTP fundamentals + REST design
    → Node.js + Express → Fastify / NestJS
    → PostgreSQL + Prisma (or SQLAlchemy)
    → Auth (JWT + OAuth 2.0 + PKCE)
    → Redis (caching + sessions + queues)
    → Testing (integration + contract tests)
    → Background jobs + async processing
    → API design patterns + versioning
    → Microservices + service communication
```
