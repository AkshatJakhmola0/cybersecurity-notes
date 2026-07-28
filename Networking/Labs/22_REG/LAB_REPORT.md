# LAB REPORT

## Experiment Title

Windows Registry Analysis Using REG Command

---

## Objective

To learn how to use the Windows **REG** command to query and examine important Registry keys, analyze Windows configuration settings, identify installed applications, inspect startup programs, and understand the role of the Windows Registry in system administration and cybersecurity.

---

## Tools Used

- Windows 10 Home Single Language
- Command Prompt (CMD)
- REG Command

---

## Commands Executed

```cmd
reg

reg /?

reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion"

reg query "HKCU\Control Panel\Desktop"

reg query "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall"

reg query "HKCU\Environment"

reg query "HKCU\Software\Microsoft\Windows\CurrentVersion\Run"

reg query "HKLM\SYSTEM\CurrentControlSet\Control\ComputerName\ActiveComputerName"
```

---

## Procedure

1. Opened Command Prompt.
2. Executed the `reg` command to view available Registry operations.
3. Displayed the REG help menu using `reg /?`.
4. Queried the Windows version Registry key.
5. Viewed desktop configuration settings stored in the Registry.
6. Listed installed software from the Uninstall Registry key.
7. Displayed user environment variables.
8. Examined startup applications configured for the current user.
9. Retrieved the active computer name from the Registry.

---

## Results

- Successfully displayed all REG operations and help information.
- Retrieved Windows version and build details from the Registry.
- Viewed desktop configuration settings for the current user.
- Listed installed applications registered in Windows.
- Displayed user environment variables such as PATH and TEMP.
- Identified applications configured to run automatically at user logon.
- Retrieved the active computer name stored in the Registry.

---

## Conclusion

The REG command successfully provided access to important Windows Registry information. The lab demonstrated how Registry keys store operating system details, user preferences, installed software, startup programs, and system configuration. Understanding Registry structure and using the REG command are valuable skills for Windows administration, digital forensics, threat hunting, and incident response.

---

## Skills Gained

- Windows Registry Navigation
- Registry Enumeration
- Windows Administration
- Startup Program Analysis
- System Configuration Analysis
- Digital Forensics
- Threat Hunting
- Incident Response Fundamentals
