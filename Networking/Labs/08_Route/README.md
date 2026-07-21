# Route Command Lab

## Objective

The objective of this lab is to understand how the **`route`** command works in Windows and how it is used to view, analyze, and manage the system's routing table. This lab demonstrates how Windows decides where to send network packets and how routing information is stored and interpreted.

---

# Prerequisites

Before performing this lab, ensure the following:

- Windows 10 or Windows 11
- Command Prompt access
- Active network connection
- Basic understanding of IP addressing and subnetting

---

# Theory

The **`route`** command is a Windows networking utility used to display and manage the IP routing table.

A routing table contains information that helps the operating system determine the best path for forwarding network packets. Every packet sent from a computer is compared against this table to decide which gateway or network interface should be used.

Windows automatically creates routing table entries when network interfaces become active, but administrators can also add, modify, or delete routes manually.

The `route` command is an essential tool for network administrators, system engineers, and cybersecurity professionals when troubleshooting connectivity, routing problems, VPN configurations, and multi-network environments.

---

# Syntax

```cmd
route [command] [destination]
```

Common commands:

```cmd
route print
route print -4
route print -6
route add
route delete
route change
```

---

# Commands Used

```cmd
route print
route print -4
route print -6
route /?
```

---

# Commands for Learning (Not Executed)

The following commands modify the routing table. They are included for learning purposes but were **not executed** in this lab.

```cmd
route add
route delete
route change
```

Examples:

```cmd
route add 192.168.10.0 mask 255.255.255.0 192.168.1.1

route delete 192.168.10.0

route change 192.168.10.0 mask 255.255.255.0 192.168.1.254
```

---

# Steps Performed

1. Opened Command Prompt.
2. Displayed the complete routing table using `route print`.
3. Displayed only the IPv4 routing table using `route print -4`.
4. Displayed only the IPv6 routing table using `route print -6`.
5. Viewed all available Route command options using `route /?`.
6. Analyzed the routing table entries.
7. Identified destination networks, gateways, interfaces, and metrics.

---

# Expected Output

The routing table contains information such as:

- Network Destination
- Netmask
- Gateway
- Interface
- Metric

Example:

```text
Network Destination    Netmask          Gateway         Interface      Metric
0.0.0.0               0.0.0.0          192.168.0.1     192.168.0.104      25
```

---

# Understanding the Routing Table

## 1. Network Destination

The destination network or host to which packets are sent.

Example:

```text
192.168.0.0
```

---

## 2. Netmask

Defines which portion of the IP address belongs to the network.

Example:

```text
255.255.255.0
```

---

## 3. Gateway

The next router through which packets are forwarded.

Example:

```text
192.168.0.1
```

---

## 4. Interface

The local network adapter used to send packets.

Example:

```text
192.168.0.104
```

---

## 5. Metric

A cost value used to choose the best route.

Lower metric = Higher priority.

---

# Important Route Entries

## Default Route

```text
0.0.0.0
```

Used when no more specific route exists.

---

## Loopback Route

```text
127.0.0.0
```

Used for communication within the local computer.

---

## Local Network Route

Represents devices connected to the same local network.

---

## Broadcast Route

Used for broadcasting packets within the local subnet.

---

## Multicast Route

Used for multicast communication.

---

# Route Commands Explained

## route print

Displays the complete routing table.

---

## route print -4

Displays only IPv4 routes.

---

## route print -6

Displays only IPv6 routes.

---

## route add

Adds a new static route.

Example:

```cmd
route add 10.10.10.0 mask 255.255.255.0 192.168.0.1
```

---

## route delete

Deletes an existing route.

Example:

```cmd
route delete 10.10.10.0
```

---

## route change

Modifies an existing route.

Example:

```cmd
route change 10.10.10.0 mask 255.255.255.0 192.168.0.254
```

---

# Why the Route Command is Important

The `route` command is commonly used for:

- Viewing the routing table
- Troubleshooting routing issues
- Configuring static routes
- Managing multiple network interfaces
- VPN troubleshooting
- Network segmentation
- Enterprise network administration

---

# Cybersecurity Perspective

The `route` command is valuable for cybersecurity because it helps professionals understand how traffic flows through a network.

It can be used to:

- Detect suspicious routing changes
- Verify VPN routing
- Analyze traffic paths
- Troubleshoot connectivity issues
- Investigate network attacks
- Validate secure network configurations
- Assist during incident response

---

# Challenge

Using your routing table, identify:

- Default Gateway
- Local IP Address
- Interface IP
- Default Route
- Loopback Route
- Number of IPv4 Routes
- Number of IPv6 Routes
- Route with the lowest metric

---

# Interview Questions

### 1. What is the purpose of the `route` command?

**Answer:** It is used to display and manage the Windows IP routing table.

---

### 2. What is a routing table?

**Answer:** A routing table is a database containing network routes that the operating system uses to forward packets.

---

### 3. What is the default route?

**Answer:** The default route (`0.0.0.0/0`) is used when no specific route matches the destination address.

---

### 4. What is a gateway?

**Answer:** A gateway is the next-hop router used to forward packets toward another network.

---

### 5. What is the purpose of the metric?

**Answer:** The metric represents the cost of a route. Windows prefers the route with the lowest metric.

---

### 6. What is the difference between static and dynamic routes?

**Answer:** Static routes are manually configured, while dynamic routes are learned automatically through routing protocols or the operating system.

---

### 7. Why should you be careful with `route add` and `route delete`?

**Answer:** Incorrect routing entries can interrupt network connectivity or make systems unreachable.

---

### 8. How does Windows choose between multiple routes?

**Answer:** Windows selects the most specific matching route first. If multiple routes match equally, it chooses the one with the lowest metric.

---

# Skills Gained

After completing this lab, I learned how to:

- View the Windows routing table
- Understand routing table entries
- Identify gateways and interfaces
- Interpret routing metrics
- Differentiate IPv4 and IPv6 routes
- Understand static and dynamic routing
- Analyze packet forwarding decisions
- Use routing information for network troubleshooting

---

# Lab Summary

In this lab, I explored the Windows `route` command and learned how the operating system uses the routing table to determine the best path for network traffic. I examined IPv4 and IPv6 routing entries, understood the purpose of gateways, interfaces, and metrics, and learned how static routes can be added, modified, or removed. This lab provided practical knowledge of routing concepts that are widely used in networking, system administration, and cybersecurity.
