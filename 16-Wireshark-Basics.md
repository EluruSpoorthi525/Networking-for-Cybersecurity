# Wireshark Basics

## Introduction

**Wireshark** is a free and open-source **network protocol analyzer** used to capture, inspect, and analyze network traffic in real time.

It allows administrators, security analysts, and researchers to examine packets traveling across a network, making it one of the most valuable tools for network troubleshooting, incident response, malware analysis, and digital forensics.

Wireshark supports hundreds of network protocols and works on Windows, Linux, and macOS.

---

# Why Use Wireshark?

Wireshark helps professionals to:

- Analyze network traffic
- Troubleshoot connectivity issues
- Detect suspicious activity
- Investigate security incidents
- Learn how network protocols work
- Verify firewall and network configurations

It is widely used by:

- Network Engineers
- SOC Analysts
- Incident Responders
- Penetration Testers
- Digital Forensics Analysts
- Security Researchers

---

# Key Features

Wireshark provides:

- Live packet capture
- Offline packet analysis
- Support for hundreds of protocols
- Powerful display filters
- Packet searching
- Statistics and graphs
- Protocol hierarchy analysis
- Export captured packets

---

# How Wireshark Works

Wireshark captures packets from a selected network interface.

```
Computer
      │
Network Interface
      │
Wireshark
      │
Captured Packets
      │
Packet Analysis
```

Each captured packet contains valuable information such as:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol
- Packet Size
- Timestamp

---

# Installing Wireshark

### Windows

1. Download Wireshark from the official website.
2. Install Wireshark.
3. Install **Npcap** when prompted.
4. Launch Wireshark.

---

### Linux

Ubuntu/Debian

```bash
sudo apt update
sudo apt install wireshark
```

---

### macOS

```bash
brew install --cask wireshark
```

---

# Wireshark Interface

The main interface consists of:

### Menu Bar

Provides access to capture, analysis, and export functions.

---

### Toolbar

Contains frequently used actions.

---

### Packet List Pane

Displays captured packets.

---

### Packet Details Pane

Shows protocol information for the selected packet.

---

### Packet Bytes Pane

Displays the raw packet data in hexadecimal and ASCII.

---

# Capturing Packets

To capture packets:

1. Open Wireshark.
2. Select the network interface.
3. Click **Start Capture**.
4. Generate network activity.
5. Click **Stop** when finished.

---

# Common Protocols in Wireshark

| Protocol | Purpose |
|----------|---------|
| HTTP | Web traffic |
| HTTPS | Secure web traffic |
| DNS | Domain name resolution |
| TCP | Reliable communication |
| UDP | Fast communication |
| ICMP | Network diagnostics |
| ARP | IP-to-MAC resolution |
| DHCP | IP address assignment |
| FTP | File transfer |
| SSH | Secure remote login |

---

# Display Filters

Display filters help narrow down captured packets.

### HTTP

```
http
```

---

### HTTPS

```
tls
```

---

### DNS

```
dns
```

---

### TCP

```
tcp
```

---

### UDP

```
udp
```

---

### ICMP

```
icmp
```

---

### ARP

```
arp
```

---

### Filter by IP Address

```
ip.addr == 192.168.1.10
```

---

### Filter by Port

```
tcp.port == 443
```

---

### Filter by HTTP Method

```
http.request.method == "GET"
```

---

# Packet Structure

Each packet generally contains:

```
Frame
│
Ethernet Header
│
IP Header
│
TCP / UDP Header
│
Application Data
```

Understanding these layers helps identify communication issues.

---

# Following a TCP Stream

Wireshark allows you to reconstruct an entire TCP conversation.

Steps:

1. Right-click a TCP packet.
2. Select **Follow → TCP Stream**.
3. Review the communication between the client and server.

This feature is useful for troubleshooting application issues and understanding protocol behavior.

---

# Useful Statistics

Wireshark provides several analysis tools:

- Protocol Hierarchy
- Endpoints
- Conversations
- Flow Graph
- I/O Graphs
- Packet Length Statistics

These tools help summarize network activity and identify unusual patterns.

---

# Common Troubleshooting Tasks

Wireshark can help diagnose:

- Slow network performance
- DNS failures
- Packet loss
- TCP retransmissions
- SSL/TLS handshake issues
- Network congestion
- Connection resets

---

# Cybersecurity Use Cases

Security professionals use Wireshark for:

- Incident response
- Malware traffic analysis
- Detecting suspicious communications
- Investigating phishing incidents
- Identifying command-and-control (C2) traffic
- Verifying firewall rules
- Detecting network reconnaissance

---

# Best Practices

- Capture only the traffic you need.
- Use display filters to simplify analysis.
- Save packet captures for future investigation.
- Avoid capturing sensitive data without authorization.
- Regularly update Wireshark.
- Analyze traffic in a controlled environment.

---

# Ethical Considerations

Packet captures may contain:

- Passwords (if transmitted unencrypted)
- Session tokens
- Personal information
- Internal network details

Always:

- Obtain proper authorization before capturing traffic.
- Follow organizational security policies.
- Protect captured files from unauthorized access.

---

# Hands-on Exercises

## Exercise 1

Capture traffic while opening a website.

Identify:

- DNS query
- TCP handshake
- HTTP or HTTPS communication

---

## Exercise 2

Run:

```bash
ping google.com
```

Capture the ICMP packets and examine:

- Echo Request
- Echo Reply

---

## Exercise 3

Apply the following display filters:

```
dns
```

```
tcp
```

```
icmp
```

Observe how the packet list changes.

---

## Exercise 4

Capture HTTPS traffic and identify:

- TLS Handshake
- Server Hello
- Certificate exchange

---

# GRC Perspective

Wireshark supports Governance, Risk, and Compliance by:

### Governance

- Verifying that network communications follow organizational policies.

### Risk Management

- Detecting unauthorized or suspicious network activity.
- Identifying misconfigurations and insecure protocols.

### Compliance

Packet analysis assists in:

- Security audits
- Incident investigations
- Network monitoring
- Regulatory compliance verification

Captured traffic can provide valuable evidence during forensic investigations.

---

# Key Takeaways

- Wireshark is a powerful packet capture and analysis tool.
- It supports hundreds of network protocols.
- Display filters simplify packet analysis.
- Wireshark is valuable for troubleshooting, cybersecurity, and digital forensics.
- Packet captures should be handled responsibly because they may contain sensitive information.

---

# Interview Questions

1. What is Wireshark?
2. What is packet capture?
3. What is the purpose of display filters?
4. Which protocol filter is used for DNS traffic?
5. What information can be found in a packet?
6. Why is Npcap required on Windows?
7. What is the purpose of "Follow TCP Stream"?
8. How can Wireshark help during incident response?
9. Why should packet captures be protected?
10. What are some common cybersecurity use cases for Wireshark?

---

# Next Topic

➡️ **17-Networking-Interview-Questions.md** – A comprehensive collection of networking interview questions and answers covering all topics from this repository to help prepare for technical interviews and certification exams.
