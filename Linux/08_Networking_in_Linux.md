# Networking in Linux

## What is Networking in Linux?

Networking in Linux refers to the configuration, management, and monitoring of network communication between devices.

Linux provides powerful tools for:

* Network configuration
* Connectivity testing
* DNS resolution
* Remote administration
* Traffic investigation
* Security monitoring

---

## Why is Linux Networking Important?

Without Networking

* Systems cannot communicate.
* Internet access is unavailable.
* Remote administration becomes impossible.
* Data sharing cannot occur.

With Networking

* Devices communicate efficiently.
* Servers provide services.
* Administrators manage systems remotely.
* Security teams investigate network activity.

---

## Real-World Example

When opening a website:

```text id="l5b8xa"
Linux System
      │
      ▼
Network Interface
      │
      ▼
Router
      │
      ▼
Internet
      │
      ▼
Web Server
```

Networking enables communication between systems worldwide.

---

## Viewing Network Configuration

### ip addr

Displays network interface information.

```bash id="1uyd0g"
ip addr
```

Example Output:

```text id="yyonjl"
2: eth0
inet 192.168.1.100/24
```

Displays:

* IP Address
* Interface Name
* MAC Address

---

### ifconfig

Legacy networking tool.

```bash id="0gj44x"
ifconfig
```

May require installation:

```bash id="zkmgkz"
sudo apt install net-tools
```

---

## View Routing Table

### ip route

```bash id="9j31e5"
ip route
```

Example:

```text id="g4x9j6"
default via 192.168.1.1 dev eth0
```

Shows:

* Default gateway
* Network routes

---

## Display Hostname

### hostname

```bash id="fd7a8n"
hostname
```

Displays the system hostname.

---

## View DNS Configuration

### cat /etc/resolv.conf

```bash id="h9k8mt"
cat /etc/resolv.conf
```

Example:

```text id="tf5rz6"
nameserver 8.8.8.8
nameserver 1.1.1.1
```

Displays configured DNS servers.

---

## Testing Connectivity

### ping

Tests network connectivity.

```bash id="2elxfm"
ping google.com
```

Example Output:

```text id="6e8zg9"
64 bytes from google.com
```

Useful for verifying connectivity.

---

## Tracing Network Path

### traceroute

Displays the path packets take.

```bash id="1vlr3r"
traceroute google.com
```

Installation:

```bash id="w2pkrm"
sudo apt install traceroute
```

Example:

```text id="0mjlwm"
Router
ISP
Google
```

Useful for troubleshooting network issues.

---

## DNS Lookup

### nslookup

Queries DNS records.

```bash id="7e6kgz"
nslookup google.com
```

Example Output:

```text id="j7hkrj"
Address: 142.250.x.x
```

---

### dig

Advanced DNS investigation tool.

```bash id="dfaw8o"
dig google.com
```

Installation:

```bash id="m8x4yx"
sudo apt install dnsutils
```

Useful for:

* DNS troubleshooting
* Security investigations
* Threat hunting

---

## Viewing Active Connections

### netstat

Displays active connections and listening ports.

```bash id="9m76ls"
netstat -tulnp
```

Example:

```text id="t7bdc4"
tcp 0 0 0.0.0.0:22 LISTEN
```

Displays:

* Protocol
* Port
* Process

---

### ss

Modern replacement for netstat.

```bash id="wz4lbw"
ss -tulnp
```

Faster and preferred on modern Linux systems.

---

## Downloading Files

### wget

Downloads files from the Internet.

```bash id="o8izw5"
wget https://example.com/file.txt
```

Useful for:

* Software downloads
* Script retrieval
* Automation

---

### curl

Transfers data using URLs.

```bash id="ly1n6r"
curl https://example.com
```

Commonly used for:

* API testing
* Web requests
* Security assessments

---

## Remote Administration

### SSH (Secure Shell)

Allows secure remote access.

```bash id="5v7kln"
ssh user@192.168.1.100
```

Example:

```bash id="hqj36u"
ssh kali@192.168.1.10
```

Widely used by Linux administrators.

---

## Secure File Transfer

### SCP

Copies files securely over SSH.

Copy file to remote system:

```bash id="f1u7r0"
scp file.txt user@192.168.1.100:/home/user
```

Copy file from remote system:

```bash id="w68r9w"
scp user@192.168.1.100:file.txt .
```

---

## Network Interface Statistics

### ip -s link

Displays interface statistics.

```bash id="8r4g6p"
ip -s link
```

Shows:

* Packets Sent
* Packets Received
* Errors
* Dropped Packets

---

## Check Open Ports

### ss -ltn

```bash id="v5tv25"
ss -ltn
```

Displays listening TCP ports.

Example:

```text id="w7o3r4"
22
80
443
```

---

## Common Ports

| Port  | Service |
| ----- | ------- |
| 20/21 | FTP     |
| 22    | SSH     |
| 23    | Telnet  |
| 25    | SMTP    |
| 53    | DNS     |
| 80    | HTTP    |
| 110   | POP3    |
| 143   | IMAP    |
| 443   | HTTPS   |
| 3306  | MySQL   |

---

## Why Linux Networking Matters in Cybersecurity

Cybersecurity professionals use Linux networking tools to:

* Investigate attacks
* Monitor traffic
* Identify open ports
* Analyze DNS activity
* Detect suspicious connections
* Secure remote access
* Perform threat hunting

Many security investigations begin with network analysis.

---

## Common SOC Investigation Commands

View IP address:

```bash id="3ddn6h"
ip addr
```

Test connectivity:

```bash id="0axk2h"
ping google.com
```

View listening ports:

```bash id="9e40w5"
ss -tulnp
```

Investigate DNS:

```bash id="9u4v6n"
dig google.com
```

Trace route:

```bash id="j2s4bo"
traceroute google.com
```

Remote login:

```bash id="wwkm3x"
ssh user@host
```

---

## Interview Questions

### Q1. Which command displays IP addresses in Linux?

```bash id="j7f4hn"
ip addr
```

---

### Q2. What does ping do?

It tests network connectivity between systems.

---

### Q3. What is SSH?

SSH (Secure Shell) provides encrypted remote access to systems.

---

### Q4. What is the difference between netstat and ss?

`ss` is faster and is the modern replacement for `netstat`.

---

### Q5. Which command performs DNS lookups?

```bash id="5r1gdx"
nslookup
```

or

```bash id="gqig6f"
dig
```

---

### Q6. Which command securely copies files between systems?

```bash id="x6egct"
scp
```

---

### Q7. Which port is used by SSH?

```text id="8h4tw3"
Port 22
```

---

## Key Takeaways

✔ Linux provides powerful networking tools.

✔ `ip addr` displays network configuration.

✔ `ping` tests connectivity.

✔ `traceroute` shows packet paths.

✔ `dig` and `nslookup` perform DNS lookups.

✔ `ss` and `netstat` display network connections.

✔ `curl` and `wget` download data.

✔ `ssh` enables secure remote administration.

✔ `scp` securely transfers files.

✔ Networking knowledge is essential for SOC Analysts, Incident Responders, and Security Engineers.
