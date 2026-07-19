# Observations

## Command 1: `arp -a`

### Observation

- The ARP cache displayed entries for two network interfaces.
- The active Wi-Fi interface (`192.168.0.104`) contained three dynamic ARP entries.
- The default gateway (`192.168.0.1`) was mapped to MAC address `d8-47-32-3a-b7-16`.
- Two additional devices (`192.168.0.113` and `192.168.0.119`) were present with dynamically learned MAC addresses.
- Static entries included broadcast and multicast addresses such as `224.0.0.251` (mDNS), `224.0.0.252` (LLMNR), and `239.255.255.250` (SSDP).
- The VirtualBox Host-Only interface (`192.168.56.1`) contained only static multicast and broadcast entries.

---

## Command 2: `arp -a -v`

### Observation

- The verbose output displayed additional interfaces, including the Loopback interface (`127.0.0.1`) and Windows multicast routing entries (`0.0.0.0`).
- The active Wi-Fi interface contained three dynamic ARP entries for devices on the local network.
- An invalid entry was present for `192.168.0.118` with MAC address `00-00-00-00-00-00`, indicating that Windows did not currently have a valid MAC mapping for that IP address.
- The VirtualBox Host-Only adapter also contained an invalid entry because no active device was communicating on that network.
- Static multicast and broadcast entries remained unchanged.

---

## Command 3: `arp -d *`

### Observation

- The command executed successfully without displaying any output.
- No error message appeared, indicating that Windows accepted the command.
- Windows removed the removable ARP cache entries while preserving the entries required for active network communication.

---

## Command 4: `arp -a`

### Observation

- Most ARP cache entries were removed after executing the delete command.
- The dynamic entries for `192.168.0.1` and `192.168.0.113` remained because Windows immediately rebuilt them due to ongoing network communication.
- The multicast entry `224.0.0.22` remained as a static entry on both network interfaces.
- The command confirmed that Windows can automatically recreate ARP entries required for maintaining network connectivity.

---

## Command 5: `ping 192.168.0.1`

### Observation

- Four ICMP Echo Requests were sent to the default gateway.
- All four replies were received successfully with **0% packet loss**.
- The response time ranged from **1 ms to 2 ms**, indicating excellent local network connectivity.
- The router responded with a **TTL value of 64**, confirming successful communication with the gateway.

---

## Command 6: `arp -a`

### Observation

- The default gateway (`192.168.0.1`) remained in the ARP cache with its dynamically learned MAC address.
- The device `192.168.0.119` reappeared in the ARP cache after network communication.
- The ARP cache was automatically rebuilt as Windows communicated with devices on the local network.
- The VirtualBox Host-Only interface remained unchanged and contained only the static multicast entry.
- The results demonstrated that Windows automatically recreates ARP entries whenever communication occurs with devices on the local network.

---

# Overall Lab Observation

- Successfully viewed the ARP cache using `arp -a`.
- Examined detailed ARP information using `arp -a -v`.
- Cleared the ARP cache using `arp -d *`.
- Verified that most cached entries were removed after deletion.
- Confirmed successful communication with the default gateway using the `ping` command.
- Observed that Windows automatically rebuilt the ARP cache during subsequent network communication.
- Gained practical understanding of IP-to-MAC address resolution and ARP cache behavior on a Windows system.
