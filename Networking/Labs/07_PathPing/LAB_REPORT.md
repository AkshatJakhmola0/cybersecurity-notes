# Lab Report

## Experiment Title

**Network Path and Packet Loss Analysis Using the `pathping` Command in Windows**

---

## Objective

To understand the working of the Windows `pathping` command by tracing the network path to different destinations, measuring latency, identifying packet loss at each hop, and analyzing network performance.

---

## Tools Used

- Windows 11 Command Prompt
- `pathping` Command
- Internet Connection

---

## Commands Executed

```cmd
pathping google.com
pathping github.com
pathping 8.8.8.8
pathping 1.1.1.1
```

---

## Procedure

1. Opened Command Prompt on the Windows system.
2. Executed `pathping google.com` and waited for route discovery and statistics collection to complete.
3. Executed `pathping github.com` to analyze the route to GitHub.
4. Executed `pathping 8.8.8.8` to analyze the route to Google Public DNS.
5. Executed `pathping 1.1.1.1` to analyze the route to Cloudflare Public DNS.
6. Observed the route, latency, packet loss, and hop information for each command.
7. Recorded the results and compared the network paths.

---

## Results

- Successfully analyzed the routes to Google, GitHub, Google Public DNS, and Cloudflare Public DNS.
- Identified the local router, ISP routers, Internet Exchange, and backbone network devices.
- Observed that several intermediate routers displayed **100% packet loss**, but subsequent hops remained reachable, indicating ICMP filtering rather than actual packet forwarding failures.
- Google's network demonstrated low latency and stable connectivity.
- Microsoft's backbone network showed stable performance with no end-to-end packet loss.
- The Cloudflare PathPing analysis was incomplete because some intermediate devices did not respond to ICMP probes, although previous Tracert results confirmed that the destination was reachable.

---

## Conclusion

The `pathping` command is a powerful Windows network diagnostic utility that combines the functionality of `ping` and `tracert`. It helps identify network routes, measure latency, and detect packet loss at each hop. This lab demonstrated that packet loss reported at intermediate routers does not always indicate network failure, as many routers intentionally filter or limit ICMP responses. Understanding this behavior is essential for accurate network troubleshooting and cybersecurity investigations.

---

## Skills Gained

- Using the `pathping` command in Windows
- Understanding packet routing across networks
- Measuring latency and packet loss
- Interpreting PathPing statistics
- Identifying ISP and backbone network paths
- Distinguishing ICMP filtering from actual network failures
- Troubleshooting connectivity issues
- Applying network diagnostic techniques in cybersecurity
