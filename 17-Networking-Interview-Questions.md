# Networking Interview Questions

## Introduction

This chapter contains commonly asked networking interview questions and concise answers. It is designed to help students, job seekers, and cybersecurity professionals revise networking concepts and prepare for technical interviews.

The questions cover the topics discussed throughout this repository, including networking fundamentals, OSI and TCP/IP models, IP addressing, DNS, HTTP/HTTPS, VPNs, firewalls, network devices, security basics, common attacks, troubleshooting, and Wireshark.

---

# Networking Fundamentals

### 1. What is a computer network?

A computer network is a group of interconnected devices that communicate and share data and resources using communication protocols.

---

### 2. What is the Internet?

The Internet is a global network of interconnected networks that enables communication and information sharing worldwide.

---

### 3. What is a protocol?

A protocol is a set of rules that defines how data is transmitted and received between devices.

Examples include TCP, IP, HTTP, HTTPS, and DNS.

---

### 4. What is the difference between LAN, MAN, and WAN?

- **LAN:** Covers a small area such as an office or home.
- **MAN:** Covers a city or metropolitan area.
- **WAN:** Covers large geographical areas, including countries and continents.

---

# OSI Model

### 5. What are the seven layers of the OSI Model?

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

---

### 6. Which OSI layer is responsible for routing?

The **Network Layer (Layer 3)**.

---

### 7. Which OSI layer uses MAC addresses?

The **Data Link Layer (Layer 2)**.

---

### 8. Which OSI layer handles encryption?

The **Presentation Layer (Layer 6)**.

---

# TCP/IP Model

### 9. How many layers are in the TCP/IP model?

The TCP/IP model has **four layers**:

- Network Access
- Internet
- Transport
- Application

---

### 10. What is the difference between TCP and UDP?

| TCP | UDP |
|------|------|
| Connection-oriented | Connectionless |
| Reliable | Faster but less reliable |
| Error checking | Minimal error recovery |
| Used for web, email | Used for streaming, gaming, VoIP |

---

# IP Addressing

### 11. What is an IP address?

An IP address is a unique numerical identifier assigned to a device on a network.

---

### 12. What is the difference between IPv4 and IPv6?

- IPv4 uses **32-bit addresses**.
- IPv6 uses **128-bit addresses**.

IPv6 provides a much larger address space.

---

### 13. What is a subnet mask?

A subnet mask separates the network portion of an IP address from the host portion.

---

# MAC Address

### 14. What is a MAC address?

A MAC address is a unique hardware address assigned to a network interface.

---

### 15. Which OSI layer uses MAC addresses?

The **Data Link Layer (Layer 2)**.

---

# DNS

### 16. What is DNS?

DNS (Domain Name System) translates domain names into IP addresses.

---

### 17. Why is DNS important?

Without DNS, users would need to remember IP addresses instead of domain names.

---

# HTTP & HTTPS

### 18. What is HTTP?

HTTP is a protocol used for transferring web pages between clients and servers.

Default port: **80**

---

### 19. What is HTTPS?

HTTPS is the secure version of HTTP that uses TLS encryption.

Default port: **443**

---

### 20. What is TLS?

TLS (Transport Layer Security) encrypts communication between clients and servers.

---

# VPN

### 21. What is a VPN?

A VPN creates an encrypted tunnel between a user and a remote network over the Internet.

---

### 22. Why do organizations use VPNs?

To provide secure remote access and protect data transmitted over public networks.

---

# Firewalls

### 23. What is a firewall?

A firewall monitors and filters network traffic according to predefined security rules.

---

### 24. What are the main types of firewalls?

- Packet Filtering
- Stateful Inspection
- Proxy Firewall
- Next-Generation Firewall (NGFW)

---

# Network Devices

### 25. What is the difference between a hub and a switch?

A hub broadcasts data to all connected devices, while a switch forwards data only to the intended destination using MAC addresses.

---

### 26. What is the role of a router?

A router connects different networks and forwards packets based on IP addresses.

---

### 27. What is an Access Point?

An Access Point (AP) provides wireless connectivity to devices on a network.

---

# Network Security Basics

### 28. What is the CIA Triad?

- Confidentiality
- Integrity
- Availability

These are the three core principles of information security.

---

### 29. What is the AAA model?

- Authentication
- Authorization
- Accounting

---

### 30. What is the Principle of Least Privilege?

Users should have only the minimum permissions required to perform their tasks.

---

### 31. What is Zero Trust?

A security model based on the principle: **"Never Trust, Always Verify."**

---

# Common Network Attacks

### 32. What is a DoS attack?

A Denial-of-Service attack attempts to make a service unavailable by overwhelming it with traffic.

---

### 33. What is a DDoS attack?

A Distributed Denial-of-Service attack uses multiple compromised devices to flood a target with traffic.

---

### 34. What is a Man-in-the-Middle (MITM) attack?

An attacker secretly intercepts communication between two parties.

---

### 35. What is phishing?

A social engineering attack that tricks users into revealing sensitive information.

---

### 36. What is ransomware?

Malware that encrypts a victim's files and demands payment for decryption.

---

# Network Troubleshooting

### 37. What does the `ping` command do?

It tests connectivity between devices using ICMP Echo Request and Echo Reply messages.

---

### 38. What is the purpose of `traceroute`?

It displays the path packets take to reach a destination.

---

### 39. What does `nslookup` do?

It queries DNS servers to resolve domain names and troubleshoot DNS issues.

---

### 40. What information does `netstat` provide?

It displays active network connections, listening ports, and network statistics.

---

# Wireshark

### 41. What is Wireshark?

Wireshark is a network protocol analyzer used to capture and inspect network traffic.

---

### 42. What is packet capture?

Packet capture is the process of recording network packets for analysis.

---

### 43. What are display filters?

Display filters allow users to show only packets that match specific criteria.

Example:

```
dns
```

```
tcp.port == 443
```

---

### 44. What is the purpose of "Follow TCP Stream"?

It reconstructs an entire TCP conversation between a client and server.

---

# Scenario-Based Questions

### 45. A user can access websites using IP addresses but not domain names. What is the likely issue?

**Answer:** A DNS resolution problem.

---

### 46. A website is slow to load. Which troubleshooting tools would you use?

- ping
- traceroute
- Wireshark
- netstat

---

### 47. An employee cannot connect to the corporate VPN. What would you check first?

- Internet connectivity
- VPN credentials
- VPN server status
- Firewall rules
- MFA status

---

### 48. Which command clears the DNS cache on Windows?

```cmd
ipconfig /flushdns
```

---

### 49. Which command displays the ARP table?

```cmd
arp -a
```

---

### 50. Why is HTTPS preferred over HTTP?

HTTPS encrypts data, authenticates the server, and protects data integrity, making communication more secure.

---

# Quick Revision Table

| Topic | Key Point |
|--------|-----------|
| OSI Model | 7 layers |
| TCP/IP | 4 layers |
| HTTP | Port 80 |
| HTTPS | Port 443 |
| DNS | Resolves domain names |
| VPN | Secure encrypted tunnel |
| Firewall | Filters network traffic |
| Router | Routes packets using IP addresses |
| Switch | Forwards frames using MAC addresses |
| Wireshark | Captures and analyzes packets |
| CIA Triad | Confidentiality, Integrity, Availability |
| AAA | Authentication, Authorization, Accounting |
| Zero Trust | Never Trust, Always Verify |

---

# Tips for Networking Interviews

- Understand concepts rather than memorizing definitions.
- Practice common networking commands (`ping`, `traceroute`, `nslookup`, `netstat`).
- Be familiar with the OSI and TCP/IP models.
- Learn the default ports for common protocols.
- Explain concepts using real-world examples.
- Review common network attacks and their defenses.
- Gain hands-on experience with Wireshark.

---

