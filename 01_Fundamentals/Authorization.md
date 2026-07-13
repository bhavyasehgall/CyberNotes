# Authorization

Authorization is the process of determining **what an authenticated user is allowed to access or perform** within a system.

After a user successfully proves their identity through **Authentication**, the system checks their permissions before allowing access to resources.

In simple terms:

- **Authentication** answers **"Who are you?"**
- **Authorization** answers **"What are you allowed to do?"**

Authorization is a critical part of access control and helps protect sensitive data from unauthorized access.

---

# Table of Contents

- What is Authorization?
- Why is Authorization Important?
- Authentication vs Authorization
- Authorization Process
- Access Control
- Principle of Least Privilege
- Types of Access Control Models
  - Discretionary Access Control (DAC)
  - Mandatory Access Control (MAC)
  - Role-Based Access Control (RBAC)
  - Attribute-Based Access Control (ABAC)
- Access Control Lists (ACL)
- Privileged Access Management (PAM)
- Common Authorization Attacks
- Best Practices
- Interview Questions
- Summary

---

# What is Authorization?

**Authorization** is the process of deciding what resources, files, applications, or actions a user is permitted to access after successful authentication.

It ensures that users only receive the permissions necessary to perform their tasks.

---

# Authorization Process

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
Permission Check
 │
 ├── Allowed ──► Access Granted
 │
 └── Denied ───► Access Blocked
```

---

# Why is Authorization Important?

Without authorization:

- Employees could access confidential data.
- Customers could view other users' information.
- Attackers with stolen credentials could access every system.
- Sensitive files could be modified or deleted.

Authorization limits what authenticated users can do.

---

# Authentication vs Authorization

| Authentication | Authorization |
|---------------|---------------|
| Verifies identity | Determines permissions |
| Happens first | Happens after authentication |
| "Who are you?" | "What can you do?" |
| Login process | Permission checking |

---

# Real-World Example

Consider a hospital management system.

### Doctor

Can:

- View patient records
- Update prescriptions
- Order medical tests

### Nurse

Can:

- View patient records
- Update vital signs

Cannot:

- Prescribe medication

### Receptionist

Can:

- Register patients
- Schedule appointments

Cannot:

- View confidential medical records

Every user logs into the same system, but each receives different permissions based on their role.

---

# Access Control

Access Control is the process of restricting access to resources.

It combines:

- Authentication
- Authorization
- Accountability (AAA)

The goal is to ensure that only authorized users can access the right resources at the right time.

---

# Principle of Least Privilege (PoLP)

The **Principle of Least Privilege** states that users should receive only the minimum permissions necessary to perform their work.

### Example

An HR employee requires access to employee records.

They do **not** need access to:

- Firewall settings
- Database administration
- Financial systems

Granting unnecessary permissions increases security risks.

---

# Types of Access Control Models

Organizations use different authorization models depending on their security requirements.

---

# 1. Discretionary Access Control (DAC)

## Definition

In DAC, the **owner of a resource** decides who can access it.

---

## Characteristics

- Flexible
- Easy to manage
- Common in desktop operating systems

---

## Example

A user creates a document and shares it with selected coworkers.

The document owner controls access.

---

## Advantages

- Easy to use
- User-controlled permissions

---

## Disadvantages

- Less secure
- Users may accidentally grant excessive permissions

---

# 2. Mandatory Access Control (MAC)

## Definition

In MAC, access is controlled by a **central authority** based on security labels and classifications.

Users cannot change permissions.

---

## Security Classifications

- Public
- Confidential
- Secret
- Top Secret

---

## Example

Military and government systems often use MAC to protect classified information.

A user with **Secret** clearance cannot access **Top Secret** data.

---

## Advantages

- Highly secure
- Centralized control

---

## Disadvantages

- Complex to manage
- Less flexible

---

# 3. Role-Based Access Control (RBAC)

## Definition

Permissions are assigned to **roles**, and users inherit permissions by being assigned to those roles.

---

## Example

| Role | Permissions |
|------|-------------|
| HR Manager | Employee Records |
| Accountant | Financial Reports |
| System Administrator | Server Management |
| Customer Support | Customer Tickets |

When a new employee joins, assigning the appropriate role automatically grants the required permissions.

---

## Advantages

- Easy to manage
- Scalable
- Reduces administrative effort

---

## Disadvantages

- May require many roles in large organizations
- Poorly designed roles can lead to excessive permissions

---

# 4. Attribute-Based Access Control (ABAC)

## Definition

Access decisions are based on **attributes** rather than fixed roles.

Attributes may include:

- User department
- Job title
- Device type
- Location
- Time of day
- Security clearance

---

## Example

Rule:

Allow access only if:

- Department = Finance
- Device = Company Laptop
- Location = Office Network
- Time = Business Hours

If any condition fails, access is denied.

---

## Advantages

- Very flexible
- Fine-grained access control
- Ideal for cloud environments

---

## Disadvantages

- More complex to configure
- Requires careful policy management

---

# Comparison of Access Control Models

| Model | Controlled By | Flexibility | Common Usage |
|--------|---------------|-------------|--------------|
| DAC | Resource Owner | High | Personal Computers |
| MAC | Central Authority | Low | Military, Government |
| RBAC | Organizational Roles | Medium | Enterprises |
| ABAC | Policies & Attributes | Very High | Cloud & Modern Applications |

---

# Access Control Lists (ACL)

An **Access Control List (ACL)** is a list of permissions attached to a resource.

It specifies:

- Who can access the resource
- What actions they can perform

---

## Example

```text
File: Payroll.xlsx

HR Manager      → Read, Write
HR Executive    → Read
Intern          → No Access
```

ACLs are commonly used in:

- Operating Systems
- File Servers
- Network Devices
- Firewalls

---

# Privileged Access Management (PAM)

Privileged accounts have elevated permissions and can make significant changes to systems.

Examples include:

- System Administrator
- Database Administrator
- Domain Administrator
- Cloud Administrator

Privileged Access Management (PAM) helps secure these accounts by:

- Limiting privileged access
- Monitoring privileged sessions
- Recording administrative activities
- Enforcing Multi-Factor Authentication (MFA)

---

# Common Authorization Attacks

## Privilege Escalation

An attacker gains higher permissions than intended.

Example:

A normal user exploits a vulnerability to obtain administrator privileges.

---

## Insecure Direct Object Reference (IDOR)

An application fails to properly verify whether a user is authorized to access a specific resource.

Example:

Changing:

```text
/user/profile?id=100
```

to

```text
/user/profile?id=101
```

allows access to another user's information if authorization checks are missing.

---

## Broken Access Control

Authorization rules are not correctly implemented, allowing unauthorized actions or access.

This is one of the most common and critical web application security issues.

---

## Excessive Permissions

Users receive more permissions than necessary, increasing the impact of compromised accounts.

---

# Best Practices

- Follow the Principle of Least Privilege.
- Implement Role-Based Access Control where appropriate.
- Review user permissions regularly.
- Remove access immediately when employees leave.
- Protect privileged accounts with MFA.
- Log authorization events.
- Validate authorization checks on every request.
- Never rely on hidden URLs or client-side controls for authorization.
- Conduct periodic access reviews and audits.

---

# Real-World Example

## Online Banking

### Customer

Can:

- View personal account
- Transfer funds
- Download statements

Cannot:

- View another customer's account

---

### Bank Employee

Can:

- View customer records
- Assist with account services

Cannot:

- Access system administration functions

---

### System Administrator

Can:

- Manage servers
- Configure systems
- Create user accounts

Cannot automatically access customer financial information unless explicitly authorized.

Each user has permissions appropriate to their responsibilities.

---

# Key Points

- Authorization determines what an authenticated user can access.
- Authentication always occurs before authorization.
- The Principle of Least Privilege reduces security risks.
- RBAC is the most common access control model in enterprises.
- ABAC provides flexible, policy-based authorization.
- Broken authorization is a leading cause of web application vulnerabilities.

---

# Interview Questions

### 1. What is authorization?

Authorization is the process of determining what actions or resources an authenticated user is permitted to access.

---

### 2. What is the difference between authentication and authorization?

Authentication verifies identity, while authorization determines permissions after identity has been verified.

---

### 3. What is the Principle of Least Privilege?

Users should receive only the minimum permissions necessary to perform their assigned tasks.

---

### 4. What is RBAC?

Role-Based Access Control assigns permissions to roles, and users receive permissions by being assigned to those roles.

---

### 5. What is the difference between RBAC and ABAC?

RBAC grants permissions based on predefined roles, while ABAC evaluates multiple attributes such as department, location, device, and time before making an access decision.

---

### 6. What is an Access Control List (ACL)?

An ACL is a list of permissions associated with a resource that specifies which users or groups can perform specific actions.

---

### 7. What is Privileged Access Management (PAM)?

PAM is a security approach for managing, monitoring, and protecting accounts with elevated privileges.

---

### 8. What is Broken Access Control?

Broken Access Control occurs when an application fails to properly enforce authorization rules, allowing unauthorized users to access restricted resources or perform unauthorized actions.

---

# Summary

Authorization ensures that authenticated users can access only the resources and perform only the actions they are permitted to use. It is implemented through access control models such as DAC, MAC, RBAC, and ABAC, supported by mechanisms like ACLs and Privileged Access Management. Applying the Principle of Least Privilege, performing regular access reviews, and enforcing strong authorization checks are essential for protecting sensitive systems and data.

---

## Next Topic

➡️ **AAA-Model.md** — Learn about the **Authentication, Authorization, and Accounting (AAA) model**, how these three components work together, and how protocols such as **RADIUS** and **TACACS+** implement AAA in enterprise networks.
