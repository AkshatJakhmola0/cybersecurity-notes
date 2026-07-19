# Lab Report

## Lab Title

**Lab 03 - Address Resolution Protocol (ARP)**

---

## Objective

To understand the working of the Address Resolution Protocol (ARP), examine the ARP cache, clear cached entries, and observe how Windows rebuilds the ARP table during network communication.

---

## Tools Used

- Windows 11
- Command Prompt (CMD)
- Active Wi-Fi Network

---

## Commands Executed

```cmd
arp -a
arp -a -v
arp -d *
arp -a
ping 192.168.0.1
arp -a
```

---

## Procedure

1. Displayed the current ARP cache using the `arp -a` command.
2. Viewed detailed ARP information using the `arp -a -v` command.
3. Deleted the ARP cache using the `arp -d *` command.
4. Verified the ARP cache after deletion.
5. Pinged the default gateway (`192.168.0.1`) to generate network traffic.
6. Displayed the ARP cache again to observe how Windows rebuilt the ARP entries.

---

## Results

- Successfully viewed both normal and verbose ARP cache entries.
- Identified dynamic and static ARP entries on the local network.
- Cleared the ARP cache successfully.
- Verified that Windows automatically recreated required ARP entries after communication with the default gateway.
- Confirmed successful communication with the router with **0% packet loss** and **1–2 ms** response time.

---

## Learning Outcome

After completing this lab, I gained practical knowledge of:

- Address Resolution Protocol (ARP)
- ARP Cache and its purpose
- Dynamic and Static ARP entries
- Mapping IPv4 addresses to MAC addresses
- Clearing and rebuilding the ARP cache
- Basic troubleshooting using ARP commands
- Security risks such as ARP Spoofing and ARP Poisoning

---

## Conclusion

This lab provided practical experience with the Address Resolution Protocol (ARP) on a Windows system. By examining, deleting, and rebuilding the ARP cache, I observed how Windows resolves IP addresses to MAC addresses for communication within a Local Area Network (LAN). The exercise also demonstrated the importance of ARP in network communication and highlighted common security concerns such as ARP spoofing and cache poisoning, which are relevant in cybersecurity investigations and network defense.
