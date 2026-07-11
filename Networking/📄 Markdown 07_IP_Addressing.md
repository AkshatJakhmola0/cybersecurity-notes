# IP Addressing

## Definition

An IP (Internet Protocol) Address is a unique logical address assigned to a device on a network for identification and communication.

---

## Why

IP addressing is essential because it:

- Identifies devices on a network.
- Allows devices to send and receive data.
- Helps routers find the destination device.
- Enables communication over the Internet.

---

## Working

When a device sends data:

```text
Source IP Address
        │
        ▼
      Router
        │
        ▼
Destination IP Address
```

The router uses IP addresses to determine where the data should go.

---

## Real-World Example

When you open Google:

```text
Your Device (192.168.1.10)
        │
        ▼
      Router
        │
        ▼
Google Server (Public IP)
```

The communication happens using IP addresses.

---

## Cybersecurity Perspective

IP addresses are important for:

- Identifying attackers.
- Blocking malicious traffic.
- Monitoring network activity.
- Investigating security incidents.

Common attacks involving IP addresses:

- IP Spoofing
- DDoS Attacks
- Port Scanning

---

# Common Types

## IPv4

### Definition

A 32-bit address consisting of four octets.

### Example

```text
192.168.1.10
```

### Key Points

- Most commonly used.
- Approximately 4.3 billion addresses.
- Limited address space.

---

## IPv6

### Definition

A 128-bit address designed to replace IPv4.

### Example

```text
2001:0db8:85a3::8a2e:0370:7334
```

### Key Points

- Huge address space.
- Better scalability.
- Increasingly used on modern networks.

---

## Public IP

### Definition

An IP address accessible over the Internet.

### Example

IP assigned by your Internet Service Provider (ISP).

### Cybersecurity Perspective

Visible to attackers on the Internet.

---

## Private IP

### Definition

An IP address used inside local networks.

### Private IP Ranges

```text
10.0.0.0 – 10.255.255.255

172.16.0.0 – 172.31.255.255

192.168.0.0 – 192.168.255.255
```

### Example

```text
192.168.1.10
```

### Cybersecurity Perspective

Not directly accessible from the Internet.

---

## Static IP

### Definition

An IP address that remains fixed.

### Example

Server IP address.

### Cybersecurity Perspective

Easy to manage but predictable for attackers.

---

## Dynamic IP

### Definition

An IP address assigned automatically by DHCP.

### Example

Home Wi-Fi devices.

### Cybersecurity Perspective

Changes periodically, making tracking slightly harder.

---

## Loopback Address

### Definition

Used by a device to communicate with itself.

### Examples

IPv4

```text
127.0.0.1
```

IPv6

```text
::1
```

### Common Use

Testing network services locally.

### Cybersecurity Perspective

Frequently used during troubleshooting and malware analysis.

---

## APIPA

### Definition

Automatic Private IP Addressing assigned when a DHCP server is unavailable.

### Range

```text
169.254.0.0 – 169.254.255.255
```

### Example

```text
169.254.10.20
```

### Common Use

Temporary communication within a local network.

### Cybersecurity Perspective

Often indicates DHCP failure or network configuration issues.

---

## Broadcast Address

### Definition

Used to send data to all devices within a network.

### Example

```text
192.168.1.255
```

### Common Use

Network-wide announcements.

### Cybersecurity Perspective

Can be abused in broadcast amplification attacks.

---

## Default Gateway

### Definition

The router through which devices access other networks or the Internet.

### Example

```text
192.168.1.1
```

### Working

```text
Device
   │
   ▼
Default Gateway
   │
   ▼
Internet
```

### Cybersecurity Perspective

A critical device often protected with strong authentication and monitoring.

---

## Interview Questions

### Q1. What is an IP Address?

**Answer:** A unique logical address used to identify a device on a network.

---

### Q2. Which version uses 32-bit addressing?

**Answer:** IPv4

---

### Q3. Which version uses 128-bit addressing?

**Answer:** IPv6

---

### Q4. What is the loopback address in IPv4?

**Answer:** 127.0.0.1

---

### Q5. What is APIPA?

**Answer:** Automatic Private IP Addressing assigned when DHCP is unavailable.

---

### Q6. What is the purpose of a default gateway?

**Answer:** To forward traffic to other networks and the Internet.

---

### Q7. Name one private IP range.

**Answer:** 192.168.0.0 – 192.168.255.255

---

## Key Takeaways

- IP Address = Unique logical identifier for a device.
- IPv4 = 32-bit address.
- IPv6 = 128-bit address.
- Public IP = Internet-facing.
- Private IP = Internal network use.
- Static IP = Fixed address.
- Dynamic IP = Assigned by DHCP.
- Loopback = 127.0.0.1.
- APIPA = 169.254.x.x.
- Broadcast = Reaches all devices in a network.
- Default Gateway = Path to other networks.

---

## Memory Trick

```text
Public      = Internet

Private     = Internal Network

Static      = Fixed

Dynamic     = Automatic

Loopback    = Self

APIPA       = No DHCP

Gateway     = Exit Door

IPv4        = 32-bit

IPv6        = 128-bit
```
