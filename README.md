<div align="center">

# Ali Saleh

### **Software Engineer**
*Specializing in Application Security, Defensive Tooling & Backend Architecture*

[![GitHub](https://img.shields.io/badge/GitHub-AliSaleh07-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/AliSaleh07)
[![Identity](https://img.shields.io/badge/Focus-Cybersecurity%20%7C%20Backend-0A66C2?style=flat-square)](https://github.com/AliSaleh07)
[![Email](https://img.shields.io/badge/Contact-Direct%20Inquiry-2ea44f?style=flat-square&logo=gmail&logoColor=white)](mailto:alisaleh@github.com)

---

</div>

## 📌 About Me

I am a **Software Engineer** focused on defensive application security, backend system design, and security automation. My work centers on building software that is secure by default: implementing robust authentication barriers, zero-trust tenant boundaries, automated container auditing, and credential-scanning tooling.

I approach engineering from both defensive and analytical perspectives—combining hands-on network traffic analysis, web application security testing, and systems programming to architect resilient backend services.

---

## 🛡️ Technical Stack & Tooling

> Practical classification based on hands-on project implementations, verified lab work, and active research.

### 1. Penetration Testing & Application Security
| Category | Tool / Framework | Experience Level | Key Application |
|---|---|---|---|
| **Web Proxy & Testing** | `Burp Suite Pro` | **Hands-on** | Request tampering, auth bypass testing, intercepting proxy analysis |
| **Password Auditing** | `John the Ripper` | **Hands-on** | Hash identification, offline credential recovery, dictionary attacks |
| **Vulnerability Standards** | `OWASP Top 10` | **Hands-on** | Defensive controls against IDOR, broken auth, injection, and SSRF |
| **Network Scanning** | `Nmap` | **Familiar** | Host discovery, port enumeration, service fingerprinting |
| **Automated Assessment** | `SQLmap`, `Nikto` | **Familiar** | Web vulnerability detection, parameter injection testing |
| **Active Directory Security** | `Kerberos & AD Lab` | **Exploring** | Kerberoasting concepts, domain privilege auditing |

### 2. Network Security & Traffic Forensics
| Tool / Technology | Experience Level | Practical Context |
|---|---|---|
| `Wireshark` | **Hands-on** | Protocol dissection, TLS handshakes, packet capture forensics |
| `tcpdump` | **Hands-on** | Headless CLI packet capture, live traffic filtering, PCAP analysis |
| `Cisco Packet Tracer` | **Hands-on** | Subnetting, VLAN segregation, routing topology simulation |
| `SSH & OpenSSL` | **Hands-on** | Public-key infrastructure, cryptographic primitives, tunnel security |
| `Netcat` | **Familiar** | Raw socket interaction, banner grabbing, debugging network ports |

### 3. Defensive Engineering & Security Tooling
| Tool / Domain | Practical Application |
|---|---|
| **Secret Detection** | Engine author of `secret-sentry` (Shannon entropy $H \ge 3.8$, custom regex, auto-redaction) |
| **Container Hardening** | Engine author of `compose-scout` (Flags socket mounts, host namespaces, privileged mode) |
| **Intrusion Detection** | Engine author of `authlog-lens` (Detects SSH brute-force bursts, credential stuffing) |
| **API Smoke & Validation** | Engine author of `openapi-smoke` (OpenAPI 3.x schema verification, JUnit XML CI reporting) |

### 4. Backend Engineering, Systems & DevSecOps
| Layer | Technologies |
|---|---|
| **Languages** | `Python 3` (Primary), `C++` (Systems programming, data structures), `Bash / Shell` |
| **Frameworks & APIs** | `FastAPI`, `Starlette`, `Pydantic v2`, `REST APIs`, `OpenAPI 3.1` |
| **Environments & OS** | `Linux CLI`, `WSL`, `Ubuntu / Debian`, `Windows Server` |
| **Containers & CI/CD** | `Docker`, `Docker Compose`, `GitHub Actions` (Matrix test automation) |
| **Databases** | `SQLite 3`, `PostgreSQL`, `Parameterized SQL`, Schema Isolation |

---

## 🚀 Featured Engineering Projects

All five repositories are fully functional, accompanied by 100% passing automated test suites and verified GitHub Actions CI workflows.

### 1. [TaskForge](https://github.com/AliSaleh07/TaskForge)
*Defensive Task Management REST API with Zero-Trust Multi-Tenancy*
- **Security Focus**: Zero-trust tenant isolation preventing Insecure Direct Object References (IDOR).
- **Cryptography**: NIST-compliant `PBKDF2-HMAC-SHA256` password hashing (600,000 rounds) and custom RFC 7519 HMAC-SHA256 JWT sessions.
- **Defensive Headers**: Enforces strict `HSTS`, `CSP`, and `X-Frame-Options: DENY` on all responses.
- **Stack**: FastAPI, Pydantic v2, SQLite, Uvicorn, pytest.

### 2. [compose-scout](https://github.com/AliSaleh07/compose-scout)
*Docker Compose Static Security Auditing & Misconfiguration Linter CLI*
- **Security Focus**: Flags dangerous host overrides (`privileged: true`, `network_mode: host`, `/var/run/docker.sock` mounts).
- **Network Boundaries**: Identifies unrestricted `0.0.0.0` bindings on sensitive database ports (Postgres, MySQL, Redis, Mongo).
- **CI/CD Integration**: Strict gating (`--strict`) returning non-zero exit codes to block insecure deployments.
- **Stack**: Python 3, PyYAML (SafeLoader), Argparse, pytest.

### 3. [secret-sentry](https://github.com/AliSaleh07/secret-sentry)
*Zero-Exfiltration Local Secret Scanner & Shannon Entropy Detector*
- **Security Focus**: 100% offline scanning guarantee with zero telemetry or network calls.
- **Heuristics**: Combines targeted token patterns (AWS, GitHub, Slack, Private Keys) with Shannon entropy calculations ($H \ge 3.8$ bits).
- **Safe Masking**: Automatic redaction (`AKIA**************DEF`) preventing accidental logging of leaked secrets.
- **Stack**: Python 3, Math/Entropy engine, pytest.

### 4. [authlog-lens](https://github.com/AliSaleh07/authlog-lens)
*Defensive Linux Authentication Log Analyzer & Intrusion Detection CLI*
- **Security Focus**: Parses `/var/log/auth.log` and syslog streams to surface active brute-force attacks.
- **Incident Heuristics**: Detects multi-account credential stuffing, root targeting, and post-failure account compromises.
- **Reporting**: Structured terminal tables, JSON incident dumps for SIEM, and Markdown summaries.
- **Stack**: Python 3, Regex Syslog Engine, pytest.

### 5. [openapi-smoke](https://github.com/AliSaleh07/openapi-smoke)
*Automated OpenAPI Specification Validator & Smoke-Testing Engine*
- **Security Focus**: Safe YAML deserialization protecting against arbitrary code execution vulnerabilities.
- **Spec Compliance**: Flags missing schemas, undeclared path parameters, and invalid HTTP response codes across OpenAPI 3.0, 3.1, and Swagger 2.0.
- **CI Tooling**: Generates JUnit XML test reports natively ingested by CI pipelines.
- **Stack**: Python 3, HTTPX, PyYAML, pytest.

---

## 🔍 Engineering Highlights

```
┌────────────────────────────────────────────────────────────────────────┐
│                        CORE ENGINEERING PRINCIPLES                     │
├────────────────────────────────┬───────────────────────────────────────┤
│ Zero Trust Tenant Boundaries   │ Never trust client-supplied IDs.      │
│ Cryptographic Rigor            │ 600k PBKDF2 rounds; constant-time cmp.│
│ Zero-Exfiltration Tooling      │ Security tools run strictly local.    │
│ Automated Security Verification│ Continuous matrix CI on every commit. │
└────────────────────────────────┴───────────────────────────────────────┘
```

---

## 💻 Behind the Logic

```json
{
  "engineer": "Ali Saleh",
  "title": "Software Engineer",
  "domains": [
    "Application Security",
    "Defensive Tooling",
    "Backend Systems",
    "Network Forensics"
  ],
  "philosophy": {
    "architecture": "Defensive by default, least-privilege by design",
    "testing": "Automated verification over manual assumptions",
    "telemetry": "Zero unnecessary data exfiltration"
  },
  "current_focus": [
    "Container runtime isolation",
    "Protocol-level traffic dissection",
    "Automated vulnerability detection"
  ]
}
```

---

<div align="center">

*Engineered with precision. Backed by verified source code and continuous automated testing.*

</div>
