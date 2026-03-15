# ☁️ DevOps & Cloud

> Getting code from your machine to the world, reliably and at scale.

---

## 🐳 Containers & Orchestration

| Tech | What it's for |
|------|--------------|
| **Docker** | Package apps + dependencies into portable, reproducible containers |
| **Docker Compose** | Define and run multi-container applications locally |
| **Kubernetes** | Container orchestration: pods, deployments, services, ingress, auto-scaling |
| **Helm** | Package manager for Kubernetes — templated, versioned chart deployments |
| **k3s / k3d** | Lightweight Kubernetes for local dev, edge, and CI environments |
| **Podman** | Rootless Docker alternative — daemonless, OCI-compatible |

---

## 🔄 CI/CD

| Tech | What it's for |
|------|--------------|
| **GitHub Actions** | YAML workflow automation built into GitHub — free tier available |
| **GitLab CI** | Full CI/CD platform integrated into GitLab — self-hostable |
| **CircleCI** | Fast pipelines with smart caching and parallelism |
| **ArgoCD** | GitOps continuous delivery — Kubernetes state reconciliation |
| **Tekton** | Cloud-native CI/CD pipeline framework on Kubernetes |
| **Jenkins** | Self-hosted automation server, highly configurable (legacy) |
| **Buildkite** | Hybrid CI — your agents, their UI |

---

## ☁️ Cloud Providers

| Cloud | Core services | Best for |
|-------|--------------|----------|
| **AWS** | EC2, S3, Lambda, RDS, EKS, CloudFront, SQS | Most comprehensive, industry standard |
| **GCP** | GKE, BigQuery, Vertex AI, Cloud Run, Pub/Sub | Data/ML, best managed Kubernetes |
| **Azure** | AKS, CosmosDB, Azure AD, Functions | Enterprise, Microsoft/Windows stack |
| **Vercel** | Frontend deployment, Edge Functions, Analytics | Next.js, frontend teams |
| **Fly.io** | App deployment globally close to users | Latency-sensitive apps |
| **Railway** | Simple infra without config overhead | Fast prototype deployments |
| **Cloudflare** | CDN, Workers, R2, DNS, DDoS protection | Edge computing, global distribution |

---

## 🏗️ Infrastructure as Code

| Tech | What it's for |
|------|--------------|
| **Terraform** | Multi-cloud IaC using HCL — industry standard |
| **Pulumi** | IaC using real languages (TypeScript, Python, Go, .NET) |
| **AWS CDK** | Define AWS infrastructure in TypeScript/Python/Java |
| **Ansible** | Agentless server configuration management via YAML playbooks |
| **Crossplane** | Kubernetes-native cloud resource management |
| **OpenTofu** | Open-source Terraform fork (post-BSL license change) |

---

## 📊 Observability Stack

| Tech | What it's for |
|------|--------------|
| **Prometheus** | Metrics collection and alerting rules — pull-based |
| **Grafana** | Visualization for metrics, logs, traces — dashboards |
| **OpenTelemetry** | Vendor-neutral standard for traces, metrics, and logs |
| **Datadog** | All-in-one monitoring platform — APM, logs, infrastructure |
| **Sentry** | Error tracking, performance monitoring, session replay |
| **Loki** | Log aggregation — part of the Grafana observability stack |
| **Jaeger** | Distributed tracing for microservices |
| **PagerDuty / OpsGenie** | On-call alerting and incident management |

---

## 🌐 Networking

| Concept | What it means |
|---------|--------------|
| **DNS** | A, CNAME, MX, TXT records, TTL, propagation |
| **Load balancers** | L4 (TCP/UDP) vs L7 (HTTP) — sticky sessions, health checks |
| **Reverse proxy** | Nginx/Caddy: SSL termination, routing, rate limiting, compression |
| **VPC / Subnets** | Private network isolation — public vs private subnets, NAT gateways |
| **Service mesh** | Istio/Linkerd: mTLS between services, traffic management |
| **CDN** | Edge-cached content delivery — CloudFront, Fastly, Cloudflare |
| **Ingress controller** | Route external traffic into a Kubernetes cluster |

---

## 🗺️ Suggested Roadmap

```
Linux basics + shell scripting + SSH
    → Docker + Docker Compose
    → GitHub Actions (CI/CD pipelines)
    → One cloud provider (start with AWS or GCP)
    → Terraform (infrastructure as code)
    → Kubernetes fundamentals
    → Observability (Prometheus + Grafana + Sentry)
    → Service mesh + advanced networking
```
