# Lab Report

## Experiment Title

**Trace Route Analysis Using the `tracert` Command in Windows**

---

## Objective

To understand how the `tracert` command traces the path taken by packets across a network, identifies intermediate routers (hops), measures latency, and assists in network troubleshooting.

---

## Tools Used

- Windows 11 Command Prompt
- `tracert` Command
- Internet Connection

---

## Commands Executed

```cmd
tracert google.com
tracert github.com
tracert 8.8.8.8
tracert 1.1.1.1
tracert -d google.com
```

---

## Procedure

1. Opened Command Prompt with normal user privileges.
2. Executed `tracert google.com` to trace the route to Google's web server.
3. Executed `tracert github.com` to analyze the network path to GitHub.
4. Executed `tracert 8.8.8.8` to trace the route to Google Public DNS.
5. Executed `tracert 1.1.1.1` to trace the route to Cloudflare Public DNS.
6. Executed `tracert -d google.com` to perform a trace without DNS hostname resolution.
7. Observed the number of hops, latency, and timeout messages.
8. Recorded and analyzed the outputs.

---

## Results

- Successfully traced routes to Google, GitHub, Google Public DNS, and Cloudflare Public DNS.
- Observed that packets passed through the local router, ISP network, and public backbone networks before reaching their destinations.
- Identified latency values for each hop.
- Observed that several intermediate routers did not respond to ICMP traceroute probes but still forwarded packets successfully.
- Verified that the `-d` option displayed only IP addresses by skipping hostname resolution, resulting in a cleaner and faster trace.

---

## Conclusion

The `tracert` command is an effective network diagnostic tool used to determine the route packets take from a source to a destination. It helps identify network hops, measure latency, detect routing issues, and troubleshoot connectivity problems. This lab demonstrated how traceroute works across different destinations and highlighted that timeout messages from intermediate routers do not necessarily indicate network failures.

---

## Skills Gained

- Using the `tracert` command in Windows
- Understanding packet routing across networks
- Identifying network hops and intermediate routers
- Measuring network latency
- Interpreting traceroute output
- Understanding ICMP timeout behavior
- Using the `-d` option for faster network diagnostics
- Applying traceroute in network troubleshooting and cybersecurity investigations
