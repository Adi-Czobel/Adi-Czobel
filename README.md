# Hello, I'm Adi! 👋

## 🛡️ CyberSecurity Projects

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

## 📫 Connect with me
[![LinkedIn](https://cdn-icons-png.flaticon.com/512/174/174857.png)](https://www.linkedin.com/in/adiczobel)
