# Lab Report

## Experiment Title

**Using the GETMAC Command to Display and Analyze Network Adapter MAC Addresses**

---

## Objective

The objective of this experiment was to study the Windows **GETMAC** command and learn how to display the MAC addresses of network adapters. The experiment also explored different output formats and detailed adapter information useful for network administration and cybersecurity.

---

## Tools Used

- Operating System: Windows 11
- Command Prompt (CMD)
- GETMAC Utility
- Active Network Connection

---

## Commands Executed

```cmd
getmac
getmac /v
getmac /fo list
getmac /fo csv
getmac /?
```

---

## Procedure

1. Opened Command Prompt.
2. Executed the `getmac` command to display the MAC addresses of all network adapters.
3. Executed the `getmac /v` command to view detailed adapter information.
4. Executed the `getmac /fo list` command to display the output in List format.
5. Executed the `getmac /fo csv` command to display the output in CSV format.
6. Executed the `getmac /?` command to view the available options and syntax.
7. Recorded the observations and captured screenshots for each command.

---

## Results

- Successfully displayed the MAC addresses of all installed network adapters.
- Identified the Ethernet, Wi-Fi, Bluetooth, and VirtualBox Host-Only network adapters.
- Verified that the Wi-Fi and VirtualBox Host-Only adapters were active.
- Observed detailed adapter information using verbose mode.
- Displayed the output in Table, List, and CSV formats.
- Reviewed the built-in help information and available command-line options.
- Learned how different output formats can be used for administration, reporting, and automation.

---

## Conclusion

The experiment successfully demonstrated the use of the Windows **GETMAC** command for viewing the physical addresses of network adapters. The command provided valuable information about installed adapters, their MAC addresses, connection status, and transport names. The different output formats improved flexibility for reporting and automation, while the verbose mode provided additional hardware details. The GETMAC utility is useful for network administration, troubleshooting, asset inventory, digital forensics, and cybersecurity investigations.

---

## Skills Gained

- Learned to use the Windows GETMAC command.
- Identified the MAC addresses of network adapters.
- Distinguished between active and disconnected network interfaces.
- Viewed detailed adapter information using verbose mode.
- Used List and CSV output formats.
- Improved Windows networking and troubleshooting skills.
- Gained practical knowledge useful for system administration, digital forensics, and cybersecurity.
