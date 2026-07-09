# TCP/IP Model

## Definition

The TCP/IP Model is the practical networking model used on the Internet. It defines how data is transmitted between devices over a network.

---

## Why

- Provides communication rules for the Internet.
- Enables devices from different vendors to communicate.
- Simpler and more practical than the OSI Model.
- Forms the foundation of modern networking.

---

## Working

When data is sent:

```text
Application
      ↓
Transport
      ↓
Internet
      ↓
Network Access
```

When data is received, the process happens in reverse (Network Access → Application).

---

## Real-World Example

When you open YouTube:

- **Application Layer** – Browser requests YouTube.
- **Transport Layer** – TCP ensures reliable delivery.
- **Internet Layer** – IP finds the destination.
- **Network Access Layer** – Data travels through Wi-Fi or Ethernet.

---

## Cybersecurity Perspective

Security engineers analyze attacks at different TCP/IP layers.

- **Application Layer** – SQL Injection, XSS, Phishing.
- **Transport Layer** – Port Scanning, TCP Floods.
- **Internet Layer** – IP Spoofing, ICMP Attacks.
- **Network Access Layer** – ARP Spoofing, MAC Attacks.

---

## Common Layers

### Application Layer

Protocols:

- HTTP
- HTTPS
- DNS
- FTP
- SMTP

---

### Transport Layer

Responsible for:

- TCP
- UDP
- Port Numbers

---

### Internet Layer

Responsible for:

- IP Addressing
- ICMP
- Routing

---

### Network Access Layer

Responsible for:

- Ethernet
- Wi-Fi
- MAC Addressing

---

## OSI vs TCP/IP

| OSI Model | TCP/IP Model |
|------------|--------------|
| 7 Layers | 4 Layers |
| Reference Model | Practical Model |
| Theoretical | Used on the Internet |

### Layer Mapping

| OSI Model | TCP/IP Model |
|------------|--------------|
| Application + Presentation + Session | Application |
| Transport | Transport |
| Network | Internet |
| Data Link + Physical | Network Access |

---

## Interview Questions

### Q1. How many layers are in the TCP/IP Model?

**Answer:** 4

---

### Q2. Which model is used in real-world networking?

**Answer:** TCP/IP Model

---

### Q3. Which layer handles IP addressing?

**Answer:** Internet Layer

---

### Q4. Which layer contains TCP and UDP?

**Answer:** Transport Layer

---

### Q5. Which layer contains HTTP and HTTPS?

**Answer:** Application Layer

---

### Q6. Which layer handles MAC addresses?

**Answer:** Network Access Layer

---

## Key Takeaways

- TCP/IP Model has **4 layers**.
- It is the networking model used on the Internet.
- It is simpler and more practical than the OSI Model.
- TCP provides reliable communication.
- IP provides addressing and routing.

---

## Memory Trick

```text
Application
      ↓
Transport
      ↓
Internet
      ↓
Network Access
```

### Mnemonic

> **All Teachers In Network**
