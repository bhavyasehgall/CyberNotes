# AAA Model (Authentication, Authorization, and Accounting)

The **AAA Model** is a security framework used to control access to computer systems, networks, and applications. It consists of three essential processes:

- **Authentication** – Verifying identity
- **Authorization** – Determining permissions
- **Accounting** – Recording user activities

Almost every modern organization uses the AAA model to ensure that only authorized users can access resources and that all important activities are logged for security and auditing purposes.

The AAA model is widely used in:

- Enterprise Networks
- Cloud Computing
- VPNs
- Wi-Fi Authentication
- Network Devices (Routers & Switches)
- Linux & Windows Servers
- Firewalls
- Identity and Access Management (IAM)

---

# Table of Contents

- What is the AAA Model?
- Why is the AAA Model Important?
- Components of AAA
  - Authentication
  - Authorization
  - Accounting
- How AAA Works
- AAA Architecture
- AAA Protocols
  - RADIUS
  - TACACS+
  - LDAP
  - Kerberos
- Real-World Examples
- AAA in Different Environments
- Best Practices
- Interview Questions
- Summary

---

# What is the AAA Model?

The **AAA Model** is a framework that manages user access by answering three questions:

| Component | Question Answered |
|-----------|-------------------|
| Authentication | **Who are you?** |
| Authorization | **What are you allowed to do?** |
| Accounting | **What did you do?** |

These three processes work together to secure systems and maintain accountability.

---

# Why is the AAA Model Important?

Without AAA:

- Anyone could access systems.
- Users might receive excessive permissions.
- Security incidents would be difficult to investigate.
- Organizations would have no record of user activities.

The AAA model improves:

- Security
- Accountability
- Compliance
- Auditing
- Access management

---

# AAA Workflow

```text
User
 │
 ▼
Authentication
 │
 ▼
Identity Verified
 │
 ▼
Authorization
 │
 ▼
Permissions Granted
 │
 ▼
Access Resource
 │
 ▼
Accounting
 │
 ▼
Activity Logged
```

---

# 1. Authentication

## Definition

Authentication verifies the identity of a user, device, or application before access is granted.

It answers:

> **Who are you?**

---

## Common Authentication Methods

### Something You Know

- Password
- PIN
- Passphrase

---

### Something You Have

- Smartphone
- Smart Card
- Hardware Token
- Security Key

---

### Something You Are

- Fingerprint
- Face Recognition
- Iris Scan

---

## Example

A user logs into a company VPN using:

- Username
- Password
- OTP from an Authenticator App

The VPN verifies the credentials before allowing access.

---

# 2. Authorization

## Definition

Authorization determines what resources an authenticated user can access and what actions they are permitted to perform.

It answers:

> **What are you allowed to do?**

---

## Examples

### Employee

Can:

- Access company email
- View internal documents

Cannot:

- Manage servers

---

### System Administrator

Can:

- Manage servers
- Create user accounts
- Configure network devices

---

## Common Authorization Models

- Role-Based Access Control (RBAC)
- Attribute-Based Access Control (ABAC)
- Discretionary Access Control (DAC)
- Mandatory Access Control (MAC)

---

# 3. Accounting

## Definition

Accounting records and monitors user activities after successful authentication and authorization.

It answers:

> **What did you do?**

---

## Information Recorded

- Username
- Login Time
- Logout Time
- Source IP Address
- Device Information
- Commands Executed
- Files Accessed
- Configuration Changes
- Failed Login Attempts

---

## Why Accounting is Important

Accounting helps organizations:

- Detect suspicious activity
- Investigate security incidents
- Meet compliance requirements
- Monitor privileged users
- Generate audit reports

---

## Example

An administrator logs into a router and changes firewall rules.

The accounting system records:

- Administrator's username
- Login time
- IP address
- Commands executed
- Logout time

This creates an audit trail.

---

# How AAA Works

Consider a corporate VPN.

## Step 1 – Authentication

The employee enters:

- Username
- Password
- MFA Code

The VPN verifies the identity.

---

## Step 2 – Authorization

The employee belongs to the HR department.

The VPN allows access only to HR resources.

Finance servers remain inaccessible.

---

## Step 3 – Accounting

The VPN logs:

- Login time
- IP address
- VPN session duration
- Resources accessed
- Logout time

---

# AAA Architecture

```text
                User
                  │
                  ▼
         Authentication Server
                  │
      ┌───────────┴───────────┐
      ▼                       ▼
Authentication         Authorization
      │                       │
      └───────────┬───────────┘
                  ▼
           Access Granted
                  │
                  ▼
             Accounting
                  │
                  ▼
             Audit Logs
```

---

# AAA Protocols

Several protocols implement AAA services in enterprise environments.

---

# 1. RADIUS

## Full Form

**Remote Authentication Dial-In User Service**

---

## Purpose

Provides centralized:

- Authentication
- Authorization
- Accounting

Primarily used for:

- Wi-Fi authentication
- VPN authentication
- Network Access Control (NAC)

---

## Characteristics

- Uses UDP
- Encrypts only the password field
- Commonly integrated with Active Directory

---

# 2. TACACS+

## Full Form

**Terminal Access Controller Access-Control System Plus**

---

## Purpose

Provides centralized AAA for administrative access to network devices.

---

## Characteristics

- Uses TCP
- Encrypts the entire communication payload
- Separates Authentication, Authorization, and Accounting
- Commonly used for routers, switches, and firewalls

---

# RADIUS vs TACACS+

| Feature | RADIUS | TACACS+ |
|---------|---------|----------|
| Transport Protocol | UDP | TCP |
| Encryption | Password Only | Entire Payload |
| Primary Use | User Network Access | Device Administration |
| AAA Separation | Combined | Fully Separated |

---

# 3. LDAP

## Full Form

**Lightweight Directory Access Protocol**

LDAP provides centralized directory services for storing user and group information.

LDAP itself is **not a complete AAA protocol**, but it is commonly used for authentication and identity management.

---

# 4. Kerberos

## Definition

Kerberos is a network authentication protocol that uses **tickets** instead of repeatedly transmitting passwords.

---

## Common Usage

- Microsoft Active Directory
- Windows Domain Authentication
- Enterprise Networks

---

# AAA in Different Environments

| Environment | Authentication | Authorization | Accounting |
|-------------|---------------|---------------|------------|
| Windows Domain | Kerberos | Group Policies | Event Logs |
| Linux Server | SSH Keys / Password | File Permissions | Syslog |
| VPN | MFA | Network Policies | VPN Logs |
| Wi-Fi | RADIUS | Network Access Policies | Session Logs |
| Cloud | IAM | IAM Policies | Cloud Audit Logs |
| Firewall | TACACS+ | Admin Roles | Command Logs |

---

# Real-World Example

## Online Banking

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

Cannot:

- Access another customer's account

---

### Accounting

The bank records:

- Login time
- Device
- Browser
- IP address
- Transactions
- Logout time

These logs help detect fraud and investigate incidents.

---

# Benefits of the AAA Model

- Strong identity verification
- Controlled access to resources
- Complete audit trail
- Easier compliance with security standards
- Better incident investigation
- Improved accountability

---

# Best Practices

- Enable Multi-Factor Authentication (MFA).
- Apply the Principle of Least Privilege.
- Review user permissions regularly.
- Protect privileged accounts with PAM.
- Store logs securely.
- Monitor authentication failures.
- Review audit logs frequently.
- Use centralized AAA servers where possible.
- Synchronize system clocks using NTP to ensure accurate log timestamps.

---

# Key Points

- AAA stands for Authentication, Authorization, and Accounting.
- Authentication verifies identity.
- Authorization determines permissions.
- Accounting records user activities.
- Authentication always occurs before authorization.
- Accounting creates an audit trail for monitoring and investigations.
- RADIUS is commonly used for user network access.
- TACACS+ is commonly used for administrative access to network devices.

---

# Interview Questions

### 1. What does AAA stand for?

- Authentication
- Authorization
- Accounting

---

### 2. What is the purpose of Authentication?

To verify the identity of a user, device, or application before access is granted.

---

### 3. What is the purpose of Authorization?

To determine what an authenticated user is allowed to access or perform.

---

### 4. What is Accounting in the AAA model?

Accounting records user activities such as logins, commands executed, accessed resources, and logout times.

---

### 5. What is the difference between RADIUS and TACACS+?

RADIUS primarily manages user network access and encrypts only the password field over UDP, whereas TACACS+ is designed for administrative access to network devices, uses TCP, and encrypts the entire communication payload.

---

### 6. Why is Accounting important?

Accounting provides audit logs that support security monitoring, incident response, compliance, and forensic investigations.

---

### 7. Which protocol is commonly used for Wi-Fi authentication?

RADIUS.

---

### 8. Which protocol is commonly used for administrator access to routers and switches?

TACACS+.

---

# Summary

The AAA Model is a core security framework used to manage access to systems and networks. Authentication verifies identity, Authorization determines permitted actions, and Accounting records user activities for monitoring and auditing. Together, these three components provide secure access control, improve accountability, support regulatory compliance, and help organizations investigate security incidents. Protocols such as RADIUS, TACACS+, LDAP, and Kerberos are widely used to implement AAA services in enterprise environments.

---

## Next Topic

➡️ **Cybersecurity-Domains.md** — Learn about the major cybersecurity domains, including **Network Security, Application Security, Cloud Security, Endpoint Security, Identity and Access Management (IAM), Digital Forensics, Incident Response, Threat Intelligence, Governance, Risk & Compliance (GRC), and Security Operations Center (SOC)**.
