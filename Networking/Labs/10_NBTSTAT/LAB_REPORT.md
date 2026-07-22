# Lab Report

## Experiment Title

**Using the NBTSTAT Command to View and Analyze NetBIOS over TCP/IP Information**

---

## Objective

The objective of this experiment was to study the Windows **NBTSTAT (NetBIOS over TCP/IP Statistics)** utility and understand its role in Windows networking. The experiment focused on viewing local NetBIOS names, examining the NetBIOS name cache, analyzing name resolution statistics, and identifying active NetBIOS sessions.

---

## Tools Used

- Operating System: Windows 11
- Command Prompt (CMD)
- NBTSTAT Utility
- Active Network Connection

---

## Commands Executed

```cmd
nbtstat
nbtstat -n
nbtstat -c
nbtstat -r
nbtstat -s
```

---

## Procedure

1. Opened Command Prompt.
2. Executed the `nbtstat` command to display the available options and syntax.
3. Displayed the local NetBIOS name table using the `nbtstat -n` command.
4. Examined the NetBIOS name cache using the `nbtstat -c` command.
5. Viewed NetBIOS name resolution and registration statistics using the `nbtstat -r` command.
6. Displayed active NetBIOS sessions using the `nbtstat -s` command.
7. Recorded observations and captured screenshots for each command.

---

## Results

- Successfully displayed the help information for the NBTSTAT utility.
- Verified the registered NetBIOS names for the **Wi-Fi** and **Ethernet 2** interfaces.
- Confirmed that the system belonged to the **WORKGROUP** workgroup.
- Identified the local computer name as **JAKHMOLA_AKSHAT**.
- Observed that no NetBIOS name cache entries were present on any network interface.
- Verified that no NetBIOS names were resolved through broadcast or a WINS server.
- Observed that **126 NetBIOS names** had been registered using broadcast.
- Confirmed that no NetBIOS name registrations were performed through a WINS server.
- Verified that no active NetBIOS sessions existed on any network interface.
- Learned that the system primarily relies on modern networking protocols instead of active NetBIOS communication.

---

## Conclusion

The experiment successfully demonstrated the functionality of the Windows **NBTSTAT** utility. It provided valuable information about local NetBIOS names, cached entries, name resolution statistics, and active NetBIOS sessions. The results showed that while NetBIOS support is available on the system, there were no active NetBIOS sessions or cached remote names during the experiment. The NBTSTAT command remains a useful tool for troubleshooting, legacy Windows network administration, digital forensics, and cybersecurity investigations.

---

## Skills Gained

- Learned to use the Windows NBTSTAT utility.
- Viewed local NetBIOS names registered on the system.
- Examined the NetBIOS name cache.
- Analyzed NetBIOS name resolution and registration statistics.
- Identified active NetBIOS sessions.
- Improved Windows networking troubleshooting skills.
- Gained practical knowledge of legacy Windows networking protocols.
- Developed skills useful for system administration, digital forensics, and cybersecurity.
