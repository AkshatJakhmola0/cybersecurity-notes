# Networking Cheatsheet

## OSI Model

| Layer | Name |
|---------|---------|
| 7 | Application |
| 6 | Presentation |
| 5 | Session |
| 4 | Transport |
| 3 | Network |
| 2 | Data Link |
| 1 | Physical |

Mnemonic:

All People Seem To Need Data Processing

---

## TCP vs UDP

### TCP

- Connection Oriented
- Reliable
- Error Checking
- Slower

Examples:

- HTTP
- HTTPS
- SSH
- FTP

### UDP

- Connectionless
- Faster
- No Delivery Guarantee

Examples:

- DNS
- DHCP
- VoIP
- Streaming

---

## Common Networking Devices

### Router

Connects different networks.

### Switch

Connects devices within same network.

### Hub

Broadcasts traffic to all ports.

### Firewall

Filters network traffic.

### Access Point

Provides wireless connectivity.

---

## Public vs Private IP

### Private Ranges

10.0.0.0/8

172.16.0.0 – 172.31.255.255

192.168.0.0/16

### Public IP

Internet routable address.

---

## Useful Commands

### Windows

ipconfig

ping

tracert

netstat

nslookup

arp -a

### Linux

ip a

ping

traceroute

ss

netstat

dig

---

## CIA Triad

Confidentiality

Integrity

Availability
