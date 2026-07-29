# LAB REPORT

## Experiment Title

Searching Text in Files Using the FIND Command

---

## Objective

To learn how to use the Windows **FIND** command to search for specific text within files, perform case-insensitive searches, display matching line numbers, and analyze command output stored in text files.

---

## Tools Used

- Windows 11 Home Single Language
- Command Prompt (CMD)
- FIND Command
- Systeminfo Utility

---

## Commands Executed

```cmd
find /?

find "Windows" C:\Windows\System32\drivers\etc\hosts

systeminfo > systeminfo.txt

find "OS" systeminfo.txt

find "Version" systeminfo.txt

find "Memory" systeminfo.txt

find /i "windows" systeminfo.txt

find /n "OS" systeminfo.txt
```

---

## Procedure

1. Opened Command Prompt.
2. Displayed the FIND command help menu.
3. Searched the Hosts file for the keyword "Windows".
4. Redirected the output of the `systeminfo` command to a text file.
5. Searched the file for operating system information.
6. Retrieved version-related details.
7. Displayed memory-related information.
8. Performed a case-insensitive search using the `/i` option.
9. Displayed matching lines with their line numbers using the `/n` option.

---

## Results

- Successfully displayed the FIND command help menu.
- Located the keyword "Windows" in the Hosts file.
- Created a text file containing system information.
- Retrieved operating system details from the file.
- Displayed Windows and BIOS version information.
- Extracted physical and virtual memory details.
- Performed a successful case-insensitive search.
- Displayed matching results with corresponding line numbers.

---

## Conclusion

The FIND command successfully searched for specific text within files and filtered relevant information from system command output. It proved useful for locating operating system details, version information, memory statistics, and other configuration data. This command is valuable for Windows administration, troubleshooting, log analysis, and basic cybersecurity investigations where quick text searching is required.

---

## Skills Gained

- Text Searching
- Windows Command Line
- Log Analysis
- System Information Filtering
- File Analysis
- Windows Administration
- Basic Incident Response
- Digital Forensics Fundamentals
