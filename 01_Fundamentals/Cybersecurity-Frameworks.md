# Cybersecurity Frameworks

Cybersecurity frameworks are **structured sets of guidelines, best practices, standards, and controls** that help organizations manage cybersecurity risks, protect information systems, detect threats, respond to incidents, and recover from cyberattacks.

Instead of creating security policies from scratch, organizations use established frameworks to build a consistent and effective security program.

Cybersecurity frameworks are used by:

- Businesses
- Government agencies
- Financial institutions
- Healthcare organizations
- Cloud providers
- Educational institutions

---

# Table of Contents

- What is a Cybersecurity Framework?
- Why are Frameworks Important?
- Types of Frameworks
- NIST Cybersecurity Framework (CSF)
- NIST Risk Management Framework (RMF)
- ISO/IEC 27001
- CIS Controls
- COBIT
- SOC 2
- PCI DSS
- HIPAA
- GDPR
- OWASP ASVS
- MITRE ATT&CK
- Cyber Kill Chain
- Framework Comparison
- Choosing the Right Framework
- Best Practices
- Interview Questions
- Summary

---

# What is a Cybersecurity Framework?

A cybersecurity framework is a structured approach that helps organizations:

- Identify cybersecurity risks.
- Protect systems and data.
- Detect security incidents.
- Respond to cyberattacks.
- Recover from disruptions.
- Continuously improve security.

Frameworks provide guidance rather than specific products or tools.

---

# Why are Frameworks Important?

Cybersecurity frameworks help organizations:

- Reduce security risks.
- Meet legal and regulatory requirements.
- Standardize security practices.
- Improve incident response.
- Protect sensitive information.
- Measure security maturity.
- Build customer trust.

---

# Types of Frameworks

Cybersecurity frameworks generally fall into three categories.

| Type | Purpose | Example |
|------|---------|---------|
| Framework | Provides overall guidance | NIST CSF |
| Standard | Defines security requirements | ISO/IEC 27001 |
| Control Set | Lists recommended security controls | CIS Controls |

---

# NIST Cybersecurity Framework (CSF)

The **NIST Cybersecurity Framework (CSF)** was developed by the **National Institute of Standards and Technology (NIST)**.

It provides a flexible, risk-based approach to managing cybersecurity.

### Core Functions

```text
Govern
   │
Identify
   │
Protect
   │
Detect
   │
Respond
   │
Recover
```

### Explanation

| Function | Purpose |
|----------|---------|
| Govern | Establish cybersecurity governance, strategy, roles, and risk oversight. |
| Identify | Understand assets, risks, and business environment. |
| Protect | Implement safeguards to protect systems and data. |
| Detect | Identify cybersecurity events quickly. |
| Respond | Contain and manage incidents. |
| Recover | Restore operations and improve resilience. |

---

# NIST Risk Management Framework (RMF)

The **NIST RMF** provides a structured process for managing security and privacy risks throughout a system's lifecycle.

### RMF Steps

1. Prepare
2. Categorize
3. Select Controls
4. Implement Controls
5. Assess Controls
6. Authorize
7. Monitor

RMF is commonly used by U.S. government agencies and organizations following NIST guidance.

---

# ISO/IEC 27001

ISO/IEC 27001 is the international standard for establishing an **Information Security Management System (ISMS).**

It helps organizations:

- Protect information assets.
- Manage information security risks.
- Improve security continuously.
- Demonstrate compliance to customers and partners.

Key concepts include:

- Risk assessment
- Risk treatment
- Security controls
- Internal audits
- Continuous improvement

---

# CIS Controls

The **Center for Internet Security (CIS) Controls** are a prioritized set of security best practices.

Examples include:

- Asset inventory
- Secure configuration
- Vulnerability management
- Access control
- Audit logging
- Malware protection
- Security awareness training

CIS Controls are practical and suitable for organizations of all sizes.

---

# COBIT

**COBIT (Control Objectives for Information and Related Technologies)** is an IT governance and management framework developed by ISACA.

COBIT focuses on:

- IT governance
- Risk management
- Compliance
- Business alignment
- Performance measurement

It is commonly used by large enterprises.

---

# SOC 2

SOC 2 is an auditing framework developed by the **American Institute of Certified Public Accountants (AICPA)**.

It evaluates service organizations using five **Trust Services Criteria**.

| Principle | Purpose |
|------------|---------|
| Security | Protect systems against unauthorized access |
| Availability | Ensure systems remain operational |
| Processing Integrity | Ensure accurate processing |
| Confidentiality | Protect confidential information |
| Privacy | Protect personal information |

SOC 2 is widely used by cloud service providers and SaaS companies.

---

# PCI DSS

**Payment Card Industry Data Security Standard (PCI DSS)** is a security standard for organizations that process, store, or transmit payment card data.

Objectives include:

- Protect cardholder data.
- Maintain secure networks.
- Encrypt sensitive information.
- Monitor access.
- Perform regular security testing.

---

# HIPAA

The **Health Insurance Portability and Accountability Act (HIPAA)** is a U.S. law that protects electronic protected health information (ePHI).

It requires healthcare organizations to implement administrative, physical, and technical safeguards.

---

# GDPR

The **General Data Protection Regulation (GDPR)** is a European Union regulation that protects the personal data and privacy of individuals.

Key principles include:

- Lawful processing
- Data minimization
- Accuracy
- Integrity and confidentiality
- Accountability

Organizations handling EU residents' data must comply with GDPR regardless of where they are located.

---

# OWASP ASVS

The **OWASP Application Security Verification Standard (ASVS)** provides security requirements for designing, developing, testing, and verifying secure web applications.

It covers areas such as:

- Authentication
- Authorization
- Session Management
- Input Validation
- Cryptography
- API Security
- Logging
- Configuration

ASVS is widely used during secure software development and security assessments.

---

# MITRE ATT&CK

MITRE ATT&CK is a knowledge base of real-world attacker **Tactics, Techniques, and Procedures (TTPs).**

Organizations use ATT&CK to:

- Improve threat detection
- Support threat hunting
- Map security controls
- Simulate attacks
- Enhance incident response

---

# Cyber Kill Chain

The **Cyber Kill Chain**, developed by Lockheed Martin, divides a cyberattack into seven stages:

1. Reconnaissance
2. Weaponization
3. Delivery
4. Exploitation
5. Installation
6. Command and Control
7. Actions on Objectives

It helps defenders identify where attacks can be interrupted.

---

# Framework Comparison

| Framework | Primary Purpose | Common Users |
|-----------|-----------------|--------------|
| NIST CSF | Cybersecurity risk management | Public and private organizations |
| NIST RMF | Risk management lifecycle | Government and regulated industries |
| ISO/IEC 27001 | Information Security Management System (ISMS) | Organizations seeking certification |
| CIS Controls | Practical security controls | Organizations of all sizes |
| COBIT | IT governance | Large enterprises |
| SOC 2 | Security assurance for service providers | SaaS and cloud providers |
| PCI DSS | Payment card security | Merchants and payment processors |
| HIPAA | Healthcare data protection | Healthcare organizations |
| GDPR | Personal data privacy | Organizations handling EU personal data |
| OWASP ASVS | Application security verification | Software developers and testers |
| MITRE ATT&CK | Adversary behavior knowledge base | SOC, Threat Hunters, Red & Blue Teams |
| Cyber Kill Chain | Attack lifecycle model | SOC and Incident Response teams |

---

# Choosing the Right Framework

The appropriate framework depends on the organization's goals.

| Organization | Recommended Frameworks |
|--------------|------------------------|
| Small Business | NIST CSF, CIS Controls |
| Enterprise | NIST CSF, ISO/IEC 27001, CIS Controls |
| Government | NIST RMF, NIST CSF |
| SaaS Provider | SOC 2, NIST CSF |
| E-commerce | PCI DSS, NIST CSF |
| Healthcare | HIPAA, ISO/IEC 27001 |
| Software Development | OWASP ASVS, NIST CSF |

Many organizations use multiple frameworks together.

---

# Best Practices

- Select frameworks that align with business objectives.
- Conduct regular risk assessments.
- Review and update security controls periodically.
- Train employees on security policies.
- Monitor compliance continuously.
- Perform regular security audits.
- Use multiple frameworks when appropriate.
- Continuously improve the security program based on assessments and incidents.

---

# Key Points

- Cybersecurity frameworks provide structured guidance for managing cybersecurity.
- NIST CSF is one of the most widely adopted cybersecurity frameworks.
- ISO/IEC 27001 focuses on establishing and maintaining an Information Security Management System (ISMS).
- CIS Controls provide practical, prioritized security controls.
- SOC 2 evaluates the security of service organizations.
- PCI DSS protects payment card data.
- HIPAA safeguards healthcare information.
- GDPR protects personal data and privacy.
- OWASP ASVS focuses on application security.
- MITRE ATT&CK and the Cyber Kill Chain help organizations understand and defend against attacker behavior.

---

# Interview Questions

### 1. What is a cybersecurity framework?

A cybersecurity framework is a structured set of guidelines, best practices, and controls that helps organizations manage cybersecurity risks and improve their security posture.

---

### 2. What are the six core functions of NIST CSF 2.0?

- Govern
- Identify
- Protect
- Detect
- Respond
- Recover

---

### 3. What is ISO/IEC 27001?

ISO/IEC 27001 is an international standard for establishing, implementing, maintaining, and continually improving an Information Security Management System (ISMS).

---

### 4. What are CIS Controls?

CIS Controls are a prioritized set of cybersecurity best practices that help organizations defend against common cyber threats.

---

### 5. What is the purpose of SOC 2?

SOC 2 evaluates how service organizations protect customer data based on the Trust Services Criteria: Security, Availability, Processing Integrity, Confidentiality, and Privacy.

---

### 6. What is the difference between MITRE ATT&CK and the Cyber Kill Chain?

MITRE ATT&CK is a detailed knowledge base of attacker tactics and techniques, while the Cyber Kill Chain describes the high-level stages of a cyberattack.

---

### 7. Can organizations use more than one framework?

Yes. Many organizations combine frameworks, standards, and regulations to meet their security, compliance, and business requirements.

---

# Summary

Cybersecurity frameworks provide organizations with proven approaches to managing security risks, protecting information assets, and responding to cyber threats. Frameworks such as **NIST CSF**, **ISO/IEC 27001**, **CIS Controls**, and **COBIT** establish governance and security practices, while standards and regulations like **SOC 2**, **PCI DSS**, **HIPAA**, and **GDPR** address specific compliance requirements. Models such as **MITRE ATT&CK** and the **Cyber Kill Chain** help security teams understand adversary behavior and improve detection and response capabilities. Selecting and implementing the right combination of frameworks enables organizations to build a mature, resilient, and continuously improving cybersecurity program.

---

## Next Topic

➡️ **Security-Policies-and-Standards.md** — Learn how organizations define **policies, standards, procedures, guidelines, and baselines** to establish clear security expectations and ensure consistent implementation of cybersecurity controls.
