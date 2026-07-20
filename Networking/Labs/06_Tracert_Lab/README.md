# Tracert Lab

## Objective

The objective of this lab is to understand how data packets travel across a network using the `tracert` utility. This lab demonstrates how to trace the route between a source and a destination, identify intermediate routers (hops), measure network latency, and troubleshoot routing issues from both networking and cybersecurity perspectives.

---

## Prerequisites

- Windows 10/11
- Command Prompt (CMD)
- Active Internet Connection
- Basic understanding of IP addresses and routing

---

## Theory

`tracert` (Trace Route) is a Windows command-line utility used to display the path that packets take from a source computer to a destination host. It identifies each router (hop) along the route and measures the time taken for packets to reach every hop.

The command works by sending Internet Control Message Protocol (ICMP) Echo Request packets with gradually increasing Time-To-Live (TTL) values. Each router decreases the TTL by one before forwarding the packet. When the TTL reaches zero, the router discards the packet and sends back an ICMP "Time Exceeded" message. By increasing the TTL one step at a time, `tracert` discovers every router along the path until the destination is reached.

Each line of the output represents one network hop and includes:

- Hop number
- Round-trip times (RTT)
- Hostname or IP address of the router

This information helps identify where delays or connectivity problems occur.

---

## Commands Used

```cmd
tracert google.com

tracert github.com

tracert 8.8.8.8

tracert 1.1.1.1

tracert -d google.com
```

---

## Steps Performed

1. Opened Command Prompt.
2. Traced the route to `google.com`.
3. Traced the route to `github.com`.
4. Traced the route to Google's Public DNS server (`8.8.8.8`).
5. Traced the route to Cloudflare's Public DNS server (`1.1.1.1`).
6. Performed a trace without resolving hostnames using the `-d` option.
7. Observed the number of hops, latency values, and routing information for each destination.

---

## Expected Output

- Display of every network hop between the local computer and the destination.
- Round-trip time (RTT) for each hop.
- Hostnames and IP addresses of intermediate routers.
- Total number of hops required to reach the destination.
- Faster output when using the `-d` option because DNS lookups are skipped.

---

## Learning Outcome

After completing this lab, I was able to:

- Understand how packets travel through different routers.
- Interpret hop numbers and latency values.
- Identify routing paths between networks.
- Use `tracert` to troubleshoot connectivity issues.
- Understand the purpose of the Time-To-Live (TTL) field.
- Compare hostname resolution with direct IP tracing.

---

## Cybersecurity Perspective

`tracert` is an important reconnaissance and troubleshooting tool in cybersecurity. Security professionals use it to identify network paths, investigate routing anomalies, detect unexpected intermediate systems, verify connectivity to remote servers, and analyze network latency during incident response. It can also assist in identifying routing problems, ISP issues, and possible network filtering devices.

Although `tracert` provides valuable routing information, some routers intentionally block or ignore ICMP packets for security reasons. As a result, some hops may display timeouts (`* * *`) even though traffic continues successfully to the destination.

---

## Challenge

During the lab, some intermediate routers may not respond to ICMP requests due to firewall rules or security policies. Understanding that these timeouts do not always indicate a network failure is important while interpreting traceroute results.

---

## Interview Questions

1. What is the purpose of the `tracert` command?
2. How does `tracert` work?
3. What is Time-To-Live (TTL)?
4. Why are there three response times for each hop?
5. What does `* * * Request timed out` mean?
6. What is the difference between `ping` and `tracert`?
7. What is the purpose of the `-d` option?
8. Why do some routers not respond to traceroute requests?
9. How can `tracert` help troubleshoot network issues?
10. How is `tracert` useful in cybersecurity investigations?

---

## Skills Gained

- Network Path Analysis
- Route Tracing
- Network Troubleshooting
- Latency Analysis
- ICMP Fundamentals
- Windows Command Line
- Routing Concepts
- Cybersecurity Reconnaissance

---

## Lab Summary

This lab demonstrated how to use the `tracert` utility to trace the path of network packets between a source and multiple destinations. By analyzing each hop and its response time, routing paths and network delays were identified. The exercises provided practical experience in network troubleshooting and reinforced the importance of routing analysis in cybersecurity and system administration.
