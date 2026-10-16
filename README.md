# Hello, I'm Adi! 👋

I'm a security engineer in Jerusalem working on application security and DevSecOps. I build
backend services in Rust and Python with the security built in rather than bolted on, and
CI pipelines that catch insecure infrastructure before it reaches production.

CompTIA Security+ · B.S. Information Technology & Management, University at Buffalo (Magna Cum Laude) · English (native) / Hebrew (fluent)

## 🛡️ CyberSecurity Projects

### 🦀 Rust & Application Security
**[axum-jwt-auth — JWT Authentication Service](https://github.com/Adi-Czobel/axum-jwt-auth)**
- Passwords hashed with Argon2id at OWASP settings, so stolen hashes are expensive to crack
- Refresh tokens work once. If a used one shows up again, every token in that chain is cancelled, because the server cannot tell the thief from the real user
- The JWT algorithm is fixed instead of read from the token, which blocks the `alg=none` and RS256-to-HS256 tricks
- Wrong password and unknown account return the same answer, and take the same amount of time, so you cannot use either to find out which emails are registered
- 27 tests, clippy clean, and a section in the README on what it still does not do

---
### 🔐 DevSecOps & Supply Chain
**[Secure IaC Pipeline](https://github.com/Adi-Czobel/Demo)**
- Checkov, Hadolint and Terraform validation run on every pull request and block the merge if they fail
- CodeQL, Trivy and gitleaks report findings to the repo's Security tab instead of blocking, so false positives do not stop work
- Tagged releases build a container image, attach a list of everything inside it (SBOM), and sign it with cosign using keyless signing, so there is no private key sitting in a secret waiting to leak
- gitleaks scans the whole git history, because deleting a password in a later commit does not make it safe

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
