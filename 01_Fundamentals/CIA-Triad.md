# CIA Triad

The **CIA Triad** is the foundation of information security (InfoSec). Almost every cybersecurity control, policy, technology, and security decision is designed to protect one or more of these three principles:

- **Confidentiality**
- **Integrity**
- **Availability**

Understanding the CIA Triad is essential because it explains **what cybersecurity aims to protect**.

---

# Table of Contents

- What is the CIA Triad?
- Why is it Important?
- Confidentiality
- Integrity
- Availability
- Relationship Between the Three
- Real-World Example
- Common Threats
- Security Controls
- CIA Triad in Different Domains
- Interview Questions
- Summary

---

# What is the CIA Triad?

The CIA Triad is a security model used to protect information and information systems.

It consists of three core principles:

| Principle | Goal |
|-----------|------|
| Confidentiality | Prevent unauthorized access to information |
| Integrity | Ensure information remains accurate and unmodified |
| Availability | Ensure information is accessible when needed |

Every security measure in cybersecurity supports at least one of these principles.

---

# Why is the CIA Triad Important?

Organizations store valuable information such as:

- Customer records
- Passwords
- Financial information
- Medical records
- Government documents
- Intellectual property

The CIA Triad helps organizations answer three important questions:

- **Can only authorized people access the data?** (Confidentiality)
- **Can the data be trusted?** (Integrity)
- **Can the data be accessed whenever required?** (Availability)

If any one of these principles fails, security is compromised.

---

# 1. Confidentiality

## Definition

Confidentiality ensures that information is accessible **only to authorized users**.

Unauthorized users should never be able to read or access sensitive information.

---

## Objective

Protect sensitive information from unauthorized disclosure.

---

## Examples

- Bank account details
- Passwords
- Aadhaar numbers
- Credit card information
- Medical records
- Company financial reports

---

## Real-World Example

Only the HR department can view employee salary information.

Other employees cannot access these records.

This maintains confidentiality.

---

## Threats to Confidentiality

- Data breaches
- Phishing attacks
- Insider threats
- Weak passwords
- Stolen devices
- Social engineering
- Misconfigured cloud storage

---

## Security Controls

- Strong passwords
- Multi-Factor Authentication (MFA)
- Encryption
- Access Control Lists (ACL)
- Role-Based Access Control (RBAC)
- VPN
- Data classification

---

## Example

A company's database is encrypted.

Even if attackers steal the database, they cannot read the information without the encryption key.

Confidentiality is preserved.

---

# 2. Integrity

## Definition

Integrity ensures that information remains **accurate, complete, and unchanged** unless modified by an authorized person.

Users should be able to trust that the information has not been tampered with.

---

## Objective

Prevent unauthorized modification of data.

---

## Examples

- Banking transactions
- Medical records
- Academic grades
- Legal documents
- Source code

---

## Real-World Example

Suppose your bank balance is ₹10,000.

An attacker changes it to ₹1,00,000.

The information is no longer accurate.

Integrity has been compromised.

---

## Threats to Integrity

- Malware
- Unauthorized editing
- SQL Injection
- Insider attacks
- Software bugs
- Data corruption

---

## Security Controls

- Hashing
- Checksums
- Digital Signatures
- Version Control
- File Integrity Monitoring
- Database Constraints
- Audit Logs

---

## Example

When downloading software, the developer provides a SHA-256 hash.

After downloading, you calculate the file's hash.

If both hashes match, the file has not been modified.

Integrity is verified.

---

# 3. Availability

## Definition

Availability ensures that systems, applications, and data are accessible whenever authorized users need them.

A secure system is useless if it cannot be accessed.

---

## Objective

Keep systems running with minimal downtime.

---

## Examples

- Online banking
- Hospital systems
- Emergency services
- Cloud applications
- E-commerce websites

---

## Real-World Example

A hospital's patient management system must be available 24/7.

If doctors cannot access patient records during an emergency, lives may be at risk.

Availability is critical.

---

## Threats to Availability

- DDoS attacks
- Hardware failure
- Power outages
- Ransomware
- Natural disasters
- Server crashes
- Network failures

---

## Security Controls

- Backups
- Redundant servers
- Load balancing
- Disaster Recovery Plans
- UPS (Uninterruptible Power Supply)
- Failover systems
- Regular maintenance

---

## Example

A website is hosted on multiple servers.

If one server fails, traffic automatically moves to another server.

Users continue accessing the website.

Availability is maintained.

---

# Relationship Between the Three Principles

```text
                CIA TRIAD

           +------------------+
           | Confidentiality  |
           +------------------+
                  /     \
                 /       \
                /         \
               /           \
+------------------+   +------------------+
|    Integrity     |   |   Availability   |
+------------------+   +------------------+

All three principles work together to secure information.
```

---

# Real-World Example

## Online Banking

### Confidentiality

Only the account owner can access account details.

Protected using:

- Login credentials
- MFA
- Encryption

---

### Integrity

Transactions cannot be altered.

Protected using:

- Digital signatures
- Database security
- Audit logs

---

### Availability

Customers can access banking services 24/7.

Protected using:

- Backup servers
- Load balancing
- Disaster recovery

---

# Common Threats Against the CIA Triad

| Threat | Confidentiality | Integrity | Availability |
|---------|-----------------|-----------|--------------|
| Phishing | ✅ | ❌ | ❌ |
| Data Breach | ✅ | ❌ | ❌ |
| SQL Injection | ✅ | ✅ | ❌ |
| Malware | ✅ | ✅ | ✅ |
| Ransomware | ❌ | ✅ | ✅ |
| DDoS | ❌ | ❌ | ✅ |
| Insider Threat | ✅ | ✅ | ✅ |
| Hardware Failure | ❌ | ❌ | ✅ |

---

# Security Controls Supporting the CIA Triad

| Security Control | C | I | A |
|------------------|:-:|:-:|:-:|
| Encryption | ✅ | ❌ | ❌ |
| MFA | ✅ | ❌ | ❌ |
| Access Control | ✅ | ❌ | ❌ |
| Hashing | ❌ | ✅ | ❌ |
| Digital Signature | ❌ | ✅ | ❌ |
| Audit Logs | ❌ | ✅ | ❌ |
| Backups | ❌ | ❌ | ✅ |
| Redundant Servers | ❌ | ❌ | ✅ |
| Load Balancing | ❌ | ❌ | ✅ |
| Disaster Recovery | ❌ | ❌ | ✅ |

---

# CIA Triad in Different Domains

| Domain | Confidentiality | Integrity | Availability |
|--------|-----------------|-----------|--------------|
| Network Security | VPN, Firewall | Packet Validation | Redundant Links |
| Cloud Security | IAM, Encryption | Cloud Audit Logs | Auto Scaling |
| Web Security | HTTPS | Input Validation | CDN |
| Mobile Security | App Permissions | Secure Updates | Backup Services |
| Database Security | RBAC | Constraints | Replication |
| SOC | Access Monitoring | Log Integrity | Continuous Monitoring |

---

# Key Points to Remember

- Confidentiality protects **who can access data**.
- Integrity protects **the accuracy of data**.
- Availability ensures **systems remain operational**.
- A secure system must satisfy all three principles.
- Security controls are implemented to protect one or more components of the CIA Triad.

---

# Interview Questions

### 1. What is the CIA Triad?

The CIA Triad is an information security model consisting of Confidentiality, Integrity, and Availability.

---

### 2. What is Confidentiality?

Protecting information from unauthorized access.

---

### 3. What is Integrity?

Ensuring information remains accurate, complete, and unaltered by unauthorized users.

---

### 4. What is Availability?

Ensuring systems and data are accessible whenever authorized users need them.

---

### 5. Which security control primarily protects Confidentiality?

Encryption and Multi-Factor Authentication.

---

### 6. Which security control primarily protects Integrity?

Hashing and Digital Signatures.

---

### 7. Which security control primarily protects Availability?

Backups, Redundant Servers, and Disaster Recovery.

---

### 8. Give one real-world example of the CIA Triad.

Online banking:
- Confidentiality: Only the customer can access the account.
- Integrity: Transactions cannot be altered.
- Availability: Banking services remain accessible 24/7.

---

# Summary

The **CIA Triad** is the core model of information security. It ensures that sensitive information remains **confidential**, **accurate**, and **available** when needed.

Every cybersecurity technology—whether it is a firewall, encryption, digital signature, backup system, or disaster recovery plan—supports one or more principles of the CIA Triad. Understanding this model is fundamental to designing secure systems and analyzing cyber threats.

---

## Next Topic

➡️ **Security-Principles.md** — Learn the fundamental security principles such as **Authentication, Authorization, Least Privilege, Defense in Depth, Zero Trust, and Security by Design**, which build upon the CIA Triad.
