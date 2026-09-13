# 🔐 Cryptography Notes

A structured guide to **cryptography, encryption, hashing, digital signatures, certificates, and common cryptographic concepts** used in cybersecurity.

---

## 📚 Table of Contents

* [What is Cryptography?](#what-is-cryptography)
* [Why Cryptography is Important](#why-cryptography-is-important)
* [Cryptography vs Encryption](#cryptography-vs-encryption)
* [Basic Cryptographic Terms](#basic-cryptographic-terms)
* [Plaintext and Ciphertext](#plaintext-and-ciphertext)
* [Encryption and Decryption](#encryption-and-decryption)
* [Keys](#keys)
* [Symmetric Encryption](#symmetric-encryption)
* [Asymmetric Encryption](#asymmetric-encryption)
* [Symmetric vs Asymmetric Encryption](#symmetric-vs-asymmetric-encryption)
* [Hashing](#hashing)
* [Encryption vs Hashing](#encryption-vs-hashing)
* [Encoding vs Encryption vs Hashing](#encoding-vs-encryption-vs-hashing)
* [Common Cryptographic Algorithms](#common-cryptographic-algorithms)
* [AES](#aes)
* [RSA](#rsa)
* [ECC](#ecc)
* [Diffie-Hellman](#diffie-hellman)
* [Digital Signatures](#digital-signatures)
* [Digital Certificates](#digital-certificates)
* [PKI](#pki)
* [SSL/TLS](#ssltls)
* [HTTPS](#https)
* [Password Storage](#password-storage)
* [Salting](#salting)
* [Common Cryptographic Attacks](#common-cryptographic-attacks)
* [Cryptography in Cybersecurity](#cryptography-in-cybersecurity)
* [Linux Cryptography Tools](#linux-cryptography-tools)
* [Quick Reference](#quick-reference)

---

# What is Cryptography?

**Cryptography** is the practice of protecting information by transforming it into a form that unauthorized people cannot understand or use.

The word comes from:

* **Crypto** → hidden or secret
* **Graphy** → writing

In cybersecurity, cryptography is used to protect:

* Passwords
* Messages
* Files
* Network communication
* Financial transactions
* Authentication information
* Digital identities

### Simple Example

Suppose Alice wants to send:

```text
Meet me at 10 PM
```

Instead of sending the message directly, cryptography can transform it into something like:

```text
8fA92xL... 
```

The receiver can use the appropriate cryptographic mechanism to recover or verify the original information.

---

# Why Cryptography is Important

Cryptography helps provide the major security properties of:

### 1. Confidentiality

Only authorized people should be able to read the information.

Example:

```text
Alice → encrypted message → Bob
```

An attacker intercepting the message should not be able to understand it.

---

### 2. Integrity

Data should not be modified without detection.

Example:

```text
Original file
    ↓
Hash
    ↓
SHA-256 value
```

If the file changes, its hash should also change.

---

### 3. Authentication

Cryptography can help verify the identity of a user, system, or server.

Example:

```text
Client → Server
       ↓
Certificate / cryptographic authentication
```

---

### 4. Non-Repudiation

Digital signatures can provide evidence that a particular private key was used to sign data.

This is useful for:

* Signed documents
* Software releases
* Digital transactions
* Certificates

---

# Cryptography vs Encryption

These terms are related but not identical.

### Cryptography

The broader field of protecting information using mathematical techniques.

It includes:

* Encryption
* Hashing
* Digital signatures
* Key exchange
* Authentication mechanisms

### Encryption

A specific cryptographic technique used to protect confidentiality by transforming readable data into unreadable ciphertext.

Therefore:

```text
Cryptography
├── Encryption
├── Hashing
├── Digital Signatures
├── Key Exchange
└── Other cryptographic mechanisms
```

---

# Basic Cryptographic Terms

| Term        | Meaning                                                          |
| ----------- | ---------------------------------------------------------------- |
| Plaintext   | Original readable data                                           |
| Ciphertext  | Encrypted/unreadable data                                        |
| Encryption  | Plaintext → Ciphertext                                           |
| Decryption  | Ciphertext → Plaintext                                           |
| Key         | Secret or mathematical value used by an algorithm                |
| Cipher      | Algorithm used for encryption/decryption                         |
| Hash        | Fixed-length representation of data                              |
| Salt        | Random data added before password hashing                        |
| Signature   | Cryptographic proof associated with data                         |
| Certificate | Digital document used to associate an identity with a public key |

---

# Plaintext and Ciphertext

## Plaintext

The original readable information.

Example:

```text
Hello World
```

## Ciphertext

The transformed output produced by encryption.

Example:

```text
X7a9P2kLm...
```

Conceptually:

```text
Plaintext
    ↓
Encryption + Key
    ↓
Ciphertext
```

To recover the original data:

```text
Ciphertext
    ↓
Decryption + Key
    ↓
Plaintext
```

---

# Encryption and Decryption

### Encryption

Converts plaintext into ciphertext.

```text
Plaintext + Key
       ↓
   Encryption
       ↓
Ciphertext
```

### Decryption

Converts ciphertext back into plaintext.

```text
Ciphertext + Key
       ↓
   Decryption
       ↓
Plaintext
```

The exact process depends on the cryptographic algorithm.

---

# Keys

A **cryptographic key** is a value used by a cryptographic algorithm.

Keys are central to modern cryptography.

For example:

```text
Data + Key + Algorithm
        ↓
    Ciphertext
```

The security of a cryptographic system depends heavily on how keys are:

* Generated
* Stored
* Protected
* Distributed
* Rotated
* Revoked

---

# Symmetric Encryption

**Symmetric encryption** uses the same secret key for encryption and decryption.

```text
             Same Key
                │
                ▼
Plaintext → Encryption → Ciphertext
                            │
                            ▼
                       Decryption
                            │
                            ▼
                         Plaintext
```

### Example

Alice and Bob both know:

```text
SecretKey123
```

Alice encrypts a message using the key.

Bob uses the same key to decrypt it.

### Advantages

* Fast
* Efficient for large amounts of data
* Suitable for files and network traffic

### Disadvantage

The secret key must be securely shared.

If an attacker obtains the key, they may be able to decrypt the protected data.

### Common Symmetric Algorithms

* AES
* ChaCha20
* 3DES — legacy/deprecated for modern use

---

# Asymmetric Encryption

**Asymmetric cryptography** uses a pair of keys:

* Public key
* Private key

The keys are mathematically related but serve different purposes.

```text
Public Key
    ↓
Can be shared openly

Private Key
    ↓
Must remain secret
```

A common confidentiality model is:

```text
Message
   ↓
Encrypt with Bob's Public Key
   ↓
Ciphertext
   ↓
Decrypt with Bob's Private Key
   ↓
Message
```

Only Bob should possess the private key.

### Advantages

* Solves many key-distribution problems
* Supports digital signatures
* Enables secure key exchange and authentication

### Disadvantage

Generally slower than symmetric encryption.

### Common Asymmetric Algorithms

* RSA
* ECC-based cryptography
* Diffie-Hellman / ECDH for key agreement

---

# Symmetric vs Asymmetric Encryption

| Feature            | Symmetric         | Asymmetric                               |
| ------------------ | ----------------- | ---------------------------------------- |
| Keys               | One shared secret | Public + private key                     |
| Speed              | Fast              | Slower                                   |
| Large data         | Suitable          | Usually not preferred                    |
| Key distribution   | More difficult    | Easier for public keys                   |
| Digital signatures | No                | Yes                                      |
| Examples           | AES, ChaCha20     | RSA, ECC                                 |
| Main use           | Data encryption   | Key exchange, signatures, authentication |

---

# Hashing

A **hash function** converts input data into a fixed-length output called a hash or digest.

```text
Input Data
    ↓
Hash Function
    ↓
Hash / Digest
```

Example:

```text
"Hello"
    ↓
SHA-256
    ↓
Fixed-length hash
```

A secure cryptographic hash function should make it computationally difficult to:

* Recover the original input
* Find another input producing the same hash
* Intentionally manipulate the hash

### Important

Hashing is generally considered **one-way**.

There is no normal "decrypt hash" operation.

---

# Common Hash Algorithms

| Algorithm | Status                                                      |
| --------- | ----------------------------------------------------------- |
| MD5       | Broken for collision resistance; avoid for security         |
| SHA-1     | Broken for collision resistance; avoid for new security use |
| SHA-256   | Widely used                                                 |
| SHA-512   | Widely used                                                 |
| SHA-3     | Modern cryptographic hash family                            |

For password storage, general-purpose hashes such as SHA-256 should **not** normally be used alone. Password-specific password hashing functions should be used instead.

---

# Encryption vs Hashing

| Feature                   | Encryption                | Hashing                                                     |
| ------------------------- | ------------------------- | ----------------------------------------------------------- |
| Purpose                   | Confidentiality           | Integrity / fingerprinting                                  |
| Reversible                | Yes, with the correct key | No                                                          |
| Uses key                  | Usually                   | Normally no secret key                                      |
| Original data recoverable | Yes                       | No                                                          |
| Example                   | AES                       | SHA-256                                                     |
| Typical use               | Protect files/messages    | Verify data / password storage with proper password hashing |

### Remember

```text
Encryption → Can be decrypted
Hashing    → Cannot normally be reversed
```

---

# Encoding vs Encryption vs Hashing

These concepts are often confused.

## Encoding

Encoding changes data into another representation so that systems can store or transmit it.

Example:

```text
Text
 ↓
Base64
 ↓
Encoded text
```

Encoding is **not encryption**.

Base64 provides no confidentiality.

---

## Encryption

Encryption protects confidentiality.

```text
Plaintext
   ↓
Encryption + Key
   ↓
Ciphertext
```

---

## Hashing

Hashing creates a fixed-size digest.

```text
Data
 ↓
Hash Function
 ↓
Digest
```

### Comparison

| Method     | Purpose                  | Secret?      | Reversible?      |
| ---------- | ------------------------ | ------------ | ---------------- |
| Encoding   | Representation           | No           | Yes, by decoding |
| Encryption | Confidentiality          | Key required | Yes, with key    |
| Hashing    | Integrity/fingerprinting | No*          | No               |

`*` Some hash constructions can use a secret key, such as HMAC.

---

# AES

**AES (Advanced Encryption Standard)** is a widely used symmetric encryption algorithm.

AES supports:

* AES-128
* AES-192
* AES-256

The numbers represent the key size in bits.

```text
AES-128 → 128-bit key
AES-192 → 192-bit key
AES-256 → 256-bit key
```

AES is commonly used for:

* File encryption
* Disk encryption
* VPNs
* Applications
* Network protocols

AES itself is a block cipher. In practical systems, it is used with a **mode of operation**, such as:

* GCM
* CTR
* CBC — legacy in many applications

For new designs, authenticated encryption modes such as **AES-GCM** are generally preferred because they provide confidentiality and integrity together.

---

# RSA

**RSA** is an asymmetric cryptographic algorithm.

It uses:

```text
Public Key
Private Key
```

RSA can be used for:

* Encryption
* Digital signatures
* Key-related operations

RSA security is based on mathematical properties involving large integers and factoring.

Modern RSA deployments require sufficiently large keys and appropriate padding schemes.

---

# ECC

**ECC (Elliptic Curve Cryptography)** is a family of public-key cryptographic techniques based on elliptic-curve mathematics.

ECC provides strong security with relatively small key sizes.

It is used in:

* TLS
* Digital signatures
* Key exchange
* Certificates
* Modern applications

Examples include:

* ECDSA
* ECDH
* Ed25519

---

# Diffie-Hellman

**Diffie-Hellman (DH)** is a key-agreement method.

It allows two parties to establish a shared secret over an insecure communication channel without directly transmitting the secret itself.

Conceptually:

```text
Alice                       Bob
  │                           │
  │──── Public information ──►│
  │                           │
  │◄─── Public information ───│
  │                           │
  └──── Shared Secret ────────┘
```

The resulting shared secret can then be used with a symmetric encryption algorithm.

### Important

Diffie-Hellman itself is primarily about **key agreement**, not encrypting the entire message.

A common modern variant is:

```text
ECDH
```

which uses elliptic curves.

---

# Digital Signatures

A **digital signature** provides a way to verify:

* Who signed the data
* Whether the data was modified

A simplified model:

```text
Message
   ↓
Hash
   ↓
Sign with Private Key
   ↓
Digital Signature
```

The receiver can use the corresponding public key to verify the signature.

Conceptually:

```text
Private Key → Signing
Public Key  → Verification
```

### Digital Signature Properties

Digital signatures help provide:

* Authentication
* Integrity
* Non-repudiation

---

# Digital Certificates

A **digital certificate** binds an identity to a public key.

A certificate commonly contains information such as:

* Subject/domain
* Public key
* Certificate issuer
* Validity period
* Serial number
* Digital signature of the issuer

For example:

```text
example.com
     │
     ▼
Digital Certificate
     │
     ├── Identity
     ├── Public Key
     ├── Validity
     └── CA Signature
```

Certificates are heavily used by HTTPS.

---

# Certificate Authorities

A **Certificate Authority (CA)** is a trusted entity that issues or signs digital certificates.

Examples of certificate authorities include organizations such as:

* DigiCert
* Let's Encrypt
* Sectigo

A simplified trust relationship:

```text
Browser
   ↓
Trusts CA
   ↓
CA signs certificate
   ↓
Certificate belongs to example.com
```

The browser can use this chain of trust to help verify the server's identity.

---

# PKI

**PKI (Public Key Infrastructure)** is the collection of technologies, policies, roles, and processes used to manage public-key cryptography.

PKI commonly involves:

* Public/private keys
* Digital certificates
* Certificate Authorities
* Certificate validation
* Certificate revocation
* Trust chains

Simplified:

```text
                Root CA
                  │
                  ▼
            Intermediate CA
                  │
                  ▼
         Server Certificate
                  │
                  ▼
               Website
```

---

# SSL/TLS

**TLS (Transport Layer Security)** is a cryptographic protocol used to secure network communication.

SSL is the older predecessor and is deprecated.

TLS provides mechanisms for:

* Confidentiality
* Integrity
* Authentication

It is widely used for:

* HTTPS
* Secure APIs
* Email security
* Other encrypted network protocols

### Simplified TLS Concept

```text
Client
   │
   │── ClientHello ────────►
   │
   │◄──── ServerHello ─────
   │◄──── Certificate ─────
   │
   │   Key Agreement
   │
   │════════ Encrypted ════│
```

Modern TLS commonly uses asymmetric cryptography for authentication/key establishment and symmetric cryptography for the actual application data because symmetric encryption is much faster.

---

# HTTPS

**HTTPS = HTTP + TLS**

HTTP by itself does not provide encryption.

HTTPS protects HTTP communication using TLS.

```text
HTTP
 +
TLS
 =
HTTPS
```

Example:

```text
https://example.com
```

HTTPS helps protect:

* Login credentials
* Cookies
* API requests
* Personal information
* Web traffic

---

# Password Storage

Passwords should **not** normally be stored as plaintext.

Bad:

```text
username: bhavya
password: MyPassword123
```

If the database is compromised, the passwords are immediately exposed.

A better approach is to use a dedicated password hashing function.

Common password-hashing algorithms include:

* Argon2
* bcrypt
* scrypt
* PBKDF2

Conceptually:

```text
Password
   ↓
Password Hashing Function
   ↓
Stored Hash
```

During login:

```text
Entered Password
       ↓
Hash using stored parameters
       ↓
Compare with stored password hash
```

---

# Salting

A **salt** is random data added to a password before password hashing.

Conceptually:

```text
Password + Random Salt
          ↓
   Password Hashing
          ↓
      Stored Hash
```

Example:

```text
Password:
password123

Salt:
A8f72K...

Hash:
...
```

Each password should generally have a unique salt.

### Why Use Salts?

Without salts, identical passwords can produce identical hashes.

Salts help defend against:

* Precomputed hash tables
* Rainbow-table attacks
* Easy identification of users with identical passwords

The salt does **not** need to be kept secret.

---

# Pepper

A **pepper** is an additional secret value used with password hashing.

Unlike a salt, a pepper should be kept secret and stored separately from the password database.

Conceptually:

```text
Password + Salt + Pepper
          ↓
    Password Hashing
```

The exact implementation depends on the application's security architecture.

---

# Common Cryptographic Attacks

Cryptographic systems can fail because of weak algorithms, poor implementation, weak keys, or bad key management.

## 1. Brute-Force Attack

An attacker tries many possible keys or passwords.

```text
Key 1
Key 2
Key 3
...
Key N
```

Strong keys and passwords make brute-force attacks more difficult.

---

## 2. Dictionary Attack

The attacker tries words and commonly used passwords from a dictionary.

Example:

```text
password
admin
qwerty
welcome
123456
```

Strong, unique passwords reduce this risk.

---

## 3. Rainbow Table Attack

An attacker uses precomputed tables of password hashes.

Unique salts make these attacks significantly less effective.

---

## 4. Man-in-the-Middle Attack

An attacker positions themselves between two communicating parties.

```text
Alice
  │
  ▼
Attacker
  │
  ▼
Bob
```

TLS certificates and authenticated key exchange help defend against this type of attack.

---

## 5. Replay Attack

An attacker captures valid communication and later retransmits it.

Security protocols can use mechanisms such as:

* Nonces
* Timestamps
* Sequence numbers
* Session-specific values

to help prevent replay.

---

## 6. Collision Attack

A collision occurs when two different inputs produce the same hash.

```text
Input A ──┐
          ├── Same Hash
Input B ──┘
```

Modern security systems should avoid cryptographically broken hash algorithms such as MD5 and SHA-1 for collision-sensitive applications.

---

## 7. Weak Key Attack

Using predictable, short, reused, or improperly generated keys can weaken encryption.

Good cryptographic systems require secure random number generation and appropriate key sizes.

---

# Cryptography in Cybersecurity

Cryptography appears throughout cybersecurity.

### Web Security

```text
HTTPS
TLS
Certificates
Cookies
Authentication
```

### Network Security

```text
VPN
TLS
IPsec
Secure protocols
```

### Application Security

```text
Password hashing
API authentication
Tokens
Digital signatures
Encrypted data
```

### Cloud Security

```text
Data-at-rest encryption
Data-in-transit encryption
Key management
Secrets management
```

### Digital Forensics

Cryptographic hashes are commonly used to verify that evidence or files have not changed.

Example:

```text
Evidence File
     ↓
SHA-256
     ↓
Hash Value
```

A later hash can be compared with the original hash to detect changes.

---

# Cryptography in Real Life

Consider logging into a website.

```text
User
 │
 │ HTTPS
 ▼
Web Server
 │
 ├── TLS protects communication
 │
 ├── Certificate helps authenticate server
 │
 └── Password stored using password hashing
```

During the connection:

```text
Asymmetric Cryptography
        ↓
Authentication / Key Establishment
        ↓
Symmetric Session Encryption
        ↓
Secure Data Transfer
```

This combination is important because asymmetric cryptography and symmetric cryptography have different strengths.

---

# Linux Cryptography Tools

Linux provides several useful tools for learning cryptography.

## OpenSSL

Check the version:

```bash
openssl version
```

Generate a random value:

```bash
openssl rand -hex 16
```

Calculate a SHA-256 hash:

```bash
openssl dgst -sha256 file.txt
```

Generate a private RSA key:

```bash
openssl genrsa -out private.key 2048
```

Extract the public key:

```bash
openssl rsa -in private.key -pubout -out public.key
```

> Use modern key-generation commands and appropriate key sizes for real deployments.

---

## SHA-256 with sha256sum

```bash
sha256sum file.txt
```

Example output:

```text
<hash>  file.txt
```

This is useful for checking file integrity.

---

## GPG

GPG is commonly used for encryption, decryption, and digital signatures.

Check installation:

```bash
gpg --version
```

Generate a key pair:

```bash
gpg --full-generate-key
```

List keys:

```bash
gpg --list-keys
```

Encrypt a file for a recipient:

```bash
gpg --encrypt --recipient user@example.com file.txt
```

Decrypt:

```bash
gpg --decrypt file.txt.gpg
```

Create a detached signature:

```bash
gpg --detach-sign file.txt
```

Verify a signature:

```bash
gpg --verify file.txt.sig file.txt
```

---

# Practical Example: File Integrity

Suppose you download:

```text
tool.zip
```

Calculate its hash:

```bash
sha256sum tool.zip
```

You receive:

```text
abc123... tool.zip
```

If the developer provides an official SHA-256 value, compare the two.

```text
Your hash
    ↓
abc123...

Official hash
    ↓
abc123...

Match → File is likely unchanged
```

A matching hash does not prove that the software is safe or trustworthy; it primarily verifies that the file matches the expected content.

---

# Practical Example: Encryption

Suppose Alice wants to send a confidential file to Bob.

A simplified asymmetric approach is:

```text
Bob generates:
    Public Key
    Private Key

Bob shares:
    Public Key

Alice:
    File
      ↓
    Encrypt using Bob's Public Key
      ↓
    Encrypted File

Bob:
    Encrypted File
      ↓
    Decrypt using Private Key
      ↓
    Original File
```

In real systems, hybrid encryption is commonly used instead of encrypting large files directly with an asymmetric algorithm.

---

# Hybrid Cryptography

Modern secure systems often combine symmetric and asymmetric cryptography.

For example:

```text
                 Asymmetric Cryptography
                         ↓
                  Establish Session Key
                         ↓
                 Symmetric Cryptography
                         ↓
                  Encrypt Actual Data
```

Why?

### Asymmetric cryptography

* Good for authentication and key establishment
* Relatively slow

### Symmetric cryptography

* Very fast
* Efficient for large amounts of data

Therefore, combining them provides practical security and performance.

---

# Cryptographic Best Practices

When designing or using cryptographic systems:

* Use well-established cryptographic algorithms.
* Do not create your own encryption algorithm.
* Use strong random number generators.
* Protect private keys.
* Never hard-code secrets in source code.
* Do not store passwords in plaintext.
* Use dedicated password-hashing algorithms.
* Use unique salts for password hashes.
* Use authenticated encryption where appropriate.
* Keep cryptographic libraries updated.
* Use TLS for sensitive network communication.
* Avoid deprecated algorithms such as MD5, SHA-1, DES, and 3DES for new security designs.
* Rotate and revoke keys when necessary.
* Minimize access to sensitive keys and secrets.

---

# Common Mistakes

### Mistake 1: Thinking Base64 is encryption

```text
Base64 ≠ Encryption
```

Base64 is an encoding scheme.

---

### Mistake 2: Thinking hashing can be decrypted

```text
Hash ≠ Encrypted Data
```

A cryptographic hash is designed to be one-way.

---

### Mistake 3: Storing plaintext passwords

```text
password123
```

should never simply be stored in a database.

Use a proper password hashing scheme.

---

### Mistake 4: Creating custom encryption

Do not invent your own cryptographic algorithm.

Use well-tested standards and libraries.

---

### Mistake 5: Protecting only data in storage

Security must consider both:

```text
Data at Rest
Data in Transit
```

For example:

* Disk/database encryption → data at rest
* TLS/HTTPS → data in transit

---

# Data at Rest vs Data in Transit

## Data at Rest

Data stored somewhere.

Examples:

* Hard drive
* Database
* Cloud storage
* Backup

Common protections:

```text
Encryption
Access Control
Key Management
```

---

## Data in Transit

Data moving across a network.

Examples:

* Web traffic
* API requests
* File transfers
* Emails

Common protections:

```text
TLS
VPN
Secure Protocols
```

---

# Cryptographic Terminology to Remember

```text
Plaintext
   ↓
Encryption
   ↓
Ciphertext
```

```text
Ciphertext
   ↓
Decryption
   ↓
Plaintext
```

```text
Data
   ↓
Hash Function
   ↓
Digest
```

```text
Private Key
   ↓
Digital Signature
   ↓
Public Key → Verification
```

```text
Public Key
   ↓
Encryption / Key Establishment

Private Key
   ↓
Decryption / Signature
```

---

# Quick Reference

| Concept                 | Main Purpose                                  | Example         |
| ----------------------- | --------------------------------------------- | --------------- |
| Encryption              | Confidentiality                               | AES             |
| Symmetric encryption    | Fast data encryption                          | AES, ChaCha20   |
| Asymmetric cryptography | Key exchange/signatures                       | RSA, ECC        |
| Hashing                 | Integrity/fingerprinting                      | SHA-256         |
| Password hashing        | Secure password storage                       | Argon2, bcrypt  |
| Salt                    | Defend password hashes against precomputation | Random salt     |
| Digital signature       | Authentication + integrity                    | ECDSA, Ed25519  |
| Certificate             | Identity ↔ public key                         | TLS certificate |
| PKI                     | Manage certificates and trust                 | CA hierarchy    |
| TLS                     | Secure network communication                  | HTTPS           |
| Base64                  | Data encoding                                 | Encoded text    |
| DH/ECDH                 | Key agreement                                 | TLS             |

---

# Cryptography Cheat Sheet

```text
Cryptography
│
├── Encryption
│   ├── Symmetric
│   │   ├── AES
│   │   └── ChaCha20
│   │
│   └── Asymmetric
│       ├── RSA
│       └── ECC
│
├── Hashing
│   ├── SHA-256
│   ├── SHA-512
│   └── SHA-3
│
├── Password Security
│   ├── Argon2
│   ├── bcrypt
│   ├── scrypt
│   └── PBKDF2
│
├── Key Exchange
│   ├── DH
│   └── ECDH
│
├── Digital Signatures
│   ├── RSA signatures
│   ├── ECDSA
│   └── Ed25519
│
└── PKI
    ├── Certificates
    ├── Certificate Authorities
    └── Trust Chains
```

---

# Final Summary

Cryptography is a fundamental part of cybersecurity.

The most important concepts to remember are:

```text
Encryption
→ Protects confidentiality

Hashing
→ Helps verify integrity and securely handle passwords
  when using appropriate password-hashing algorithms

Symmetric Cryptography
→ Fast encryption using shared secrets

Asymmetric Cryptography
→ Public/private key cryptography

Digital Signatures
→ Verify authenticity and integrity

Certificates
→ Bind identities to public keys

PKI
→ Provides infrastructure for managing trust

TLS
→ Protects network communication

Salting
→ Strengthens password hashing against precomputed attacks
```

A simple mental model:

```text
                 CRYPTOGRAPHY
                      │
       ┌──────────────┼──────────────┐
       │              │              │
   Encryption      Hashing       Signatures
       │              │              │
   ┌───┴───┐          │        Private Key
   │       │          │              ↓
Symmetric Asymmetric  │          Signature
   │       │           │             ↓
  AES    RSA/ECC     SHA-256      Verification
```

**Learn → Practice → Understand → Teach**
