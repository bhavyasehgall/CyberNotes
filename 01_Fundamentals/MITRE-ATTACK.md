# MITRE ATT&CK Framework

The **MITRE ATT&CK Framework** is a globally recognized knowledge base of **real-world cyberattack behaviors**. It documents how attackers operate by organizing their **Tactics, Techniques, and Procedures (TTPs)**.

Unlike traditional security frameworks that focus on defense, MITRE ATT&CK focuses on **attacker behavior**. It helps organizations understand how adversaries compromise systems, move through networks, maintain persistence, steal data, and achieve their objectives.

Today, MITRE ATT&CK is widely used by:

- Security Operations Centers (SOC)
- Threat Hunters
- Incident Response Teams
- Blue Teams
- Red Teams
- Purple Teams
- Malware Analysts
- Security Engineers

---

# Table of Contents

- What is MITRE ATT&CK?
- Why is it Important?
- History
- ATT&CK Matrices
- Tactics
- Techniques
- Procedures
- Tactics Explained
- ATT&CK Workflow
- ATT&CK vs Cyber Kill Chain
- ATT&CK Use Cases
- Benefits
- Limitations
- Best Practices
- Interview Questions
- Summary

---

# What is MITRE ATT&CK?

**MITRE ATT&CK** stands for:

> **Adversarial Tactics, Techniques, and Common Knowledge**

It is a publicly available framework that documents the methods attackers use during real-world cyberattacks.

Instead of describing attacks as a simple sequence of stages, ATT&CK maps the individual techniques attackers use throughout an intrusion.

---

# Why is MITRE ATT&CK Important?

MITRE ATT&CK helps organizations:

- Understand attacker behavior.
- Improve threat detection.
- Build better security monitoring.
- Perform threat hunting.
- Simulate attacks.
- Measure security coverage.
- Improve incident response.

Many security vendors also map their products to the ATT&CK framework.

---

# History

The framework was developed by the **MITRE Corporation** and released publicly in **2015**.

It is continuously updated using information gathered from:

- Real-world cyber incidents
- Threat intelligence
- Malware analysis
- Security researchers
- Nation-state activity

---

# ATT&CK Matrices

MITRE provides different matrices for different environments.

| Matrix | Purpose |
|---------|----------|
| Enterprise | Windows, Linux, macOS, Cloud, Azure AD, SaaS |
| Mobile | Android and iOS attacks |
| ICS | Industrial Control Systems |

The **Enterprise Matrix** is the most widely used.

---

# Tactics, Techniques, and Procedures (TTPs)

---

# Tactics

A **Tactic** describes **why** an attacker performs an action.

It represents the attacker's objective at a particular stage.

Example:

- Initial Access
- Persistence
- Privilege Escalation

---

# Techniques

A **Technique** describes **how** an attacker achieves a tactic.

Example:

For the tactic **Initial Access**, techniques include:

- Phishing
- Exploiting Public-Facing Applications
- Valid Accounts

---

# Procedures

A **Procedure** is the specific implementation of a technique by an attacker.

Example:

An attacker sends a phishing email containing a malicious Microsoft Word document that installs malware.

---

# Relationship Between TTPs

```text
Goal
 │
 ▼
Tactic (Why?)
 │
 ▼
Technique (How?)
 │
 ▼
Procedure (Specific implementation)
```

---

# Enterprise ATT&CK Tactics

The Enterprise ATT&CK Matrix currently contains the following tactics:

| Tactic | Purpose |
|---------|----------|
| Reconnaissance | Gather information about the target |
| Resource Development | Prepare infrastructure and resources |
| Initial Access | Gain entry into the target environment |
| Execution | Run malicious code |
| Persistence | Maintain long-term access |
| Privilege Escalation | Gain higher permissions |
| Defense Evasion | Avoid detection |
| Credential Access | Steal usernames and passwords |
| Discovery | Learn about the environment |
| Lateral Movement | Move between systems |
| Collection | Gather sensitive data |
| Command and Control | Communicate with attacker infrastructure |
| Exfiltration | Steal data from the environment |
| Impact | Disrupt, destroy, or encrypt systems |

---

# Example Attack Using ATT&CK

Suppose an attacker launches a ransomware attack.

| Tactic | Example Technique |
|---------|-------------------|
| Initial Access | Phishing |
| Execution | PowerShell |
| Persistence | Scheduled Task |
| Privilege Escalation | Exploiting a Vulnerability |
| Credential Access | Credential Dumping |
| Discovery | System Information Discovery |
| Lateral Movement | Remote Services |
| Collection | Archive Collected Data |
| Command and Control | HTTPS |
| Impact | Data Encrypted for Impact |

This mapping helps defenders identify where they can detect or stop the attack.

---

# ATT&CK Workflow

```text
Attacker Goal
       │
       ▼
Choose Tactic
       │
       ▼
Use Technique
       │
       ▼
Perform Procedure
       │
       ▼
Security Detection
       │
       ▼
Incident Response
```

---

# ATT&CK Navigator

The **ATT&CK Navigator** is an official visualization tool for the ATT&CK framework.

It allows security teams to:

- View the ATT&CK Matrix
- Highlight detected techniques
- Identify defensive gaps
- Compare threat actor behavior
- Plan detection improvements

---

# ATT&CK vs Cyber Kill Chain

| MITRE ATT&CK | Cyber Kill Chain |
|---------------|------------------|
| Knowledge base of attacker behavior | Linear attack lifecycle |
| Focuses on tactics and techniques | Focuses on attack stages |
| Very detailed | High-level overview |
| Continuously updated | Relatively static |
| Excellent for detection engineering | Excellent for understanding attack flow |

Both frameworks complement each other and are frequently used together.

---

# ATT&CK Use Cases

## Security Operations Center (SOC)

SOC analysts map security alerts to ATT&CK techniques to understand attacker activity.

---

## Threat Hunting

Threat hunters proactively search for evidence of ATT&CK techniques in logs and endpoint telemetry.

---

## Incident Response

Responders identify which tactics and techniques were used during an attack to guide containment and recovery.

---

## Red Team

Red Teams emulate attacker behavior using ATT&CK techniques to test an organization's defenses.

---

## Blue Team

Blue Teams develop detections and defensive controls based on ATT&CK techniques.

---

## Purple Team

Purple Teams use ATT&CK to coordinate collaboration between Red and Blue Teams, improving overall security.

---

# Benefits

- Based on real-world attacker behavior.
- Standardizes security terminology.
- Improves detection engineering.
- Supports threat hunting.
- Enhances incident response.
- Identifies defensive gaps.
- Widely supported by security vendors.

---

# Limitations

- Can be overwhelming for beginners due to its size.
- Requires continuous updates as new techniques emerge.
- Does not prescribe specific defensive controls.
- Should be used alongside other frameworks and security practices.

---

# Best Practices

- Map security alerts to ATT&CK techniques.
- Develop detections for high-risk techniques.
- Use ATT&CK during threat hunting exercises.
- Perform regular Purple Team exercises.
- Review ATT&CK coverage after security incidents.
- Combine ATT&CK with the Cyber Kill Chain and Defense in Depth strategies.
- Keep detection rules aligned with the latest ATT&CK updates.

---

# Key Points

- MITRE ATT&CK is a knowledge base of attacker behavior.
- It is based on Tactics, Techniques, and Procedures (TTPs).
- It is used by SOCs, Threat Hunters, Incident Responders, Red Teams, Blue Teams, and Purple Teams.
- The Enterprise Matrix is the most commonly used ATT&CK matrix.
- ATT&CK improves threat detection, security monitoring, and defensive planning.

---

# Interview Questions

### 1. What is MITRE ATT&CK?

MITRE ATT&CK is a publicly available knowledge base that documents real-world attacker tactics, techniques, and procedures (TTPs).

---

### 2. What does ATT&CK stand for?

**Adversarial Tactics, Techniques, and Common Knowledge.**

---

### 3. What are TTPs?

- **Tactics** – Why an attacker performs an action.
- **Techniques** – How the attacker performs the action.
- **Procedures** – The specific implementation of a technique.

---

### 4. What is the Enterprise ATT&CK Matrix?

It is the ATT&CK matrix that documents attacker behavior across enterprise environments, including Windows, Linux, macOS, cloud platforms, and enterprise applications.

---

### 5. What is the ATT&CK Navigator?

The ATT&CK Navigator is an official visualization tool that helps organizations analyze, customize, and assess their ATT&CK coverage.

---

### 6. How is MITRE ATT&CK different from the Cyber Kill Chain?

The Cyber Kill Chain describes the stages of an attack, while MITRE ATT&CK provides a detailed catalog of attacker tactics and techniques used throughout those stages.

---

### 7. Why do SOC analysts use MITRE ATT&CK?

SOC analysts use ATT&CK to map alerts to attacker techniques, improve detection rules, prioritize investigations, and understand adversary behavior.

---

# Summary

The MITRE ATT&CK Framework is one of the most important resources in modern cybersecurity. By documenting real-world adversary Tactics, Techniques, and Procedures (TTPs), it enables organizations to understand how attackers operate, improve threat detection, guide incident response, and strengthen defensive capabilities. Used alongside frameworks such as the Cyber Kill Chain and Defense in Depth, MITRE ATT&CK provides a comprehensive approach to understanding and defending against cyber threats.

---

## Next Topic

➡️ **Cybersecurity-Frameworks.md** — Learn about widely adopted cybersecurity frameworks such as **NIST Cybersecurity Framework (CSF), ISO/IEC 27001, CIS Controls, COBIT, SOC 2, and OWASP ASVS**, and understand how organizations use them to build, assess, and improve their security programs.
