# Lab 04 - Network Statistics (Netstat)

## Objective

To understand how the `netstat` command is used to monitor network connections, identify listening ports, examine active TCP and UDP sessions, and associate network connections with running processes on a Windows system.

---

## Prerequisites

- Windows Operating System
- Command Prompt (Administrator privileges required for some commands)
- Active Network Connection
- Basic understanding of IP addresses, ports, and network protocols

---

## Theory

**Netstat (Network Statistics)** is a command-line utility that displays information about active network connections, listening ports, routing tables, and network interface statistics.

It is widely used by system administrators, network engineers, and cybersecurity professionals to monitor network activity, troubleshoot connectivity issues, and investigate suspicious connections.

Netstat provides detailed information about both incoming and outgoing connections, making it an essential tool for network diagnostics and security analysis.

---

## Commands Used

```cmd
netstat
netstat -a
netstat -n
netstat -o
netstat -b
netstat -ano
```

---

## Steps Performed

1. Displayed the default network statistics.
2. Listed all active and listening TCP and UDP connections.
3. Displayed numerical IP addresses and port numbers.
4. Displayed Process IDs (PID) associated with each connection.
5. Displayed executable names responsible for network connections.
6. Combined all information using the `netstat -ano` command.

---

## Key Concepts

### Network Connection

A network connection is a communication link established between two devices over a network using protocols such as TCP or UDP.

---

### TCP (Transmission Control Protocol)

TCP is a connection-oriented protocol that ensures reliable and ordered delivery of data between devices.

Examples:
- HTTP
- HTTPS
- FTP
- SSH

---

### UDP (User Datagram Protocol)

UDP is a connectionless protocol that provides faster communication without guaranteeing packet delivery.

Examples:
- DNS
- DHCP
- Online Gaming
- Video Streaming

---

### Listening Port

A listening port is a port on which an application or service is waiting for incoming network connections.

---

### Established Connection

An established connection indicates that two devices have successfully completed the TCP handshake and are actively exchanging data.

---

### Local Address

The Local Address represents the IP address and port number of the local computer involved in the connection.

Example:

```
192.168.0.104:49721
```

---

### Foreign Address

The Foreign Address represents the remote computer or server communicating with the local system.

Example:

```
142.250.x.x:443
```

---

### Port Number

A port number identifies a specific service or application running on a device.

Examples:

| Port | Service |
|------|---------|
| 20/21 | FTP |
| 22 | SSH |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 143 | IMAP |
| 443 | HTTPS |
| 3389 | Remote Desktop (RDP) |

---

### Process ID (PID)

A Process ID (PID) uniquely identifies a running process in Windows. Using the PID, a network connection can be mapped to the application responsible for it.

---

## Cybersecurity Perspective

Netstat is an essential tool during cybersecurity investigations because it helps identify:

- Active network connections
- Listening services
- Unknown or suspicious ports
- Remote systems communicating with the host
- Processes responsible for network activity
- Indicators of malware or unauthorized access

Security analysts frequently use Netstat during incident response, malware analysis, and digital forensics.

---

## Skills Gained

- Network Monitoring
- TCP/IP Analysis
- Port Analysis
- Process Identification
- Windows Networking
- Network Troubleshooting
- Incident Response Basics
- Cybersecurity Investigation

---
## Lab Summary

This lab demonstrates how the Netstat utility can be used to inspect active network connections, monitor listening ports, identify processes responsible for network communication, and troubleshoot network-related issues. It also highlights the importance of Netstat in cybersecurity for detecting suspicious connections, investigating malware activity, and performing host-based network analysis.
