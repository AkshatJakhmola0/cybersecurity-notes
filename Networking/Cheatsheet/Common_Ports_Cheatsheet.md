# Common Ports Cheatsheet

## Well-Known Ports (0–1023)

| Port | Protocol | Service |
|--------|----------|----------|
| 20 | TCP | FTP Data |
| 21 | TCP | FTP Control |
| 22 | TCP | SSH |
| 23 | TCP | Telnet |
| 25 | TCP | SMTP |
| 53 | TCP/UDP | DNS |
| 67 | UDP | DHCP Server |
| 68 | UDP | DHCP Client |
| 69 | UDP | TFTP |
| 80 | TCP | HTTP |
| 110 | TCP | POP3 |
| 123 | UDP | NTP |
| 135 | TCP | MS RPC |
| 137 | UDP | NetBIOS Name Service |
| 138 | UDP | NetBIOS Datagram |
| 139 | TCP | NetBIOS Session |
| 143 | TCP | IMAP |
| 161 | UDP | SNMP |
| 162 | UDP | SNMP Trap |
| 179 | TCP | BGP |
| 389 | TCP/UDP | LDAP |
| 443 | TCP | HTTPS |
| 445 | TCP | SMB |
| 514 | UDP | Syslog |
| 636 | TCP | LDAPS |
| 993 | TCP | IMAPS |
| 995 | TCP | POP3S |

---

## Common Enterprise Ports

| Port | Protocol | Service |
|--------|----------|----------|
| 1433 | TCP | MS SQL Server |
| 1521 | TCP | Oracle Database |
| 2049 | TCP/UDP | NFS |
| 3306 | TCP | MySQL |
| 3389 | TCP | RDP |
| 5432 | TCP | PostgreSQL |
| 5900 | TCP | VNC |
| 5985 | TCP | WinRM HTTP |
| 5986 | TCP | WinRM HTTPS |
| 8080 | TCP | HTTP Alternate |

---

## Security Monitoring Focus

### High-Risk Ports

- 21 (FTP)
- 23 (Telnet)
- 135 (RPC)
- 139 (NetBIOS)
- 445 (SMB)
- 3389 (RDP)

---

## Common Exam Questions

### SSH Port?

22/TCP

### DNS Port?

53/TCP and UDP

### HTTPS Port?

443/TCP

### RDP Port?

3389/TCP

### SMB Port?

445/TCP
