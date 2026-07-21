# Lab Report

## Experiment Title

**Windows Route Command – Viewing and Understanding the Routing Table**

---

## Objective

The objective of this experiment was to study the Windows `route` command and understand how routing tables are maintained. The experiment focused on viewing IPv4 and IPv6 routing tables, identifying network interfaces, default gateways, loopback routes, multicast routes, and understanding the syntax and usage of the Route utility.

---

## Tools Used

- Operating System: Windows 11
- Command Prompt (CMD)
- Route Command
- Wi-Fi Network Connection

---

## Commands Executed

```cmd
route print
route print -4
route print -6
route /?
```

---

## Procedure

1. Opened **Command Prompt** with administrative privileges.
2. Executed the `route print` command to display the complete routing table.
3. Examined the available network interfaces and identified the default gateway, local IP address, loopback routes, and VirtualBox network entries.
4. Executed the `route print -4` command to display only the IPv4 routing table.
5. Analyzed IPv4 routes including the default route, local network routes, multicast routes, and broadcast routes.
6. Executed the `route print -6` command to display only the IPv6 routing table.
7. Examined IPv6 loopback, link-local, and multicast routes.
8. Executed the `route /?` command to study the syntax, options, parameters, and examples of the Route utility.
9. Recorded observations and captured screenshots for each command.

---

## Results

- Successfully displayed the complete Windows routing table.
- Identified multiple network interfaces including Wi-Fi, Ethernet, VirtualBox Host-Only Adapter, Bluetooth PAN, and Software Loopback Interface.
- Verified the default gateway as **192.168.0.1**.
- Identified the local IPv4 address as **192.168.0.104**.
- Observed loopback routes for both IPv4 (`127.0.0.1`) and IPv6 (`::1`).
- Identified the local network (`192.168.0.0/24`) and VirtualBox Host-Only network (`192.168.56.0/24`).
- Observed multicast and broadcast routing entries.
- Confirmed that no persistent static routes were configured.
- Learned the syntax and functionality of the `PRINT`, `ADD`, `DELETE`, and `CHANGE` commands using the Route help documentation.

---

## Conclusion

The experiment successfully demonstrated how Windows maintains its routing table and how the `route` command can be used to inspect routing information. The routing table provides important details such as the default gateway, network interfaces, routing metrics, loopback routes, multicast routes, and local network routes. Understanding the routing table is essential for network troubleshooting, configuring static routes, and analyzing packet forwarding decisions in Windows systems.

---

## Skills Gained

- Learned to use the Windows `route` command.
- Understood the structure of IPv4 and IPv6 routing tables.
- Identified network interfaces and default gateways.
- Understood loopback, multicast, broadcast, and link-local routes.
- Learned the purpose of routing metrics and route selection.
- Gained knowledge of Route utility commands such as `PRINT`, `ADD`, `DELETE`, and `CHANGE`.
- Improved practical networking and troubleshooting skills.
