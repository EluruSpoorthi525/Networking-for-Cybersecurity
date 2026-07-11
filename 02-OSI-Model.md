# OSI Model (Open Systems Interconnection Model)

## Introduction

The **OSI (Open Systems Interconnection) Model** is a conceptual framework developed by the **International Organization for Standardization (ISO)** to standardize network communication. It divides the communication process into **seven distinct layers**, each with a specific responsibility.

The OSI model helps network engineers, cybersecurity professionals, and system administrators understand how data moves from one device to another, making it easier to design, troubleshoot, and secure networks.

Although modern networks primarily use the **TCP/IP model**, the OSI model remains widely used for learning, troubleshooting, and understanding networking concepts.

---

# Why is the OSI Model Important?

The OSI model provides a structured way to understand how networks operate. Each layer performs a specific function and communicates only with the layers directly above and below it.

Benefits include:

- Standardizes network communication
- Simplifies troubleshooting
- Improves interoperability between vendors
- Helps identify where network issues occur
- Provides a foundation for understanding cybersecurity attacks and defenses

---

# The Seven Layers of the OSI Model

| Layer | Name | Main Function |
|--------|------|---------------|
| 7 | Application | Provides network services to end users |
| 6 | Presentation | Formats, encrypts, and compresses data |
| 5 | Session | Establishes, manages, and terminates sessions |
| 4 | Transport | Ensures reliable data delivery |
| 3 | Network | Determines the best path for data using IP addresses |
| 2 | Data Link | Transfers data between devices on the same network |
| 1 | Physical | Transmits raw bits over physical media |

---

# Layer 7 – Application Layer

## Purpose

The Application Layer is the closest layer to the user. It provides services that allow applications such as web browsers, email clients, and file-sharing software to communicate over a network.

It does **not** refer to the application itself, but rather the network services that applications use.

### Responsibilities

- Web browsing
- Email communication
- File transfers
- Remote access
- Name resolution

### Common Protocols

- HTTP
- HTTPS
- FTP
- SMTP
- POP3
- IMAP
- DNS
- SSH

### Cybersecurity Relevance

Many cyberattacks target this layer, including:

- Phishing
- SQL Injection
- Cross-Site Scripting (XSS)
- Malware downloads

---

# Layer 6 – Presentation Layer

## Purpose

The Presentation Layer ensures that data is presented in a format that both sender and receiver can understand.

It also handles encryption, compression, and data conversion.

### Responsibilities

- Data encryption
- Data decryption
- Data compression
- Character encoding
- Data formatting

### Examples

- SSL/TLS encryption
- JPEG
- PNG
- GIF
- ASCII
- Unicode

### Cybersecurity Relevance

This layer protects sensitive information through encryption, ensuring confidentiality during transmission.

---

# Layer 5 – Session Layer

## Purpose

The Session Layer establishes, manages, and terminates communication sessions between devices.

### Responsibilities

- Session establishment
- Session maintenance
- Session termination
- Synchronization

### Example

When participating in a video conference, the Session Layer keeps the communication active until the meeting ends.

### Cybersecurity Relevance

Session hijacking attacks target this layer by stealing session identifiers to impersonate legitimate users.

---

# Layer 4 – Transport Layer

## Purpose

The Transport Layer ensures complete and reliable data delivery between sender and receiver.

### Responsibilities

- Segmentation
- Error detection
- Flow control
- Reliability
- Port addressing

### Protocols

#### TCP (Transmission Control Protocol)

Features:

- Reliable
- Connection-oriented
- Error recovery
- Packet retransmission
- Ordered delivery

Examples:

- HTTPS
- SSH
- Email

#### UDP (User Datagram Protocol)

Features:

- Faster
- Connectionless
- No retransmission
- Lower overhead

Examples:

- Online gaming
- Video streaming
- Voice calls
- DNS queries

### Cybersecurity Relevance

Firewalls often filter traffic based on TCP and UDP ports. Many network attacks, such as SYN floods, target this layer.

---

# Layer 3 – Network Layer

## Purpose

The Network Layer determines the best route for data to travel between networks.

### Responsibilities

- Logical addressing
- Routing
- Packet forwarding
- Path selection

### Protocols

- IP
- ICMP
- IPSec

### Devices

- Routers
- Layer 3 Switches

### Cybersecurity Relevance

IP spoofing and routing attacks occur at this layer. Access control lists (ACLs) are commonly used to filter traffic.

---

# Layer 2 – Data Link Layer

## Purpose

The Data Link Layer transfers data between devices connected to the same network.

### Responsibilities

- MAC addressing
- Error detection
- Frame synchronization
- Switching

### Devices

- Switches
- Bridges

### Protocols

- Ethernet
- PPP
- ARP

### Cybersecurity Relevance

Common attacks include:

- MAC spoofing
- ARP spoofing
- VLAN hopping

---

# Layer 1 – Physical Layer

## Purpose

The Physical Layer transmits raw binary data over physical media.

### Responsibilities

- Electrical signals
- Fiber optic transmission
- Wireless radio signals
- Cabling

### Devices

- Hubs
- Repeaters
- Cables
- Connectors

### Cybersecurity Relevance

Physical security is essential. Attackers may disconnect cables, install rogue devices, or physically damage infrastructure.

---

# Data Encapsulation

As data moves down the OSI model, each layer adds its own header.

```
Application Data
        ↓
Presentation Data
        ↓
Session Data
        ↓
Segment (Transport)
        ↓
Packet (Network)
        ↓
Frame (Data Link)
        ↓
Bits (Physical)
```

At the receiving device, the process is reversed. Each layer removes its corresponding header until the original data reaches the application.

---

# OSI Model Example

Suppose you open your browser and visit:

```
https://www.example.com
```

1. **Application Layer** creates the HTTP request.
2. **Presentation Layer** encrypts the request using TLS.
3. **Session Layer** establishes the communication session.
4. **Transport Layer** breaks the data into TCP segments.
5. **Network Layer** adds IP addresses and routes the packets.
6. **Data Link Layer** adds MAC addresses and creates frames.
7. **Physical Layer** transmits the bits over Ethernet or Wi-Fi.

The server processes the request and sends the response back through the same layers in reverse order.

---

# OSI Model Mnemonics

### Top to Bottom

```
All People Seem To Need Data Processing
```

- Application
- Presentation
- Session
- Transport
- Network
- Data Link
- Physical

### Bottom to Top

```
Please Do Not Throw Sausage Pizza Away
```

- Physical
- Data Link
- Network
- Transport
- Session
- Presentation
- Application

---

# Security Controls by Layer

| Layer | Example Security Control |
|--------|--------------------------|
| Application | Web Application Firewall (WAF) |
| Presentation | TLS/SSL Encryption |
| Session | Session Tokens |
| Transport | TCP Filtering, Port Security |
| Network | Firewalls, ACLs, VPNs |
| Data Link | MAC Filtering, VLAN Security |
| Physical | CCTV, Locks, Access Control |

---

# Key Takeaways

- The OSI Model has **7 layers**, each with a specific responsibility.
- It provides a standard framework for understanding network communication.
- Each layer performs unique functions and communicates with adjacent layers.
- Understanding the OSI model helps with troubleshooting, network design, and cybersecurity.
- Many cyberattacks and security controls are associated with specific OSI layers.

---

# Interview Questions

1. What is the OSI Model?
2. How many layers are in the OSI Model?
3. Which layer is responsible for routing?
4. Which layer uses MAC addresses?
5. What is the role of the Transport Layer?
6. What is the difference between TCP and UDP?
7. Which layer handles encryption?
8. Which devices operate at Layer 2 and Layer 3?
9. What is data encapsulation?
10. Why is the OSI Model important in cybersecurity?

---

# Next Topic

➡️ **03-TCP-IP-Model.md** – Learn how the TCP/IP model works, its four layers, and how it differs from the OSI model.
