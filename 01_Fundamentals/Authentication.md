# Authentication

Authentication is the process of verifying the identity of a user, device, or application before granting access to a system or resource.

It is the **first step** in access control. Before a system decides **what you are allowed to do (Authorization)**, it must first verify **who you are (Authentication)**.

Authentication is one of the most fundamental concepts in cybersecurity and is used in almost every digital service, including online banking, email, cloud platforms, operating systems, and enterprise networks.

---

# Table of Contents

- What is Authentication?
- Why is Authentication Important?
- Authentication vs Authorization
- Authentication Factors
- Types of Authentication
- Multi-Factor Authentication (MFA)
- Password Security
- Passwordless Authentication
- Single Sign-On (SSO)
- Common Authentication Protocols
- Authentication Attacks
- Best Practices
- Interview Questions
- Summary

---

# What is Authentication?

**Authentication** is the process of confirming that a user or system is genuinely who they claim to be.

It answers the question:

> **"Who are you?"**

Only after successful authentication does the system decide what resources the user can access.

---

# Authentication Process

```text
User
 │
 ▼
Enter Credentials
 │
 ▼
Authentication Server
 │
 ▼
Credentials Verified?
 │
 ├── Yes ──► User Authenticated
 │
 └── No ───► Access Denied
```

---

# Why is Authentication Important?

Without authentication:

- Anyone could access sensitive information.
- Attackers could impersonate legitimate users.
- Confidential business data could be exposed.
- Financial fraud could occur.

Authentication ensures that only verified users can access protected systems.

---

# Authentication vs Authorization

These two concepts are often confused.

| Authentication | Authorization |
|---------------|---------------|
| Verifies identity | Determines permissions |
| Happens first | Happens after authentication |
| "Who are you?" | "What can you access?" |
| Login process | Access control process |

### Example

An employee logs into a company portal.

- Username and password verify the employee's identity (**Authentication**).
- The employee is allowed to access only the HR portal (**Authorization**).

---

# Authentication Factors

Authentication is based on one or more **factors**.

## 1. Something You Know (Knowledge Factor)

Information known only to the user.

### Examples

- Password
- PIN
- Security Question
- Passphrase

---

## 2. Something You Have (Possession Factor)

A physical object owned by the user.

### Examples

- Smartphone
- Hardware Token
- Smart Card
- USB Security Key
- OTP Device

---

## 3. Something You Are (Inherence Factor)

A unique biological characteristic.

### Examples

- Fingerprint
- Face Recognition
- Iris Scan
- Retina Scan
- Voice Recognition

---

## 4. Somewhere You Are (Location Factor)

Authentication based on the user's geographic location.

### Examples

- Office Network
- GPS Location
- Country-Based Access

---

## 5. Something You Do (Behavior Factor)

Authentication based on user behavior.

### Examples

- Typing Speed
- Mouse Movement
- Signature Pattern
- Walking Style (Gait Analysis)

---

# Types of Authentication

## Password-Based Authentication

The most common authentication method.

The user enters:

- Username
- Password

### Advantages

- Easy to use
- Low cost

### Disadvantages

- Weak passwords
- Password reuse
- Phishing attacks
- Brute-force attacks

---

## PIN-Based Authentication

A short numeric code used to unlock devices or applications.

Example:

- ATM PIN
- Mobile Phone PIN

---

## Biometric Authentication

Uses physical characteristics for authentication.

### Examples

- Fingerprint
- Face ID
- Iris Scan
- Palm Recognition

### Advantages

- Convenient
- Difficult to copy

### Limitations

- Sensor failures
- Privacy concerns
- Cannot be changed if compromised

---

## Token-Based Authentication

A temporary token is generated after successful login.

Examples include:

- Session Tokens
- JSON Web Tokens (JWT)
- OAuth Access Tokens

Widely used in web applications and APIs.

---

## Certificate-Based Authentication

Uses digital certificates to verify identity.

Commonly used for:

- VPN
- Enterprise Wi-Fi
- Smart Cards
- Client Authentication

---

# Multi-Factor Authentication (MFA)

## Definition

Multi-Factor Authentication requires users to provide **two or more different authentication factors**.

Example:

- Password (Something You Know)
- OTP from Mobile App (Something You Have)

---

## Why MFA is Important

Even if an attacker steals a password, they still need the second authentication factor.

This significantly reduces the risk of account compromise.

---

## Common MFA Methods

- SMS OTP
- Email OTP
- Authenticator Apps
- Hardware Security Keys
- Push Notifications
- Biometrics

---

# Password Security

Passwords remain one of the most widely used authentication methods.

A strong password should:

- Be at least 12–16 characters long
- Include uppercase and lowercase letters
- Include numbers
- Include special characters
- Avoid dictionary words
- Be unique for every account

---

## Weak Password Examples

- 123456
- password
- admin
- qwerty
- iloveyou

---

## Strong Password Example

```text
MyC@tLovesP1zza!2026
```

A long passphrase is generally easier to remember and harder to crack than a short, complex password.

---

# Password Managers

Password managers securely store and generate strong, unique passwords.

### Benefits

- Unique password for every account
- Automatic password generation
- Secure storage
- Reduced password reuse

---

# Passwordless Authentication

Passwordless authentication eliminates traditional passwords.

Instead, users authenticate using:

- Biometrics
- Security Keys
- Passkeys
- Device-Based Authentication

### Benefits

- Resistant to phishing
- Better user experience
- Reduced password management

---

# Single Sign-On (SSO)

Single Sign-On allows users to authenticate once and access multiple applications without logging in repeatedly.

### Example

An employee logs into Microsoft Entra ID (Azure AD) and automatically gains access to Outlook, Teams, and SharePoint.

### Advantages

- Improved user experience
- Fewer passwords
- Centralized identity management

---

# Common Authentication Protocols

| Protocol | Purpose |
|----------|---------|
| Kerberos | Network authentication in Active Directory environments |
| LDAP | Directory service authentication |
| OAuth 2.0 | Authorization for third-party applications |
| OpenID Connect (OIDC) | User authentication built on OAuth 2.0 |
| SAML | Enterprise Single Sign-On |
| RADIUS | Network access authentication |
| TACACS+ | Administrative access to network devices |

> **Note:** OAuth is primarily an **authorization** framework, while OpenID Connect extends OAuth to provide authentication.

---

# Common Authentication Attacks

## Brute Force Attack

Attempts every possible password until the correct one is found.

---

## Dictionary Attack

Uses a predefined list of common passwords.

---

## Password Spraying

Attempts a few common passwords against many user accounts.

---

## Credential Stuffing

Uses usernames and passwords leaked from previous data breaches.

---

## Phishing

Tricks users into revealing login credentials through fake emails or websites.

---

## Keylogging

Records everything typed on a keyboard, including usernames and passwords.

---

## Session Hijacking

Steals a valid session token to impersonate an authenticated user.

---

# Best Practices

- Enable Multi-Factor Authentication (MFA).
- Use long, unique passwords.
- Use a password manager.
- Never reuse passwords.
- Change default credentials immediately.
- Lock accounts after repeated failed login attempts.
- Use HTTPS for authentication pages.
- Monitor login activity for suspicious behavior.
- Implement least privilege after authentication.
- Prefer passwordless authentication where appropriate.

---

# Real-World Example

## Online Banking

### Step 1 – Username

The user enters their username.

### Step 2 – Password

The user enters their password.

### Step 3 – OTP

The bank sends a one-time password (OTP) to the registered mobile device.

### Step 4 – Verification

The server verifies both the password and the OTP.

### Step 5 – Access Granted

The user is successfully authenticated and can access their account.

This is an example of **Multi-Factor Authentication** because it combines:

- Something You Know (Password)
- Something You Have (Mobile Phone)

---

# Key Points

- Authentication verifies identity.
- Authorization determines permissions.
- Authentication always occurs before authorization.
- Multi-Factor Authentication provides stronger security than passwords alone.
- Passwordless authentication is becoming increasingly common.
- Strong authentication significantly reduces the risk of unauthorized access.

---

# Interview Questions

### 1. What is authentication?

Authentication is the process of verifying the identity of a user, device, or application before granting access.

---

### 2. What is the difference between authentication and authorization?

Authentication verifies identity ("Who are you?"), while authorization determines what an authenticated user is allowed to access ("What can you do?").

---

### 3. What are the three primary authentication factors?

- Something You Know
- Something You Have
- Something You Are

---

### 4. What is Multi-Factor Authentication (MFA)?

MFA requires two or more different authentication factors to verify a user's identity.

---

### 5. Why is MFA more secure than password-only authentication?

Because compromising one factor (such as a password) is not sufficient to gain access; the attacker must also compromise an additional factor.

---

### 6. What is Single Sign-On (SSO)?

SSO allows users to authenticate once and access multiple applications without logging in separately to each one.

---

### 7. What is the purpose of a password manager?

A password manager securely stores and generates strong, unique passwords for different accounts.

---

### 8. What is passwordless authentication?

Passwordless authentication verifies identity using methods such as biometrics, passkeys, or security keys instead of traditional passwords.

---

# Summary

Authentication is the process of verifying identity before granting access to systems and resources. It forms the first layer of access control and is essential for protecting sensitive information. Modern authentication combines multiple factors, such as passwords, biometrics, and security tokens, to improve security. Techniques like Multi-Factor Authentication (MFA), Single Sign-On (SSO), and passwordless authentication help organizations balance security and usability while defending against common authentication attacks.

---

## Next Topic

➡️ **Authorization.md** — Learn how organizations control access to resources using authorization models such as **Role-Based Access Control (RBAC), Attribute-Based Access Control (ABAC), Discretionary Access Control (DAC), and Mandatory Access Control (MAC)**.
