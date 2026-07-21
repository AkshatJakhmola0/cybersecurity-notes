# Observations

## Commands Executed

The following PathPing commands were executed during this lab:

- `pathping google.com`
- `pathping github.com`
- `pathping 8.8.8.8`
- `pathping 1.1.1.1`

---

## Route to Google

- Successfully traced the route to **google.com** using the `pathping` command.
- The destination was reached through **8 network hops**.
- The local router showed **1% packet loss**, which is considered acceptable.
- The ISP private router displayed **100% packet loss**, but subsequent hops responded normally, indicating that the router filters ICMP probes while continuing to forward packets.
- Google's backbone routers showed **0% packet loss**.
- The destination maintained low latency ranging from **4 ms to 17 ms**.
- The overall network path was stable with no end-to-end packet loss.

---

## Route to GitHub

- Successfully traced the route to **github.com** using the `pathping` command.
- The route passed through the local router, ISP network, an Internet Exchange, and Microsoft's backbone network.
- The local router responded with **0% packet loss**.
- The ISP private router displayed **100% packet loss**, but subsequent hops responded normally, indicating ICMP filtering rather than a forwarding failure.
- Microsoft backbone routers showed stable connectivity with latency ranging from **7 ms to 27 ms**.
- Some backbone routers did not return ICMP statistics, resulting in **100% values** in the PathPing report.
- The overall connection remained stable with no evidence of end-to-end packet loss.

---

## Route to Google Public DNS

- Successfully traced the route to **Google Public DNS (8.8.8.8)**.
- The destination was reached through **7 network hops**.
- The home router responded with **0% packet loss**.
- The ISP private router displayed **100% packet loss**, but all subsequent hops responded normally, indicating ICMP filtering.
- Google's backbone routers showed **0% packet loss** and stable latency.
- The destination (**dns.google**) responded with **0% packet loss** and approximately **4 ms** latency.
- The overall network path was healthy and stable.

---

## Route to Cloudflare Public DNS

- Executed `pathping 1.1.1.1` to analyze the route to Cloudflare Public DNS.
- The local computer, home router, ISP private router, and ISP public router were identified successfully.
- The home router showed **0% packet loss** with approximately **2 ms** latency.
- The ISP private router displayed **100% packet loss**, but the following ISP public router responded normally, indicating ICMP filtering rather than forwarding failure.
- The ISP public router showed **0% packet loss** with approximately **6 ms** latency.
- Routers beyond the ISP network did not return PathPing statistics.
- The destination did not appear in the final statistics table, most likely because intermediate routers or the destination filtered ICMP probes.
- Previous `tracert` results confirmed that **1.1.1.1** was reachable despite the incomplete PathPing statistics.

---

## Packet Loss Analysis

During the lab, **100% packet loss** was observed at some intermediate routers.

This did **not** indicate an actual network failure because:

- Subsequent hops continued to respond successfully.
- The destination remained reachable in previous tests.
- Many enterprise and ISP routers intentionally ignore or rate-limit ICMP packets used by diagnostic tools.

Therefore, packet loss reported at an intermediate hop should always be interpreted alongside the responses from later hops.

---

## Latency Analysis

- The home router consistently responded within **1–20 ms**.
- ISP routers maintained low latency throughout the tests.
- Google's backbone provided consistently low response times.
- Microsoft's backbone maintained stable latency despite a longer route.
- No significant latency spikes or routing instability were observed.

---

## Security Observations

The `pathping` command provides valuable information for cybersecurity and network administration by:

- Identifying packet loss across network paths.
- Detecting unstable routers and congested links.
- Verifying ISP routing behavior.
- Assisting in troubleshooting VPN and internet connectivity issues.
- Supporting incident response and network diagnostics.
- Helping distinguish between ICMP filtering and genuine connectivity problems.

---

## Learning Outcome

After completing this lab, I gained practical experience in:

- Using the Windows `pathping` command.
- Measuring packet loss at each network hop.
- Analyzing latency across network routes.
- Understanding ICMP filtering behavior.
- Differentiating between packet loss and ICMP response suppression.
- Comparing routes to multiple public services.
- Troubleshooting network connectivity using advanced diagnostic tools.
