# Network Security Basics

## Introduction

**Network Security** is the practice of protecting computer networks, systems, and data from unauthorized access, misuse, cyberattacks, and disruptions. It involves implementing policies, technologies, and security controls to ensure that network resources remain secure and available.

Organizations use network security to protect sensitive information, maintain business operations, and comply with legal and regulatory requirements.

Network security is based on the principle of **Defense in Depth**, where multiple layers of security controls work together to reduce risks.

---

# Why is Network Security Important?

Network security helps organizations:

- Protect confidential information
- Prevent unauthorized access
- Detect cyber threats
- Ensure business continuity
- Maintain customer trust
- Meet regulatory compliance requirements
- Reduce financial and reputational risks

Without proper network security, organizations are vulnerable to data breaches, malware, ransomware, and other cyber threats.

---

# The CIA Triad

The **CIA Triad** is the foundation of information security.

## 1. Confidentiality

Confidentiality ensures that sensitive information is accessible only to authorized users.

### Examples

- Encryption
- Access controls
- VPNs
- Data classification

---

## 2. Integrity

Integrity ensures that data remains accurate, complete, and unaltered.

### Examples

- Hashing
- Digital signatures
- Checksums
- Version control

---

## 3. Availability

Availability ensures that systems and data are accessible when needed.

### Examples

- Backups
- Redundant systems
- Load balancing
- Disaster recovery planning

---

# AAA Security Model

The **AAA Model** is used to control and monitor access to systems.

## Authentication

Verifies the identity of a user or device.

Examples:

- Passwords
- Biometrics
- Smart cards
- Multi-Factor Authentication (MFA)

---

## Authorization

Determines what an authenticated user is allowed to access.

Examples:

- Role-Based Access Control (RBAC)
- Access Control Lists (ACLs)
- Permissions

---

## Accounting

Tracks and records user activities for auditing and monitoring.

Examples:

- Login logs
- Audit trails
- Security event logs

---

# Authentication Methods

Organizations use various authentication methods to verify identities.

- Username and Password
- Multi-Factor Authentication (MFA)
- Biometrics
- Smart Cards
- One-Time Passwords (OTP)
- Security Keys (FIDO2/U2F)

MFA significantly improves security by requiring multiple forms of verification.

---

# Access Control Models

## Role-Based Access Control (RBAC)

Users receive permissions based on their job role.

Example:

- HR Staff → Employee Records
- IT Administrator → Server Management

---

## Principle of Least Privilege (PoLP)

Users should receive only the minimum permissions necessary to perform their job.

This reduces the impact of compromised accounts.

---

## Zero Trust

The Zero Trust model follows the principle:

> **"Never Trust, Always Verify."**

Every access request is verified regardless of whether it originates inside or outside the organization's network.

---

# Encryption

Encryption converts readable data (plaintext) into unreadable data (ciphertext).

### Types of Encryption

#### Symmetric Encryption

Uses the same key for encryption and decryption.

Examples:

- AES
- ChaCha20

---

#### Asymmetric Encryption

Uses a public key and a private key.

Examples:

- RSA
- ECC

---

# Hashing

Hashing converts data into a fixed-length value.

Characteristics:

- One-way process
- Used for integrity verification
- Cannot be reversed

Common algorithms:

- SHA-256
- SHA-3

---

# Digital Signatures

Digital signatures provide:

- Authentication
- Integrity
- Non-repudiation

They help verify that data has not been altered and confirm the sender's identity.

---

# Network Segmentation

Network segmentation divides a network into smaller sections to improve security.

Benefits:

- Limits attacker movement
- Reduces attack surface
- Improves performance
- Simplifies management

Technologies include:

- VLANs
- Firewalls
- Access Control Lists (ACLs)

---

# Common Network Security Controls

Organizations use multiple security controls, including:

- Firewalls
- Intrusion Detection Systems (IDS)
- Intrusion Prevention Systems (IPS)
- Antivirus/Endpoint Protection
- VPNs
- Network Access Control (NAC)
- Security Information and Event Management (SIEM)

---

# Security Policies

Security policies define how users and systems should behave.

Common policies include:

- Password Policy
- Acceptable Use Policy (AUP)
- Remote Access Policy
- Data Classification Policy
- Incident Response Policy
- Backup Policy

Policies help ensure consistent and secure operations.

---

# Defense in Depth

Defense in Depth is a layered security strategy.

Example layers:

```
Users
   │
Applications
   │
Endpoints
   │
Network Security
   │
Firewalls
   │
IDS / IPS
   │
Data Encryption
```

If one control fails, additional layers continue to provide protection.

---

# Cybersecurity Relevance

Network security is essential for:

- Protecting sensitive business information
- Preventing cyberattacks
- Meeting compliance requirements
- Supporting secure remote work
- Detecting suspicious activities
- Responding to security incidents

Security professionals apply these principles when designing, implementing, and maintaining secure networks.

---

# GRC Perspective

Network security supports Governance, Risk, and Compliance by:

### Governance

- Enforcing security policies
- Defining roles and responsibilities

### Risk Management

- Identifying and mitigating network risks
- Reducing the likelihood of security incidents

### Compliance

Network security controls help organizations meet standards such as:

- ISO/IEC 27001
- NIST Cybersecurity Framework
- PCI DSS
- HIPAA
- GDPR

Regular audits verify that these controls are effective.

---

# Best Practices

- Enable Multi-Factor Authentication (MFA).
- Use strong, unique passwords.
- Apply the Principle of Least Privilege.
- Encrypt sensitive data in transit and at rest.
- Keep systems and software updated.
- Monitor network activity.
- Segment networks using VLANs.
- Train users on cybersecurity awareness.
- Regularly review access permissions.

---

# Key Takeaways

- Network security protects systems, data, and users.
- The CIA Triad forms the foundation of information security.
- AAA consists of Authentication, Authorization, and Accounting.
- Encryption, hashing, and digital signatures help secure data.
- Defense in Depth uses multiple layers of security.
- Zero Trust and Least Privilege are essential modern security principles.
- Strong network security supports business continuity and regulatory compliance.

---

# Interview Questions

1. What is network security?
2. Explain the CIA Triad.
3. What is the difference between authentication and authorization?
4. What is the AAA model?
5. What is the Principle of Least Privilege?
6. What is Zero Trust?
7. What is the difference between encryption and hashing?
8. What are digital signatures used for?
9. Why is network segmentation important?
10. How does network security support compliance?

---

# Next Topic

➡️ **14-Common-Network-Attacks.md** – Learn about common cyberattacks targeting networks, including DoS, DDoS, Man-in-the-Middle (MITM), ARP spoofing, DNS spoofing, phishing, packet sniffing, and ransomware.
