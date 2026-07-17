# Lab 02 - IPConfig Command

## Objective

To learn how to inspect, analyze, and troubleshoot network configuration using the Windows `ipconfig` command and its commonly used options.

---

## Prerequisites

- Windows Operating System
- Command Prompt
- Internet Connection

---

## Theory

`ipconfig` is a Windows command-line utility used to display and manage the TCP/IP network configuration of a computer.

It helps users and security professionals identify:

- Network adapters
- IP addresses
- Subnet masks
- Default gateway
- DNS servers
- DHCP information
- DNS cache

These details are essential for network troubleshooting, system administration, and cybersecurity investigations.

---

## Commands Used

```cmd
ipconfig

ipconfig /all

ipconfig /displaydns

ipconfig /flushdns
```

---

## Steps Performed

1. Displayed the basic network configuration using `ipconfig`.
2. Displayed detailed adapter information using `ipconfig /all`.
3. Viewed the local DNS resolver cache using `ipconfig /displaydns`.
4. Cleared the DNS resolver cache using `ipconfig /flushdns`.

---

## Expected Output

- Network adapter information
- IPv4 and IPv6 addresses
- Subnet mask
- Default gateway
- MAC address
- DHCP information
- DNS server information
- Cached DNS entries
- DNS cache successfully cleared

---

## Learning Outcome

After completing this lab, I learned how to:

- Identify active and inactive network adapters.
- Find the system's IPv4 and IPv6 addresses.
- Identify the subnet mask and default gateway.
- View MAC addresses.
- Determine DHCP configuration.
- Inspect the Windows DNS cache.
- Clear the DNS resolver cache.

---

## Cybersecurity Perspective

The `ipconfig` command is frequently used by SOC Analysts, Incident Responders, and System Administrators to:

- Troubleshoot network connectivity.
- Verify network configuration.
- Investigate DNS-related issues.
- Detect suspicious DNS resolutions.
- Confirm DHCP configuration.
- Inspect local DNS cache during incident response.

---

## Challenge

- Identify the active network adapter.
- Find the system's IPv4 address.
- Identify the default gateway.
- Determine whether DHCP is enabled.
- View cached DNS records.
- Flush the DNS cache.

---

## Interview Questions

1. What is the purpose of the `ipconfig` command?
2. What information does `ipconfig /all` provide?
3. What is the function of `ipconfig /displaydns`?
4. Why is `ipconfig /flushdns` used?
5. What is DHCP?
6. What is the purpose of a default gateway?
7. What is DNS cache?

---

## Skills Gained

- Network Troubleshooting
- Windows Networking
- DNS Analysis
- DHCP Analysis
- Network Configuration Analysis
- Incident Response Basics

---

## Lab Summary

This lab demonstrated how to use the Windows `ipconfig` utility to examine system network configuration, inspect DNS cache entries, and clear the local DNS resolver cache. These commands are essential for network administration and cybersecurity troubleshooting.

---

