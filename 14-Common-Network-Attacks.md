# Common Network Attacks

## Introduction

A **network attack** is an attempt by a malicious actor to gain unauthorized access, disrupt network operations, steal sensitive information, or compromise systems connected to a network.

Cybercriminals use various attack techniques to exploit vulnerabilities in network protocols, applications, and user behavior. Understanding these attacks helps organizations implement effective security controls and reduce cyber risks.

---

# Why Learn About Network Attacks?

Understanding common network attacks helps security professionals:

- Identify threats
- Prevent unauthorized access
- Protect sensitive data
- Improve network defenses
- Respond to security incidents
- Meet security and compliance requirements

Knowledge of network attacks is essential for cybersecurity analysts, penetration testers, SOC analysts, and GRC professionals.

---

# Types of Common Network Attacks

Some of the most common network attacks include:

- Denial-of-Service (DoS)
- Distributed Denial-of-Service (DDoS)
- Man-in-the-Middle (MITM)
- ARP Spoofing
- DNS Spoofing
- Packet Sniffing
- Phishing
- Ransomware
- Password Attacks
- Session Hijacking

---

# 1. Denial-of-Service (DoS)

A **Denial-of-Service (DoS)** attack attempts to make a system or service unavailable by overwhelming it with excessive traffic or requests.

### How It Works

```
Attacker
     │
大量 Requests
     ▼
Target Server
     │
Service Unavailable
```

### Impact

- Website downtime
- Service disruption
- Financial loss

### Prevention

- Firewalls
- Rate limiting
- Traffic filtering
- Load balancing

---

# 2. Distributed Denial-of-Service (DDoS)

A **Distributed Denial-of-Service (DDoS)** attack uses multiple compromised devices (often a botnet) to flood a target with traffic.

### How It Works

```
Bot 1 ─┐
Bot 2 ─┼──► Target Server
Bot 3 ─┘
```

### Impact

- Large-scale service outages
- High bandwidth consumption

### Prevention

- DDoS protection services
- Content Delivery Networks (CDNs)
- Traffic analysis
- Rate limiting

---

# 3. Man-in-the-Middle (MITM)

A **Man-in-the-Middle (MITM)** attack occurs when an attacker secretly intercepts and possibly alters communication between two parties.

### Example

```
User
   │
Attacker
   │
Website
```

### Impact

- Credential theft
- Data interception
- Session hijacking

### Prevention

- HTTPS
- VPNs
- Certificate validation
- Multi-Factor Authentication (MFA)

---

# 4. ARP Spoofing

ARP Spoofing occurs when an attacker sends forged ARP messages to associate their MAC address with another device's IP address.

### Impact

- Traffic interception
- Network monitoring
- MITM attacks

### Prevention

- Dynamic ARP Inspection (DAI)
- Static ARP entries
- Secure switches

---

# 5. DNS Spoofing

DNS Spoofing redirects users to fake websites by providing false DNS responses.

### Example

```
bank.com
      │
Fake DNS Response
      │
Malicious Website
```

### Prevention

- DNSSEC
- Secure DNS resolvers
- Monitor DNS traffic

---

# 6. Packet Sniffing

Packet sniffing involves capturing and analyzing network traffic.

Attackers may use packet sniffers to steal sensitive information transmitted without encryption.

### Prevention

- HTTPS
- VPN
- Encryption
- Secure Wi-Fi

---

# 7. Phishing

Phishing is a social engineering attack where attackers trick users into revealing sensitive information.

### Common Targets

- Passwords
- Credit card numbers
- Banking information
- Corporate credentials

### Prevention

- Security awareness training
- Email filtering
- MFA
- Verify suspicious emails

---

# 8. Ransomware

Ransomware encrypts a victim's files and demands payment to restore access.

### Impact

- Data loss
- Business disruption
- Financial damage

### Prevention

- Regular backups
- Endpoint protection
- Software updates
- User awareness training

---

# 9. Password Attacks

Attackers attempt to gain access by compromising passwords.

### Common Techniques

- Brute-force attack
- Dictionary attack
- Password spraying
- Credential stuffing

### Prevention

- Strong passwords
- MFA
- Account lockout policies
- Password managers

---

# 10. Session Hijacking

Session hijacking occurs when an attacker steals a valid session token to impersonate a legitimate user.

### Prevention

- HTTPS
- Secure cookies
- Short session timeouts
- MFA

---

# Comparison of Network Attacks

| Attack | Primary Goal | Common Defense |
|--------|--------------|----------------|
| DoS | Disrupt services | Rate limiting, firewalls |
| DDoS | Overwhelm systems | CDN, DDoS protection |
| MITM | Intercept communication | HTTPS, VPN |
| ARP Spoofing | Redirect LAN traffic | Dynamic ARP Inspection |
| DNS Spoofing | Redirect users | DNSSEC |
| Packet Sniffing | Capture data | Encryption |
| Phishing | Steal credentials | User awareness, MFA |
| Ransomware | Encrypt files | Backups, endpoint protection |
| Password Attacks | Guess passwords | MFA, strong passwords |
| Session Hijacking | Steal sessions | HTTPS, secure cookies |

---

# Cybersecurity Relevance

Understanding network attacks enables professionals to:

- Detect malicious activity
- Implement preventive controls
- Investigate security incidents
- Conduct risk assessments
- Improve organizational resilience

Network attacks are studied extensively in penetration testing, threat hunting, SOC operations, and incident response.

---

# GRC Perspective

From a Governance, Risk, and Compliance perspective:

### Governance

- Define security policies to reduce attack risks.
- Establish user awareness training.

### Risk Management

- Assess attack likelihood and business impact.
- Implement appropriate security controls.

### Compliance

Protecting against network attacks helps organizations comply with frameworks such as:

- ISO/IEC 27001
- NIST Cybersecurity Framework
- PCI DSS
- HIPAA
- GDPR

---

# Best Practices

- Keep systems updated.
- Enable Multi-Factor Authentication (MFA).
- Use firewalls and Intrusion Prevention Systems (IPS).
- Encrypt sensitive communications.
- Monitor network traffic.
- Perform regular vulnerability assessments.
- Train employees to recognize phishing.
- Maintain secure backups.
- Apply the Principle of Least Privilege.

---

# Key Takeaways

- Network attacks target systems, services, and users.
- Common attacks include DoS, DDoS, MITM, ARP spoofing, DNS spoofing, phishing, ransomware, and password attacks.
- Encryption, MFA, firewalls, and security awareness significantly reduce risk.
- Defense in Depth provides multiple layers of protection.
- Understanding attacks helps organizations improve security and compliance.

---

# Interview Questions

1. What is the difference between DoS and DDoS?
2. What is a Man-in-the-Middle (MITM) attack?
3. How does ARP spoofing work?
4. What is DNS spoofing?
5. What is packet sniffing?
6. How does ransomware affect an organization?
7. What is credential stuffing?
8. How can phishing attacks be prevented?
9. Why is MFA important?
10. What security controls help defend against network attacks?

---

# Next Topic

➡️ **15-Network-Troubleshooting.md** – Learn how to diagnose and resolve common network issues using tools such as **ping**, **traceroute**, **nslookup**, **ipconfig**, **netstat**, and **arp**.
