# Common Cyber Attacks

Cyber attacks are attempts to gain **unauthorized access**, **steal information**, **damage systems**, or **disrupt services**.

Understanding how common attacks work is one of the most important skills in cybersecurity. Security professionals must know **how attackers operate** and **how to defend against them**.

> **Note:** This document explains attacks for educational and defensive purposes only.

---

# Table of Contents

- What is a Cyber Attack?
- Cyber Attack Lifecycle
- Types of Cyber Attacks
  - Phishing
  - Malware
  - Virus
  - Worm
  - Trojan
  - Ransomware
  - Spyware
  - Rootkit
  - Password Attacks
  - Social Engineering
  - Denial of Service (DoS)
  - Distributed Denial of Service (DDoS)
  - Man-in-the-Middle (MITM)
  - SQL Injection (SQLi)
  - Cross-Site Scripting (XSS)
  - Cross-Site Request Forgery (CSRF)
  - Directory Traversal
  - File Inclusion (LFI/RFI)
  - Command Injection
- Attack Comparison
- Defense Strategies
- Interview Questions
- Summary

---

# What is a Cyber Attack?

A **cyber attack** is any attempt to compromise the confidentiality, integrity, or availability (CIA Triad) of computer systems, networks, applications, or data.

Attackers may attempt to:

- Steal sensitive information
- Gain unauthorized access
- Install malware
- Disrupt services
- Extort money
- Spy on users

---

# Cyber Attack Lifecycle

Most attacks follow a similar pattern.

```text
Reconnaissance
      │
      ▼
Scanning & Enumeration
      │
      ▼
Initial Access
      │
      ▼
Privilege Escalation
      │
      ▼
Data Access or System Control
      │
      ▼
Maintain Access
      │
      ▼
Cover Tracks
```

---

# 1. Phishing

## Definition

Phishing is a **social engineering attack** where an attacker pretends to be a trusted entity to trick users into revealing sensitive information.

---

## Common Targets

- Passwords
- OTPs
- Credit card details
- Banking credentials
- Company logins

---

## Example

You receive an email that appears to be from your bank asking you to "verify your account." The link opens a fake login page that steals your username and password.

---

## Prevention

- Verify the sender's email address.
- Do not click suspicious links.
- Enable Multi-Factor Authentication (MFA).
- Check URLs before entering credentials.
- Report phishing emails.

---

# 2. Malware

## Definition

**Malware** (Malicious Software) is software designed to harm, disrupt, or gain unauthorized access to systems.

Malware includes:

- Virus
- Worm
- Trojan
- Ransomware
- Spyware
- Rootkit

---

# 3. Virus

## Definition

A **virus** attaches itself to legitimate files or programs and spreads when the infected file is executed.

---

## Characteristics

- Requires user action
- Infects files
- Can corrupt or delete data

---

## Prevention

- Use antivirus software.
- Avoid unknown downloads.
- Keep software updated.

---

# 4. Worm

## Definition

A **worm** is malware that spreads automatically across networks without user interaction.

---

## Characteristics

- Self-replicating
- Consumes bandwidth
- Spreads rapidly

---

## Prevention

- Patch systems regularly.
- Disable unnecessary services.
- Use network segmentation.

---

# 5. Trojan

## Definition

A **Trojan Horse** disguises itself as legitimate software but performs malicious actions after installation.

---

## Example

A fake "Free Game" installer secretly installs a Remote Access Trojan (RAT).

---

## Prevention

- Download software only from trusted sources.
- Verify digital signatures.
- Avoid pirated software.

---

# 6. Ransomware

## Definition

Ransomware encrypts files or systems and demands payment for the decryption key.

---

## Impact

- Data becomes inaccessible.
- Business operations stop.
- Financial losses occur.

---

## Prevention

- Regular backups
- Security patches
- Email filtering
- Endpoint Detection and Response (EDR)
- Employee awareness training

---

# 7. Spyware

## Definition

Spyware secretly monitors user activity and collects sensitive information.

---

## Information Collected

- Passwords
- Browsing history
- Banking information
- Keystrokes

---

## Prevention

- Install trusted software only.
- Keep antivirus updated.
- Avoid suspicious browser extensions.

---

# 8. Rootkit

## Definition

A **rootkit** is malware designed to hide itself and provide attackers with persistent, privileged access to a system.

---

## Characteristics

- Hides processes
- Hides files
- Avoids detection
- Maintains long-term access

---

## Prevention

- Secure Boot
- OS updates
- EDR solutions
- System integrity monitoring

---

# 9. Password Attacks

Password attacks attempt to obtain user credentials.

---

## Common Types

### Brute Force

Tries every possible password combination.

### Dictionary Attack

Uses a predefined list of common passwords.

### Credential Stuffing

Uses stolen credentials from previous data breaches.

### Password Spraying

Attempts a few common passwords across many accounts.

---

## Prevention

- Strong passwords
- MFA
- Account lockout policies
- Password managers

---

# 10. Social Engineering

## Definition

Social engineering manipulates people into revealing confidential information or performing unsafe actions.

---

## Examples

- Phishing
- Vishing (Voice phishing)
- Smishing (SMS phishing)
- Tailgating
- Pretexting
- Baiting

---

## Prevention

- Security awareness training
- Verify requests
- Never share passwords
- Follow company security policies

---

# 11. Denial of Service (DoS)

## Definition

A Denial of Service attack overwhelms a service from a **single source**, making it unavailable to legitimate users.

---

## Prevention

- Firewalls
- Rate limiting
- Traffic filtering

---

# 12. Distributed Denial of Service (DDoS)

## Definition

A DDoS attack uses **multiple compromised systems (botnets)** to flood a target with traffic.

---

## Impact

- Website downtime
- Revenue loss
- Poor user experience

---

## Prevention

- CDN
- Web Application Firewall (WAF)
- DDoS protection services
- Load balancing

---

# 13. Man-in-the-Middle (MITM)

## Definition

In a MITM attack, an attacker secretly intercepts communication between two parties.

---

## Example

Connecting to an unsecured public Wi-Fi network allows an attacker to capture unencrypted traffic.

---

## Prevention

- HTTPS
- VPN
- Secure Wi-Fi
- Certificate validation

---

# 14. SQL Injection (SQLi)

## Definition

SQL Injection occurs when unsanitized user input is interpreted as SQL commands by the database.

---

## Impact

- Read database contents
- Modify records
- Delete data
- Bypass authentication

---

## Prevention

- Parameterized queries
- Prepared statements
- Input validation
- Least privilege for database accounts

---

# 15. Cross-Site Scripting (XSS)

## Definition

XSS occurs when attackers inject malicious JavaScript into web pages viewed by other users.

---

## Impact

- Cookie theft
- Session hijacking
- Fake login forms
- Browser redirection

---

## Prevention

- Output encoding
- Input validation
- Content Security Policy (CSP)
- Secure cookie settings

---

# 16. Cross-Site Request Forgery (CSRF)

## Definition

CSRF tricks an authenticated user into submitting unwanted requests to a trusted website.

---

## Example

A logged-in user visits a malicious webpage that silently submits a request to change their account settings.

---

## Prevention

- CSRF tokens
- SameSite cookies
- Re-authentication for sensitive actions

---

# 17. Directory Traversal

## Definition

Directory Traversal allows attackers to access files outside the intended web directory.

---

## Example

Instead of accessing:

```text
/images/logo.png
```

The attacker attempts to access:

```text
../../etc/passwd
```

---

## Prevention

- Validate file paths
- Restrict file access
- Use allowlists

---

# 18. File Inclusion (LFI/RFI)

## Local File Inclusion (LFI)

Allows attackers to include files already present on the server.

---

## Remote File Inclusion (RFI)

Allows attackers to include files from remote locations (only in vulnerable configurations).

---

## Prevention

- Disable unnecessary inclusion features
- Validate file names
- Restrict user input

---

# 19. Command Injection

## Definition

Command Injection occurs when user input is passed directly to the operating system as a command.

---

## Impact

- Execute arbitrary commands
- Read sensitive files
- Gain system control

---

## Prevention

- Avoid shell execution where possible
- Validate input
- Use parameterized APIs
- Run services with least privilege

---

# Attack Comparison

| Attack | Primary Target | Main Goal |
|--------|----------------|-----------|
| Phishing | Users | Steal credentials |
| Virus | Files | Corrupt data |
| Worm | Networks | Rapid spread |
| Trojan | Users | Install malware |
| Ransomware | Systems | Extort money |
| Spyware | Users | Collect information |
| Rootkit | Operating System | Hide malicious activity |
| Password Attack | Accounts | Gain access |
| DoS | Service | Disrupt availability |
| DDoS | Service | Overwhelm systems |
| MITM | Communication | Intercept data |
| SQL Injection | Database | Access or modify data |
| XSS | Web Users | Execute malicious scripts |
| CSRF | Authenticated Users | Perform unauthorized actions |
| Directory Traversal | File System | Read restricted files |
| File Inclusion | Web Server | Execute or expose files |
| Command Injection | Operating System | Execute system commands |

---

# General Defense Strategies

- Use Multi-Factor Authentication (MFA).
- Keep operating systems and software updated.
- Apply security patches promptly.
- Follow the Principle of Least Privilege.
- Encrypt sensitive data.
- Deploy firewalls and IDS/IPS.
- Use Endpoint Detection and Response (EDR).
- Maintain regular backups.
- Conduct security awareness training.
- Perform regular vulnerability assessments and penetration testing.

---

# Interview Questions

### 1. What is the difference between a Virus and a Worm?

A virus requires user action to spread, while a worm spreads automatically without user interaction.

---

### 2. What is the purpose of ransomware?

To encrypt files or systems and demand payment for their recovery.

---

### 3. What is the difference between DoS and DDoS?

A DoS attack originates from a single source, whereas a DDoS attack uses multiple compromised devices (a botnet).

---

### 4. How can SQL Injection be prevented?

By using parameterized queries, prepared statements, proper input validation, and least-privileged database accounts.

---

### 5. What is the primary goal of phishing?

To trick users into revealing sensitive information such as usernames, passwords, or financial details.

---

### 6. Why is HTTPS important in preventing MITM attacks?

HTTPS encrypts communication and authenticates the server using digital certificates, reducing the risk of interception and tampering.

---

# Summary

Cyber attacks target people, systems, networks, and applications using a wide range of techniques. Some attacks exploit human behavior, such as phishing and social engineering, while others exploit technical weaknesses, such as SQL Injection or Command Injection. Understanding how these attacks work and implementing layered security controls are essential for reducing organizational risk and protecting the confidentiality, integrity, and availability of information.

---

## Next Topic

➡️ **Security-Controls.md** — Learn how organizations defend against cyber threats using **Administrative, Technical, and Physical Security Controls**, along with preventive, detective, corrective, deterrent, compensating, and recovery controls.
