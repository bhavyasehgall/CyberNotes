# Cybersecurity Domains

> Understanding the different domains of cybersecurity is essential because cybersecurity is a broad field. No single professional is expected to master every area. Instead, cybersecurity is divided into specialized domains, each focusing on protecting a specific aspect of information systems.

---

# Table of Contents

1. Introduction
2. What is a Cybersecurity Domain?
3. Why are Cybersecurity Domains Important?
4. Major Cybersecurity Domains
5. Domain Comparison Table
6. Choosing the Right Domain
7. How Domains Work Together
8. Career Roadmap
9. Summary
10. Interview Questions

---

# Introduction

Cybersecurity is the practice of protecting digital systems, networks, applications, devices, and data from cyber threats.

As technology evolved, cybersecurity became too large for one person to specialize in everything. Today, it is divided into multiple **domains**, where each domain focuses on protecting a specific part of an organization's infrastructure.

For example:

- A SOC Analyst monitors security alerts.
- A Penetration Tester finds vulnerabilities.
- A Cloud Security Engineer secures AWS or Azure.
- A Digital Forensics Analyst investigates cybercrimes.

Although these professionals perform different tasks, they all work together to improve an organization's security.

---

# What is a Cybersecurity Domain?

A **cybersecurity domain** is a specialized area of cybersecurity that focuses on protecting a particular type of technology, data, or process.

Think of cybersecurity like a hospital.

| Hospital | Cybersecurity |
|-----------|---------------|
| Cardiologist | Network Security Engineer |
| Dentist | Application Security Engineer |
| Neurologist | Malware Analyst |
| Surgeon | Incident Response Team |

Just as doctors specialize in different areas of medicine, cybersecurity professionals specialize in different domains.

---

# Why are Cybersecurity Domains Important?

Organizations use different technologies:

- Networks
- Websites
- Mobile Apps
- Cloud Services
- Databases
- IoT Devices
- Email Systems

Each technology has unique security challenges.

Instead of relying on one expert for everything, organizations hire specialists for different domains.

Benefits include:

- Better protection
- Faster incident response
- Specialized expertise
- Improved compliance
- Reduced business risk

---

# Major Cybersecurity Domains

---

# 1. Network Security

## Purpose

Protect computer networks from unauthorized access, attacks, and misuse.

## What it Protects

- Routers
- Switches
- Firewalls
- Servers
- VPNs
- Wireless Networks

## Common Tasks

- Configure firewalls
- Monitor traffic
- Block malicious IPs
- Secure Wi-Fi
- Create network segmentation

## Common Tools

- Wireshark
- Nmap
- pfSense
- Cisco ASA
- Snort
- Suricata

## Real-World Example

A company firewall blocks incoming traffic from known malicious IP addresses before attackers reach internal servers.

---

# 2. Application Security

## Purpose

Protect software applications throughout their lifecycle.

## Focus Areas

- Secure coding
- Code review
- Vulnerability testing
- Security patches

## Common Vulnerabilities

- SQL Injection
- Cross-Site Scripting (XSS)
- CSRF
- IDOR
- Authentication flaws

## Common Tools

- Burp Suite
- OWASP ZAP
- Snyk
- SonarQube
- Semgrep

## Example

A banking application validates user input to prevent SQL Injection attacks.

---

# 3. Web Security

Web Security focuses specifically on protecting websites and web applications.

Topics include:

- HTTP & HTTPS
- Cookies
- Sessions
- Authentication
- APIs
- JWT
- OAuth
- CORS
- CSP

Common Tools

- Burp Suite
- OWASP ZAP
- ffuf
- Nikto

---

# 4. Cloud Security

Cloud Security protects cloud environments such as:

- AWS
- Microsoft Azure
- Google Cloud Platform (GCP)

## Responsibilities

- Secure cloud storage
- Identity management
- Encryption
- Monitoring
- Cloud compliance

## Common Tools

- AWS Security Hub
- AWS IAM
- Trivy
- Prisma Cloud
- Wiz

---

# 5. Endpoint Security

Endpoints include:

- Laptops
- Desktops
- Mobile devices
- Servers

Security focuses on:

- Antivirus
- EDR
- Patch Management
- Device Encryption
- Device Monitoring

Popular Tools

- Microsoft Defender
- CrowdStrike
- SentinelOne

---

# 6. Mobile Security

Protects Android and iOS devices.

Topics include:

- APK Analysis
- Malware Detection
- Reverse Engineering
- Mobile Permissions
- Secure Storage

Common Tools

- MobSF
- jadx
- APKTool
- ADB

---

# 7. Identity and Access Management (IAM)

IAM ensures only authorized users can access resources.

Topics include:

- Authentication
- Authorization
- Single Sign-On (SSO)
- Multi-Factor Authentication (MFA)
- Role-Based Access Control (RBAC)

Common Platforms

- Okta
- Azure AD
- Keycloak

---

# 8. Digital Forensics

Digital Forensics investigates cyber incidents.

Responsibilities

- Collect evidence
- Recover deleted files
- Analyze malware
- Investigate attacks
- Prepare legal evidence

Tools

- Autopsy
- FTK
- Volatility
- Magnet AXIOM

---

# 9. Incident Response

Incident Response focuses on handling security incidents.

Lifecycle

1. Preparation
2. Detection
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

Tools

- TheHive
- Cortex
- Splunk
- Microsoft Sentinel

---

# 10. Security Operations Center (SOC)

A SOC continuously monitors an organization's security.

Responsibilities

- Monitor alerts
- Investigate suspicious activity
- Threat hunting
- Incident response
- Log analysis

Common Tools

- Splunk
- QRadar
- Microsoft Sentinel
- Elastic SIEM

---

# 11. Malware Analysis

Malware analysts study malicious software.

Types of Malware

- Virus
- Worm
- Trojan
- Ransomware
- Rootkit
- Spyware

Tools

- Ghidra
- IDA Free
- x64dbg
- PEStudio
- VirusTotal

---

# 12. Penetration Testing

Penetration testers simulate cyberattacks.

Typical Process

1. Reconnaissance
2. Enumeration
3. Vulnerability Analysis
4. Exploitation
5. Post Exploitation
6. Reporting

Common Tools

- Nmap
- Burp Suite
- Metasploit
- SQLMap
- Hydra
- Gobuster

---

# 13. Threat Intelligence

Threat Intelligence collects information about attackers.

Sources

- Malware reports
- OSINT
- Security blogs
- Dark Web
- IOC feeds

Frameworks

- MITRE ATT&CK
- STIX
- TAXII

---

# 14. Governance, Risk, and Compliance (GRC)

GRC ensures organizations meet legal and security requirements.

Focus Areas

- Policies
- Risk Assessment
- Compliance Audits
- Security Standards
- Business Continuity

Common Standards

- ISO 27001
- NIST CSF
- PCI DSS
- GDPR
- HIPAA

---

# 15. Cloud & DevSecOps Security

DevSecOps integrates security into software development.

Responsibilities

- Secure CI/CD
- Container Security
- Infrastructure as Code
- Secrets Management
- Automated Security Testing

Tools

- Docker
- Kubernetes
- Trivy
- GitHub Actions
- Jenkins

---

# Domain Comparison

| Domain | Main Goal | Example Tools |
|---------|-----------|---------------|
| Network Security | Protect Networks | Wireshark, Snort |
| Application Security | Secure Software | Burp Suite |
| Web Security | Protect Websites | Burp, ZAP |
| Cloud Security | Secure Cloud | AWS IAM, Trivy |
| SOC | Monitor Threats | Splunk |
| Incident Response | Handle Attacks | TheHive |
| Malware Analysis | Analyze Malware | Ghidra |
| Digital Forensics | Investigate Incidents | Autopsy |
| Penetration Testing | Find Vulnerabilities | Nmap |
| IAM | Manage User Access | Okta |
| GRC | Compliance | ISO 27001 |
| DevSecOps | Secure Development | Jenkins |

---

# How Domains Work Together

```text
                  Users
                    │
                    ▼
           Identity & Access
                    │
                    ▼
             Network Security
                    │
                    ▼
            Application Security
                    │
                    ▼
              Cloud Security
                    │
                    ▼
              SOC Monitoring
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
 Threat Intelligence   Incident Response
          │                   │
          └─────────┬─────────┘
                    ▼
           Digital Forensics
                    │
                    ▼
             Lessons Learned
```

---

# Which Domain Should You Choose?

| If You Like... | Consider... |
|----------------|-------------|
| Networking | Network Security |
| Programming | Application Security |
| Breaking Systems | Penetration Testing |
| Monitoring | SOC |
| Investigating | Digital Forensics |
| Cloud Platforms | Cloud Security |
| Policies & Audits | GRC |
| Android Apps | Mobile Security |
| Reverse Engineering | Malware Analysis |
| Automation | DevSecOps |

---

# Career Roadmap

```text
Cybersecurity Fundamentals
            │
            ▼
Networking + Linux
            │
            ▼
Choose a Domain
            │
            ▼
Learn Tools
            │
            ▼
Practice Labs
            │
            ▼
Earn Certifications
            │
            ▼
Build Projects
            │
            ▼
Get a Cybersecurity Job
```

---

# Key Takeaways

- Cybersecurity consists of many specialized domains.
- Every domain has different responsibilities and tools.
- All domains work together to protect organizations.
- Strong fundamentals in networking, Linux, and operating systems are useful regardless of the domain you choose.
- Specializing in one domain does not prevent you from learning others over time.

---

# Interview Questions

### 1. What is a cybersecurity domain?

A specialized area of cybersecurity focused on protecting a particular aspect of technology, such as networks, applications, cloud infrastructure, or digital identities.

---

### 2. What is the difference between Network Security and Application Security?

- **Network Security** protects the communication infrastructure (routers, switches, firewalls, traffic).
- **Application Security** protects software by preventing vulnerabilities such as SQL Injection and Cross-Site Scripting.

---

### 3. What does a SOC Analyst do?

A SOC Analyst monitors security events, investigates alerts, detects attacks, and assists with incident response.

---

### 4. Why is Cloud Security important?

Organizations increasingly store applications and data in the cloud. Cloud Security ensures these resources are configured securely, protected from unauthorized access, and compliant with security standards.

---

### 5. Which cybersecurity domain is best for beginners?

There is no single "best" domain. A strong foundation in networking, Linux, operating systems, and cybersecurity fundamentals is recommended before specializing based on your interests and career goals.

---

# Summary

Cybersecurity is a diverse field composed of multiple specialized domains. Each domain addresses unique security challenges, from protecting networks and applications to investigating incidents and securing cloud environments. Understanding these domains helps you identify career paths, build the right skills, and appreciate how different security teams collaborate to defend modern organizations.

---

## Next Topic

➡️ **CIA-Triad.md** — Learn about the three core principles of information security: **Confidentiality, Integrity, and Availability (CIA)**, and why they are the foundation of every cybersecurity program.
