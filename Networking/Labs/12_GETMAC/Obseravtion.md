# Observations

## 1. Display MAC Addresses

- Executed the `getmac` command to display the physical (MAC) addresses of all available network adapters.
- Observed four network adapters installed on the system.
- Identified two active adapters and two disconnected adapters.
- Recorded the following MAC addresses:
  - **B4-45-06-D1-49-4D** – Ethernet adapter (Media disconnected).
  - **16-B2-01-6D-3B-7D** – Wi-Fi adapter (Active).
  - **30-03-C8-3F-97-76** – Bluetooth adapter (Media disconnected).
  - **0A-00-27-00-00-12** – VirtualBox Host-Only Ethernet Adapter (Active).
- Verified that active adapters displayed their corresponding TCP/IP Transport Names.
- Learned that every network adapter has a unique MAC address used for communication within a local network.

---

## 2. Verbose Output

- Executed the `getmac /v` command to display detailed information about all network adapters.
- Observed the connection name, network adapter name, physical address, and transport name.
- Identified the installed adapters as:
  - **Ethernet** – Realtek PCIe Gb Ethernet Adapter.
  - **Wi-Fi** – Realtek 8821CE Wireless LAN Adapter.
  - **Bluetooth Network Connection** – Bluetooth Device.
  - **Ethernet 2** – VirtualBox Host-Only Ethernet Adapter.
- Verified that the Wi-Fi and VirtualBox Host-Only adapters were active, while the Ethernet and Bluetooth adapters were disconnected.
- Learned that verbose mode provides detailed information useful for identifying hardware and troubleshooting network issues.

---

## 3. List Format Output

- Executed the `getmac /fo list` command.
- Observed that the adapter information was displayed in a vertical list format.
- Verified the MAC address and Transport Name for each network adapter individually.
- Learned that the list format improves readability when reviewing adapter information one device at a time.

---

## 4. CSV Format Output

- Executed the `getmac /fo csv` command.
- Observed that the output was displayed in Comma-Separated Values (CSV) format.
- Verified that each network adapter was represented as an individual CSV record.
- Learned that CSV output can be easily exported or imported into spreadsheets and automation tools for reporting and analysis.

---

## 5. GETMAC Help

- Executed the `getmac /?` command to display the built-in help information.
- Reviewed the syntax and available command-line options.
- Learned the purpose of the following parameters:
  - `/S` – Connect to a remote system.
  - `/U` – Specify the user account.
  - `/P` – Specify the password.
  - `/FO` – Select the output format (TABLE, LIST, or CSV).
  - `/NH` – Hide column headers.
  - `/V` – Display detailed (verbose) output.
- Observed example commands for retrieving MAC addresses from both local and remote systems.
- Confirmed that GETMAC supports remote administration when appropriate permissions are available.

---

## Summary

- Successfully displayed the MAC addresses of all network adapters.
- Identified active and disconnected network interfaces.
- Examined detailed adapter information using verbose mode.
- Viewed the output in Table, List, and CSV formats.
- Reviewed the available command-line options of the GETMAC utility.
- Learned how GETMAC assists in network administration, asset management, incident response, digital forensics, and cybersecurity investigations.
