# Network Topologies

## Definition

A network topology is the physical or logical layout of how devices are connected and communicate in a network.

---

## Why

Network topology determines:

- How devices communicate
- Network performance
- Scalability
- Fault tolerance
- Security

Choosing the right topology improves network efficiency and reliability.

---

## Working

A topology defines the path through which data travels between devices.

Different topologies connect devices in different ways:

- One common cable
- Central device
- Circular connection
- Multiple paths
- Hierarchical structure

---

## Real-World Example

- Home Wi-Fi networks typically use **Star Topology**.
- Large ISPs and data centers often use **Mesh Topology**.
- Schools and offices commonly use **Tree Topology**.

---

## Cybersecurity Perspective

Topology affects both security and attack impact.

- **Bus** – Easy traffic interception because all devices share the same communication medium.
- **Star** – The central device becomes a critical target.
- **Ring** – Failure or attack on one node can affect communication.
- **Mesh** – More resilient against attacks and network failures.
- **Tree** – Requires security at multiple levels.
- **Hybrid** – Security depends on the combined topologies being used.

---

# Common Types

## Bus Topology

### Definition

All devices share a single communication cable.

### Working

Data travels across the shared cable, and every connected device receives it.

### Real-World Example

Early Ethernet networks.

### Cybersecurity Perspective

Easy packet sniffing because all devices share the same communication medium.

---

## Star Topology

### Definition

All devices connect to a central switch or hub.

### Working

Data passes through the central device before reaching its destination.

### Real-World Example

Home Wi-Fi and office networks.

### Cybersecurity Perspective

The switch or router becomes a critical target. If compromised, the entire network can be monitored or disrupted.

---

## Ring Topology

### Definition

Each device connects to two neighboring devices, forming a circular network.

### Working

Data travels around the ring until it reaches the destination.

### Real-World Example

Token Ring networks (historically).

### Cybersecurity Perspective

Failure or attack on one node can interrupt communication across the network.

---

## Mesh Topology

### Definition

Devices are connected through multiple communication paths.

### Working

If one path fails, data automatically uses another available path.

### Real-World Example

Internet backbone networks and modern data centers.

### Cybersecurity Perspective

Highly resilient against failures, link disruptions, and many network outages.

---

## Tree Topology

### Definition

A hierarchical topology that combines multiple Star networks.

### Working

Devices connect to switches, which connect to higher-level switches.

### Real-World Example

University campuses and large corporate networks.

### Cybersecurity Perspective

Higher-level switches become important targets because they control communication for large parts of the network.

---

## Hybrid Topology

### Definition

A combination of two or more different network topologies.

### Working

Different sections of the network use different topologies based on requirements.

### Real-World Example

Modern enterprises combining Star, Mesh, and Tree topologies.

### Cybersecurity Perspective

Provides flexibility but increases the complexity of network security and management.

---

## Interview Questions

### Q1. Which topology is most commonly used today?

**Answer:** Star Topology

---

### Q2. Which topology uses a single backbone cable?

**Answer:** Bus Topology

---

### Q3. Which topology provides the highest fault tolerance?

**Answer:** Mesh Topology

---

### Q4. Which topology is commonly used in home and office networks?

**Answer:** Star Topology

---

### Q5. Which topology connects devices in a circular manner?

**Answer:** Ring Topology

---

### Q6. Which topology combines multiple topologies?

**Answer:** Hybrid Topology

---

## Key Takeaways

- **Bus** = Single communication cable.
- **Star** = Central switch or hub.
- **Ring** = Circular communication path.
- **Mesh** = Multiple communication paths.
- **Tree** = Hierarchical structure.
- **Hybrid** = Combination of multiple topologies.

---

## Memory Trick

```text
Bus    = One Road
Star   = One Center
Ring   = Circle
Mesh   = Multiple Paths
Tree   = Hierarchy
Hybrid = Mix of Everything
```
