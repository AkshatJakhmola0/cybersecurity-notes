# Observations

## Lab Name
Netstat - Windows Network Connection Analysis

---

## Commands Executed

1. netstat
2. netstat -a
3. netstat -ano
4. tasklist

---

## Observations

### Basic Network Connections
- The `netstat` command displayed all active TCP connections established by the system.
- Multiple HTTPS (Port 443) connections were observed, indicating secure communication with remote servers.
- Several connections were in the `ESTABLISHED` state, confirming active communication between local applications and external hosts.

---

### Listening Ports
Using `netstat -a`, several listening ports were identified, including:

- Port 135 (RPC Endpoint Mapper)
- Port 139 (NetBIOS Session Service)
- Port 445 (SMB File Sharing)
- Port 8080
- Port 6881
- Several dynamic Windows ports (49664–49672)

These ports indicate that Windows services and installed applications were waiting for incoming connections.

---

### Connection States

The following TCP states were observed:

- LISTENING
- ESTABLISHED
- TIME_WAIT
- CLOSE_WAIT

Each state represented different phases of the TCP connection lifecycle.

---

### Loopback Connections

Several connections used the loopback address (127.0.0.1), indicating communication between applications running on the same computer.

---

### IPv4 and IPv6

Both IPv4 and IPv6 network interfaces were active.

The system contained listening sockets for both protocols.

---

### UDP Services

Several UDP services were active, including:

- Port 1900 (SSDP)
- Port 5353 (mDNS)
- Port 5355 (LLMNR)
- Other dynamically allocated UDP ports

These services are commonly used for local network discovery and communication.

---

### PID Mapping

Using `netstat -ano`, every network connection was mapped to its corresponding Process ID (PID).

Examples included:

- PID 4 → Windows System
- PID 2064 → utweb.exe
- PID 5004 → AgentService.exe
- PID 4068 → Google Chrome
- PID 1212 → OneDrive

This demonstrated how network activity can be associated with individual running processes.

---

### Application Identification

Using `tasklist`, the running processes corresponding to the identified PIDs were verified.

This confirmed that:

- Windows services were responsible for standard system ports.
- Chrome generated multiple HTTPS connections.
- µTorrent Web (utweb.exe) owned Port 6881.
- Dell services and OneDrive created expected network connections.

---

## Security Observations

- No immediately suspicious or malicious network connections were observed during the investigation.
- Most active connections belonged to trusted Windows services or installed applications.
- Ports 6666 and 8080 were associated with AgentService.exe.
- Port 6881 was confirmed to belong to µTorrent Web.
- The investigation highlighted the importance of validating a process before considering a listening port suspicious.

---

## Learning Outcome

This lab demonstrated how to:

- View active network connections.
- Identify listening ports.
- Understand TCP connection states.
- Examine UDP endpoints.
- Map network connections to running processes using PIDs.
- Investigate which application owns a network connection.
- Perform the initial steps of a host-based network investigation.
