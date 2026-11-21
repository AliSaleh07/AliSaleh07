# Ali Saleh

**Software Engineer** — Backend Architecture, DevOps, and Application Security

I build defensive, scalable backend systems and developer tooling. My focus centers on reliable API design, container security, distributed systems, and defensive security automation.

---

## Technical Focus

- **Backend Development**: Python, Go, FastAPI, REST API Architecture, Async Systems, Microservices
- **Application Security**: Defensive Engineering, Cryptography (PBKDF2/JWT), Secret Scanning, Access Control
- **DevOps & Infrastructure**: Docker, Container Hardening, CI/CD Pipelines (GitHub Actions), Linux Systems
- **Databases & Storage**: PostgreSQL, SQLite, Redis, Schema Design, Data Integrity

---

## Featured Engineering Projects

### [TaskForge](https://github.com/AliSaleh07/TaskForge)
*Production-ready task management REST API with defensive cryptography.*
- Strict user-level tenant isolation preventing horizontal privilege escalation.
- PBKDF2-HMAC-SHA256 password hashing (600,000 rounds) and HMAC-SHA256 JWT sessions.
- Automated security headers middleware (HSTS, CSP, X-Frame-Options) and SQLite transactional persistence.

### [Compose Scout](https://github.com/AliSaleh07/compose-scout)
*Static security auditing and configuration linter for Docker Compose.*
- Detects insecure container configurations: privileged flags, socket mounts (`docker.sock`), public port bindings, and plaintext secrets.
- Supports strict exit codes for automated CI/CD gating and outputs machine-readable JSON and Markdown reports.

### [Secret Sentry](https://github.com/AliSaleh07/secret-sentry)
*High-performance, zero-exfiltration local secret scanner for codebases and repositories.*
- Identifies exposed API tokens, cloud keys, database URIs, and private keys.
- Combines regex heuristics with Shannon entropy thresholding ($H(X) \ge 3.8$ bits) and safe terminal redaction.
- 100% offline with zero external network exfiltration.

### [AuthLog Lens](https://github.com/AliSaleh07/authlog-lens)
*Defensive authentication log analyzer and intrusion detection CLI.*
- Ingests Linux authentication logs (`auth.log`, `secure`, syslog) to surface active security incidents.
- Detects SSH brute-force attempts, credential stuffing, root targeting, and post-failure account compromises.

### [OpenAPI Smoke](https://github.com/AliSaleh07/openapi-smoke)
*OpenAPI specification validator and automated smoke testing CLI.*
- Parses OpenAPI 3.0, 3.1, and Swagger 2.0 specs with safe YAML parsing guards.
- Executes automated HTTP smoke runs and generates JUnit XML test reports for CI dashboards.

---

## Engineering Practices

- **Test-Driven Rigor**: Comprehensive automated test coverage across unit, integration, and edge scenarios.
- **Defensive Defaults**: Principle of least privilege, strict input validation, and zero trust architecture.
- **Continuous Integration**: GitHub Actions matrix pipelines testing multiple runtime environments on every commit.

---

## Contact & Links

- **GitHub**: [github.com/AliSaleh07](https://github.com/AliSaleh07)
- **Profile**: Software Engineer
