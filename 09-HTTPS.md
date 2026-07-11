# Hypertext Transfer Protocol Secure (HTTPS)

## Introduction

**HTTPS (Hypertext Transfer Protocol Secure)** is the secure version of HTTP. It enables encrypted communication between a client (such as a web browser) and a web server, ensuring that sensitive information remains private and protected during transmission.

HTTPS combines the **Hypertext Transfer Protocol (HTTP)** with **Transport Layer Security (TLS)** (previously Secure Sockets Layer or SSL). By encrypting data exchanged between the client and the server, HTTPS prevents attackers from reading or modifying the information while it is in transit.

Today, HTTPS is the standard protocol for secure websites, online banking, e-commerce, cloud services, and web applications.

---

# Why is HTTPS Important?

HTTPS protects users and organizations by providing:

- Confidentiality through encryption
- Data integrity to prevent tampering
- Authentication using digital certificates
- Protection against many network attacks
- Secure online transactions

Modern browsers mark websites that do not use HTTPS as **"Not Secure"**.

---

# How HTTPS Works

When a user visits a secure website:

```
https://www.example.com
```

the following steps occur:

1. The browser resolves the domain name using DNS.
2. The browser establishes a TCP connection with the server (Port 443).
3. The browser and server perform the **TLS Handshake**.
4. The server presents its digital certificate.
5. The browser verifies the certificate.
6. An encrypted session is established.
7. HTTP data is exchanged securely.

---

# HTTPS Communication Flow

```
Browser
    │
DNS Lookup
    │
TCP Connection (Port 443)
    │
TLS Handshake
    │
Encrypted HTTPS Communication
    │
Web Server
```

---

# Default Port

HTTPS uses:

```
Port 443
```

This is the standard port for secure web communication.

---

# What is TLS?

**Transport Layer Security (TLS)** is a cryptographic protocol that provides:

- Encryption
- Authentication
- Data integrity

TLS replaced the older **SSL (Secure Sockets Layer)** protocol because SSL contains known security weaknesses.

Today, people often say "SSL certificate," but modern websites actually use **TLS**.

---

# What is a Digital Certificate?

A **digital certificate** verifies the identity of a website.

It contains:

- Domain name
- Public key
- Certificate issuer
- Validity period
- Digital signature

Certificates are issued by trusted organizations known as **Certificate Authorities (CAs)**.

Examples include:

- DigiCert
- GlobalSign
- Let's Encrypt
- Sectigo

---

# Public Key Cryptography

HTTPS uses **asymmetric encryption** during the TLS handshake.

Each server has:

- A **Public Key** (shared with everyone)
- A **Private Key** (kept secret)

### Public Key

Used to encrypt information.

### Private Key

Used to decrypt information.

Only the server possessing the private key can decrypt data encrypted with its corresponding public key.

---

# Symmetric Encryption

After the TLS handshake, the client and server generate a shared **session key**.

This key is used for **symmetric encryption**, which is much faster than asymmetric encryption.

The session key protects all data exchanged during the session.

---

# TLS Handshake

The TLS Handshake establishes a secure connection before any sensitive information is exchanged.

### Step 1 – Client Hello

The browser sends:

- Supported TLS versions
- Supported cipher suites
- Random value

---

### Step 2 – Server Hello

The server responds with:

- Selected TLS version
- Cipher suite
- Server random value
- Digital certificate

---

### Step 3 – Certificate Verification

The browser verifies:

- Certificate validity
- Certificate Authority (CA)
- Domain name
- Expiration date

If the certificate is trusted, the process continues.

---

### Step 4 – Session Key Generation

Both client and server securely generate the same session key.

---

### Step 5 – Secure Communication

All future HTTP traffic is encrypted using the session key.

---

# TLS Handshake Diagram

```
Browser                     Server

Client Hello  ------------->

               <-------------  Server Hello
               <-------------  Certificate

Verify Certificate

Session Key Exchange

Encrypted Communication Begins
```

---

# HTTPS Security Features

## 1. Encryption

Protects sensitive information from being read by unauthorized users.

Example:

- Passwords
- Credit card numbers
- Personal information

---

## 2. Authentication

Verifies that users are communicating with the legitimate website.

This helps prevent impersonation attacks.

---

## 3. Data Integrity

Ensures that data cannot be modified during transmission.

If someone attempts to alter the data, the communication will fail integrity checks.

---

# HTTP vs HTTPS

| Feature | HTTP | HTTPS |
|----------|-------|--------|
| Full Form | Hypertext Transfer Protocol | Hypertext Transfer Protocol Secure |
| Default Port | 80 | 443 |
| Encryption | No | Yes |
| TLS/SSL | No | Yes |
| Authentication | No | Yes |
| Data Integrity | No | Yes |
| Browser Warning | Yes | No |

---

# HTTPS Advantages

- Secure communication
- Protects user privacy
- Prevents eavesdropping
- Improves trust
- Required for online payments
- Better search engine rankings
- Supports secure authentication

---

# Limitations

HTTPS protects data **in transit**, but it does **not** protect against:

- Malware on the user's device
- Phishing websites with valid certificates
- Weak passwords
- Server vulnerabilities
- Application-level attacks

Organizations should combine HTTPS with other security controls.

---

# Cybersecurity Relevance

HTTPS plays an essential role in cybersecurity.

Security professionals use HTTPS to:

- Secure web applications
- Protect login credentials
- Secure APIs
- Prevent packet sniffing
- Prevent Man-in-the-Middle (MITM) attacks
- Meet compliance requirements

Many security standards, including PCI DSS, require encryption of sensitive data during transmission.

---

# Real-World Example

Suppose you log in to your online banking website.

```
https://bank.example
```

The process is:

1. Browser connects to the server.
2. TLS Handshake begins.
3. The bank's certificate is verified.
4. A secure session key is created.
5. Username and password are encrypted.
6. Secure communication continues until the session ends.

Without HTTPS, anyone intercepting the network traffic could potentially read sensitive information.

---

# Key Takeaways

- HTTPS is the secure version of HTTP.
- HTTPS uses **Port 443**.
- TLS provides encryption, authentication, and data integrity.
- Digital certificates verify website identity.
- TLS uses asymmetric encryption to establish a secure session.
- Symmetric encryption protects ongoing communication.
- HTTPS helps defend against eavesdropping and Man-in-the-Middle attacks.

---

# Interview Questions

1. What is HTTPS?
2. What is the difference between HTTP and HTTPS?
3. Which port does HTTPS use?
4. What is TLS?
5. What is a digital certificate?
6. What is the role of a Certificate Authority (CA)?
7. What is the TLS Handshake?
8. What is the difference between symmetric and asymmetric encryption?
9. Does HTTPS protect against phishing attacks?
10. Why is HTTPS important in cybersecurity?

---

# Next Topic

➡️ **10-VPN.md** – Learn how Virtual Private Networks (VPNs) create secure encrypted tunnels, the different VPN protocols, and their importance for remote access and secure communication.
