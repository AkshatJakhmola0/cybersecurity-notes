# Common Network Protocols

## Definition

Protocols are a set of rules that devices follow to communicate over a network.

---

## Why

Protocols are important because they:

- Standardize communication.
- Allow different devices to understand each other.
- Enable Internet access, email, file sharing, and remote administration.

---

## Working

```text
Device A
    │
Uses a Protocol
    │
    ▼
Device B
    │
Understands the Protocol
    │
    ▼
Communication Occurs
```

---

## Real-World Example

### Opening Google

```text
Browser
   │
 HTTPS
   │
Google Server
```

### Sending an Email

```text
Email Client
     │
    SMTP
     │
Mail Server
```

---

## Cybersecurity Perspective

Security engineers monitor network protocols because attackers often abuse them for:

- Reconnaissance
- Credential Theft
- Malware Communication
- Data Exfiltration

---

# Common Protocols

## HTTP

### Definition

HyperText Transfer Protocol.

### Purpose

Transfers web pages over the Internet.

### Port

```text
80
```

### Example

Opening a website without encryption.

### Cybersecurity

Data is transmitted in plaintext and can be intercepted.

---

## HTTPS

### Definition

HyperText Transfer Protocol Secure.

### Purpose

Secure web communication using SSL/TLS.

### Port

```text
443
```

### Example

Online banking and e-commerce websites.

### Cybersecurity

Protects data using encryption but can be targeted through SSL stripping and certificate attacks.

---

## DNS

### Definition

Domain Name System.

### Purpose

Converts domain names into IP addresses.

### Port

```text
53
```

### Example

```text
google.com → 142.250.x.x
```

### Cybersecurity

DNS Spoofing and DNS Poisoning attacks.

---

## DHCP

### Definition

Dynamic Host Configuration Protocol.

### Purpose

Automatically assigns IP addresses.

### Port

```text
67 / 68
```

### Example

Connecting a phone to Wi-Fi and automatically receiving an IP address.

### Cybersecurity

Rogue DHCP servers can assign malicious network configurations.

---

## FTP

### Definition

File Transfer Protocol.

### Purpose

Transfers files between systems.

### Port

```text
20 / 21
```

### Example

Uploading website files to a server.

### Cybersecurity

Usernames and passwords are transmitted in plaintext.

---

## SSH

### Definition

Secure Shell.

### Purpose

Secure remote login and administration.

### Port

```text
22
```

### Example

Managing a Linux server remotely.

### Cybersecurity

Often targeted by brute-force attacks but much safer than Telnet.

---

## SMTP

### Definition

Simple Mail Transfer Protocol.

### Purpose

Sends emails.

### Port

```text
25
```

### Example

Sending an email from Gmail.

### Cybersecurity

Frequently abused for spam and phishing campaigns.

---

## POP3

### Definition

Post Office Protocol Version 3.

### Purpose

Downloads emails from the mail server.

### Port

```text
110
```

### Example

Downloading emails to a local computer.

### Cybersecurity

Less secure unless encryption is enabled.

---

## IMAP

### Definition

Internet Message Access Protocol.

### Purpose

Accesses emails while keeping them on the mail server.

### Port

```text
143
```

### Example

Checking the same mailbox from multiple devices.

### Cybersecurity

Commonly used with encryption for secure email access.

---

## Telnet

### Definition

Remote login protocol.

### Purpose

Remote administration.

### Port

```text
23
```

### Example

Managing older network devices.

### Cybersecurity

Insecure because all communication is transmitted in plaintext.

---

## ICMP

### Definition

Internet Control Message Protocol.

### Purpose

Network diagnostics and error reporting.

### Port

```text
N/A
```

### Example

Ping and Traceroute.

### Cybersecurity

Used for reconnaissance, ping sweeps, and ICMP flood attacks.

---

## ARP

### Definition

Address Resolution Protocol.

### Purpose

Maps IP addresses to MAC addresses.

### Port

```text
N/A
```

### Example

Finding the MAC address of a device within a LAN.

### Cybersecurity

ARP Spoofing and Man-in-the-Middle (MITM) attacks.

---

## Common Ports

| Protocol | Port | Purpose |
|----------|------|---------|
| HTTP | 80 | Web Traffic |
| HTTPS | 443 | Secure Web Traffic |
| FTP | 20/21 | File Transfer |
| SSH | 22 | Secure Remote Login |
| Telnet | 23 | Remote Login |
| SMTP | 25 | Send Email |
| DNS | 53 | Name Resolution |
| DHCP | 67/68 | Automatic IP Assignment |
| POP3 | 110 | Receive Email |
| IMAP | 143 | Receive Email |
| ICMP | N/A | Network Diagnostics |
| ARP | N/A | IP to MAC Mapping |

---

## Interview Questions

### Q1. Which protocol uses port 80?

**Answer:** HTTP

---

### Q2. What is the difference between HTTP and HTTPS?

**Answer:** HTTPS uses SSL/TLS encryption, while HTTP does not.

---

### Q3. Which protocol automatically assigns IP addresses?

**Answer:** DHCP

---

### Q4. Which protocol converts domain names into IP addresses?

**Answer:** DNS

---

### Q5. Which protocol maps IP addresses to MAC addresses?

**Answer:** ARP

---

### Q6. Why is SSH preferred over Telnet?

**Answer:** SSH encrypts communication, while Telnet sends data in plaintext.

---

### Q7. Which protocol is used for secure websites?

**Answer:** HTTPS

---

## Key Takeaways

- HTTP = Web Traffic
- HTTPS = Secure Web Traffic
- DNS = Domain Name to IP Address
- DHCP = Automatic IP Assignment
- FTP = File Transfer
- SSH = Secure Remote Login
- SMTP = Send Email
- POP3 = Download Email
- IMAP = Access Email on Server
- Telnet = Insecure Remote Login
- ICMP = Network Diagnostics
- ARP = IP to MAC Mapping

---

## Memory Tricks

```text
80      → HTTP

443     → HTTPS

22      → SSH

23      → Telnet

20/21   → FTP

25      → SMTP

53      → DNS

67/68   → DHCP

110     → POP3

143     → IMAP
```

### Easy Memory

```text
Web            → 80 / 443

Remote Login   → 22 / 23

Email          → 25 / 110 / 143

Network        → 53 / 67 / 68

File Transfer  → 20 / 21

LAN            → ARP

Diagnostics    → ICMP
```
