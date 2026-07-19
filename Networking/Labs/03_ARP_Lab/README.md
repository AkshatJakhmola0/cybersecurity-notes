# Lab 03 - Address Resolution Protocol (ARP)

## Objective

To understand how the Address Resolution Protocol (ARP) works and how Windows maintains the ARP cache for communication within a Local Area Network (LAN).

---

## Prerequisites

- Windows Operating System
- Command Prompt
- Active Network Connection
- Basic knowledge of IP and MAC Addresses

---

## Theory

The **Address Resolution Protocol (ARP)** is used to map an **IPv4 Address** to a **MAC Address** within the same local network.

When a device wants to communicate with another device on the LAN, it knows the destination IP address but needs the corresponding MAC address to send Ethernet frames. ARP performs this mapping automatically and stores the result in the **ARP Cache** to avoid repeated broadcasts.

---

## Commands Used

```cmd
arp -a
arp -a -v
arp -d *
arp -a
ping 192.168.0.1
arp -a
```

---

## Steps Performed

1. Viewed the current ARP cache.
2. Displayed the ARP cache with verbose information.
3. Cleared all dynamic ARP entries.
4. Verified the ARP cache after deletion.
5. Pinged the default gateway to generate a new ARP request.
6. Verified that the ARP cache was rebuilt automatically.

---

## Key Concepts

### ARP Cache

The ARP Cache stores recently resolved **IP Address → MAC Address** mappings to improve communication efficiency and reduce unnecessary network broadcasts.

---

### Dynamic ARP Entries

- Automatically created by Windows.
- Learned through ARP communication.
- Removed automatically after a timeout.

---

### Static ARP Entries

- Added manually by an administrator.
- Do not expire automatically.
- Commonly used in secure or controlled environments.

---

### ARP Request

When the MAC address of a destination device is unknown, the sender broadcasts an ARP Request asking:

> "Who has this IP address?"

---

### ARP Reply

The device owning the requested IP responds with its MAC address, allowing communication to begin.

---

## Cybersecurity Perspective

ARP operates without authentication, making it vulnerable to attacks such as:

- ARP Spoofing
- ARP Poisoning
- Man-in-the-Middle (MITM)

Understanding ARP is essential for identifying suspicious network activity and investigating LAN-based attacks.

---

## Learning Outcome

After completing this lab, I will be able to:

- View the ARP cache.
- Understand IP-to-MAC address mapping.
- Differentiate between Dynamic and Static ARP entries.
- Delete ARP cache entries.
- Observe how Windows rebuilds the ARP cache.
- Understand common ARP-related attacks.

---

## Interview Questions

1. What is ARP?
2. Why is ARP required?
3. What is an ARP Cache?
4. What is the difference between Dynamic and Static ARP entries?
5. What does the `arp -a` command display?
6. What happens after deleting the ARP cache?
7. How does ARP Spoofing work?
8. Why is ARP vulnerable to attacks?

---

## Skills Gained

- Windows Networking
- ARP Cache Analysis
- MAC Address Identification
- LAN Communication
- Basic Network Troubleshooting
- Cybersecurity Fundamentals

---

## Lab Summary

This lab demonstrates how ARP resolves IPv4 addresses to MAC addresses, how Windows stores ARP entries, and how the ARP cache is rebuilt after deletion. It also introduces ARP-related security risks such as ARP Spoofing and Man-in-the-Middle attacks.
