# Observations

## Commands Executed

The following trace route commands were performed during this lab:

- `tracert google.com`
- `tracert github.com`
- `tracert 8.8.8.8`
- `tracert 1.1.1.1`
- `tracert -d google.com`

---

## Route to Google

- Successfully traced the route to **google.com**.
- The destination was reached in **15 hops**.
- The first hop was the local router (`192.168.0.1`).
- The second hop was a private ISP address (`172.16.128.1`).
- Several intermediate routers belonged to Google's network.
- Multiple hops displayed **Request timed out**, but the destination remained reachable.
- The destination responded successfully, confirming that the network path was operational.

---

## Route to GitHub

- Successfully traced the route to **github.com**.
- The destination was reached in **16 hops**.
- The route passed through the local router, ISP network, and Microsoft's backbone network.
- Intermediate routers included hostnames associated with Microsoft (`msn.net`).
- Some routers did not respond to ICMP traceroute probes, resulting in request timeouts.
- Stable latency was observed at the destination.

---

## Route to Google Public DNS

- Successfully traced the route to **8.8.8.8 (dns.google)**.
- The destination was reached in **7 hops**.
- The trace passed through the local router, ISP network, and Google infrastructure.
- One intermediate hop did not respond, but the destination remained reachable.
- Low and consistent latency indicated a healthy network path.

---

## Route to Cloudflare Public DNS

- Successfully traced the route to **1.1.1.1 (one.one.one.one)**.
- The destination was reached in **6 hops**.
- The route passed through the ISP network and Cloudflare infrastructure.
- Some intermediate probes timed out due to ICMP filtering.
- The destination responded with consistently low latency.

---

## Trace Route Without DNS Resolution

- Successfully traced the route to **google.com** using the `-d` option.
- Only IP addresses were displayed because hostname resolution was disabled.
- The destination was reached successfully in **15 hops**.
- The output was cleaner and completed without performing reverse DNS lookups.
- The command is useful for faster troubleshooting and network analysis.

---

## Latency Analysis

- The local router consistently responded within **1–5 ms**.
- The ISP network showed low latency with occasional fluctuations.
- Public internet routers maintained acceptable response times.
- A few temporary latency spikes were observed but did not affect connectivity.
- Final destination latency remained stable throughout the traces.

---

## Request Timed Out Messages

Several hops displayed:

```text
* * * Request timed out.
```

These timeouts did **not** indicate a network failure.

Possible reasons include:

- Router configured to ignore ICMP requests.
- Firewall filtering traceroute packets.
- Rate limiting of ICMP responses.
- Security policies on intermediate routers.

Since the destinations responded successfully, packet forwarding continued normally.

---

## Security Observations

- `tracert` reveals the path packets take across different networks.
- It helps identify routers, ISPs, and network providers involved in communication.
- It is useful for troubleshooting routing problems and high latency.
- It assists in detecting routing anomalies and network outages.
- Traceroute is commonly used during incident response, penetration testing, and network reconnaissance.
- The `-d` option speeds up troubleshooting by skipping hostname resolution.

---

## Learning Outcome

After completing this lab, I gained practical experience in:

- Tracing packet routes across the Internet.
- Understanding network hops.
- Measuring latency between routers.
- Identifying ISP and backbone network paths.
- Interpreting request timeout messages.
- Using the `-d` option for faster trace routes.
- Applying traceroute during network troubleshooting and cybersecurity investigations.
