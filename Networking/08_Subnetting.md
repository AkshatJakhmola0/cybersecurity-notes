# Subnetting

## Definition

Subnetting is the process of dividing a large network into smaller networks called **subnets**.

---

## Why

Subnetting helps to:

- Better manage networks
- Reduce broadcast traffic
- Improve security
- Efficiently use IP addresses
- Improve network performance

---

## Working

A network is divided using a **Subnet Mask**.

### Example

```text
192.168.1.0/24
```

Can be divided into:

```text
192.168.1.0/25

192.168.1.128/25
```

One large network is divided into two smaller subnets.

---

## Real-World Example

A company has three departments:

- HR
- Finance
- IT

Instead of placing every department on one large network, each department is assigned its own subnet.

---

## Cybersecurity Perspective

Subnetting improves security by:

- Limiting attacker movement between departments
- Improving network segmentation
- Reducing the attack surface
- Making network monitoring easier

---

# Subnet Mask

## Definition

A Subnet Mask identifies which part of an IP address represents the **Network ID** and which part represents the **Host ID**.

### Common Subnet Masks

| CIDR | Subnet Mask |
|------|-------------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |

---

# CIDR Notation

## Definition

CIDR (Classless Inter-Domain Routing) is a shorter way to represent a subnet mask.

### Examples

| CIDR | Subnet Mask |
|------|-------------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |

---

# Network Address

## Definition

The **first address** of a subnet.

### Purpose

Identifies the subnet itself.

### Example

```text
Network: 192.168.1.0/24

Network Address: 192.168.1.0
```

---

# Broadcast Address

## Definition

The **last address** of a subnet.

### Purpose

Used to send data to every device within the subnet.

### Example

```text
Network: 192.168.1.0/24

Broadcast Address: 192.168.1.255
```

---

# Number of Hosts

## Formula

```text
Usable Hosts = 2^(Host Bits) - 2
```

> The **-2** represents the **Network Address** and **Broadcast Address**, which cannot be assigned to devices.

### Common Values

| CIDR | Host Bits | Usable Hosts |
|------|----------:|-------------:|
| /24 | 8 | 254 |
| /25 | 7 | 126 |
| /26 | 6 | 62 |
| /27 | 5 | 30 |
| /28 | 4 | 14 |

---

# Practical Examples

## Example 1

```text
Network:           192.168.1.0/24

Subnet Mask:       255.255.255.0

Network Address:   192.168.1.0

Broadcast Address: 192.168.1.255

Usable Hosts:      254
```

---

## Example 2

```text
Network:           192.168.1.0/26

Subnet Mask:       255.255.255.192

Network Address:   192.168.1.0

Broadcast Address: 192.168.1.63

Usable Hosts:      62

Host Range:
192.168.1.1 – 192.168.1.62
```

---

## Interview Questions

### Q1. What is subnetting?

**Answer:** Dividing a large network into smaller subnets.

---

### Q2. Why is subnetting used?

**Answer:** Better management, improved security, reduced broadcast traffic, and efficient IP utilization.

---

### Q3. What is CIDR?

**Answer:** A shorthand notation used to represent a subnet mask.

---

### Q4. How many usable hosts are available in a /24 network?

**Answer:** 254

---

### Q5. What is the subnet mask of /26?

**Answer:** 255.255.255.192

---

### Q6. What is the formula for usable hosts?

**Answer:**

```text
2^(Host Bits) - 2
```

---

### Q7. What are the two reserved addresses in every subnet?

**Answer:**

- Network Address
- Broadcast Address

---

## Key Takeaways

- Subnetting divides a large network into smaller subnets.
- A Subnet Mask separates the Network ID and Host ID.
- CIDR is the shorthand notation for subnet masks.
- The first address is the Network Address.
- The last address is the Broadcast Address.
- Usable Hosts = 2^(Host Bits) - 2.
- Subnetting improves performance, scalability, and security.

---

## Memory Tricks

### CIDR → Subnet Mask

```text
/24 = 255.255.255.0

/25 = 255.255.255.128

/26 = 255.255.255.192

/27 = 255.255.255.224

/28 = 255.255.255.240
```

---

### Host Formula

```text
2^(Host Bits) - 2
```

---

### Remember

```text
First Address  = Network Address

Last Address   = Broadcast Address

Everything in between = Usable Hosts
```

---

### Quick Rule

```text
More CIDR Bits

(/24 → /25 → /26)

        ↓

More Subnets

        ↓

Fewer Hosts per Subnet
```
