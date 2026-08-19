# Wireshark Cheatsheet

## Start Capture

Select Interface → Start

Common Interfaces:

- Ethernet
- Wi-Fi
- VirtualBox Adapter
- VPN Adapter

---

## Most Useful Display Filters

### IP Address

```text
ip.addr == 192.168.1.10
```

---

### Source IP

```text
ip.src == 192.168.1.10
```

---

### Destination IP

```text
ip.dst == 192.168.1.10
```

---

### TCP Traffic

```text
tcp
```

---

### UDP Traffic

```text
udp
```

---

### DNS Traffic

```text
dns
```

---

### HTTP Traffic

```text
http
```

---

### HTTPS Traffic

```text
tls
```

---

### ICMP (Ping)

```text
icmp
```

---

### ARP

```text
arp
```

---

### DHCP

```text
dhcp
```

---

### FTP

```text
ftp
```

---

### SSH

```text
ssh
```

---

### SMTP

```text
smtp
```

---

### RDP

```text
tcp.port == 3389
```

---

### Filter by Port

```text
tcp.port == 80
```

Example:

```text
tcp.port == 443
```

---

### Filter by Protocol and IP

```text
ip.addr == 192.168.1.10 && tcp
```

---

## Packet Inspection

### Follow TCP Stream

Right Click Packet

```text
Follow → TCP Stream
```

Useful for:

- Credentials
- HTTP Requests
- Malware Communication
- Data Exfiltration

---

### View Packet Details

Expand:

```text
Frame
Ethernet II
Internet Protocol
Transmission Control Protocol
Application Layer Protocol
```

---

## Useful Statistics

### Protocol Hierarchy

```text
Statistics → Protocol Hierarchy
```

Shows:

- TCP
- UDP
- HTTP
- DNS
- TLS

---

### Conversations

```text
Statistics → Conversations
```

Shows:

- Source IP
- Destination IP
- Packets
- Bytes

---

### Endpoints

```text
Statistics → Endpoints
```

Lists all communicating hosts.

---

## Export Data

### Export Packets

```text
File → Export Specified Packets
```

---

### Save Capture

```text
File → Save As
```

Extensions:

```text
.pcap
.pcapng
```

---

## SOC Analyst Filters

### Failed DNS Queries

```text
dns.flags.rcode != 0
```

---

### Large Traffic Volume

```text
tcp.len > 1000
```

---

### Suspicious HTTP Requests

```text
http.request
```

---

### Search Credentials

```text
http.authorization
```

---

### Detect File Downloads

```text
http contains "exe"
```

---

## Common Shortcuts

| Shortcut | Function |
|-----------|-----------|
| Ctrl + E | Start/Stop Capture |
| Ctrl + R | Reload Capture |
| Ctrl + F | Find Packet |
| Ctrl + S | Save Capture |
| Ctrl + Shift + F | Find Packet String |

---

## Quick SOC Workflow

1. Open PCAP
2. Check Protocol Hierarchy
3. Check Endpoints
4. Check Conversations
5. Filter DNS
6. Filter HTTP/HTTPS
7. Investigate Suspicious IPs
8. Follow TCP Streams
9. Export Evidence
10. Document Findings

---

## Interview Questions

### Q1. What is Wireshark?

Wireshark is a network protocol analyzer used to capture and inspect network traffic.

---

### Q2. What is a PCAP file?

A PCAP file stores captured network packets for analysis.

---

### Q3. What is Follow TCP Stream?

It reconstructs a complete conversation between two hosts.

---

### Q4. Which filter shows DNS traffic?

```text
dns
```

---

### Q5. Which filter shows HTTP traffic?

```text
http
```

---

## Key Takeaways

✔ Wireshark captures network packets.

✔ Display filters help isolate traffic.

✔ Follow TCP Stream reconstructs conversations.

✔ Protocol Hierarchy shows protocol usage.

✔ Wireshark is heavily used by SOC Analysts and Incident Responders.
