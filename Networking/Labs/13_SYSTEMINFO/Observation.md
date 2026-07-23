# Observations

## 1. System Information

- Executed the `systeminfo` command to display detailed information about the operating system and hardware.
- Observed the computer hostname as **JAKHMOLA_AKSHAT**.
- Verified that the operating system was **Microsoft Windows 11 Home Single Language** (Build **26200**).
- Identified the system manufacturer as **Dell Inc.** and the model as **Vostro 3420**.
- Confirmed that the system architecture was **64-bit (x64-based PC)**.
- Observed one installed Intel processor running at approximately **2419 MHz**.
- Verified the BIOS version as **Dell Inc. 1.39.0** dated **24-12-2025**.
- Observed that the computer belonged to the **WORKGROUP** workgroup.
- Verified that the total installed physical memory was **7,933 MB**.
- Observed the available physical memory at the time of execution was **764 MB**.
- Examined the virtual memory configuration, including maximum size, available memory, and page file location.
- Identified four installed network adapters, including Ethernet, Wi-Fi, Bluetooth, and VirtualBox Host-Only Ethernet Adapter.
- Verified that the Wi-Fi adapter was connected and had the IPv4 address **192.168.0.104**.
- Observed that Virtualization-Based Security (VBS) was running with Hypervisor-Enforced Code Integrity enabled.
- Learned that the `systeminfo` command provides comprehensive hardware, operating system, network, memory, BIOS, and security information useful for system administration and cybersecurity investigations.

---

## 2. Display System Information Page by Page

- Executed the `systeminfo | more` command.
- Observed that the output of the `systeminfo` command was displayed one page at a time.
- Verified that the displayed information was identical to the standard `systeminfo` command.
- Learned that the `more` command is useful for viewing lengthy command outputs without excessive scrolling.
- Understood that paging improves readability during system administration and forensic investigations.

---

## 3. Filter Host Name

- Executed the `systeminfo | findstr /B /C:"Host Name"` command.
- Used the `findstr` utility to filter the output of the `systeminfo` command.
- Observed that only the **Host Name** field was displayed.
- Verified the computer hostname as **JAKHMOLA_AKSHAT**.
- Learned that the `/B` option searches only at the beginning of a line, while `/C:` treats the enclosed text as an exact search string.
- Understood that output filtering is useful for quickly extracting required information from lengthy command outputs.

---

## 4. SYSTEMINFO Help

- Executed the `systeminfo /?` command to display the built-in help information.
- Reviewed the syntax and available command-line options.
- Learned the purpose of the following parameters:
  - `/S` – Connect to a remote computer.
  - `/U` – Specify the user account.
  - `/P` – Specify the password.
  - `/FO` – Display output in TABLE, LIST, or CSV format.
  - `/NH` – Hide column headers.
- Observed example commands demonstrating both local and remote usage.
- Confirmed that the SYSTEMINFO command supports remote administration when appropriate permissions are available.

---

## Summary

- Successfully examined detailed hardware and operating system information.
- Identified the Windows version, BIOS, processor, memory, network adapters, and security configuration.
- Used the `more` command to improve readability of long outputs.
- Filtered specific information using the `findstr` command.
- Reviewed the available options and syntax of the SYSTEMINFO utility.
- Learned how SYSTEMINFO is used in system administration, incident response, digital forensics, vulnerability assessment, and cybersecurity investigations.
