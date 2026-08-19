# TCP/IP Cheatsheet

## TCP/IP Model

| Layer | Function |
|---------|---------|
| Application | User Services |
| Transport | End-to-End Communication |
| Internet | Routing |
| Network Access | Physical Transmission |

---

## TCP Three-Way Handshake

Step 1

Client → SYN

Step 2

Server → SYN-ACK

Step 3

Client → ACK

Connection Established

---

## TCP Flags

| Flag | Meaning |
|--------|---------|
| SYN | Start Connection |
| ACK | Acknowledgement |
| FIN | Close Connection |
| RST | Reset Connection |
| PSH | Push Data |
| URG | Urgent Data |

---

## IPv4 Structure

32 Bits

Example:

192.168.1.1

Split into:

Network Portion

Host Portion

---

## IPv6

128 Bits

Example:

2001:db8::1

Benefits:

- Larger Address Space
- Better Routing
- No NAT Requirement

---

## Common Protocols

| Protocol | Purpose |
|------------|----------|
| IP | Addressing |
| TCP | Reliable Delivery |
| UDP | Fast Delivery |
| ICMP | Diagnostics |
| ARP | MAC Resolution |
| DNS | Name Resolution |
| DHCP | IP Assignment |

---

## ICMP Messages

### Echo Request

Ping Request

### Echo Reply

Ping Response

### Destination Unreachable

Host unreachable.

### Time Exceeded

TTL expired.

---

## Important Terms

### TTL

Time To Live

### MTU

Maximum Transmission Unit

### MSS

Maximum Segment Size

### RTT

Round Trip Time
