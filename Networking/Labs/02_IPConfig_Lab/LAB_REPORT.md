# Lab Report

## Lab Information

- **Lab Name:** Windows IPConfig Commands
- **Status:** Completed
- **Platform:** Windows Command Prompt

---

## Objective

To explore the Windows `ipconfig` utility for viewing network configuration, analyzing the DNS Resolver Cache, and managing DHCP leases.

---

## Commands Executed

```cmd
ipconfig
ipconfig /all
ipconfig /displaydns
ipconfig /flushdns
ipconfig /release
ipconfig /renew
```

---

## Work Performed

- Displayed the basic network configuration.
- Viewed detailed adapter information.
- Examined the DNS Resolver Cache.
- Cleared the DNS Resolver Cache.
- Released the current DHCP lease.
- Renewed the DHCP lease.

---

## Key Findings

| Item | Result |
|------|--------|
| Initial IPv4 Address | 192.168.0.118 |
| Renewed IPv4 Address | 192.168.1.34 |
| Initial Gateway | 192.168.0.1 |
| Renewed Gateway | 192.168.1.1 |
| VirtualBox Adapter | 192.168.56.1 (Unchanged) |
| DHCP | Enabled |

---

## Challenges

- Executed `ipconfig / flushdns` with incorrect syntax.
- Corrected the command to `ipconfig /flushdns` and successfully flushed the DNS cache.

---

## Skills Practiced

- Windows Networking
- TCP/IP Configuration
- DNS Cache Analysis
- DHCP Lease Management
- Windows Command Line
- Basic Network Troubleshooting

---

## Conclusion

This lab provided practical experience with the Windows `ipconfig` utility. I learned how to inspect network configuration, analyze and clear the DNS Resolver Cache, and release and renew DHCP leases. The exercise also reinforced the importance of correct command syntax and understanding the role of active, disconnected, and virtual network adapters during troubleshooting.
