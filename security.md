# 🔐 Security

> The thing no one notices until it breaks. Build with security from day one.

---

## 🔑 Authentication & Authorization

| Concept | What it is |
|---------|-----------|
| **JWT** | Stateless signed tokens. Store in httpOnly cookies — not localStorage |
| **Sessions** | Server-side state with session ID in cookie — supports revocation |
| **OAuth 2.0** | Delegated authorization — Auth Code flow with PKCE for SPAs |
| **OpenID Connect** | Identity layer on OAuth — provides `id_token` with user claims |
| **PKCE** | Proof Key for Code Exchange — required for SPAs and mobile apps |
| **RBAC** | Role-based: users get roles, roles get permissions |
| **ABAC** | Attribute-based: fine-grained policy engine on resource + user attrs |
| **MFA / TOTP** | Second factor: TOTP apps (Authy), hardware keys (FIDO2/WebAuthn) |
| **WebAuthn / Passkeys** | Passwordless auth using device biometrics + public key crypto |

---

## 🛡️ OWASP Top 10

| # | Vulnerability | How to prevent it |
|---|--------------|------------------|
| A01 | **Broken Access Control** | Enforce permissions server-side on every request, deny by default |
| A02 | **Cryptographic Failures** | TLS 1.3, AES-256, SHA-256+. Never MD5/SHA-1. Encrypt data at rest |
| A03 | **Injection** | Parameterized queries + ORMs. Never concatenate user input into queries |
| A04 | **Insecure Design** | Threat modeling, secure design patterns, least privilege |
| A05 | **Security Misconfiguration** | Secure defaults, disable unused features, no exposed stack traces |
| A06 | **Vulnerable Components** | `npm audit`, Snyk, Dependabot — automate dependency scanning |
| A07 | **Auth Failures** | Rate limiting, brute force protection, secure session management |
| A08 | **Software Integrity Failures** | Verify checksums, signed packages, secure CI/CD pipelines |
| A09 | **Logging Failures** | Log security events, never log credentials/PII, monitor anomalies |
| A10 | **SSRF** | Validate + allowlist URLs before server-side HTTP requests |
| — | **XSS** | Escape outputs. Content-Security-Policy headers. DOMPurify for HTML |
| — | **CSRF** | SameSite=Strict/Lax cookies + CSRF tokens for state-changing requests |

---

## 🔒 Security HTTP Headers

| Header | What it does |
|--------|-------------|
| **Content-Security-Policy** | Restrict sources for scripts, styles, images — prevents XSS |
| **Strict-Transport-Security** | Force HTTPS for N seconds — prevents SSL stripping |
| **X-Frame-Options** | Prevent clickjacking via iframe (`DENY` or `SAMEORIGIN`) |
| **X-Content-Type-Options** | Prevent MIME type sniffing (`nosniff`) |
| **Referrer-Policy** | Control what's included in the Referer header |
| **Permissions-Policy** | Disable browser APIs (camera, geolocation, microphone) |
| **CORS** | `Access-Control-Allow-Origin` — whitelist trusted origins |

---

## 🔑 Cryptography Essentials

| Concept | What it is |
|---------|-----------|
| **Symmetric (AES)** | Same key encrypts + decrypts. Fast for bulk data |
| **Asymmetric (RSA/ECC)** | Public key encrypts, private key decrypts. Key exchange |
| **Hashing (SHA-256/SHA-3)** | One-way. Integrity, digital signatures, HMACs |
| **Password hashing (Argon2/bcrypt)** | Slow by design + salt — defeats rainbow tables and brute force |
| **TLS 1.3** | Transport encryption. Only support TLS 1.2+ in production |
| **HMAC** | Keyed hash for message authentication — JWT signatures (HS256) |
| **X.509 certificates** | PKI infrastructure — CA-signed certs for domain identity |
| **Key management** | HashiCorp Vault, AWS KMS, Azure Key Vault — never manage keys manually |

---

## 🧰 Security Tools

| Tool | What it's for |
|------|--------------|
| **Snyk** | Automated vulnerability scanning in dependencies, containers, IaC |
| **OWASP ZAP** | Active + passive web application security scanning |
| **Burp Suite** | Intercepting proxy for manual penetration testing |
| **HashiCorp Vault** | Secrets management — store, rotate, audit credentials |
| **Trivy** | Container image + filesystem + IaC vulnerability scanning |
| **Semgrep** | Static analysis — find security anti-patterns in code |
| **Nmap** | Network scanning and host discovery |
| **Metasploit** | Penetration testing framework (ethical hacking only) |

---

## ✅ Best Practices Checklist

- [ ] Never hardcode secrets — use environment variables or a secrets manager
- [ ] HTTPS everywhere — TLS 1.2+ minimum, 1.3 preferred
- [ ] Validate all inputs server-side — client can always be bypassed
- [ ] Apply least privilege — grant minimum permissions needed
- [ ] Rate limit all auth endpoints — prevent brute force
- [ ] Log security events — but never log credentials or PII
- [ ] Automate dependency scanning — Snyk or Dependabot on every PR
- [ ] Rotate secrets regularly — especially after team member leaves
- [ ] Use parameterized queries everywhere — never string-concatenate SQL

---

## 🗺️ Suggested Roadmap

```
HTTPS + TLS basics
    → OWASP Top 10
    → Auth (JWT + OAuth 2.0 + sessions)
    → Web security headers
    → Secrets management
    → Dependency scanning
    → Cryptography fundamentals
    → Basic penetration testing (OWASP ZAP, Burp Suite)
```
