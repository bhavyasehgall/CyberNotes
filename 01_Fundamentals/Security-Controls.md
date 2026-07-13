# Security Controls

Security controls are the safeguards implemented to protect an organization's assets from cyber threats. They help reduce risk by preventing attacks, detecting suspicious activities, minimizing damage, and supporting recovery after an incident.

Security controls are the foundation of every cybersecurity program. Whether it is a firewall, a password policy, CCTV cameras, or employee security training, they all serve as security controls.

---

# Table of Contents

- What are Security Controls?
- Why are Security Controls Important?
- Objectives of Security Controls
- Categories of Security Controls
  - Administrative Controls
  - Technical Controls
  - Physical Controls
- Functional Types of Security Controls
- Defense in Depth
- Real-World Example
- Best Practices
- Interview Questions
- Summary

---

# What are Security Controls?

A **Security Control** is any measure used to reduce cybersecurity risks by protecting systems, networks, applications, people, or data.

Security controls help organizations:

- Prevent attacks
- Detect attacks
- Respond to incidents
- Recover from attacks

A good cybersecurity strategy always combines multiple security controls instead of relying on just one.

---

# Why are Security Controls Important?

Without security controls:

- Anyone could access sensitive information.
- Malware could spread easily.
- Attackers could steal customer data.
- Organizations could suffer financial and reputational losses.

Security controls reduce these risks and improve an organization's overall security posture.

---

# Objectives of Security Controls

The primary objectives are to:

- Protect Confidentiality
- Maintain Integrity
- Ensure Availability
- Reduce cybersecurity risks
- Meet legal and regulatory requirements
- Protect business operations
- Detect and respond to threats quickly

---

# Categories of Security Controls

Security controls are generally divided into three categories:

1. Administrative Controls
2. Technical Controls
3. Physical Controls

---

# 1. Administrative Controls

## Definition

Administrative controls are policies, procedures, standards, and guidelines that define how security should be managed within an organization.

These controls focus on **people and processes**.

---

## Examples

- Information Security Policy
- Password Policy
- Acceptable Use Policy
- Incident Response Plan
- Disaster Recovery Plan
- Security Awareness Training
- Background Verification
- Employee Onboarding and Offboarding
- Vendor Risk Management

---

## Real-World Example

A company requires all employees to complete cybersecurity awareness training every six months to recognize phishing emails.

---

## Advantages

- Reduces human error
- Standardizes security practices
- Improves compliance
- Defines responsibilities

---

# 2. Technical Controls

## Definition

Technical controls use hardware or software to protect information systems.

These are also called **Logical Controls**.

---

## Examples

### Network Security

- Firewalls
- IDS
- IPS
- VPN

### Endpoint Security

- Antivirus
- EDR
- Device Encryption

### Identity Security

- Multi-Factor Authentication (MFA)
- Role-Based Access Control (RBAC)
- Single Sign-On (SSO)

### Data Security

- Encryption
- Hashing
- Digital Signatures

### Monitoring

- SIEM
- Log Management
- Security Monitoring

---

## Real-World Example

A firewall blocks incoming traffic from malicious IP addresses before it reaches the company's internal network.

---

## Advantages

- Automated protection
- Fast detection
- Continuous monitoring
- Scalable security

---

# 3. Physical Controls

## Definition

Physical controls protect buildings, equipment, and people from unauthorized physical access.

---

## Examples

- Security Guards
- CCTV Cameras
- Biometric Access
- Smart Cards
- Locked Server Rooms
- Fences
- Alarm Systems
- Fire Suppression Systems

---

## Real-World Example

Only authorized employees can enter the server room using biometric fingerprint authentication.

---

## Advantages

- Prevents physical theft
- Protects critical infrastructure
- Reduces unauthorized access

---

# Functional Types of Security Controls

Security controls can also be classified based on **their purpose**.

---

# 1. Preventive Controls

## Purpose

Prevent attacks before they happen.

### Examples

- Firewalls
- MFA
- Encryption
- Strong Password Policies
- Secure Configuration

---

# 2. Detective Controls

## Purpose

Identify attacks that are occurring or have already occurred.

### Examples

- IDS
- SIEM
- Log Monitoring
- Security Audits
- CCTV

---

# 3. Corrective Controls

## Purpose

Reduce damage after an incident and restore normal operations.

### Examples

- Malware Removal
- Security Patches
- Password Reset
- System Reconfiguration

---

# 4. Deterrent Controls

## Purpose

Discourage attackers from attempting an attack.

### Examples

- Warning Banners
- CCTV Cameras
- Security Guards
- Legal Notices

---

# 5. Compensating Controls

## Purpose

Provide an alternative security measure when the preferred control cannot be implemented.

### Example

If a legacy application does not support MFA, access may be restricted through a VPN and additional monitoring.

---

# 6. Recovery Controls

## Purpose

Restore systems and data after a security incident.

### Examples

- Data Backups
- Disaster Recovery Plan
- Business Continuity Plan
- Backup Servers

---

# Security Control Summary

| Functional Type | Purpose | Examples |
|-----------------|---------|----------|
| Preventive | Stop attacks | Firewall, MFA |
| Detective | Detect attacks | IDS, SIEM |
| Corrective | Fix issues | Patching, Malware Removal |
| Deterrent | Discourage attacks | CCTV, Warning Signs |
| Compensating | Alternative protection | VPN, Additional Monitoring |
| Recovery | Restore operations | Backups, Disaster Recovery |

---

# Administrative vs Technical vs Physical Controls

| Category | Focus | Examples |
|----------|-------|----------|
| Administrative | Policies and People | Security Policy, Training |
| Technical | Hardware and Software | Firewall, Antivirus, MFA |
| Physical | Buildings and Equipment | CCTV, Biometrics, Locks |

---

# Defense in Depth

Organizations should never rely on a single security control.

Instead, they implement **multiple layers of protection**.

```text
Internet
      │
      ▼
Firewall
      │
      ▼
IDS / IPS
      │
      ▼
VPN
      │
      ▼
Authentication (MFA)
      │
      ▼
Application Security
      │
      ▼
Database Encryption
      │
      ▼
Regular Backups
```

If one layer fails, another layer continues to protect the organization.

This approach is known as **Defense in Depth**.

---

# Real-World Example

## Online Banking System

### Administrative Controls

- Password Policy
- Employee Security Training
- Incident Response Plan

### Technical Controls

- Firewall
- MFA
- HTTPS
- Database Encryption
- SIEM

### Physical Controls

- CCTV
- Biometric Server Room Access
- Security Guards

Together, these controls protect customer information and ensure secure banking services.

---

# Best Practices

- Apply the Principle of Least Privilege.
- Keep systems updated with security patches.
- Enable Multi-Factor Authentication.
- Encrypt sensitive information.
- Perform regular security audits.
- Monitor logs continuously.
- Train employees to recognize phishing attacks.
- Test backup and disaster recovery procedures.
- Review access permissions regularly.
- Use layered security instead of relying on a single control.

---

# Key Points

- Security controls reduce cybersecurity risk.
- Controls can be Administrative, Technical, or Physical.
- Functional controls include Preventive, Detective, Corrective, Deterrent, Compensating, and Recovery controls.
- Multiple security controls working together provide stronger protection than a single control.
- Effective security requires a combination of technology, policies, and trained people.

---

# Interview Questions

### 1. What is a security control?

A security control is any safeguard or countermeasure used to protect systems, networks, people, or data from cyber threats.

---

### 2. What are the three categories of security controls?

- Administrative Controls
- Technical Controls
- Physical Controls

---

### 3. What is the difference between Preventive and Detective controls?

- **Preventive Controls** stop attacks before they occur.
- **Detective Controls** identify attacks that are occurring or have already occurred.

---

### 4. Give examples of Technical Controls.

- Firewall
- Antivirus
- IDS/IPS
- MFA
- Encryption
- SIEM

---

### 5. Why are backups considered Recovery Controls?

Because they help restore systems and data after a failure, ransomware attack, or disaster.

---

### 6. What is Defense in Depth?

Defense in Depth is a security strategy that uses multiple layers of security controls so that if one control fails, others continue protecting the system.

---

# Summary

Security controls are the practical measures organizations use to protect their assets and reduce cybersecurity risks. They include administrative controls that define policies and procedures, technical controls that use hardware and software for protection, and physical controls that secure facilities and equipment. Additionally, security controls can be categorized by their purpose, such as preventing, detecting, correcting, deterring, compensating for, or recovering from security incidents. A layered approach, known as **Defense in Depth**, provides the most effective protection against modern cyber threats.

---

## Next Topic

➡️ **Authentication.md** — Learn how systems verify identities using passwords, biometrics, smart cards, tokens, and Multi-Factor Authentication (MFA), along with common authentication methods and best practices.
