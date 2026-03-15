# 🏗️ System Design

> Architecture, scalability, and distributed systems — thinking at scale.

---

## 📈 Scalability Patterns

| Pattern | What it is |
|---------|-----------|
| **Horizontal scaling** | Add more machines (scale out) vs bigger machine (scale up) |
| **Vertical scaling** | Increase CPU/RAM on existing machines — simpler but has a ceiling |
| **Load balancing** | Distribute requests — round-robin, least-connections, IP hash |
| **Database sharding** | Split data across multiple DB instances by key range or hash |
| **Read replicas** | Route read queries to replicas, writes to primary |
| **Eventual consistency** | Trade immediate consistency for availability/performance |
| **Denormalization** | Duplicate data to speed up reads at the cost of write complexity |

---

## 💾 Caching Strategies

| Strategy | What it is |
|----------|-----------|
| **Cache-aside (Lazy loading)** | App checks cache first, reads DB on miss, writes to cache |
| **Write-through** | Write to cache and DB simultaneously — always consistent |
| **Write-behind (Write-back)** | Write to cache immediately, async write to DB |
| **Read-through** | Cache sits in front of DB, handles reads transparently |
| **Cache invalidation** | TTL expiry, event-based invalidation, versioned keys |
| **CDN caching** | Cache at edge nodes globally for static and dynamic content |

---

## 🏛️ Architectural Patterns

| Pattern | When to use |
|---------|------------|
| **Monolith** | Start here. Simple to deploy, debug, and iterate |
| **Modular monolith** | Well-defined module boundaries before splitting into services |
| **Microservices** | Independent deployable services — each owns its data |
| **Event-driven** | Services communicate via events asynchronously — loose coupling |
| **CQRS** | Separate read and write models — optimize each independently |
| **Event sourcing** | Store events as source of truth — derive current state by replaying |
| **Hexagonal / Clean arch** | Ports & adapters — isolate business logic from infrastructure |
| **BFF pattern** | Backend-for-Frontend — tailored API layer per client type |
| **Strangler fig** | Gradually migrate legacy — route traffic to new services incrementally |

---

## 🌐 Distributed Systems Concepts

| Concept | What it is |
|---------|-----------|
| **CAP theorem** | Can only guarantee 2 of: Consistency, Availability, Partition tolerance |
| **PACELC** | Extends CAP — normal operation: latency vs consistency trade-off |
| **Raft consensus** | Leader election + log replication — used in etcd, CockroachDB |
| **Two-phase commit** | Atomic distributed transactions — coordinator + participant protocol |
| **Saga pattern** | Distributed transactions via sequence of compensating actions |
| **Vector clocks** | Track causality in distributed systems without synchronized clocks |
| **Consistent hashing** | Distribute load with minimal key remapping when nodes change |
| **Leader election** | Zookeeper, etcd — dynamically elect primary in distributed cluster |

---

## 🔌 API Design Principles

| Principle | What it means |
|-----------|--------------|
| **Idempotency** | Same request → same result. Critical for safe retries (PUT, DELETE) |
| **Versioning** | URI (/v1/), Accept header, or query string versioning |
| **Pagination** | Cursor-based (scalable, consistent) vs offset-based (simple) |
| **Rate limiting** | Token bucket, leaky bucket, sliding window algorithms |
| **Circuit breaker** | Stop calling failing services — fail fast, avoid cascading failures |
| **Retry with exponential backoff** | Increasing delays + jitter to avoid thundering herd |
| **Graceful degradation** | Return partial/cached data vs total failure |
| **Idempotency keys** | Client-provided key to make non-idempotent ops safe to retry |

---

## 📊 Data Storage Decisions

| Need | Pick |
|------|------|
| Default relational | PostgreSQL |
| Serverless / auto-scale | Neon or PlanetScale |
| Cache / sessions | Redis |
| Full-text search | Elasticsearch or Typesense |
| Massive write throughput | Cassandra |
| Document / flexible schema | MongoDB |
| Vector similarity search | pgvector or Pinecone |
| Analytics / OLAP | DuckDB (local), BigQuery (cloud) |
| Graph / connected data | Neo4j |
| Time-series / metrics | InfluxDB or TimescaleDB |
| Files / blobs | S3 or GCS |

---

## 📏 Reliability Concepts

| Concept | What it means |
|---------|--------------|
| **SLI** | Service Level Indicator — the metric being measured (latency, error rate) |
| **SLO** | Service Level Objective — target threshold for an SLI (99.9% success) |
| **SLA** | Service Level Agreement — contractual commitment to SLOs |
| **Availability math** | 99.9% = 8.7h/yr · 99.99% = 52min/yr · 99.999% = 5min/yr downtime |
| **RTO** | Recovery Time Objective — max time to restore service after outage |
| **RPO** | Recovery Point Objective — max acceptable data loss in time |
| **Chaos engineering** | Intentionally inject failures (Chaos Monkey) to test resilience |
| **Bulkhead pattern** | Isolate failures — separate thread pools per downstream service |
| **Backpressure** | Signal upstream to slow down when overwhelmed |

---

## 🗺️ Suggested Roadmap

```
HTTP + REST + basic API design
    → Caching strategies (Redis, CDN)
    → Database selection trade-offs
    → Scalability patterns (horizontal, read replicas)
    → Distributed systems theory (CAP, Raft, Saga)
    → Reliability (SLO/SLA, circuit breakers, retries)
    → Architecture patterns (event-driven, CQRS)
    → System design interview practice
```
