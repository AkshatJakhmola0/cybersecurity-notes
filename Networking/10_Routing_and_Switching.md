# Routing and Switching

## Definition

Routing is the process of forwarding data between different networks using IP addresses.

Switching is the process of forwarding data within the same network using MAC addresses.

---

## Why

- Switching allows devices in the same LAN to communicate.
- Routing allows different networks to communicate.
- Both are required for Internet access.

---

## Working

### Same Network

```text
PC
 │
 ▼
Switch
 │
 ▼
Printer
```

### Different Network

```text
PC
 │
 ▼
Router
 │
 ▼
Internet
 │
 ▼
Server
```

---

## Real-World Example

### Switching

A laptop sends a file to a printer in the same office network.

### Routing

A laptop accesses Google through a router and the Internet.

---

## Cybersecurity Perspective

- ARP Spoofing targets switching.
- VLAN Hopping bypasses network segmentation.
- Route Manipulation can redirect traffic.
- Attackers often move laterally inside switched networks.
- Security teams monitor routing and switching behavior to detect suspicious activity.

---

# Common Concepts

## What is Routing?

### Definition

Routing is the process of sending packets between different networks using IP addresses.

### Device Used

- Router

### Example

```text
192.168.1.10 → Google Server
```

### Cybersecurity

Route manipulation can redirect traffic to malicious destinations.

---

## What is Switching?

### Definition

Switching is the process of sending frames within the same network using MAC addresses.

### Device Used

- Switch

### Example

```text
Laptop → Switch → Printer
```

### Cybersecurity

Attackers may perform MAC Flooding attacks against switches.

---

## MAC Address Table

### Definition

A table maintained by a switch that stores MAC addresses and the ports where they are located.

### Example

| MAC Address | Port |
|-------------|------|
| AA-AA-AA-AA | 1 |
| BB-BB-BB-BB | 2 |

### Purpose

Allows the switch to forward data only to the intended device.

### Cybersecurity

MAC Flooding can overflow the table and force the switch to broadcast traffic.

---

## Routing Table

### Definition

A table maintained by a router that contains network destinations and the best path to reach them.

### Example

| Network | Next Hop |
|---------|----------|
| 192.168.1.0 | Direct |
| 0.0.0.0 | Gateway |

### Purpose

Helps routers determine where packets should be sent.

### Cybersecurity

Attackers may alter routes to intercept or redirect traffic.

---

## Collision Domain

### Definition

A part of the network where multiple devices compete to send data and collisions may occur.

### Example

Hub-based networks.

### Key Point

Each switch port creates a separate collision domain.

### Cybersecurity

Small collision domains improve performance and reduce unnecessary traffic exposure.

---

## Broadcast Domain

### Definition

A group of devices that receive the same broadcast message.

### Example

All devices in the same VLAN.

### Key Point

Routers separate broadcast domains.

### Cybersecurity

Large broadcast domains increase attack exposure and unnecessary network traffic.

---

## ARP

### Definition

Address Resolution Protocol maps an IP address to a MAC address.

### Example

```text
192.168.1.10 → AA:BB:CC:DD:EE:FF
```

### How It Fits Into Switching

Before a switch can deliver data, the sender must know the destination MAC address.

ARP provides that MAC address.

### Cybersecurity

ARP Spoofing can trick devices into sending traffic to an attacker.

---

## Default Gateway

### Definition

The router used to reach devices outside the local network.

### Example

```text
192.168.1.1
```

### How It Fits Into Routing

When a device wants to communicate outside its local network, it sends the traffic to the default gateway.

### Cybersecurity

A compromised default gateway can monitor, redirect, or manipulate outgoing traffic.

---

## Interview Questions

### Q1. What is the difference between routing and switching?

**Answer:** Routing uses IP addresses to communicate between different networks, while switching uses MAC addresses to communicate within the same network.

---

### Q2. Which device maintains a MAC Address Table?

**Answer:** Switch

---

### Q3. Which device maintains a Routing Table?

**Answer:** Router

---

### Q4. What does ARP do?

**Answer:** Maps an IP address to a MAC address.

---

### Q5. What is the purpose of a default gateway?

**Answer:** To forward traffic to other networks.

---

### Q6. Which device separates broadcast domains?

**Answer:** Router

---

### Q7. What attack targets ARP?

**Answer:** ARP Spoofing

---

### Q8. What attack targets VLANs?

**Answer:** VLAN Hopping

---

## Key Takeaways

- Routing = Between Networks = IP Address = Router
- Switching = Within Network = MAC Address = Switch
- MAC Address Table belongs to a Switch.
- Routing Table belongs to a Router.
- ARP = IP Address → MAC Address.
- Default Gateway = Exit point from the local network.
- Routers separate Broadcast Domains.
- Switches separate Collision Domains.
- VLANs improve security through network segmentation.

---

## Memory Tricks

```text
Switch = MAC

Router = IP

ARP = IP → MAC

Gateway = Exit Door

MAC Table = Switch

Routing Table = Router

Collision Domain = Switch Port

Broadcast Domain = VLAN
```

### Quick Exam Rule

```text
Same Network      = Switch

Different Network = Router

Need MAC?         = ARP

Need Internet?    = Default Gateway
```
