# LAB_REPORT.md

# Experiment 05 - Networking Basics in Linux

## Aim

To study and practice Linux networking commands for analyzing IP configuration, routing, DNS resolution, connectivity testing, active connections, and network troubleshooting.

---

## Tools Used

- Kali Linux
- Linux Terminal
- ip
- ping
- nslookup
- dig
- ss
- netstat
- traceroute
- curl
- wget

---

## Theory

Networking is an essential component of Linux system administration and cybersecurity. Linux provides several command-line utilities to inspect network interfaces, routing tables, DNS configurations, active connections, and connectivity status.

These tools help administrators troubleshoot network issues and verify communication between systems.

---

## Procedure

### Step 1: Display Network Interfaces

```bash
ip addr
```

Used to display IP addresses assigned to network interfaces.

---

### Step 2: View Routing Table

```bash
ip route
```

Used to display routing information and default gateway.

---

### Step 3: Verify Interface Status

```bash
ip link show
```

Displays interface operational status.

---

### Step 4: Test Internet Connectivity

```bash
ping 8.8.8.8
```

Tests network connectivity using Google's public DNS server.

---

### Step 5: Test DNS Resolution

```bash
ping google.com
```

Verifies DNS name resolution.

---

### Step 6: Perform DNS Lookup

```bash
nslookup google.com
```

Queries DNS records using the configured DNS server.

---

### Step 7: Perform Detailed DNS Query

```bash
dig google.com
```

Retrieves detailed DNS information.

---

### Step 8: Check Open Ports

```bash
ss -tulnp
```

```bash
netstat -tulnp
```

Displays listening network services.

---

### Step 9: Trace Packet Route

```bash
traceroute google.com
```

Shows the path packets take to reach a destination.

---

### Step 10: Send HTTP Request

```bash
curl https://google.com
```

Retrieves webpage content and HTTP responses.

---

### Step 11: Download Remote File

```bash
wget https://example.com
```

Downloads files from a remote server.

---

### Step 12: View Neighbor Table

```bash
ip neigh
```

Displays ARP and neighbor discovery information.

---

### Step 13: View Active TCP Connections

```bash
ss -ant
```

Displays active TCP sessions and states.

---

### Step 14: Check Hostname

```bash
hostname
```

Displays the system hostname.

---

### Step 15: Verify DNS Configuration

```bash
cat /etc/resolv.conf
```

Displays configured DNS resolver information.

---
This experiment successfully demonstrated the use of Linux networking commands for network analysis and troubleshooting. The system was able to communicate with external hosts, resolve domain names, perform HTTP requests, download files, and inspect routing and interface information. The lab provided practical exposure to essential networking concepts used in Linux administration and cybersecurity.
