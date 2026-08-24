# Linux Networking Commands Cheat Sheet

## IP Address Information

### View IP Addresses

```bash
ip addr
```

```bash
hostname -I
```

---

## Routing Information

```bash
ip route
```

---

## Connectivity Testing

### Ping

```bash
ping 8.8.8.8
```

### DNS Lookup

```bash
nslookup google.com
```

### Dig

```bash
dig google.com
```

---

## Active Connections

### Netstat

```bash
netstat -tulpn
```

### ss

```bash
ss -tulpn
```

---

## Network Interfaces

```bash
ip link show
```

```bash
ifconfig
```

---

## Packet Capture

```bash
tcpdump -i eth0
```

---

## Port Scanning

```bash
nmap 192.168.1.1
```

---

## SOC Analyst Usage

- Network troubleshooting
- Port investigation
- Connection monitoring
- Threat hunting
- Incident response

---

## Quick Examples

```bash
ip addr
ping 8.8.8.8
ss -tulpn
tcpdump -i eth0
```
