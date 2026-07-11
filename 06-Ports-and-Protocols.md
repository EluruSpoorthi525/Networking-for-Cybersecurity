# Ports and Protocols

## Introduction

In computer networking, **ports** and **protocols** work together to enable communication between devices and applications.

- A **protocol** defines the rules for how data is transmitted and received.
- A **port** is a logical communication endpoint that identifies a specific application or service running on a device.

For example, when you visit a website, your browser uses the **HTTP** or **HTTPS** protocol and connects to the appropriate port on the web server.

Understanding ports and protocols is essential for networking, cybersecurity, firewall configuration, vulnerability assessment, and incident response.

---

# What is a Protocol?

A **protocol** is a set of standardized rules that govern how devices exchange information over a network.

Protocols ensure that devices from different manufacturers can communicate successfully.

Examples of networking protocols include:

- HTTP
- HTTPS
- FTP
- SSH
- DNS
- DHCP
- SMTP
- TCP
- UDP
- ICMP

---

# What is a Port?

A **port** is a virtual communication endpoint used by applications and services to send and receive data.

While an IP address identifies a device, a port identifies the specific application or service running on that device.

For example:

```
192.168.1.10:443
```

- **192.168.1.10** → IP Address
- **443** → Port Number (HTTPS)

---

# Port Number Range

Ports range from **0 to 65535** and are divided into three categories.

| Port Range | Name | Description |
|------------|------|-------------|
| 0–1023 | Well-Known Ports | Reserved for common services |
| 1024–49151 | Registered Ports | Used by applications |
| 49152–65535 | Dynamic/Ephemeral Ports | Temporary ports assigned to clients |

---

# Common Ports and Protocols

| Port | Protocol | Transport | Purpose |
|------|----------|-----------|---------|
| 20 | FTP (Data) | TCP | File Transfer Data |
| 21 | FTP (Control) | TCP | File Transfer Commands |
| 22 | SSH | TCP | Secure Remote Login |
| 23 | Telnet | TCP | Remote Login (Unencrypted) |
| 25 | SMTP | TCP | Sending Email |
| 53 | DNS | TCP/UDP | Domain Name Resolution |
| 67 | DHCP Server | UDP | Assign IP Addresses |
| 68 | DHCP Client | UDP | Receive IP Address |
| 69 | TFTP | UDP | Simple File Transfer |
| 80 | HTTP | TCP | Web Browsing |
| 110 | POP3 | TCP | Retrieve Email |
| 123 | NTP | UDP | Network Time Synchronization |
| 143 | IMAP | TCP | Email Retrieval |
| 161 | SNMP | UDP | Network Management |
| 389 | LDAP | TCP/UDP | Directory Services |
| 443 | HTTPS | TCP | Secure Web Browsing |
| 445 | SMB | TCP | File Sharing |
| 465 | SMTPS | TCP | Secure Email |
| 514 | Syslog | UDP | Log Collection |
| 587 | SMTP Submission | TCP | Secure Email Sending |
| 636 | LDAPS | TCP | Secure Directory Services |
| 993 | IMAPS | TCP | Secure IMAP |
| 995 | POP3S | TCP | Secure POP3 |
| 1433 | Microsoft SQL Server | TCP | Database Communication |
| 1521 | Oracle Database | TCP | Database Communication |
| 3306 | MySQL | TCP | Database Communication |
| 3389 | RDP | TCP | Remote Desktop |
| 5432 | PostgreSQL | TCP | Database Communication |
| 5900 | VNC | TCP | Remote Desktop |
| 8080 | HTTP Alternate | TCP | Web Applications |

---

# TCP and UDP Ports

Some protocols use **TCP**, while others use **UDP** depending on their communication requirements.

### TCP

Used when reliability is important.

Examples:

- HTTP
- HTTPS
- SSH
- FTP
- SMTP
- IMAP
- POP3

### UDP

Used when speed is more important than guaranteed delivery.

Examples:

- DNS
- DHCP
- NTP
- TFTP
- SNMP

---

# How Ports Work

Suppose you visit:

```
https://www.example.com
```

The process is:

1. Your browser finds the server's IP address using DNS.
2. It opens a TCP connection to **port 443**.
3. The server accepts the connection.
4. Data is exchanged securely using HTTPS.

---

# Open Ports

An **open port** means a service is actively listening for incoming connections.

Example:

```
Port 22 → SSH Server Running
```

Open ports allow legitimate communication but may also become entry points for attackers if not secured.

---

# Closed Ports

A **closed port** means no application is listening on that port.

The device responds that the port is unavailable.

---

# Filtered Ports

A **filtered port** is protected by a firewall or security device.

Attackers cannot determine whether the service exists because the firewall blocks the connection attempt.

---

# Port Scanning

Port scanning is the process of checking which ports are open on a system.

Security professionals use port scanning to:

- Discover running services
- Identify vulnerabilities
- Verify firewall configurations

Attackers also use port scanning during reconnaissance.

Common tools include:

- Nmap
- Masscan
- Angry IP Scanner

---

# Why Do Attackers Target Open Ports?

Open ports may expose services that contain:

- Weak passwords
- Outdated software
- Misconfigurations
- Known vulnerabilities

For example:

- Open RDP (3389) may be targeted for brute-force attacks.
- Open SMB (445) has been exploited by ransomware such as WannaCry.
- Open SSH (22) may be targeted by password guessing attacks.

---

# Securing Network Ports

Best practices include:

- Close unused ports.
- Use firewalls to restrict access.
- Disable unnecessary services.
- Keep software updated.
- Use strong authentication.
- Monitor network traffic.
- Regularly scan systems for exposed ports.

---

# Checking Open Ports

### Windows

```cmd
netstat -ano
```

### Linux

```bash
ss -tuln
```

or

```bash
netstat -tuln
```

---

# Cybersecurity Relevance

Ports and protocols are fundamental to cybersecurity because they help professionals:

- Configure firewalls
- Detect unauthorized services
- Perform vulnerability assessments
- Investigate network incidents
- Monitor suspicious traffic
- Conduct penetration testing

Knowledge of common ports is also essential for certifications such as Security+, Network+, CEH, CISSP, and GRC-related roles.

---

# Key Takeaways

- Protocols define the rules for communication.
- Ports identify specific applications and services.
- Port numbers range from 0 to 65535.
- Well-known ports (0–1023) are assigned to common services.
- Open ports should be monitored and secured.
- Port scanning helps identify active services and potential vulnerabilities.
- Firewalls help control access to network ports.

---

# Interview Questions

1. What is a network protocol?
2. What is a port?
3. What is the difference between TCP and UDP?
4. What are well-known ports?
5. Which port does HTTPS use?
6. Which protocol uses port 53?
7. What is port scanning?
8. What is the difference between an open and a filtered port?
9. Why are open ports a security risk?
10. How can organizations secure network ports?

---

# Next Topic

➡️ **07-DNS.md** – Learn how the Domain Name System (DNS) translates domain names into IP addresses, how DNS queries work, common DNS record types, and DNS-related security threats.
