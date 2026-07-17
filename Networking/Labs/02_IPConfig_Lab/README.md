# Lab 02 - Windows IPConfig Commands

## Objective

To learn how to inspect, analyze, and troubleshoot Windows network configuration using the `ipconfig` command and its commonly used options.

---

## Prerequisites

- Windows Operating System
- Command Prompt
- Active Wi-Fi or Ethernet connection
- Administrator privileges (recommended)

---

## Theory

`ipconfig` is a Windows command-line utility used to display and manage TCP/IP configuration.

It helps administrators and cybersecurity professionals inspect:

- IPv4 and IPv6 addresses
- Subnet masks
- Default gateways
- DNS servers
- DHCP configuration
- DNS Resolver Cache
- Active and disconnected network adapters

Understanding these details is essential for network troubleshooting, system administration, SOC operations, and incident response.

---

## Commands Used

```cmd
ipconfig
ipconfig /all
ipconfig /displaydns
ipconfig /flushdns
ipconfig /release
ipconfig /renew
```

During the lab, an incorrect command was also tested:

```cmd
ipconfig / flushdns
```

This produced an error because Windows commands do **not** allow a space after `/`.

---

## Steps Performed

1. Displayed the basic network configuration using `ipconfig`.
2. Displayed complete adapter information using `ipconfig /all`.
3. Viewed the Windows DNS Resolver Cache using `ipconfig /displaydns`.
4. Executed an incorrect `flushdns` command and analyzed the error.
5. Successfully flushed the DNS Resolver Cache.
6. Released the DHCP-assigned IPv4 address.
7. Renewed the DHCP lease and restored network connectivity.

---

## Results

### Initial Wi-Fi Configuration

| Parameter | Value |
|-----------|-------|
| IPv4 Address | 192.168.0.118 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.0.1 |
| DHCP | Enabled |
| DHCP Server | 192.168.0.1 |

---

### VirtualBox Host-Only Adapter

| Parameter | Value |
|-----------|-------|
| IPv4 Address | 192.168.56.1 |
| DHCP | Disabled |
| Default Gateway | None |

---

### DNS Resolver Cache

The DNS cache contained records related to services such as:

- Google
- GitHub
- ChatGPT
- WhatsApp
- Microsoft
- Google Drive
- Cloudflare

Observed record types included:

- A Record
- AAAA Record
- CNAME Record
- PTR Record

TTL values were also displayed for each cached record.

---

### After `ipconfig /flushdns`

Windows successfully cleared the DNS Resolver Cache.

Output:

```text
Successfully flushed the DNS Resolver Cache.
```

---

### After `ipconfig /release`

- IPv4 address was released.
- IPv4 Default Gateway disappeared.
- Link-local IPv6 address remained.
- VirtualBox adapter remained unchanged.
- Disconnected adapters displayed "Media disconnected".

---

### After `ipconfig /renew`

New DHCP configuration:

| Parameter | Value |
|-----------|-------|
| IPv4 Address | 192.168.1.34 |
| Default Gateway | 192.168.1.1 |
| DNS Suffix | bbrouter |

The IP address changed from **192.168.0.x** to **192.168.1.x**, indicating that the DHCP server assigned a new address from a different subnet.

---

## DHCP DORA Process

When `ipconfig /renew` is executed, Windows follows the DHCP process:

1. Discover
2. Offer
3. Request
4. Acknowledgement

---

## Cybersecurity Perspective

These commands are useful during:

- Network troubleshooting
- DNS investigations
- Incident response
- Malware analysis
- DHCP troubleshooting
- DNS cache analysis
- Initial evidence collection

The DNS Resolver Cache provides useful investigative information but should not be considered complete browsing history.

---

## Challenge Completed

- ✅ Viewed basic IP configuration
- ✅ Viewed detailed adapter information
- ✅ Inspected DNS Resolver Cache
- ✅ Cleared DNS Resolver Cache
- ✅ Released DHCP lease
- ✅ Renewed DHCP lease
- ✅ Identified VirtualBox Host-Only adapter
- ✅ Corrected command syntax error

---

## Skills Gained

- Windows Networking
- TCP/IP Analysis
- DNS Investigation
- DHCP Troubleshooting
- Windows Command Line
- Incident Response Basics
- Network Documentation

---

## Lab Summary

This lab demonstrated how to inspect Windows network configuration, analyze cached DNS records, clear the DNS Resolver Cache, release and renew DHCP leases, and understand how Windows manages IP addressing through DHCP.
