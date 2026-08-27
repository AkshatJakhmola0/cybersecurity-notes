# Observation.md

# Observations - 05_Networking_Basics

## Objective
Learn basic Linux networking commands and analyze network configuration, connectivity, DNS resolution, routing, and active connections.

---

## 1. IP Address Information

### Command

```bash
ip addr
```

### Observation

#### Loopback Interface (lo)
- IPv4 Address: 127.0.0.1/8
- IPv6 Address: ::1/128

#### Interface: eth0
- IPv4 Address: 10.0.2.15/24
- MAC Address: 08:00:27:63:b0:05
- Network Type: NAT Adapter

#### Interface: eth1
- IPv4 Address: 192.168.56.101/24
- MAC Address: 08:00:27:bc:c0:43
- Network Type: Host-Only Adapter

### Conclusion

The Kali Linux VM is connected using two network interfaces:

1. NAT Adapter (eth0) for Internet access.
2. Host-Only Adapter (eth1) for communication with the host system.

---

## 2. Routing Table

### Command

```bash
ip route
```

### Observation

Default Gateway:

```text
10.0.2.2
```

Available Routes:

```text
10.0.2.0/24 via eth0
192.168.56.0/24 via eth1
```

### Conclusion

All Internet traffic is routed through the NAT gateway 10.0.2.2.

---

## 3. Network Interface Status

### Command

```bash
ip link show
```

### Observation

Interfaces Detected:
- lo
- eth0
- eth1

All interfaces are UP and operational.

### Conclusion

Network interfaces are functioning correctly.

---

## 4. Internet Connectivity Test

### Command

```bash
ping 8.8.8.8
```

### Observation

Results:
- Packets Sent: 19
- Packets Received: 19
- Packet Loss: 0%
- Average Latency: ~6 ms

### Conclusion

Internet connectivity is working successfully.

---

## 5. DNS Resolution Test

### Command

```bash
ping google.com
```

### Observation

Resolved Domain:

```text
google.com → 142.250.118.102
```

Results:
- Packets Sent: 25
- Packets Received: 25
- Packet Loss: 0%

### Conclusion

DNS resolution is functioning correctly.

---

## 6. DNS Lookup Using nslookup

### Command

```bash
nslookup google.com
```

### Observation

DNS Server Used:

```text
192.168.0.1
```

Multiple IPv4 and IPv6 addresses were returned.

### Conclusion

The local router DNS server is resolving queries successfully.

---

## 7. DNS Lookup Using dig

### Command

```bash
dig google.com
```

### Observation

Response Status:

```text
NOERROR
```

Query Time:

```text
8 ms
```

Several Google A records were returned.

### Conclusion

DNS queries are processed correctly.

---

## 8. Open Ports Analysis

### Commands

```bash
ss -tulnp
```

```bash
netstat -tulnp
```

### Observation

No listening services were detected.

### Conclusion

No network services are actively listening on the system.

---

## 9. Traceroute Analysis

### Command

```bash
traceroute google.com
```

### Observation

First Hop:

```text
10.0.2.2
```

Subsequent hops returned:

```text
*
```

### Conclusion

Intermediate routers are likely configured to block ICMP responses.

---

## 10. HTTP Request Using curl

### Command

```bash
curl https://google.com
```

### Observation

Received Response:

```text
301 Moved Permanently
```

Redirected To:

```text
https://www.google.com
```

### Conclusion

Google redirects requests to its canonical domain.

---

## 11. File Download Using wget

### Command

```bash
wget https://example.com
```

### Observation

Downloaded File:

```text
index.html
```

Size:

```text
559 Bytes
```

### Conclusion

HTTP/HTTPS file downloads are functioning correctly.

---

## 12. Neighbor Table Inspection

### Command

```bash
ip neigh
```

### Observation

Gateway Entry:

```text
10.0.2.2
```

MAC Address:

```text
52:55:0a:00:02:02
```

### Conclusion

Neighbor discovery and ARP resolution are working correctly.

---

## 13. TCP Connections

### Commands

```bash
ss -lnt
```

```bash
ss -ant
```

### Observation

Observed TCP Sessions:

```text
104.20.23.154:443
142.250.118.102:443
```

Connection State:

```text
TIME-WAIT
```

### Conclusion

Recently established HTTPS connections were closed successfully.

---

## 14. Hostname Verification

### Command

```bash
hostname
```

### Observation

Hostname:

```text
kali
```

### Conclusion

The system hostname is configured correctly.

---

## 15. DNS Configuration File

### Command

```bash
cat /etc/resolv.conf
```

### Observation

Configured DNS Server:

```text
192.168.0.1
```

### Conclusion

NetworkManager has automatically configured the DNS resolver.
