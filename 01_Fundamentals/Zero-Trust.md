# Zero Trust

**Zero Trust** is a cybersecurity security model based on the principle:

> **"Never Trust, Always Verify."**

Unlike traditional security models that automatically trust users or devices inside an organization's network, Zero Trust assumes that **no user, device, application, or network should be trusted by default**, whether inside or outside the network perimeter.

Every access request must be continuously verified before access is granted.

Today, Zero Trust is widely adopted in:

- Cloud Computing
- Enterprise Networks
- Remote Work Environments
- Hybrid Cloud
- Government Organizations
- Financial Institutions
- Healthcare

---

# Table of Contents

- What is Zero Trust?
- Why Zero Trust is Needed
- Traditional Security vs Zero Trust
- Core Principles of Zero Trust
- Pillars of Zero Trust
- Zero Trust Architecture
- Zero Trust Access Process
- Zero Trust Technologies
- Benefits
- Challenges
- Best Practices
- Interview Questions
- Summary

---

# What is Zero Trust?

Zero Trust is a security strategy that assumes **every access request is potentially malicious until it has been verified**.

Instead of trusting users because they are connected to the internal network, Zero Trust verifies:

- User identity
- Device health
- Location
- Time
- Application
- Risk level
- Requested resource

Only after these checks are completed is access granted.

---

# Why Zero Trust is Needed

Traditional networks assumed that users inside the organization's network were trustworthy.

However, modern attacks involve:

- Stolen credentials
- Insider threats
- Remote work
- Cloud services
- Compromised devices
- Supply chain attacks

Once attackers entered the internal network, they could often move freely.

Zero Trust eliminates this assumption by requiring verification for every access request.

---

# Traditional Security vs Zero Trust

| Traditional Security | Zero Trust |
|----------------------|------------|
| Trust internal users | Trust no one by default |
| Perimeter-focused | Identity-focused |
| Verify once | Verify continuously |
| Broad network access | Least-privilege access |
| Large trusted network | Micro-segmented environment |

---

# Core Principles of Zero Trust

---

## 1. Never Trust, Always Verify

Every user, device, and application must be authenticated and authorized before access is granted.

Being inside the corporate network does not automatically make a request trustworthy.

---

## 2. Verify Explicitly

Access decisions should be based on multiple factors, including:

- User identity
- Device compliance
- Location
- Time
- Requested resource
- Risk score
- Authentication strength

---

## 3. Least Privilege Access

Users receive only the permissions required to perform their work.

Example:

A marketing employee should not have administrator access to database servers.

---

## 4. Assume Breach

Organizations should operate under the assumption that attackers may already be inside the environment.

The focus is on:

- Detecting attackers quickly
- Limiting their movement
- Containing incidents
- Recovering efficiently

---

# Pillars of Zero Trust

Microsoft's Zero Trust model defines six key pillars.

| Pillar | Purpose |
|---------|---------|
| Identities | Verify users and service accounts |
| Devices | Verify device security and compliance |
| Applications | Secure application access |
| Data | Protect sensitive information |
| Infrastructure | Secure servers and cloud resources |
| Networks | Segment networks and monitor traffic |

---

# Zero Trust Architecture

```text
                User
                  │
                  ▼
         Identity Verification
          (Password + MFA)
                  │
                  ▼
         Device Compliance Check
                  │
                  ▼
        Risk & Policy Evaluation
                  │
                  ▼
       Authorization Decision
                  │
        ┌─────────┴─────────┐
        │                   │
        ▼                   ▼
  Access Granted      Access Denied
                  │
                  ▼
     Continuous Monitoring
```

Every access request passes through these verification steps before reaching the requested resource.

---

# Zero Trust Access Process

## Step 1 – User Requests Access

The user attempts to access a resource.

---

## Step 2 – Identity Verification

The IAM system verifies the user's identity using:

- Password
- Passkey
- Multi-Factor Authentication (MFA)
- Security Key

---

## Step 3 – Device Verification

The system checks:

- Operating system version
- Security patches
- Antivirus status
- Device compliance
- Encryption status

---

## Step 4 – Policy Evaluation

Policies evaluate factors such as:

- User role
- Department
- Location
- Time of access
- Device trust level
- Resource sensitivity

---

## Step 5 – Access Decision

If all policy requirements are satisfied:

Access is granted.

Otherwise:

Access is denied or additional verification is required.

---

## Step 6 – Continuous Monitoring

Even after access is granted, user activity is continuously monitored.

If suspicious behavior is detected:

- Session may be terminated.
- Additional authentication may be requested.
- Security teams may be alerted.

---

# Microsegmentation

Microsegmentation divides a network into smaller, isolated segments.

Instead of allowing unrestricted communication between systems, access is explicitly controlled.

### Example

A compromised employee laptop can communicate only with approved HR servers and cannot directly access finance or database servers.

Benefits include:

- Limits lateral movement
- Reduces attack surface
- Improves containment

---

# Continuous Verification

Zero Trust continuously evaluates trust throughout a session.

Changes that may trigger re-evaluation include:

- Login from a new country
- Device becomes non-compliant
- Impossible travel detected
- Suspicious user behavior
- Elevated risk score

---

# Zero Trust Technologies

Common technologies used to implement Zero Trust include:

- Identity and Access Management (IAM)
- Multi-Factor Authentication (MFA)
- Single Sign-On (SSO)
- Privileged Access Management (PAM)
- Endpoint Detection and Response (EDR)
- Security Information and Event Management (SIEM)
- Network Access Control (NAC)
- Virtual Private Networks (VPNs)
- Zero Trust Network Access (ZTNA)
- Data Loss Prevention (DLP)

---

# Real-World Example

## Employee Accessing a Cloud CRM

### Step 1

The employee signs in using:

- Username
- Password
- MFA

---

### Step 2

The system verifies:

- Device encryption
- Antivirus status
- Operating system updates

---

### Step 3

The IAM platform checks:

- Employee role
- Office location
- Business hours
- Device compliance

---

### Step 4

Access is granted only to CRM resources.

The employee cannot access:

- Payroll systems
- Database servers
- Network administration tools

---

### Step 5

If the employee later connects from an unknown country using an unmanaged device, the system may:

- Block access
- Require additional MFA
- Notify the security team

---

# Benefits

- Reduces unauthorized access.
- Limits lateral movement.
- Protects remote workers.
- Improves cloud security.
- Enhances identity protection.
- Supports regulatory compliance.
- Minimizes the impact of stolen credentials.
- Provides better visibility into user activity.

---

# Challenges

- Complex implementation.
- Legacy applications may not support Zero Trust.
- Initial deployment costs.
- Requires accurate identity and device management.
- Continuous monitoring increases operational complexity.

---

# Zero Trust vs Defense in Depth

| Defense in Depth | Zero Trust |
|------------------|------------|
| Layered security strategy | Identity-centric security model |
| Uses multiple security controls | Verifies every access request |
| Focuses on prevention, detection, response, and recovery | Focuses on continuous verification and least privilege |
| Protects systems using multiple layers | Protects resources regardless of network location |

**Note:** Zero Trust and Defense in Depth are complementary strategies and are often implemented together.

---

# Best Practices

- Enable Multi-Factor Authentication (MFA).
- Follow the Principle of Least Privilege.
- Implement Role-Based Access Control (RBAC).
- Segment networks using microsegmentation.
- Continuously monitor user and device activity.
- Keep devices updated and compliant.
- Protect privileged accounts with PAM.
- Encrypt sensitive data.
- Review access permissions regularly.
- Log and audit all access events.

---

# Key Points

- Zero Trust is based on the principle **"Never Trust, Always Verify."**
- Every access request must be authenticated and authorized.
- Device health and user identity are continuously evaluated.
- Least Privilege and microsegmentation reduce the impact of attacks.
- Zero Trust is particularly effective for cloud environments and remote work.

---

# Interview Questions

### 1. What is Zero Trust?

Zero Trust is a security model that assumes no user, device, or application should be trusted by default. Every access request must be verified before access is granted.

---

### 2. What is the main principle of Zero Trust?

**Never Trust, Always Verify.**

---

### 3. Why is Zero Trust important?

It reduces the risk of unauthorized access, insider threats, and lateral movement by continuously verifying users, devices, and applications.

---

### 4. What is microsegmentation?

Microsegmentation divides a network into smaller isolated segments, restricting communication between systems and limiting lateral movement.

---

### 5. What is Least Privilege?

Least Privilege means granting users only the minimum permissions necessary to perform their job.

---

### 6. Is Zero Trust only for cloud environments?

No. Zero Trust can be implemented across on-premises, cloud, hybrid, and remote work environments.

---

### 7. Can Zero Trust replace Defense in Depth?

No. Zero Trust and Defense in Depth address different aspects of security and are most effective when used together.

---

# Summary

Zero Trust is a modern cybersecurity model that eliminates implicit trust and requires continuous verification of every user, device, and application requesting access to organizational resources. By combining identity verification, device compliance, least-privilege access, microsegmentation, and continuous monitoring, Zero Trust significantly reduces the risk of unauthorized access and limits the impact of successful attacks. It has become a foundational security strategy for cloud computing, hybrid work environments, and modern enterprise networks.

---

## Next Topic

➡️ **Cyber-Kill-Chain.md** — Learn about the **Lockheed Martin Cyber Kill Chain**, a framework that breaks a cyberattack into seven stages, helping security teams understand, detect, and disrupt attacks before attackers achieve their objectives.
