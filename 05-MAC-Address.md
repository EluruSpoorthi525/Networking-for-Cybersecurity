# MAC Address (Media Access Control Address)

## Introduction

A **MAC (Media Access Control) Address** is a unique hardware identifier assigned to a device's **Network Interface Card (NIC)** by the manufacturer. It operates at **Layer 2 (Data Link Layer)** of the OSI Model and is used to identify devices within a **Local Area Network (LAN)**.

Unlike an IP address, which can change depending on the network, a MAC address is generally fixed and remains associated with the network interface.

Think of it this way:

- **IP Address** → Like your home address (changes based on location)
- **MAC Address** → Like your fingerprint (unique to your device)

---

# Why is a MAC Address Important?

MAC addresses help network devices identify each other within the same local network.

They are used for:

- Delivering frames to the correct device
- Device identification
- Network access control
- Troubleshooting
- Security monitoring

---

# MAC Address Format

A MAC address is a **48-bit (6-byte)** hexadecimal number.

### Example

```
00:1A:2B:3C:4D:5E
```

It may also appear as:

```
00-1A-2B-3C-4D-5E
```

or

```
001A.2B3C.4D5E
```

Each pair represents one byte written in hexadecimal.

---

# Structure of a MAC Address

A MAC address has two parts:

| Part | Description |
|------|-------------|
| OUI (Organizationally Unique Identifier) | First 24 bits identify the manufacturer |
| Device Identifier | Last 24 bits uniquely identify the network interface |

Example:

```
00:1A:2B : 3C:4D:5E
^^^^^^^^   ^^^^^^^^^
Manufacturer   Device ID
```

---

# OUI (Organizationally Unique Identifier)

The first half of a MAC address identifies the hardware manufacturer.

Examples:

| Manufacturer | Example OUI |
|--------------|-------------|
| Cisco | 00:40:96 |
| Dell | F0:1F:AF |
| Intel | 3C:52:82 |
| Apple | A4:5E:60 |

The IEEE assigns OUIs to manufacturers.

---

# How MAC Addresses Work

Suppose two computers are connected to the same switch.

```
Computer A
MAC: AA:AA:AA:AA:AA:AA

↓

Switch

↓

Computer B
MAC: BB:BB:BB:BB:BB:BB
```

When Computer A sends data, the switch forwards the frame based on the destination MAC address.

---

# MAC Address vs IP Address

| Feature | MAC Address | IP Address |
|----------|-------------|------------|
| Layer | Data Link (Layer 2) | Network (Layer 3) |
| Purpose | Identify hardware | Identify devices on a network |
| Assigned By | Manufacturer | ISP or DHCP |
| Changes | Usually No | Yes (can change) |
| Format | Hexadecimal | Decimal (IPv4) / Hexadecimal (IPv6) |

---

# Types of MAC Addresses

## Unicast

Communication from one sender to one receiver.

Example:

```
Laptop → Printer
```

---

## Broadcast

Sent to every device on the local network.

Broadcast MAC:

```
FF:FF:FF:FF:FF:FF
```

Used by protocols such as ARP.

---

## Multicast

Sent to a selected group of devices instead of all devices.

Example:

Streaming video to multiple receivers.

---

# ARP (Address Resolution Protocol)

## What is ARP?

ARP is a protocol used to find the MAC address associated with a known IPv4 address on a local network.

Without ARP, devices would know the destination IP address but not the destination MAC address needed for local communication.

---

# How ARP Works

Suppose:

```
Computer A

IP: 192.168.1.10
MAC: AA:AA:AA:AA:AA:AA
```

Wants to communicate with:

```
Computer B

IP: 192.168.1.20
MAC: BB:BB:BB:BB:BB:BB
```

### Step 1

Computer A sends an ARP Request:

```
Who has 192.168.1.20?
```

---

### Step 2

Every device receives the request.

---

### Step 3

Computer B replies:

```
192.168.1.20 is BB:BB:BB:BB:BB:BB
```

---

### Step 4

Computer A stores this information in its ARP Cache and sends frames directly to Computer B.

---

# ARP Cache

The ARP Cache stores recently resolved IP-to-MAC mappings to reduce unnecessary ARP requests.

You can view it using:

### Windows

```cmd
arp -a
```

### Linux

```bash
ip neigh
```

---

# MAC Address Spoofing

## What is MAC Spoofing?

MAC spoofing is the process of changing a device's MAC address to impersonate another device.

Attackers may use MAC spoofing to:

- Bypass MAC filtering
- Hide their identity
- Gain unauthorized access
- Evade network monitoring

---

# ARP Spoofing

ARP Spoofing (or ARP Poisoning) is an attack in which an attacker sends fake ARP replies to associate their MAC address with another device's IP address.

Example:

```
Victim

↓

Attacker pretends to be Router

↓

Victim sends traffic to Attacker

↓

Attacker forwards traffic to Router
```

This allows the attacker to intercept, modify, or monitor network traffic.

---

# Preventing ARP Spoofing

Common defenses include:

- Dynamic ARP Inspection (DAI)
- Static ARP entries
- Network segmentation
- Port Security
- Intrusion Detection Systems (IDS)
- Secure switches

---

# Finding Your MAC Address

### Windows

```cmd
ipconfig /all
```

or

```cmd
getmac
```

---

### Linux

```bash
ip link
```

or

```bash
ifconfig
```

---

### macOS

```bash
ifconfig
```

---

# Cybersecurity Relevance

MAC addresses are widely used in:

- Network Access Control (NAC)
- Device identification
- Digital forensics
- Packet analysis
- Switch security
- Incident response

Security professionals often examine MAC addresses when investigating unauthorized devices or suspicious network activity.

---

# Key Takeaways

- A MAC address uniquely identifies a network interface.
- MAC addresses operate at the Data Link Layer (Layer 2).
- They are 48-bit hexadecimal values.
- ARP maps IP addresses to MAC addresses.
- Broadcast MAC addresses are `FF:FF:FF:FF:FF:FF`.
- MAC spoofing and ARP spoofing are common Layer 2 attacks.
- Understanding MAC addresses is essential for network troubleshooting and cybersecurity.

---

# Interview Questions

1. What is a MAC address?
2. How is a MAC address different from an IP address?
3. Which OSI layer uses MAC addresses?
4. What is the purpose of ARP?
5. What is the broadcast MAC address?
6. What is MAC spoofing?
7. What is ARP spoofing?
8. How can ARP spoofing be prevented?
9. How do you find the MAC address on Windows?
10. Why are MAC addresses important in cybersecurity?

---

# Next Topic

➡️ **06-Ports-and-Protocols.md** – Learn about well-known ports, common network protocols (HTTP, HTTPS, FTP, SSH, DNS, SMTP, etc.), and how they enable communication between applications and services.
