# Security Principles

Security principles are the fundamental guidelines used to design, implement, and maintain secure systems. They help organizations protect data, systems, and users from cyber threats.

These principles are applied across every area of cybersecurity, from network security and application development to cloud computing and incident response.

---

# Table of Contents

- What are Security Principles?
- Why are Security Principles Important?
- Authentication
- Authorization
- Accounting (AAA)
- Principle of Least Privilege (PoLP)
- Need to Know
- Separation of Duties
- Defense in Depth
- Zero Trust
- Security by Design
- Fail Secure
- Complete Mediation
- Security Through Obscurity
- Least Functionality
- Comparison Table
- Real-World Example
- Interview Questions
- Summary

---

# What are Security Principles?

Security principles are best practices that guide how systems should be designed and operated to reduce security risks.

They help answer questions such as:

- Who should access the system?
- What actions are users allowed to perform?
- How can attacks be prevented?
- What happens if security controls fail?
- How can damage be minimized?

---

# Why are Security Principles Important?

Without security principles:

- Users may receive unnecessary permissions.
- Attackers can exploit weak security.
- Data may be exposed.
- Systems become difficult to protect.
- Recovery from attacks becomes harder.

Security principles provide a structured approach to building secure environments.

---

# 1. Authentication

## Definition

Authentication is the process of **verifying the identity** of a user, device, or application.

It answers the question:

> **"Who are you?"**

---

## Authentication Factors

### Something You Know

- Password
- PIN
- Security Question

### Something You Have

- Smartphone
- Smart Card
- Security Token
- OTP Device

### Something You Are

- Fingerprint
- Face Recognition
- Iris Scan
- Voice Recognition

---

## Multi-Factor Authentication (MFA)

MFA combines two or more authentication factors.

Example:

- Password
- OTP sent to phone

Even if a password is stolen, an attacker cannot log in without the second factor.

---

# 2. Authorization

## Definition

Authorization determines **what an authenticated user is allowed to do**.

It answers the question:

> **"What are you allowed to access?"**

---

## Example

A hospital system:

| User | Permission |
|------|------------|
| Doctor | View & Update Records |
| Nurse | View Records |
| Receptionist | Register Patients |
| Patient | View Own Records |

All users are authenticated, but each has different permissions.

---

# 3. Accounting (AAA)

Accounting records user activities after authentication and authorization.

It answers:

- Who logged in?
- When?
- From where?
- What actions were performed?

Examples include:

- Login logs
- Audit trails
- Access logs
- Event logs

---

# AAA Model

```text
Authentication
        │
        ▼
Authorization
        │
        ▼
Accounting
```

---

# 4. Principle of Least Privilege (PoLP)

## Definition

Users should receive **only the minimum permissions necessary** to perform their job.

No more.

---

## Example

An HR employee needs access to employee records.

They do **not** need access to:

- Database configuration
- Firewall settings
- Financial servers

Providing extra permissions increases security risks.

---

## Benefits

- Reduces attack surface
- Limits insider threats
- Minimizes accidental damage
- Prevents privilege abuse

---

# 5. Need to Know

A user should only access information required for their specific task.

Even if someone has high-level clearance, they should not automatically access every document.

---

## Example

Two doctors work in the same hospital.

Doctor A treats Patient A.

Doctor B treats Patient B.

Doctor A should not access Patient B's medical records without a valid reason.

---

# 6. Separation of Duties (SoD)

Critical tasks should be divided among multiple people.

No single person should control an entire sensitive process.

---

## Example

Online Banking

Person A

- Creates payment

Person B

- Approves payment

Person C

- Audits payment

This prevents fraud and mistakes.

---

# 7. Defense in Depth

## Definition

Use multiple layers of security instead of relying on a single control.

If one layer fails, another layer continues to provide protection.

---

## Example

```text
Internet
     │
Firewall
     │
IDS/IPS
     │
VPN
     │
Authentication
     │
Application Security
     │
Database Encryption
```

If the firewall fails, IDS may detect the attack.

If IDS misses it, authentication or encryption may still prevent damage.

---

## Common Layers

- Physical Security
- Network Security
- Endpoint Security
- Application Security
- Identity Security
- Data Security

---

# 8. Zero Trust

## Principle

> **Never Trust, Always Verify.**

Zero Trust assumes that **no user or device is trusted by default**, even if it is inside the organization's network.

Every access request must be verified.

---

## Key Concepts

- Verify every request
- Use MFA
- Least Privilege
- Continuous monitoring
- Device verification

---

## Example

An employee logs in from a new laptop.

The system requests:

- Password
- MFA
- Device verification

Only after successful verification is access granted.

---

# 9. Security by Design

Security should be included during system design—not added after development.

---

## Example

While developing an online shopping website:

Instead of:

- Building the website first
- Adding security later

Developers should include:

- Input validation
- HTTPS
- Password hashing
- Access control
- Secure coding practices

from the beginning.

---

# 10. Fail Secure

If a system fails, it should remain secure rather than becoming insecure.

---

## Example

A secure electronic door loses power.

Instead of unlocking automatically, it remains locked to protect the building.

---

# 11. Complete Mediation

Every request to access a resource should be checked before permission is granted.

Never assume a previously approved request is still valid.

---

## Example

A user accesses confidential files.

Every file request is checked against current permissions before access is allowed.

---

# 12. Security Through Obscurity

Security should **not rely solely on secrecy**.

Hiding a system or configuration is not a replacement for proper security controls.

---

## Bad Example

Changing an admin login URL without authentication.

If someone discovers the URL, the system is still vulnerable.

---

## Better Approach

Use:

- Authentication
- Authorization
- MFA
- Encryption

---

# 13. Least Functionality

Enable only the services and features that are required.

Disable everything else.

---

## Example

A web server only needs:

- HTTP
- HTTPS

Disable:

- FTP
- Telnet
- SMB
- Unused ports

Fewer services mean fewer opportunities for attackers.

---

# Comparison Table

| Principle | Purpose |
|-----------|---------|
| Authentication | Verify identity |
| Authorization | Control permissions |
| Accounting | Record user activity |
| Least Privilege | Minimum required permissions |
| Need to Know | Access only required information |
| Separation of Duties | Divide critical tasks |
| Defense in Depth | Multiple security layers |
| Zero Trust | Verify every access request |
| Security by Design | Build security from the beginning |
| Fail Secure | Remain secure during failures |
| Complete Mediation | Check every access request |
| Least Functionality | Disable unnecessary services |
| Security Through Obscurity | Never rely only on secrecy |

---

# Real-World Example

## Online Banking System

### Authentication

Customer logs in using:

- Username
- Password
- OTP

---

### Authorization

Customer can:

- View account
- Transfer money
- Download statements

The customer cannot access another person's account.

---

### Accounting

The bank records:

- Login time
- Device
- IP address
- Transactions

---

### Least Privilege

Customer service representatives cannot modify the banking database.

---

### Defense in Depth

The bank uses:

- Firewalls
- IDS/IPS
- MFA
- Encryption
- Antivirus
- Monitoring
- Secure coding

---

### Zero Trust

Every login attempt is verified, even from trusted devices.

---

# Key Points

- Authentication verifies identity.
- Authorization grants permissions.
- Accounting records activities.
- Least Privilege minimizes permissions.
- Defense in Depth uses multiple security layers.
- Zero Trust requires verification for every access request.
- Security should be built into systems from the beginning.
- Disable unnecessary services to reduce the attack surface.

---

# Interview Questions

### 1. What is the difference between Authentication and Authorization?

Authentication verifies **who you are**.

Authorization determines **what you can access**.

---

### 2. What does AAA stand for?

- Authentication
- Authorization
- Accounting

---

### 3. What is the Principle of Least Privilege?

Users should receive only the permissions necessary to perform their job.

---

### 4. What is Defense in Depth?

Using multiple security controls so that if one fails, others continue protecting the system.

---

### 5. What is Zero Trust?

A security model that assumes no user or device is trusted by default. Every access request must be verified.

---

### 6. What is Separation of Duties?

Dividing sensitive tasks among multiple people to reduce fraud and mistakes.

---

### 7. Why is Security by Design important?

It ensures security is integrated into a system from the beginning instead of being added later.

---

### 8. What is Least Functionality?

Only enable the services, ports, and features that are required for normal operation.

---

# Summary

Security principles provide the foundation for building secure systems. Concepts such as Authentication, Authorization, Least Privilege, Defense in Depth, and Zero Trust are used across all areas of cybersecurity to reduce risk and protect information.

Understanding these principles is essential before studying networking, cloud security, penetration testing, malware analysis, or security operations because they influence how secure systems are designed and managed.

---

## Next Topic

➡️ **Threat-Vulnerability-Risk.md** — Learn the difference between **assets, threats, vulnerabilities, exploits, risks, impacts, and mitigations**, and how organizations assess and reduce cybersecurity risk.
