# Subnetting Cheatsheet

## What is Subnetting?

Subnetting divides a network into smaller networks.

Benefits:

- Better performance
- Better security
- Efficient IP utilization

---

## CIDR Quick Reference

| CIDR | Subnet Mask |
|---------|---------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |
| /30 | 255.255.255.252 |

---

## Hosts Per Subnet

| CIDR | Hosts |
|---------|---------|
| /24 | 254 |
| /25 | 126 |
| /26 | 62 |
| /27 | 30 |
| /28 | 14 |
| /29 | 6 |
| /30 | 2 |

Formula:

2^HostBits - 2

---

## Address Types

### Network Address

First address in subnet.

### Broadcast Address

Last address in subnet.

### Usable Hosts

Addresses between network and broadcast.

---

## Example

Network:

192.168.1.0/24

Network Address:

192.168.1.0

Broadcast:

192.168.1.255

Usable:

192.168.1.1 – 192.168.1.254

Hosts:

254

---

## Common Interview Question

How many hosts in /27?

2^5 - 2

30 Hosts
