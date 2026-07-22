# Observations

## 1. NBTSTAT Help

- Executed the `nbtstat` command to display the built-in help information.
- Reviewed the syntax and available options of the NBTSTAT utility.
- Learned the purpose of commands such as `-n`, `-c`, `-r`, `-R`, `-RR`, `-s`, and `-S`.
- Identified options for viewing local NetBIOS names, cached entries, name resolution statistics, and active NetBIOS sessions.
- Learned that remote NetBIOS information can be queried using either a computer name (`-a`) or an IP address (`-A`).
- Confirmed that the command provides reference information only and does not make any changes to the system.

---

## 2. Local NetBIOS Names

- Executed the `nbtstat -n` command to display the local NetBIOS name table.
- Observed registered NetBIOS names for the **Wi-Fi** and **Ethernet 2** interfaces.
- Verified that the computer belonged to the **WORKGROUP** workgroup.
- Identified the local computer name as **JAKHMOLA_AKSHAT**.
- Observed the `<00>` unique name representing the computer name and the `<20>` unique name representing the File and Printer Sharing service.
- Verified that all displayed NetBIOS names were successfully registered.
- Observed that the Ethernet, Bluetooth, and Local Area Connection interfaces had no registered NetBIOS names because they were inactive or disconnected.

---

## 3. NetBIOS Name Cache

- Executed the `nbtstat -c` command to display the NetBIOS name cache.
- Checked all available network interfaces, including Wi-Fi, Ethernet, Ethernet 2, Bluetooth, and Local Area Connection interfaces.
- Observed that no cached NetBIOS name entries were present on any interface.
- Confirmed that the system had not recently resolved any remote NetBIOS names.
- Learned that an empty NetBIOS cache is common on modern Windows networks where DNS is primarily used for name resolution.
- Understood that the NetBIOS name cache stores recently resolved remote computer names and their corresponding IP addresses when NetBIOS communication occurs.

---

## 4. NetBIOS Name Resolution Statistics

- Executed the `nbtstat -r` command to display NetBIOS name resolution and registration statistics.
- Observed that **0 names** were resolved by broadcast.
- Observed that **0 names** were resolved by a WINS (Windows Internet Name Service) server.
- Verified that **126 NetBIOS names** had been registered using broadcast.
- Confirmed that no NetBIOS name registrations were performed through a WINS server.
- Learned that the system primarily relied on broadcast registration and was not using a WINS server for NetBIOS name services.

---

## 5. NetBIOS Sessions

- Executed the `nbtstat -s` command to display active NetBIOS sessions.
- Checked all available network interfaces, including Wi-Fi, Ethernet, Ethernet 2, Bluetooth, and Local Area Connection interfaces.
- Observed that no active NetBIOS sessions were present on any network interface.
- Confirmed that the system was not currently communicating with any remote hosts using the NetBIOS protocol.
- Learned that modern Windows networks typically rely on DNS and SMB over TCP/IP instead of active NetBIOS sessions.

---

## Summary

- Successfully explored the Windows NBTSTAT utility and its available options.
- Examined the local NetBIOS name table and identified the registered computer and workgroup names.
- Verified that no NetBIOS name cache entries were present.
- Analyzed NetBIOS name resolution and registration statistics.
- Confirmed that no active NetBIOS sessions existed on the system.
- Learned how NBTSTAT assists in network troubleshooting, Windows administration, legacy network support, digital forensics, and cybersecurity investigations.
