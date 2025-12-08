# Back-End Mastery

## Foundations
### [How does the Internet Works?](/backend/core-foundations/how-the-internet-works.md)
- [What is a Server](/backend/core-foundations/what-is-a-server.md)
- [What is a Client](/backend/core-foundations/what-is-a-client.md)
- [HTTP vs HTTPS](/backend/core-foundations//http-vs-https.md)
- [DNS (Domain Name Server](/backend/core-foundations/dns.md)
- [IP address](/backend/core-foundations/ip-address.md)
- [Ports](/backend/core-foundations/ports.md)
- [Domain vs Hosting vs Server](/backend/core-foundations/domain-vs-hosting-vs-server.md)
- [Request & Response cycle](/backend/core-foundations/request-and-response-cycle.md)
- [Status Codes](/backend/core-foundations/http-status-codes.md)
- [JSON Handling](/backend/core-foundations/json-handling.md)
- [Request Parsing](/backend/core-foundations/request-parsing.md)
- [CORS (Cross-Origin Resource Sharing)](/backend/core-foundations/cors.md)

### [Networking](/backend/core-foundations/networking.md)
- [TCP vs UDP](/backend/core-foundations/tcp-vs-udp.md)
- [3-Way Handshake](/backend/core-foundations/3-way-handshake.md)
- [NAT (Network Address Translation)](/backend/core-foundations/nat.md)
- [Firewalls](/backend/core-foundations/firewalls.md)
- [Reverse Proxy](/backend/core-foundations/reverse-proxy.md)
- [Forward Proxy](/backend/core-foundations/forward-proxy.md)
- [Load Balancer](/backend/core-foundations/load-balancer.md)
- [CDN (Content Delivery Network)](/backend/core-foundations/cdn.md)
- [SSL/TLS Handshake](/backend/core-foundations/ssl-tls-handshake.md)
- [WebSockets](/backend/core-foundations/websockets.md)
- [VPN vs Proxy](/backend/core-foundations/vpn-vs-proxy.md)
- [Port Forwarding](/backend/core-foundations/port-forwarding.md)
- [Sockets](/backend/core-foundations/sockets.md)

## Backend Servers
- Node.js
   - Express.js
   - Fastify
   - Middlewares
   - Routing
   - Controllers
   - Services
- PHP (Laravel)
   - Routing
   - Controllers
   - Models
   - ORM (Eloquent)
   - API development
- Python
   - Flask
   - Django

#### CRUD example:
```txt
GET /users
POST /users
PUT /users/:id
DELETE /users/:id
```

**Goal:** Build multiple CRUD APIs

## Databases
- Normalization vs Denormalization
- ACID vs BASE
- Query planner (EXPLAIN)

- SQL:
   - MySQL
   - PostgreSQL
   - SELECT, INSERT, UPDATE, DELETE
   - JOINs
   - Relations
   - Indexing
   - Foreign keys
   - Transactions

- NoSQL:
   - MongoDB
   - Redis (cache, sessions, rate limit)

- **Database Design:**
   - users
   - orders
   - products
   - roles
   - payments
   - logs


## Authentication and Security
### Auth systems:
   - Register
   - Login
   - Logout
   - Forgot / Reset password
   - Email verification
   
### Authorization
   - Roles & Permissions (RBAC)
   - Policies & Gates
   - Token expiration
   - Refresh tokens

### Security:
   - Hashing (bcrypt)
   - JWT
   - Refresh tokens
   - OAuth (Google, GitHub)
   - Token expiration
   - Rate limiting

### Protection against:
   - SQL Injection
   - XSS
   - CSRF
   - Brute force
   - DDoS (concept)

## APIs
- REST APIs
- API versioning (/v1, /v2)
- Swagger / OpenAPI
- Postman / Insomnia
- Webhooks
- File uploads
- Cloud storage
- Pagination
- Filtering
- Sorting
- GraphQL
- Rate limit
- API keys

## Real-time & Advanced Backend
- WebSockets
- Socket.io
- Laravel Echo
- Real-time chat
- Notifications
- Live dashboards
- Queues explained
- Redis Pub/Sub

## System Design & Architecture
- MVC Architecture
- Clean Architecture
- SOLID Principles
- Repository Pattern
- Service Pattern
- CQRS
- Event Driven Architecture
- CAP Theorem
- Vertical slice architecture

### System Types
- Monolith
- Microservices
- Microservices communication
- API Gateway
- Service Discovery

### Infrastructure
- Load Balancers
- Reverse Proxy
- Horizontal vs Vertical scaling
- CDN
- Sharding
- Health checks
- Circuit Breaker
- Rate Limiting
- Failover systems

## DevOps & Cloud
- Linux basics
- Docker
- Docker Compose
- Kubernetes (intro)
- GitHub Actions
- CI/CD pipelines
- NGINX / Apache
- PM2 / Supervisor
- Monitoring
- Logs
- Domain & DNS
- SSL/TLS
- VPS setup
- DigitalOcean
- AWS (EC2, S3, RDS, Lambda)
- Railway / Vercel / Render

## Performance & Scaling
- Redis caching
- Query optimization
- Indexes
- Lazy vs eager loading
- CDN
- Gzip / Brotli
- Memory management
- Performance monitoring
- Stress testing
- Load testing
- N+1 problem
- Bottlenecks analysis

## Tools:
- [Backend Tools](/backend/tools.md)