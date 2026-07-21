# Observations

## 1. Route Print

- Displayed the complete IPv4 and IPv6 routing tables using the `route print` command.
- Identified multiple network interfaces, including the Wi-Fi adapter, Ethernet adapter, VirtualBox Host-Only adapter, Bluetooth PAN, and Software Loopback Interface.
- Verified the default gateway as **192.168.0.1**, which is used for destinations outside the local network.
- Identified the local IPv4 address as **192.168.0.104**.
- Observed loopback routes (`127.0.0.1` and `::1`) used for internal communication within the system.
- Identified the local network (`192.168.0.0/24`) and the VirtualBox Host-Only network (`192.168.56.0/24`).
- Observed multicast and broadcast routing entries for both IPv4 and IPv6.
- Confirmed that no persistent (static) routes were configured on the system.

---

## 2. IPv4 Routing Table (`route print -4`)

- Displayed only the IPv4 routing table using the `route print -4` command.
- Verified the default route (`0.0.0.0/0`) through the gateway **192.168.0.1**.
- Confirmed that the active network interface was the Wi-Fi adapter with the IP address **192.168.0.104**.
- Observed routes for the local network (`192.168.0.0/24`) and the VirtualBox Host-Only network (`192.168.56.0/24`).
- Verified loopback routes (`127.0.0.0/8`) used for internal communication.
- Observed multicast (`224.0.0.0/4`) and broadcast (`255.255.255.255`) routing entries.
- Confirmed that there were no persistent IPv4 routes configured.

---

## 3. IPv6 Routing Table (`route print -6`)

- Displayed only the IPv6 routing table using the `route print -6` command.
- Observed the IPv6 loopback route (`::1/128`) used for internal communication.
- Identified link-local IPv6 routes (`fe80::/64`) assigned automatically to the Wi-Fi and VirtualBox network interfaces.
- Observed interface-specific IPv6 addresses associated with the available network adapters.
- Identified IPv6 multicast routes (`ff00::/8`) used for multicast communication.
- All IPv6 routes used **On-link** as the gateway, indicating direct communication through the local interface.
- No default IPv6 route (`::/0`) was present, indicating that IPv6 internet routing was not configured on the network.
- Confirmed that no persistent IPv6 routes were configured.

---

## 4. Route Help (`route /?`)

- Displayed the built-in help documentation for the Windows `route` command.
- Reviewed the syntax and usage of the Route utility.
- Learned the purpose of the `PRINT`, `ADD`, `DELETE`, and `CHANGE` commands.
- Understood the use of command-line options such as `-f`, `-p`, `-4`, and `-6`.
- Reviewed the parameters required to create and manage static routes, including destination, subnet mask, gateway, interface, and metric.
- Examined the built-in command examples and diagnostic notes for troubleshooting routing configurations.
- Confirmed that the `route /?` command provides reference information only and does not modify the routing table.

---

## Summary

- Successfully viewed the complete routing table along with separate IPv4 and IPv6 routing tables.
- Identified the system's default gateway, local IP address, loopback routes, multicast routes, and VirtualBox Host-Only network.
- Verified that Windows automatically manages the routing table and that no persistent static routes were configured.
- Learned how to view, add, modify, and delete routes using the Windows `route` command.
- Gained a better understanding of routing table entries, gateway selection, interface usage, and routing metrics in Windows.
