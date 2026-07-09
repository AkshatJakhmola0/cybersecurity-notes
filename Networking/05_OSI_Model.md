# OSI Model

## Definition

OSI (Open Systems Interconnection) Model is a conceptual framework that divides network communication into 7 layers to standardize how devices communicate.

---

## Why

The OSI Model helps to:

- Simplify networking concepts
- Troubleshoot network issues
- Provide a standard for communication
- Identify where an attack or problem occurs

---

## Working

When data is sent, it travels from the top layer to the bottom layer.

```text
Application
      ↓
Presentation
      ↓
Session
      ↓
Transport
      ↓
Network
      ↓
Data Link
      ↓
Physical
```

When data is received, the process happens in reverse (Physical → Application).

---

## Real-World Example

When you open a website:

- **Application Layer** – Browser requests the website.
- **Presentation Layer** – Data is encrypted or decrypted if required.
- **Session Layer** – Establishes and manages the communication session.
- **Transport Layer** – Data is divided into segments using TCP or UDP.
- **Network Layer** – IP addresses are added for routing.
- **Data Link Layer** – MAC addresses are added for local communication.
- **Physical Layer** – Data travels as electrical, optical, or wireless signals.

---

## Cybersecurity Perspective

Security professionals use the OSI Model to identify where attacks occur.

- **Layer 7 (Application)** – SQL Injection, XSS
- **Layer 4 (Transport)** – Port Scanning
- **Layer 3 (Network)** – IP Spoofing, DDoS
- **Layer 2 (Data Link)** – ARP Spoofing
- **Layer 1 (Physical)** – Physical Tampering

---

## Common Layers

### Layer 7 – Application

User-facing services such as:

- HTTP
- HTTPS
- DNS

---

### Layer 6 – Presentation

Responsible for:

- Encryption
- Decryption
- Compression

---

### Layer 5 – Session

Responsible for:

- Establishing sessions
- Managing sessions
- Terminating sessions

---

### Layer 4 – Transport

Responsible for:

- TCP
- UDP
- Reliability
- Port Numbers

---

### Layer 3 – Network

Responsible for:

- IP Addressing
- Routing

---

### Layer 2 – Data Link

Responsible for:

- MAC Addressing
- Switching

---

### Layer 1 – Physical

Responsible for:

- Network Cables
- Fiber Optics
- Wireless Signals

---

## Interview Questions

### Q1. What does OSI stand for?

**Answer:** Open Systems Interconnection

---

### Q2. How many layers are in the OSI Model?

**Answer:** 7

---

### Q3. Which layer uses IP addresses?

**Answer:** Network Layer (Layer 3)

---

### Q4. Which layer uses MAC addresses?

**Answer:** Data Link Layer (Layer 2)

---

### Q5. Which layer contains TCP and UDP?

**Answer:** Transport Layer (Layer 4)

---

### Q6. Which layer is closest to the user?

**Answer:** Application Layer (Layer 7)

---

## Key Takeaways

- OSI Model has **7 layers**.
- It standardizes network communication.
- It helps troubleshoot networking issues.
- Each layer performs a specific function.
- Cyberattacks can target different layers.

---

## Memory Trick

### Top to Bottom

```text
Application
Presentation
Session
Transport
Network
Data Link
Physical
```

### Mnemonic

> **All People Seem To Need Data Processing**

### Layer Numbers

| Layer | Name |
|------:|----------------|
| 7 | Application |
| 6 | Presentation |
| 5 | Session |
| 4 | Transport |
| 3 | Network |
| 2 | Data Link |
| 1 | Physical |
