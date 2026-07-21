# PathPing Command Lab

## Objective

The objective of this lab is to understand how the **`pathping`** command works in Windows and how it combines the functionality of **`ping`** and **`tracert`**. This lab demonstrates how to trace the network path to a destination while measuring latency and detecting packet loss at each intermediate hop.

---

# Prerequisites

Before performing this lab, ensure the following:

- Windows 10 or Windows 11
- Command Prompt access
- Active Internet connection
- Basic understanding of IP addresses and network routing

---

# Theory

`pathping` is a Windows network diagnostic utility that combines the features of **`ping`** and **`tracert`**.

It first discovers the route to the destination like `tracert` and then sends multiple ICMP Echo Requests to every router along that route. After collecting the responses, it calculates packet loss and latency for each hop.

Unlike `ping`, which checks only the destination, and `tracert`, which only displays the path, `pathping` provides detailed statistics for every intermediate router.

Because it performs additional analysis, `pathping` usually takes several minutes to complete.

---

# Syntax

```cmd
pathping <hostname/IP>
```

Example:

```cmd
pathping google.com
```

---

# Commands Used

```cmd
pathping google.com
pathping github.com
pathping 8.8.8.8
pathping 1.1.1.1
```

---

# Steps Performed

1. Opened Command Prompt.
2. Executed `pathping google.com`.
3. Waited for the route discovery and statistics collection to complete.
4. Executed `pathping github.com`.
5. Executed `pathping 8.8.8.8`.
6. Executed `pathping 1.1.1.1`.
7. Recorded latency and packet loss for each hop.
8. Saved screenshots of all outputs.

---

# Expected Output

The command displays:

- Destination IP address
- Network hops
- Round-trip time (RTT)
- Packet loss percentage
- Packet forwarding statistics
- Intermediate routers between the source and destination

Example:

```text
Hop  RTT   Lost/Sent = Pct   Address
```

---

# Why PathPing is Important

`pathping` helps administrators identify exactly where packet loss occurs along a network path.

It is commonly used for:

- Troubleshooting slow networks
- Detecting packet loss
- Finding unstable routers
- Diagnosing ISP connectivity issues
- Verifying routing paths
- Network performance analysis

---

# Difference Between Ping, Tracert and PathPing

| Feature | Ping | Tracert | PathPing |
|----------|------|---------|-----------|
| Checks connectivity | ✅ | ❌ | ✅ |
| Shows route | ❌ | ✅ | ✅ |
| Measures latency | ✅ | ✅ | ✅ |
| Detects packet loss | Limited | ❌ | ✅ |
| Shows packet loss at each hop | ❌ | ❌ | ✅ |
| Time required | Fast | Medium | Slow |

---

# Cybersecurity Perspective

The `pathping` command is useful for cybersecurity professionals because it provides detailed information about network paths and packet loss.

It can be used to:

- Investigate network connectivity problems
- Detect unstable or overloaded routers
- Identify routing anomalies
- Troubleshoot VPN connectivity
- Verify secure communication paths
- Assist during incident response
- Support network reconnaissance during authorized security assessments

---

# Challenge

Use the `pathping` command to compare the routes and packet loss for:

- Google (`google.com`)
- GitHub (`github.com`)
- Google Public DNS (`8.8.8.8`)
- Cloudflare Public DNS (`1.1.1.1`)

Record:

- Number of hops
- Average latency
- Packet loss
- Any timeout messages
- Differences between the routes

---

# Interview Questions

### 1. What is the purpose of the `pathping` command?

**Answer:** It combines the features of `ping` and `tracert` to display the network route while measuring latency and packet loss at each hop.

---

### 2. How is `pathping` different from `tracert`?

**Answer:** `tracert` only shows the route to the destination, whereas `pathping` also calculates packet loss statistics for every hop.

---

### 3. Why does `pathping` take longer than `tracert`?

**Answer:** Because it sends multiple ICMP packets to every router on the route to calculate packet loss and latency.

---

### 4. What protocol does `pathping` use?

**Answer:** ICMP (Internet Control Message Protocol).

---

### 5. Can packet loss occur at intermediate hops without affecting connectivity?

**Answer:** Yes. Many routers limit or ignore ICMP responses while continuing to forward packets normally.

---

### 6. Why is packet loss analysis important?

**Answer:** It helps identify faulty routers, network congestion, unstable links, or connectivity issues.

---

### 7. Which command is better for identifying packet loss?

**Answer:** `pathping`, because it calculates packet loss statistics for every hop.

---

### 8. Why do some routers show "Request timed out"?

**Answer:** They may block or deprioritize ICMP responses due to firewall rules, security policies, or rate limiting.

---

# Skills Gained

After completing this lab, I learned how to:

- Use the `pathping` command
- Analyze packet loss
- Measure network latency
- Interpret routing paths
- Identify problematic network hops
- Troubleshoot connectivity issues
- Compare network routes
- Perform basic network diagnostics

---

# Lab Summary

In this lab, I used the Windows `pathping` command to analyze network routes to multiple destinations. The command helped identify each hop between the source and destination while measuring latency and packet loss. This lab provided practical experience in diagnosing network performance and understanding how data travels across different networks.

