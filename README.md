# Hello, I'm Adi! 👋

Security engineer in Jerusalem application security and DevSecOps. I build hardened backend
services in Rust and Python, and CI pipelines that stop insecure infrastructure before it ships.

CompTIA Security+ · B.S. Information Technology & Management, University at Buffalo (Magna Cum Laude) · English (native) / Hebrew (fluent)

## 🛡️ CyberSecurity Projects

### 🦀 Rust & Application Security
**[axum-jwt-auth — Hardened JWT Authentication Service](https://github.com/Adi-Czobel/axum-jwt-auth)**
- Argon2id password hashing at OWASP parameters (19 MiB, t=2, p=1) — the memory cost is what makes offline cracking expensive
- Refresh-token rotation with reuse detection: replaying a spent token revokes the entire token family, since there is no way to tell attacker from legitimate client
- JWT validation pinned to a single algorithm, blocking `alg=none` and RS256→HS256 confusion — a hand-forged unsigned token is asserted rejected in the tests
- Login timing equalised against a dummy hash so response time cannot be used to enumerate accounts
- 27 tests, `clippy -D warnings` clean, README documents known limitations rather than only strengths

---
### 🔐 DevSecOps & Supply Chain
**[Secure IaC Pipeline](https://github.com/Adi-Czobel/Demo)**
- Checkov, Hadolint, and Terraform validation gate every pull request; CodeQL, Trivy, and gitleaks report SARIF to the GitHub Security tab
- Tagged releases build to GHCR with SLSA build provenance and a Syft SBOM attached to the release
- Container images signed with **cosign keyless via Sigstore** — no long-lived signing key exists to be stolen
- gitleaks scans full history (`fetch-depth: 0`), because a secret removed in a later commit is still valid until rotated

---
### ☁️ AWS
**[AWS GuardDuty Real-Time Alerts with EventBridge & SNS](https://github.com/Adi-Czobel/AWS-Real-Time-Alerts-)**
- Enabled AWS GuardDuty for continuous threat detection across the account
- Configured EventBridge rules to capture GuardDuty findings in real time
- Integrated SNS to send instant email alerts for high-severity threats
- Tested alert pipeline with sample GuardDuty findings to validate response flow

---
## 🐋 Docker

### [SecureStack — Multi-Container Docker Project](https://github.com/Adi-Czobel/securestack)

- Built a production-style multi-container application using Docker Compose
- Stack: nginx reverse proxy, Flask API, PostgreSQL database, Redis cache
- Implemented network segmentation — backend containers have no internet access
- Applied security hardening: non-root containers, read-only filesystems, resource limits
- Used named volumes for database persistence across container restarts

## 🕵️ Network Security

**[Network Incident Response Simulator](https://github.com/Adi-Czobel/incident-response-simulator)**
- Built a real-time port-scan detector using Scapy, sniffing raw traffic on an isolated VirtualBox lab network
- Automatically blocks the offending IP via `iptables` and logs a simulated alert on detection
- Live Flask dashboard polls and displays incidents as they're detected
- Verified end-to-end across two VMs (attacker → detector → dashboard) with `curl`-based API testing

## 🧰 Working with

`Rust` `Axum` `Python` `Docker` `Terraform` `Kubernetes` `GitHub Actions` `AWS` `Linux`
`Checkov` `Trivy` `CodeQL` `cosign` `gitleaks` `Scapy` `Wireshark` `nginx` `PostgreSQL`

## 📫 Connect with me
[![LinkedIn](https://cdn-icons-png.flaticon.com/512/174/174857.png)](https://www.linkedin.com/in/adiczobel)
