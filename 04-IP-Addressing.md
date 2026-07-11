# IP Addressing

## Introduction

An **IP (Internet Protocol) address** is a unique numerical identifier assigned to every device connected to a network that uses the Internet Protocol. It allows devices to locate and communicate with each other, much like a postal address helps deliver mail to the correct destination.

Without IP addresses, devices would not know where to send or receive data, making communication over networks impossible.

IP addresses are managed by the Internet Protocol (IP), which is responsible for delivering packets from the source device to the destination device.

---

# Why Are IP Addresses Important?

IP addresses play a critical role in networking by:

- Identifying devices on a network
- Enabling communication between devices
- Supporting routing across networks
- Facilitating Internet access
- Assisting in network management and troubleshooting

In cybersecurity, IP addresses are essential for monitoring traffic, identifying malicious activity, and implementing security controls.

---

# Versions of IP

There are two versions of Internet Protocol currently in use:

- **IPv4 (Internet Protocol Version 4)**
- **IPv6 (Internet Protocol Version 6)**

---

# IPv4

IPv4 is the most widely used version of the Internet Protocol.

It uses **32-bit addresses**, allowing approximately **4.3 billion unique addresses**.

### Format

An IPv4 address consists of four decimal numbers separated by periods.

Example:

```
192.168.1.10
```

Each number ranges from **0 to 255**.

Example:

```
172.16.25.100
```

### Characteristics

- 32-bit addressing
- Four octets
- Decimal notation
- Most commonly used today

---

# IPv6

IPv6 was introduced to overcome the shortage of IPv4 addresses.

It uses **128-bit addresses**, providing an enormous number of unique addresses.

### Format

Example:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

IPv6 addresses are written in hexadecimal and separated by colons.

### Characteristics

- 128-bit addressing
- Hexadecimal notation
- Larger address space
- Improved security support
- Better routing efficiency

---

# IPv4 vs IPv6

| Feature | IPv4 | IPv6 |
|----------|------|------|
| Address Size | 32 bits | 128 bits |
| Format | Decimal | Hexadecimal |
| Number of Addresses | ~4.3 Billion | 340 Undecillion (approx.) |
| Header Size | Variable | Fixed |
| Security | Optional IPsec | Native IPsec Support |
| Example | 192.168.1.1 | 2001:db8::1 |

---

# Public IP Address

A **Public IP Address** is assigned by an Internet Service Provider (ISP) and is accessible over the Internet.

### Characteristics

- Globally unique
- Routable on the Internet
- Assigned by ISP

### Example

```
103.45.210.15
```

---

# Private IP Address

A **Private IP Address** is used within local networks such as homes, offices, or schools. It cannot be accessed directly from the Internet.

### Private IPv4 Ranges

| Range | CIDR |
|--------|------|
| 10.0.0.0 – 10.255.255.255 | 10.0.0.0/8 |
| 172.16.0.0 – 172.31.255.255 | 172.16.0.0/12 |
| 192.168.0.0 – 192.168.255.255 | 192.168.0.0/16 |

### Example

```
192.168.1.20
```

---

# Static IP Address

A **Static IP Address** remains the same until it is manually changed.

### Advantages

- Suitable for servers
- Easy remote access
- Reliable hosting

### Disadvantages

- Manual configuration
- Less flexible
- Higher management effort

---

# Dynamic IP Address

A **Dynamic IP Address** is assigned automatically by a DHCP server and may change over time.

### Advantages

- Automatic configuration
- Efficient address management
- Ideal for home users

### Disadvantages

- Address changes periodically
- Less suitable for hosting services

---

# Loopback Address

The loopback address is used to test the local network interface.

IPv4:

```
127.0.0.1
```

IPv6:

```
::1
```

It allows a device to communicate with itself for testing and troubleshooting.

---

# APIPA (Automatic Private IP Addressing)

If a DHCP server is unavailable, Windows assigns an APIPA address.

Range:

```
169.254.0.0 – 169.254.255.255
```

An APIPA address usually indicates that the device could not obtain an IP address from the network.

---

# Network ID and Host ID

An IP address consists of two parts:

- **Network ID** – Identifies the network
- **Host ID** – Identifies the specific device on that network

Example:

```
192.168.1.25/24
```

- Network ID: `192.168.1.0`
- Host ID: `25`

---

# Subnet Mask

A **Subnet Mask** determines which portion of an IP address represents the network and which represents the host.

Example:

```
255.255.255.0
```

Equivalent CIDR notation:

```
/24
```

---

# CIDR Notation

CIDR (Classless Inter-Domain Routing) simplifies subnet representation.

Examples:

| CIDR | Subnet Mask |
|------|-------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /30 | 255.255.255.252 |

---

# Default Gateway

A **Default Gateway** is the router that forwards traffic from a local network to external networks, such as the Internet.

Example:

```
192.168.1.1
```

Without a default gateway, devices can communicate only within the same local network.

---

# How IP Communication Works

Suppose your computer has the IP address:

```
192.168.1.10
```

You visit:

```
https://www.example.com
```

The communication process is:

1. Your browser sends a request.
2. DNS translates the domain name into an IP address.
3. Your router forwards the packets.
4. Packets travel across multiple networks.
5. The destination server receives the request.
6. The server sends a response back to your device.

---

# Cybersecurity Relevance

Understanding IP addressing is essential because many attacks target or rely on IP communication.

Examples include:

- IP Spoofing
- DDoS Attacks
- Network Scanning
- Unauthorized Access
- Firewall Rule Configuration
- VPN Configuration
- Access Control Lists (ACLs)

Security professionals use IP addresses to:

- Identify attackers
- Monitor network traffic
- Investigate incidents
- Configure security devices
- Analyze logs

---

# Key Takeaways

- Every network device requires an IP address.
- IPv4 uses 32-bit addresses, while IPv6 uses 128-bit addresses.
- Public IP addresses are Internet-accessible, while private IP addresses are used within local networks.
- Static IP addresses remain constant; dynamic IP addresses are assigned automatically.
- Subnet masks and CIDR define network boundaries.
- Default gateways connect local networks to external networks.
- IP addressing is fundamental for networking and cybersecurity.

---

# Interview Questions

1. What is an IP address?
2. What is the difference between IPv4 and IPv6?
3. What is a private IP address?
4. What is a public IP address?
5. What is the purpose of a subnet mask?
6. What is CIDR notation?
7. What is a default gateway?
8. What is the loopback address?
9. What is APIPA?
10. Why are IP addresses important in cybersecurity?

---

# Next Topic

➡️ **05-MAC-Address.md** – Learn about MAC addresses, how devices are identified within a local network, ARP, MAC spoofing, and Layer 2 communication.
