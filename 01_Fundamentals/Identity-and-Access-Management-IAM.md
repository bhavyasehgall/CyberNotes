# Identity and Access Management (IAM)

Identity and Access Management (IAM) is a cybersecurity framework that ensures **the right people have the right access to the right resources at the right time, and for the right reasons**.

IAM helps organizations manage **digital identities**, control access to systems, and protect sensitive information from unauthorized access.

It is one of the most important concepts in modern cybersecurity and is widely used in:

- Enterprise Networks
- Cloud Computing
- Banking
- Government Organizations
- Healthcare
- Software Development
- Identity Providers (IdPs)

---

# Table of Contents

- What is IAM?
- Why is IAM Important?
- IAM Components
- Identity Lifecycle
- Authentication
- Authorization
- Access Control Models
- Single Sign-On (SSO)
- Multi-Factor Authentication (MFA)
- Federation
- Privileged Access Management (PAM)
- Identity Governance and Administration (IGA)
- IAM in Cloud Computing
- IAM Best Practices
- Real-World Example
- Interview Questions
- Summary

---

# What is IAM?

**Identity and Access Management (IAM)** is a collection of policies, technologies, and processes used to manage digital identities and control access to organizational resources.

IAM ensures that:

- Every user has a unique identity.
- Users are authenticated before accessing resources.
- Users receive only the permissions they need.
- User activities are logged and monitored.
- Access is removed when no longer required.

---

# Why is IAM Important?

Without IAM:

- Anyone could access sensitive information.
- Employees might receive unnecessary permissions.
- Former employees could retain access.
- Stolen credentials could be abused.
- Organizations would struggle to meet compliance requirements.

IAM reduces these risks by enforcing strong identity verification and access control.

---

# IAM Components

IAM consists of several key components.

| Component | Purpose |
|-----------|---------|
| Identity | Represents a user, device, or service |
| Authentication | Verifies identity |
| Authorization | Determines permissions |
| Access Control | Restricts access to resources |
| Accounting | Logs user activities |
| Identity Governance | Manages identity lifecycle and compliance |
| PAM | Protects privileged accounts |

---

# Digital Identity

A **digital identity** uniquely represents a user, device, application, or service.

A digital identity may include:

- Username
- Employee ID
- Email Address
- User ID
- Department
- Role
- Security Clearance
- Authentication Credentials

---

# Identity Lifecycle

Managing identities throughout their lifecycle is an important IAM function.

## 1. Provisioning

Provisioning is the process of creating a new user account and assigning appropriate permissions.

Example:

A new employee joins the HR department.

The IAM system automatically:

- Creates an account
- Assigns the HR role
- Grants email access
- Provides HR application access

---

## 2. Modification

When an employee changes roles, permissions must also change.

Example:

An employee is promoted from Support Engineer to System Administrator.

The IAM system:

- Removes old permissions
- Assigns new administrator permissions

---

## 3. Deprovisioning

Deprovisioning removes user access when it is no longer required.

Example:

An employee leaves the company.

The IAM system:

- Disables the account
- Revokes VPN access
- Removes cloud access
- Deletes administrator privileges

This prevents unauthorized access by former employees.

---

# Authentication

Authentication verifies the identity of a user before granting access.

It answers:

> **Who are you?**

Common authentication methods include:

- Password
- PIN
- Biometrics
- Smart Cards
- Security Keys
- One-Time Passwords (OTP)
- Passkeys

---

# Authorization

Authorization determines what an authenticated user is allowed to access.

It answers:

> **What are you allowed to do?**

Example:

A Finance employee can access financial reports but cannot modify firewall settings.

---

# Access Control Models

IAM uses different authorization models.

---

## Role-Based Access Control (RBAC)

Permissions are assigned to roles.

Example:

| Role | Permission |
|------|------------|
| HR | Employee Records |
| Finance | Financial Reports |
| IT Administrator | Server Management |

---

## Attribute-Based Access Control (ABAC)

Access decisions are based on attributes.

Examples of attributes:

- Department
- Device Type
- Time
- Location
- Security Clearance

---

## Mandatory Access Control (MAC)

Access is determined by security classifications.

Commonly used in:

- Military
- Government

---

## Discretionary Access Control (DAC)

The resource owner decides who can access the resource.

Commonly used in desktop operating systems.

---

# Single Sign-On (SSO)

Single Sign-On allows users to authenticate once and access multiple applications without repeated logins.

Example:

An employee logs into Microsoft 365 and automatically gains access to:

- Outlook
- Teams
- SharePoint
- OneDrive

---

## Benefits

- Better user experience
- Fewer passwords
- Reduced password fatigue
- Centralized authentication

---

# Multi-Factor Authentication (MFA)

MFA requires two or more authentication factors.

Example:

- Password
- Authenticator App
- Fingerprint

Even if a password is stolen, the attacker still needs the second factor.

---

# Federation

Federation allows users from one organization to access another organization's resources using the same identity.

Example:

A company allows employees to log into a partner's application using their corporate Microsoft Entra ID account.

Common federation technologies include:

- SAML
- OpenID Connect (OIDC)
- OAuth 2.0 (for delegated authorization)

---

# Privileged Access Management (PAM)

Privileged accounts have elevated permissions and require additional protection.

Examples:

- Domain Administrator
- Database Administrator
- Cloud Administrator
- Network Administrator

PAM solutions provide:

- Privileged account vaulting
- Session recording
- Just-In-Time (JIT) access
- Password rotation
- Approval workflows

---

# Identity Governance and Administration (IGA)

IGA helps organizations manage identities throughout their lifecycle while maintaining compliance.

IGA focuses on:

- Identity lifecycle management
- Access reviews
- Role management
- Compliance reporting
- Separation of Duties (SoD)
- Policy enforcement

---

# IAM in Cloud Computing

Cloud providers include built-in IAM services.

| Cloud Provider | IAM Service |
|---------------|-------------|
| AWS | AWS IAM |
| Microsoft Azure | Microsoft Entra ID (formerly Azure AD) |
| Google Cloud | Cloud IAM |

Cloud IAM enables administrators to:

- Create users
- Create groups
- Assign roles
- Manage permissions
- Enforce MFA
- Generate audit logs

---

# IAM Workflow

```text
User
 │
 ▼
Login Request
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
Access Control
 │
 ▼
Resource Access
 │
 ▼
Activity Logging
```

---

# Real-World Example

## Online Banking

### Customer

Authentication:

- Username
- Password
- OTP

Authorization:

- View account
- Transfer money
- Download statements

Cannot:

- Access another customer's account

Accounting:

The bank logs:

- Login time
- Device
- IP Address
- Transactions
- Logout time

This entire process is managed through IAM.

---

# Benefits of IAM

- Improves security
- Reduces unauthorized access
- Simplifies user management
- Supports regulatory compliance
- Enhances user experience
- Automates account management
- Protects privileged accounts
- Provides complete audit trails

---

# IAM Best Practices

- Enable Multi-Factor Authentication (MFA).
- Follow the Principle of Least Privilege.
- Use Role-Based Access Control (RBAC).
- Review permissions regularly.
- Remove inactive accounts.
- Automate provisioning and deprovisioning.
- Protect privileged accounts using PAM.
- Monitor authentication and authorization logs.
- Perform periodic access reviews.
- Use Single Sign-On (SSO) where appropriate.

---

# Key Points

- IAM manages identities and controls access to resources.
- Authentication verifies identity.
- Authorization determines permissions.
- Provisioning creates accounts.
- Deprovisioning removes access.
- MFA significantly improves account security.
- SSO simplifies user authentication.
- PAM protects privileged accounts.
- IGA ensures identities are managed securely and compliantly.

---

# Interview Questions

### 1. What is Identity and Access Management (IAM)?

IAM is a framework of policies, technologies, and processes used to manage digital identities and control access to resources.

---

### 2. What is the difference between Authentication and Authorization?

Authentication verifies identity, while Authorization determines what an authenticated user is allowed to access.

---

### 3. What is provisioning?

Provisioning is the process of creating user accounts and assigning the necessary permissions.

---

### 4. What is deprovisioning?

Deprovisioning is the process of removing user accounts and revoking access when it is no longer needed.

---

### 5. What is Single Sign-On (SSO)?

SSO allows users to authenticate once and access multiple applications without logging in repeatedly.

---

### 6. What is Multi-Factor Authentication (MFA)?

MFA requires two or more different authentication factors to verify a user's identity.

---

### 7. What is Privileged Access Management (PAM)?

PAM is a security approach used to protect, monitor, and control privileged accounts with elevated permissions.

---

### 8. What is Identity Governance and Administration (IGA)?

IGA manages the identity lifecycle, access reviews, compliance, and governance of user permissions within an organization.

---

# Summary

Identity and Access Management (IAM) is the foundation of modern access control. It ensures that identities are properly managed, users are authenticated, permissions are correctly assigned, and all activities are monitored. Features such as Authentication, Authorization, SSO, MFA, PAM, and IGA work together to provide secure and efficient access to organizational resources. Effective IAM reduces security risks, supports compliance, and helps organizations protect critical systems and sensitive information.

---

## Next Topic

➡️ **Defense-in-Depth.md** — Learn how organizations implement **multiple layers of security controls** to protect systems, networks, applications, and data, ensuring that if one control fails, others continue to provide protection.
